# notes
Take quick notes in a KISS way

Just add this function in your shell config ($HOME/.bashrc if bash)

```
notes() {
	if [ -z "$1" ]; then
		less $HOME/notes 2> /dev/null
	else
		date >> $HOME/notes
		echo -e "$1\n" >> $HOME/notes
	fi
}
```

## Usage

### view your notes
```
$ notes
```

### add a new note
```
$ notes "a new note"
```
