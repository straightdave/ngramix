ngramix
======
Customized N-gram parser plugin of MySQL for mixed use of ideographic and alphabetic languages

## the main purpose
MySQL provides a built-in full-text parser for ideographic languages: Ngram, which is simply good enough for fulltext search.
While using its index to search English/English words embedded phrases, it goes the same way to seperate whole word letter by letter and this is not what I want.   

So, I need another simple alternative that could parse both Chinese and English words/characters properly.
This will be (yes, future tense) a simple plugin to MySQL, same as original 'Ngram' plugin.   

## the basic ideas
1. Do the normal N-gram parsing, treat letters as one single word just like one ideographic character
2. Add such words into fulltext indexes if the length is great than a threshold (users who search may search with single English words)

## examples

```
if Bigram:
"你好啊dave大帅哥" ==> "你好 好啊 啊dave dave大 大帅 帅哥" and the word "dave"
```

