# Puzzle 2 Intent

[Ref](http://developer.android.com/guide/components/intents-filters.html)
```
Caution: If you want to set both the URI and MIME type, do not call setData() and setType() 
because they each nullify the value of the other. 
Always use setDataAndType() to set both URI and MIME type.
```

- `PendingIntent`