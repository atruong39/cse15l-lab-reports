# CSE 15L: Lab Report 4, Week 8

Link to my markdown-parse repository: [markdown-parse](https://github.com/atruong39/markdown-parse)

## Expected Results

For the first code snippet

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

The expected result was 

```
[`google.com, google.com, ucsd.edu]
```

For the second code snippet 

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

The expected result was

```
[a.com, a.com(()), example.com]
```

For the third code snippet 

```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

The expected result was 

```
[https://www.twitter.com, https://ucsd-cse15l-w22.github.io/, https://cse.ucsd.edu/]
```