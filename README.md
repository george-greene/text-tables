# text-tables
Plain-text reference tables.

The files are tab-delimited, you can pass `-F '\t'` to awk to work with tabs. For example, if you want to look at the first column:

```bash
cat <file_name> | awk -F '\t' '{print $1}'
```

You can use the following command to format and print a file with aligned columns:

```bash
cat <file_name> | awk '/\t/ {for (i = 0; i < 2; i++) gsub(/\t/, t t)} 1' | column -t -s $'\t'
```
