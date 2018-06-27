## freq 
A tiny stand alone (g)awk script to count word frequncies. 
It lowercases input, removes punctuation, and tallies the count of each value. 
(An easy to use stand-alone awk script, instead of having to load a function library from gawk itself.)  

### To install: 
`$chmod +x freq` <br/>
`$cp freq /usr/local/bin` (or somewhere in the your PATH)

### To use, a few examples:

#### Count the frequency of values in a (sql) script:
`$< ./createdb.ddl | freq | sort -rn -k2 | head -n 3` <br/>
`commit	2884` <br/>
`date	2096` <br/>
`tablespace	2094` <br/>

#### Count the frequency of all the words in the complete works of William Shakespeare: 
`$curl -s "http://www.gutenberg.org/files/100/100-0.txt" | freq | sort -rn -k2 | head` <br/>
`the	30002` <br/>
`and	28358` <br/>
`i	21867` <br/>
`to	20816` <br/>
`of	18815` <br/>
`a	15992` <br/>
`you	14437` <br/>
`my	13191` <br/>
`in	12032` <br/>
`that	11781`
