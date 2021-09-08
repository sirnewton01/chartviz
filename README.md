# Chartviz - text representation of line, bar and gauge graphs

Chartviz is a tool that works with graphs that are written in plain text. Here are some examples.

```
  0                                                150
 +---------------------------------------------------+
1|               *                                   | 20
2|              *                                    | 15
3|                *                                  | 21
4|                   *                               | 25
 +---------------------------------------------------+
 .=low_temp *=high_temp

  0                                                150
 +---------------------------------------------------+
1|****************                                   | 20
2|***************                                    | 15
3|*****************                                  | 21
4|********************                               | 35
 +---------------------------------------------------+

 0                                                 150
+----------------------------------------------------+
|===============================                     | 76
+----------------------------------------------------+
```

Since these charts are a bit difficult construct manually, chartviz will create these for you from simple delimited text data or even clean up an existing chart as a formatter. The charts are difficult to injest by other tools, such as sed, grep, or a spreadsheet so chartviz will also export a chart as a delimited text stream.

```
1 20
2 15
3 21
4 35

76
```

