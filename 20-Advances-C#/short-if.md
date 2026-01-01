# Short if
warunek ? jeśli prawda : jeśli fałsz <br>
<br>
<br>
string nazwa = "aaa";
wynik =  nazwa ?? jeśli null to się wykona ta część
<br>
Jest jeszcze <br>
```
string nazwa = null;
nazwa ??= "aaaaa"  
```
Jeśli nazwa jest null to ??= się wywoła.
## Przykłady

### Przykład 1
```
int a = 5;
a > 4 ? return a : return 4
```

jeśli a > 4 wypisuje a, natomiast jeśli równe lub mniejsze to wypisze 4. 

<br>

### Przykład 2
```
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
