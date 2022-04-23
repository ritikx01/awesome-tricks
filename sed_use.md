## Efficiently use sed (Stream Editor)

### Sed use:
sed 's/mysql/MySQL/g' /etc/snort/snort.conf

Breakdown:
sed	-	Command to call sed
s	-	For search
mysql	-	Search for this term or pattern
MySQL	-	Replace with this term or pattern
/etc/..	-	File path

Examples:
```bash
cat file.txt
Apples are red. red colour is also present in rainbow.		//Initial text

sed 's/red/Red/g file.txt'					//Replace globally, i.e, all the matches
Apples are Red. Red colour is also present in rainbow.

sed 's/red/Red/ file.txt'					//Replace only first occurance
Apples are Red. red colour is also present in rainbow.

sed 's/red/Red/2 file.txt'					//Replace the deined occurance. (Here 2nd)
Apples are red. Red colour is also present in rainbow.
```

To delete a pattern, for example all the empty lines in a file
`sed '/^$/d' file.txt`						// ^$ matches nothing (empty line). `d`	deletes the previous match

To read a part of file, for example from 20th to 25th line:
`sed -n '20,25p' file.txt`					//This will include 20th and 25th line
