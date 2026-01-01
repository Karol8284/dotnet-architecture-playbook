# Short if
? : <br>
warunek ? jeśli prawda : jeśli fałsz <br>
<br>
??
<br>
string nazwa = "aaa";  <br>
wynik =  nazwa ?? jeśli null to się wykona ta część
<br>
??=
<br>
string nazwa = null;
nazwa ??= "aaaaa"  <br>
Jeśli nazwa jest null to ??= się wywoła.
## Przykłady

### Przykład 1
```charp
int a = 5;
a > 4 ? return a : return 4
```

jeśli a > 4 wypisuje a, natomiast jeśli równe lub mniejsze to wypisze 4. 

<br>

### Przykład 2
```charp
string nazwa = null;
string wynik = nazwa ??= "aaaaa"   
```
wnik będzie równy nazaw ale jeśli nazwa jest null to w tedy "aaaaa".
### Przykład 3
```charp
wordPasswordGeneratorInput = new
    (
        passwordWords:WordPassordLength,
        passwordSeperator: WordPasswordSeperator,
        includeLowercaseLength: IncludeLowercase  == true ? WordPasswordIncludeLowercaseLength : 0 ,
        includeUppercaseLength: IncludeUppercase == true ? WordPasswordIncludeUppercaseLength : 0,
        includeNumbersLength: IncludeNumbers == true ? WordPasswordIncludeNumbersLength : 0,
        includeSymbolsLength: IncludeSymbols == true ? WordPasswordIncludeSymbolsLength : 0,
        includeFirstLetersUpercaseLength: IncludeFirstLittersUpercase == true ? WordPasswordIncludeFirstLetersUpercaseLength : 0
    );
```
Fragment z mojego generatora haseł.
