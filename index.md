# CECS 282
### Week 7 (3/7/22 - 3/9/22)

- Start writing notes. Any interesting facts

      struct Movie
      {
          char name[20]  // can have smaller word, but not larger word
          int running;
          double rating;
          myDate release;
          string actor;
      }

Prog3
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
        case 2:: sortbyRelease(); break;
    }
}
```

- compare string by using '<' or .compare()

Example of cstring

`char fname[10];
char lname[5];
strcpy(lname, "Smith");
strcpy(fname, "Bartholomue");`

imagine a rectangle horizontal
fname | lname
Bartholomue // overwrites Smith, strcpy does not prevent overwrite
strncpy will set a limit of the char

- use bubble sort cuz its ez
`
void sortbyName(Movie *m[])  // OR **m  poiner to a pointer, in the () is the array of pointers
{
    for (int i = 0; i < 9; i++)
    {
        for (int j -= 0; j < i; j++)
        {
            if (strcmp(m[j]->name, m[j+1]->name) > 0)
                swap()
        }
    }
}
`
Comparing example
strcmp(x,y)
- if x > y return greater than 0
- if x < y retrun less than 0
`char a[] = "zapple"
char b[] = "banana";
if (strcmp(a,b) > 0)
{
    swap(a,b)
}
`

`
void sortbyRelease(Movie *m[])  // OR **m  poiner to a pointer, in the () is the array of pointers
{
    for (int i = 0; i < 9; i++)
        for (int j -= 0; j < i; j++)
            if (strcmp(m[j]->release, m[j+1]->release) > 0)   daysBetween
                swap()
}
`

Example of strcpy(x,y);
`
char a[10] = "apple";
char b[10] = "banana";
strcpy(a,b);
cout << a << b;

// could use char x[], char y[]
void strcpy(char *p, char *q)     // x is pointing to the first element of array a and y is to array b
{
    while (*p++ = *q++);   // assigns q into p (true until reach null(not '\0', its empty) in banana
}
`













