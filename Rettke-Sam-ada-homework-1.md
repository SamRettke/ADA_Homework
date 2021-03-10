Rettke-Sam-ada-homework-1
================
Sam Rettke
3/7/2021

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

## Challenge 1

load(tidyverse) f &lt;- read.delim(“darwin.txt”, header = TRUE)
length(f) length(f\[\[1\]\]) p34 &lt;- slice(f,34) print(p34) split
&lt;- str\_split(p34, boundary(“word”), n = Inf, simplify = FALSE) split
word\_list &lt;- as.data.frame(table(split)) word\_list
length(word\_list\[\[1\]\]) hightolow &lt;-
word\_list\[order(-word\_list$Freq),\] hightolow hightolow\[1, \] freq1
&lt;- filter(hightolow, Freq == 1) length(freq1\[\[1\]\]) freq5 &lt;-
filter(hightolow, Freq &gt;= 5) length(freq5\[\[1\]\]) p56 &lt;-
slice(f,56) final\_quote &lt;- tibble(p56\[\[1\]\]) print(final\_quote)
split\_quote &lt;- str\_split(final\_quote, boundary(“word”), n = Inf,
simplify = FALSE)

new3col &lt;- matrix( data = split\_quote\[\[1\]\], nrow = round(222/3),
ncol = 3, byrow = TRUE ) every\_third &lt;- new3col\[,3\]
print(every\_third) every\_third &lt;- sort(every\_third, decreasing =
TRUE) print(every\_third)

## Challenge 2

t &lt;- c(35, 88, 42, 84, 81, 30) city &lt;- c(“Beijing”, “Lagos”,
“Paris”, “Rio de Janeiro”, “San Juan”, “Toronto”) names(t) &lt;- city t
t\[1:3\] t\[3\] t\[5\]

## Challenge 3 (with original instructions)

m1 &lt;- matrix(data = 159:0, nrow = 8, ncol = 20, byrow = FALSE) m1\[8,
20\] &lt;- ’’ m1 print(m1\[5,2\]) print(m1\[5:7, 1:20\])

m2 &lt;- m1\[3:6, 4:9\] class(m2) mode(m2)

## Challenge 3 (with new instructions)

m1\_new &lt;- matrix(data = 160:1, nrow = 8, ncol = 20, byrow = FALSE)

## Challenge 4

evenlist &lt;- matrix(data = 800:1, nrow = 400, ncol = 2, byrow = TRUE)
evenlist &lt;- evenlist\[1:400,1:1\]

(a &lt;- array( evenlist, dim = c(5,5,4,4) ))

(a\[1, 1, 1, 2\]) (a\[2, 3, 2, \]) (a\[1:5, 1:5, 3, 3\])

## Challenge 5

names(Superfamily\_Lorisoidea) &lt;- c(“Lorisidae”, “Galagidae”)
names(Infraorder\_Lorisiformes) &lt;- c(“Superfamily\_Lorisoidea”)
names(Superfamily\_Lemuroidea) &lt;- c(“Cheirogaleidae”,
“Lepilemuridae”, “Indriidae”, “Lemuridae”, “Daubentoniidae”)
names(Infraorder\_Lemuriformes) &lt;- c(“Superfamily\_Lemuroidea”)
names(Suborder\_Strepsirrhini) &lt;- c(“Infraorder\_Lorisiformes”,
“Infraorder\_Lemuriformes”) names(Superfamily\_Tarsioidea) &lt;-
c(“Tarsiidae”) names(Infraorder\_Tarsiiformes) &lt;-
c(“Superfamily\_Tarsioidea”) names(Superfamily\_Ceboidea) &lt;-
c(“Cebidae”, “Atelidae”, “Pitheciidae”) names(Parvorder\_Platyrrhini)
&lt;- c(“Superfamily\_Ceboidea”) names(Superfamily\_Hominoidea) &lt;-
c(“Hylobatidae”, “Hominidae”) names(Superfamily\_Cercopithecoidea) &lt;-
c(“Cercopithecidae”) names(Parvorder\_Catarrhini) &lt;-
c(“Superfamily\_Hominoidea”, “Superfamily\_Cercopithecoidea”)
names(Infraorder\_Simiiformes) &lt;- c(“Parvorder\_Platyrrhini”,
“Parvorder\_Catarrhini”) names(Suborder\_Haplorhini) &lt;-
c(“Infraorder\_Tarsiiformes”, “Infraorder\_Simiiformes”)
names(Order\_Primates) &lt;- c(“Suborder\_Strepsirrhini”,
“Suborder\_Haplorhini”) Order\_Primates

Platyrrhini &lt;- Infraorder\_Simiiformes\[\[1\]\] print(Platyrrhini)
class(Platyrrhini) mode(Platyrrhini)

Infraorder\_Tarsiiformes$Superfamily\_Tarsioidea
