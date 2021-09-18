Activity 3
================
Levi D Rosendall

Today you will be creating and manipulating vectors, lists, and data
frames to uncover a top secret message.

As you work through this document with your Team members, remember to:

-   Ask questions
-   Google is your friend! If an error is confusing, copy it into Google
    and see what other people are saying. If you don’t know how to do
    something, search for it.
-   Just because there is no error message doesn’t mean everything went
    smoothly. Use the console to check each step and make sure you have
    accomplished what you wanted to accomplish.

Do not edit this first R code chunk. This will allow you to knit your
document and view errors within the knitted report.

### Setup

Each of the following R chunks will cause an error and/or do the desired
task incorrectly. Find the mistake, and correct it to complete the
intended action.

Create three vectors that contain: 1) the lower case letters, 2) the
lower case letters, and 3) some punctuation marks.

``` r
lower_case <- c("a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z")
lower_case
```

    ##  [1] "a" "b" "c" "d" "e" "f" "g" "h" "i" "j" "k" "l" "m" "n" "o" "p" "q" "r" "s"
    ## [20] "t" "u" "v" "w" "x" "y" "z"

``` r
upper_case <- c("A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z")

punctuation <- c(".", ",", "!", "?", "'", "\"", "(", ")", " ", "-", ";", ":")
punctuation
```

    ##  [1] "."  ","  "!"  "?"  "'"  "\"" "("  ")"  " "  "-"  ";"  ":"

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**:The first error was in uppercase, it had a double " The
second issue was in punctuation and for " to show up you have to do "

Make one long vector containing all the symbols.

``` r
my_symbols <- c(lower_case, upper_case, punctuation)
my_symbols
```

    ##  [1] "a"  "b"  "c"  "d"  "e"  "f"  "g"  "h"  "i"  "j"  "k"  "l"  "m"  "n"  "o" 
    ## [16] "p"  "q"  "r"  "s"  "t"  "u"  "v"  "w"  "x"  "y"  "z"  "A"  "B"  "C"  "D" 
    ## [31] "E"  "F"  "G"  "H"  "I"  "J"  "K"  "L"  "M"  "N"  "O"  "P"  "Q"  "R"  "S" 
    ## [46] "T"  "U"  "V"  "W"  "X"  "Y"  "Z"  "."  ","  "!"  "?"  "'"  "\"" "("  ")" 
    ## [61] " "  "-"  ";"  ":"

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**: cbind makes each vector a column, whereas c() just makes
it one long vector.

Turn the `my_symbols` vector into a data frame, with the variable name
“Symbol”.

``` r
my_symbols <- data.frame(my_symbols)
names(my_symbols) =  "Symbol"
my_symbols
```

    ##    Symbol
    ## 1       a
    ## 2       b
    ## 3       c
    ## 4       d
    ## 5       e
    ## 6       f
    ## 7       g
    ## 8       h
    ## 9       i
    ## 10      j
    ## 11      k
    ## 12      l
    ## 13      m
    ## 14      n
    ## 15      o
    ## 16      p
    ## 17      q
    ## 18      r
    ## 19      s
    ## 20      t
    ## 21      u
    ## 22      v
    ## 23      w
    ## 24      x
    ## 25      y
    ## 26      z
    ## 27      A
    ## 28      B
    ## 29      C
    ## 30      D
    ## 31      E
    ## 32      F
    ## 33      G
    ## 34      H
    ## 35      I
    ## 36      J
    ## 37      K
    ## 38      L
    ## 39      M
    ## 40      N
    ## 41      O
    ## 42      P
    ## 43      Q
    ## 44      R
    ## 45      S
    ## 46      T
    ## 47      U
    ## 48      V
    ## 49      W
    ## 50      X
    ## 51      Y
    ## 52      Z
    ## 53      .
    ## 54      ,
    ## 55      !
    ## 56      ?
    ## 57      '
    ## 58      "
    ## 59      (
    ## 60      )
    ## 61       
    ## 62      -
    ## 63      ;
    ## 64      :

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**: It requires Symbol to be a string

Find the total number of symbols we have in our data frame.

``` r
len <- nrow(my_symbols)
len
```

    ## [1] 64

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**: length() gives the number of variables, while nrow() gives
the number of observations.

5.  Create a new variable in your dataframe that assigns a number to
    each symbol.

``` r
my_symbols$Num <- 1:len
my_symbols
```

    ##    Symbol Num
    ## 1       a   1
    ## 2       b   2
    ## 3       c   3
    ## 4       d   4
    ## 5       e   5
    ## 6       f   6
    ## 7       g   7
    ## 8       h   8
    ## 9       i   9
    ## 10      j  10
    ## 11      k  11
    ## 12      l  12
    ## 13      m  13
    ## 14      n  14
    ## 15      o  15
    ## 16      p  16
    ## 17      q  17
    ## 18      r  18
    ## 19      s  19
    ## 20      t  20
    ## 21      u  21
    ## 22      v  22
    ## 23      w  23
    ## 24      x  24
    ## 25      y  25
    ## 26      z  26
    ## 27      A  27
    ## 28      B  28
    ## 29      C  29
    ## 30      D  30
    ## 31      E  31
    ## 32      F  32
    ## 33      G  33
    ## 34      H  34
    ## 35      I  35
    ## 36      J  36
    ## 37      K  37
    ## 38      L  38
    ## 39      M  39
    ## 40      N  40
    ## 41      O  41
    ## 42      P  42
    ## 43      Q  43
    ## 44      R  44
    ## 45      S  45
    ## 46      T  46
    ## 47      U  47
    ## 48      V  48
    ## 49      W  49
    ## 50      X  50
    ## 51      Y  51
    ## 52      Z  52
    ## 53      .  53
    ## 54      ,  54
    ## 55      !  55
    ## 56      ?  56
    ## 57      '  57
    ## 58      "  58
    ## 59      (  59
    ## 60      )  60
    ## 61         61
    ## 62      -  62
    ## 63      ;  63
    ## 64      :  64

Comment on what you noticed about the errors and how you used this
information to correct the issues.

**Response**: $ instead of % when accessing variables.

![](README-img/noun_pause.png) **Planned Pause Point**: If things made
sense, feel free to continue on while you wait. Otherwise, contact your
instructor to have them verify your work.

### Decoding the secret message.

This chunk will load up the encoded secret message data and assign it as
a vector. There are no errors here.

``` r
# Read in full csv file
top_secret <- readr::read_csv("data/secret_code.csv", col_names = FALSE)
```

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
    ## cols(
    ##   X1 = col_double()
    ## )

``` r
# Pick off only the column X1
top_secret <- top_secret$X1
```

By altering this top secret set of numbers, you will be able to create a
message. Write your own code to complete the steps below.

1.  Add 14 to every number.
2.  Multiply every number by 18, then subtract 257.
3.  Exponentiate every number. (That is, do e ^ \[each number\]. You may
    need to Google how to this!)
4.  Square every number.

``` r
top_secret <- top_secret + 14
top_secret <- (top_secret*18)-257
top_secret <- exp(top_secret)
top_secret <- top_secret*top_secret
```

**HQ UPDATE:** Headquarters has informed you that at this stage of
decoding, there should be 496 numbers in the secret message that are
below 17.

5.  Turn your vector of numbers into a matrix with 5 columns.
6.  Separately from your top secret numbers, create a vector of all the
    even numbers between 1 and 502. Name it “`evens`”. That is, `evens`
    should be an R object that contain the values 2, 4, 6, 8, …, 502.
7.  Subtract the “evens” vector from the first column of your secret
    message matrix.
8.  Subtract 100 from all numbers 18-24th rows of the 3rd column.
9.  Multiply all numbers in the 4th and 5th column by 2.
10. Turn your matrix back into a vector.

``` r
sum(top_secret<17)
```

    ## [1] 497

``` r
sum(top_secret)
```

    ## [1] 484325

``` r
top_secret_matrix <- matrix(data=top_secret, ncol=5)
evens <- seq(2, 502, 2)
top_secret_matrix[,1] <- top_secret_matrix[,1]-evens
top_secret_matrix[18:24,3] <- top_secret_matrix[18:24,3]-100
top_secret_matrix[,4:5] <- top_secret_matrix[,4:5]*2
top_secret <- c(top_secret_matrix)
top_secret
```

    ##    [1]   41    8   61   25    5    1    8   61   35   14   61   32   18    1
    ##   [15]   14    3    5   61    1   61   19   11    9   14   14   25   61   13
    ##   [29]    1   14   61    4    9    5    4   61   15   36 3721    1 3721    4
    ##   [43]   81   49 3721   16   81  361   25    1  361   25 3721  529   81 1521
    ##   [57]   64 3721    1 3721  144   81 1521 1521  144   25 3721  196    1  169
    ##   [71]   25 3721  784  625 3721    9   64    1  196    9   25 3721   64   81
    ##   [85]  361 3721   49   81  324  144   36  324   81   25  196   16 3721    9
    ##   [99]    1  169   25 3721    1    9  324  225  361  361 3721    1 3721  196
    ##  [113]   25   25   16  144   25 3721    1  196   16 3721  361  225  225  196
    ##  [127] 3721  361   64   25 3721   16   81   16 3721 1521   64   25 3721  361
    ##  [141]    1  169   25 3721  729 1521 3721   64  225  169   25 3721 1521   64
    ##  [155]   25  324   25 3721    1  324   25 3721  361   25  484   25  196 1521
    ##  [169]   25   25  196 3844  625   25    1  324 3844  225  144   16 3721    4
    ##  [183]  225  625  361 3721    1  196   16 3721 1521   64   25   81  324 3721
    ##  [197]   81   16   25    1 3721  225   36 3721   36  441  196 3721 1225  361
    ##  [211] 3721    4   25   81  196   49 3721   81  196 3721    1 3721   49    1
    ##  [225]  196   49 3721    9    1  144  144   25   16 3721 2116   64   25 3721
    ##  [239]  900   81  361    9   81  256  144   25  361 2916 3721   64   81   49
    ##  [253]   64 3721  225  196 3721    9  324    1    9  121 2916 3721 1521  225
    ##  [267] 1521   81  196 3249 3721    1 3721  169    1    9   64   81  196   25
    ##  [281] 3721   49  441  196 3721 2116   81  169   25 3721 2116   81  169   25
    ##  [295] 3721 3721 1156  441  324  324   81    9    1  196   25 3721  729  196
    ##  [309]  196   81   25 3721  324   81  256  256   25   16 3721 1521   64   25
    ##  [323] 3721    9   25   81  144   81  196   49 3721  225   36   36 3721    1
    ##  [337] 3721    9   64  441  324    9   64 3721    1  196   16 3721  121   81
    ##  [351]  144  144   25   16 3721   25  484   25  324  625  225  196   25 3721
    ##  [365]   81  196  361   81   16   25 3721 2601  225  441 3721 1521  441  324
    ##  [379]  196 3721  225  196 3721 1521   64   25 3721 1521   25  144  144  625
    ##  [393] 3721    1  196   16 3721   25  484   25  324  625 3721  225 1521   64
    ##  [407]   25  324 3721  361 1521  225  324  625 3721   81  361 3721 1521   25
    ##  [421]  144  144   81  196 3249 3721  625  225  441 3721  361  225  169   25
    ##  [435]    4  225   16  625 3721   16   81   25   16 3721 2025   81  361 1521
    ##  [449]   25  324 3721  121   81  144  144   25   16 3721   64   25  324 3721
    ##  [463]    4    1    4   25   61   57    3    1   21   19    5   61   19    8
    ##  [477]    5   61    3   15   21   12    4   14   57   39   61    1    6    6
    ##  [491]   15   18    4   61   39   15   61    6    5    5    4   61    9   39
    ##  [505]   61   27   14    4   61   23    5   57   18    5   61   19    5   14
    ##  [519]    4    9   14    7   61   16    5   15   16   12    5   61   39   15
    ##  [533]   61   39    8    5   61   13   15   15   14   61   45    5   16   39
    ##  [547]    5   13    2    5   18   61   13   25   61    3   15   21   19    9
    ##  [561]   14   61   39   18    9    5    4   61   18    5    5    6    5   18
    ##  [575]   61    6   15   18   61   39    8    5   61   22    5   18   25   61
    ##  [589]    6    9   18   19   39   61   39    9   13    5   61   40   15   23
    ##  [603]   61    8    5   57   19   61    4   15    9   14    7   61    8   15
    ##  [617]   18   19    5   63   61    9   39   57   19   61   36   21   14    5
    ##  [631]   61   46    9   13    5   61   46    9   13    5   61   61   35   39
    ##  [645]   57   19   61   19    9   12   12   25   54   61   14   15   56   61
    ##  [659]   49    8    5   14   61    1   61   18   15    3   11    5   39   61
    ##  [673]   19    8    9   16   61    5   24   16   12   15    4    5   19   61
    ##  [687]   27   14    4   61    5   22    5   18   25    2   15    4   25   61
    ##  [701]   19   39    9   12   12   61   23    1   14   39   19   61   39   15
    ##  [715]   61    6   12   25   61   45   15   13    5   61   19    1   25   61
    ##  [729]    1   61   13    1   14   61    1    9   14   57   39   61    8    1
    ##  [743]   16   16   25   61   47   14   12    5   19   19   61    1   61   13
    ##  [757]    1   14   61   39   18   21   12   25   61    4    9    5   19   61
    ##  [771]   41    8   54   61   23    8   25   56   61   46    9   13    5   61
    ##  [785]   46    9   13    5   61   61   28    1    2   25   61   13    1   11
    ##  [799]    5   61    1   61   19   16    5    5    3    8   54   61   19   39
    ##  [813]    1   18   61   23    1   18   19   61    6   12   25   61   40    5
    ##  [827]    9    7    8    2   15   18   19   61   10   21   19   39   61   19
    ##  [841]    8    9   14    5   61    9   39   61   15   14   61   28   21   39
    ##  [855]   61    9    6   61    1   61   14    9    7    8   39   61    6    1
    ##  [869]   12   12   19   61    1   14    4   61    1   61    2   15   13    2
    ##  [883]   61    6    1   12   12   19   61   49    9   12   12   61    1   14
    ##  [897]   25    2   15    4   25   61   19    5    5   61   39    8    5   61
    ##  [911]    4    1   23   14   61   46    9   13    5   61   46    9   13    5
    ##  [925]   61   61   35   19   61    9   39   61   19    9   12   12   25   54
    ##  [939]   61   14   15   56   61   49    8    5   14   61    1   61   18   15
    ##  [953]    3   11    5   39   61    2   12   15   23   19   61   21   16   61
    ##  [967]   27   14    4   61    5   22    5   18   25    2   15    4   25   61
    ##  [981]   19   39    9   12   12   61   23    1   14   39   19   61   39   15
    ##  [995]   61    6   12   25   61   45   15   13    5   61   19    1   25   61
    ## [1009]   13    1   14   61    1    9   14   57   39   61    8    1   16   16
    ## [1023]   25   54   61   39   18   21   12   25   61   47   14   39    9   12
    ## [1037]   61    1   61   13    1   14   61   39   18   21   12   25   61    4
    ## [1051]    9    5   19   61   41    8   54   61   23    8   25   56   61   41
    ## [1065]    8   54   61   23    8   25   56   61   45    9    7   14   61   15
    ## [1079]   57   61   39    8    5   61   46    9   13    5   19   61   46    9
    ## [1093]   13    5   61   46    9   13    5   61   61   45    9    7   14   61
    ## [1107]   15   57   61   39    8    5   61   39    9   13    5   19   61   13
    ## [1121]    5   19   19   61   23    9   39    8   61   25   15   21   18   61
    ## [1135]   13    9   14    4   61   34   21   18   18   25   61    2    5    6
    ## [1149]   15   18    5   61    9   39   57   19   61   39   15   15   61   12
    ## [1163]    1   39    5   61   38    5   39   57   19   61    6    1   12   12
    ## [1177]   61    9   14   61   12   15   22    5   54   61    7    5   39   61
    ## [1191]   13    1   18   18    9    5    4   54   61    8    1   22    5   61
    ## [1205]    1   61    2    1    2   25   61   49    5   57   12   12   61    3
    ## [1219]    1   12   12   61    8    9   13   61   40    1   39    5   54   61
    ## [1233]    9    6   61    9   39   57   19   61    1   61    2   15   25   61
    ## [1247]   46    9   13    5   61   46    9   13    5

**HQ UPDATE:** Headquarters has informed you that at this stage of
decoding, all numbers in indices 500 and beyond are below 100.

11. Take the square root of all numbers in indices 38 to 465.
12. Round all numbers to the nearest whole number.
13. Replace all instances of the number 39 with 20.

``` r
top_secret[38:465] <- sqrt(top_secret[38:465])
top_secret <- round(top_secret, 0)
top_secret[top_secret == 39] <- 20
```

**HQ UPDATE:** Headquarters has informed you that your final message
should have 421 even numbers.

``` r
x <- 0
for (n in top_secret){
  if (n %% 2 == 0){
    x <- x+1
  } 
}
x
```

    ## [1] 421

![](README-img/noun_pause.png) **Planned Pause Point**: If things made
sense, feel free to continue on while you wait. Otherwise, contact your
instructor to have them verify your work.

## The secret message!

Use your final vector of numbers as indices for `my_symbols` to discover
the final message, by running the following code:

``` r
stringr::str_c(my_symbols$Symbol[top_secret], collapse = "")
```

    ## [1] "Oh yeah In France a skinny man died of a big disease with a little name By chance his girlfriend came across a needle and soon she did the same At home there are seventeen-year-old boys and their idea of fun Is being in a gang called The Disciples, high on crack, totin' a machine gun Time Time  Hurricane Annie ripped the ceiling off a church and killed everyone inside You turn on the telly and every other story is tellin' you somebody died Sister killed her baby 'cause she couldn't afford to feed it And we're sending people to the moon September my cousin tried reefer for the very first time Now he's doing horse; it's June Time Time  It's silly, no? When a rocket ship explodes And everybody still wants to fly Some say a man ain't happy Unless a man truly dies Oh, why? Time Time  Baby make a speech, star wars fly Neighbors just shine it on But if a night falls and a bomb falls Will anybody see the dawn Time Time  Is it silly, no? When a rocket blows up And everybody still wants to fly Some say man ain't happy, truly Until a man truly dies Oh, why? Oh, why? Sign o' the Times Time Time  Sign o' the times mess with your mind Hurry before it's too late Let's fall in love, get married, have a baby We'll call him Nate, if it's a boy Time Time"

Google the first line of this message, if you do not recognize it, to
see what it is.

**delete this line and comment on what on the activity as a whole**

Comment on what you noticed about the activity as a whole.

**Response**: The activity used a lot of different functions to modify
vectors and matrices. The biggest thing that I noticed was the need to
store evey function you did.

Push your updated report to your `<username>` branch - you are done with
this `.Rmd` file and can go back to the README directions while you wait
for you Team Members.

## Attribution

This activity is based on a lab from [Dr. Kelly
Bodwin](https://www.kelly-bodwin.com/)’s Stat 331 course
