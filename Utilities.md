# Searching and Processing Text
> grep <word> <file> #search for all instances of <word>
> grep error /var/log/*.log # search for all instances of error
> grep error -B 3 -A 2 /var/log/*.log #this returns the three lines before and two lines after the error instance

To filter out duplicates
> sort <txt> | uniq
this is because uniq only filters out duplicate adjacent
> wc <file> #outputs word counts
> grep bob <file> | wc -l #counts isntances of bob
> grep -v e <file> #grep out all words without e in file

# Text Manipulation
> sed 's/Suite/Ste' <file> #this replaces all the first instance of Suite with Ste for each line
> sed 's/Suite/Ste/g' <file> #this replaces ALL instances
> sed '$s/Suite/ste' <file> #this only replaces the Suite in the ifnal line
> sed '/Suite/d' <file> #this deletes any lines that has Suite inside
> 