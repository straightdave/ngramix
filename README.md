# ngramix 
## 修改的MySQL N-gram 全文搜索插件，中英文单字区别对待
```
ngramix = N-gram + Mix of both ideographic character indexing and normal alphabetic words
```

Basically _ngramix_ is a customized N-gram parser plugin of MySQL which is pretty good for simple use of Chinese full-text search at some not-that-big sites.

## It is simple since
1. It is simply a MySQL (5.7+) plugin that you can just install and enable it. No other software or applications required to install or configure
2. It is simply build MySQL full-text indexes. As you know, the bigger web sites however choose more professional solutions like Lucene or other Chinese tokenizer/indexer combinations

But if you run a start-up and small web site, it could be one of the most proper choice.

## features
- treat one alphabetic word as a token to be indexed, rather than seeing it as combination of letters


## examples

```
if Bigram:
"你好啊dave大帅哥" ==> "你好 好啊 啊dave dave大 大帅 帅哥" and the word "dave"
```

## contribution

This is still in process of development/improving.

- Please pull requests for your updates
- Talk about issues by opening ISSUES

