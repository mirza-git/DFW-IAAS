# Repeat a Command Until It Runs Successfully

Often time I have to repeat task over and over - to do this it is very simple in Linux, you can achive that by running "for loop", for loop will run the task till you declare it to complete.

let try it together and understand how it works by looking at simple code below:

```
for i in Mon Tues Wed Thus Fri
do
echo "Day is : $i"
done
```

Now lets print numeric dates:

```
for d in Mon Tue Wed Thu Fri
do
     date +%Y%m%d -d "last $d"
done | sort
```

bit more complex code:

```
N=10
for i in $(seq $(($N + $N / 5 * 2)) -1 1)
do
    [ `date --date="-$i day" +%u` -le 5 ] &&
       date -d "-$i day" +"File date is : %Y%m%d"
done
```
