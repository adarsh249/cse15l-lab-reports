# Lab Report 5
Below is my grade.sh:

```bash
# Create your grading script here
rm -rf student-submission
git clone $1 student-submission

echo "Cloning..."

cd student-submission

if [ -f ListExamples.java ]
then
    echo "Found student's file."
else
    echo "Student file not found."
    exit
fi

cp ListExamples.java ..

cd ..

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java 2> err.txt

if [ $? -ne 0 ]
then
    echo "Compiler Error"
    exit
fi

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > grade.txt

OK=$(grep -c OK grade.txt)

if [ $OK -eq 1 ]
then
    echo "Pass"
else
    echo "Fail"
fi

exit
```

Below are the outputs for three different repositories:

Repository 1: `https://github.com/ucsd-cse15l-f22/list-methods-corrected`

![Image 1](Screen Shot 2022-11-23 at 3.14.59 PM.png)

Repository 2: `https://github.com/ucsd-cse15l-f22/list-methods-compile-error`

![Image 2](Screen Shot 2022-11-23 at 3.17.15 PM.png)

Repository 3: `https://github.com/ucsd-cse15l-f22/list-methods-filename`

![Image 3](Screen Shot 2022-11-23 at 3.18.30 PM.png)

