# CECS 282
### Week 7 (3/7/22 - 3/9/22)

- Prog3 Due 3/14/22 
- Movie.cpp, myDate.cpp, myDate.h

```
struct Movie
{
    char name[20]  // can have smaller word, but not larger word
    int running;
    double rating;
    myDate release;
    string actor;
}

// int x; this is global variable, placed before main (DO NOT USE)
int main()
{
    Movie *mov[10];
    populate(mov);    // strcpy(), strncpy()
    switch(choice)
    {
        case 1: sortbyName(mov); 
        eak;
        case 2: sortbyRelease(mov); break;
        ...
    }
}
```

- compare string by using '>, <, ==' or .compare()

<p>x.compare(y)</p>

- if x > y return greater than 0
- if x < y return less than 0
- if x == y return 0
- 0 is false and non-zero is true

Example of cstring
```
char fname[10];
char lname[5];
strcpy(lname, "Smith");
strcpy(fname, "Bartholomue");
```
- imagine a horizontal rectangle which rep array
<p>| fname | lname |<br>
Bartholomue // with strcpy, it overwrites Smith, strcpy does not prevent overwrite<br></p>

- strncpy will set a limit of the char
[More info on strncpy](https://en.cppreference.com/w/cpp/string/byte/strncpy)

- use bubble sort cuz its ez
```
void sortbyName(Movie *m[])  // OR **m  poiner to a pointer, in the () is the array of pointers
{
    for (int i = 9; i > 0; i--)
    {
        for (int j = 0; j < i; j++)       // j highest is 8, j lowest is 0
        {
            if (strcmp(m[j]->name, m[j+1]->name) > 0)
                swap()
        }
    }
}
```

Comparing cstring example
strcmp(x,y)
- if x > y return greater than 0
- if x < y return less than 0
- if x == y return 0
```
char a[] = "zapple"
char b[] = "banana";
if (strcmp(a,b) > 0)    // true
{
    swap(a,b)
}
```

```
void sortbyRelease(Movie *m[])  // OR **m  poiner to a pointer, in the () is the array of pointers
{
    for (int i = 0; i < 9; i++)
        for (int j -= 0; j < i; j++)
            if (strcmp(m[j]->release, m[j+1]->release) > 0)       // daysBetween
                swap()
}
```

Example of strcpy(x,y);
```
char a[10] = "apple";
char b[10] = "banana";
strcpy(a,b);
cout << a << b;

// could use char p[], char q[]
void strcpy(char *p, char *q)     // p is pointing to the first element of array a and q is to array b
{
    while (*p++ = *q++);   // assigns q to p (true until reach null in banana, (its blank, empty) (not '\0', this is null terminator))
}
```


### Week 8 (3/14 - 3/16)
- study quizzes for midterm
- check if 

<p>
<br></p>

code example of operator-
```
int operator-(Time t1, Time t2)
{
}

#include "Time.h"
int main()
{
    Time evening(18,0);
    Time bedTime(23, 0);
    cout << bedTime - evening;
}

// operator overloading
// int in () is size
// return month
int operator[] (myDate, int)
```

Ternary operator
```
a ? b : c
exprssion  ? if true execute : else false execute
cout << (x > y) ? x : y;
```

```
#include "upDate.h"
int main()
{
    upDate today(3, 16, 2022);
    upDate nextWeek(3, 23, 2022);
    today = nextWeek;       // overwrite the assignment operator b/c memory leak
}
```

















