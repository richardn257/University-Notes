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
        case 1: sortbyName(mov); break;
        case 2: sortbyRelease(mov); break;
        ...
    }
}
```

- compare string by using '>, <, ==' or .compare()

Example of cstring
```
char fname[10];
char lname[5];
strcpy(lname, "Smith");
strcpy(fname, "Bartholomue");
```
<p>imagine a horizontal rectangle which rep array<br>
| fname | lname |<br>
Bartholomue // with strcpy, it overwrites Smith, strcpy does not prevent overwrite<br>
strncpy will set a limit of the char<br></p>

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
