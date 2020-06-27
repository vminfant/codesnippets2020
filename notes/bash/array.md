# How to read array from delimited text

use ```readarray``` with ```-d``` option to read the delimited
text as array in bash

```bash
#!/usr/bin/env bash

# User inputs
echo -n "Enter Number of elements: "
read -r no_of_elements
echo -n "Enter delimiter: "
read -r del
echo -n "Enter array elements as delimited text: "
readarray -n $no_of_elements -d $del elements

# Output
echo ""
echo "Array elements: "
for item in ${elements[@]};
do
        echo $item
done;
```

Output of the above snippet is,

```bash
$ ./test.sh
Enter Number of elements: 3
Enter delimiter: ,
Enter array elements as delimited text: 1,2,3,

Array elements:
1,
2,
3,
```

If we like to remove the delimiter captured as part of an array element we can pass ```-t``` option.

Note:

 - ```-t``` must be passed before supplying the ```-d``` option.

 Eg, ```readarray -t -n $no_of_elements -d $del elements ```
 - ```-d``` option uses the delimiter to parse and split the array elements. So, it is mandatory to pass the delimiter after the last element
