# getopts
`getopts` is the tool to parse command line arguments.

```bash
#!/bin/sh
while getopts a: OPT
do
    case $OPT in
        "a" ) echo "$OPTARG";;
    esac
done
```

# save time/date format to the shell variable
```bash
dtStr="$(date +"%Y%m%d")"
```

# parse option for date format
```bash
while getopts "d:" opt; do
  case "$opt" in
  d) dtStr=$OPTARG
  esac
done
```

# date format
```bash
dtStr="#$(date -d '2 days agp' +'%m%d')"
```
