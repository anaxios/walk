Simple implementation of 'walk' and 'sor' from Plan9 in Bash. Can replace the find command.

walk prints files and dirs recursively.

This will print all regular files 3 level deep from your home dir.
```shell
walk -d 3 ~/ | sor 'test -f'
```

This will print all regular files 3 level deep from your home dir that have .mkv in the file name.
```shell
walk -d 3 ~/ | sor 'test -f' | grep .mkv
