# StateHasChanged
Niepozorna metoda w Razor, wymuszająca ponowne załadowanie strony.
Renderuje ponownie stronę.
Niezbędna do wyświetlania zmian wywyłanych async. 

## Przykłady

### Przykładd 1
```charp
private async void GeneratePassword()
{
    System.Diagnostics.Debug.WriteLine("Generate Password Clicked");

    if (PasswordValid())
    {
        ResetAlerts();
        ResetPasswords();
        AlertMessage = "Generating Password... \n";
        passwordGeneratorInput = new
       (
           passwordLength: PasswordLength,
           isIncludeLowercase: PasswordIncludeLowercase,
           isIncludeUppercase: PasswordIncludeUppercase,
           isIncludeNumbers: PasswordIncludeNumbers,
           isIncludeSymbols: PasswordIncludeSymbols
       );
        passwordGeneratorOutput = Generator.Generate(passwordGeneratorInput);
        SuccessMessage += "Password Generated";
    }
    else
    {
        ErrorMessage = "ERROR GeneratePassword";
        ErrorMessage = $"PasswordIncludeLowercase: {PasswordIncludeLowercase}, PasswordIncludeUppercase: {PasswordIncludeUppercase}, PassowrdIncludeNumbers: {PasswordIncludeNumbers}, PassowrdIncludeSymbols: {PasswordIncludeSymbols}, ";
    }
 -> !!!TU JEST!!!    StateHasChanged();
}
private async void GenerateWordPassword()
{
    System.Diagnostics.Debug.WriteLine("Generate Word Password Clicked");
    try
    {
        if (WordPasswordLength > 0)
        {
            ResetAlerts();
            ResetPasswords();
            AlertMessage = "Generating Password... \n";
            AlertMessage += "Loading 370000 words to generator.";
            wordPasswordGeneratorInput = new
                (
                    passwordWords:WordPasswordLength,
                    passwordSeperator: WordPasswordSeparator,
                    includeLowercaseLength: IncludeLowercase  == true ? WordPasswordIncludeLowercaseLength : 0 ,
                    includeUppercaseLength: IncludeUppercase == true ? WordPasswordIncludeUppercaseLength : 0,
                    includeNumbersLength: IncludeNumbers == true ? WordPasswordIncludeNumbersLength : 0,
                    includeSymbolsLength: IncludeSymbols == true ? WordPasswordIncludeSymbolsLength : 0,
                    includeFirstLetersUpercaseLength: IncludeFirstLettersUppercase == true ? WordPasswordIncludeFirstLettersUppercaseLength : 0
                );
            wordPasswordGeneratorOutput = await Generator.Generate(wordPasswordGeneratorInput);
            SuccessMessage += "Password Generated";
      -> !!!TU JEST!!!       StateHasChanged();
        }
    }catch (Exception ex)
    {
        ErrorMessage = ex.Message;
    }

}
```
