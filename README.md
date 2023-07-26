# practice
Hi new repository created in remote console in github
welcome to satish new repository practice.
wish you all the best 
#!/bin/bash/
#vaidate Head and tailor in shell script.
dt=$(sed -n 1p /home/satish/data.txt)
tdt=`date +%Y%m%d`
count=8
Record_length=$(tail -1 data.txt)
echo "header date is:$dt and record length :$Record_length \n both conditions satisfied"
if [ $dt = $tdt -a $Record_length -lt $count ]
then
echo "now moving first column into last column in data file. please check below output"
awk -F"," '{print $4,$3,$2,$1}' /home/satish/data.txt > /home/satish/newdata.txt
cat /home/satish/newdata.txt
fi
