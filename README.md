# cpr = copy (cp) and rename (r) 
Create a copy of a directory, renaming the directory and each filename within by finding and replacing based on a pattern.

## Assumptions
* New directory is copied into the same location as the original directory
* Only rename the directory and files if the from_pattern matches
    * e.g. `--from 20160101` would match for the file `myfile_20160101.csv`

## Usage
```
cpr --dir dirname --from from_patter --to to_pattern

    -h, --help                  display help
    -d, --dir dirname           directory to copy
    -f, --from from_pattern     pattern to search for in directory and filenames
    -t, --to to_pattern         pattern to replace in directory and filenames
```

## Example
```
$ cpr --dir 20160101 --from 20160101 --to 20160201
```

## Requirements
* Requires the command `readlink`
