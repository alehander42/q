# q

Hack: functions which return results that can adapt to the call site context?!

```python
f = read_file('a')

for ugh in f:
    print(ugh)
# letters

for word_x in f:
    print(word_x)
# words

for i, long_sentence in enumerate(f):
    print('%d:%s' % (i, long_sentence))
# sentences


for i, paragraph in enumerate(f):
    print('%d:%s' % (i, paragraph))
# CAN YOU BELIEVE IT PARAGRAPHS?
```

I had some thought experiments on how non-programmers would deal with a language-like 
interface (something in the middle of applescript / siri)

In this experiment we expect that people would try to do an action (often corresponding to a function) and to deal with its results in various and unexpected ways. 
One explanation is: humans are used to see concepts and real life objects as complex ideas with many possible interpretations and they're very good at switching between them based on the context:
e.g. a coffee place can be a place for refreshments, a good place for chatting with someone, a good place to find wifi and a place that symbolizes your hangover after the latest pub crawl all based on the context of the conversation or your goals.

In the same way a file can be an image / a string / a list of words / a list of sentences / a configuration based on what you already know about it and the way you want to use it.
Of course, for a programmer it's natural to extract or access this kind of "view" of the data, but a normal user might expect to be able to do all of this with this abstract "file", e.g.:

Alexander Ivanov, 2017