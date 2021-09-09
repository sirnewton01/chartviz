# Chartviz - text representation of line, bar and gauge graphs

Chartviz is a tool that works with graphs that are written in plain text. Here are some examples.

```.cv
day,high_temp (*)

  0                                                150
 +---------------------------------------------------+
1|               *                                   | 20
2|              *                                    | 15
3|                *                                  | 21
4|                   *                               | 25
 +---------------------------------------------------+

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

Since these charts are a bit difficult construct manually, chartviz will create these for you from simple delimited text data or even clean up an existing chart as a formatter. The charts are difficult to injest by other tools, such as sed, grep, or a spreadsheet so chartviz will also export a chart as a delimited text stream. Here is the comma-separated value (CSV) equivalent of the charts above.

```.cv
day,high_temp
1,20
2,15
3,21
4,35

1,20
2,15
3,21
4,35

76
```

The two formats can be mixed like this so that you can insert data into the charts easily. Chartviz can parse and format the chart with this new data.

```.cv
  0                                                150
 +---------------------------------------------------+
1|               *                                   | 20
2|              *                                    | 15
3|                *                                  | 21
4|                   *                               | 25
5,55
6,22
 +---------------------------------------------------+
```

Chartviz will also produce image files for either chart, CSV, or mixed input.
