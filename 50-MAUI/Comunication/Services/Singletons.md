# Singleton 
 Singleton pozwala udostępniać pojedyńczą instancje elementu w całym projektci, tak aby nie były one,
  tylko lokalnie dostępne np. w shered, ale wszędzie. /
  
## Urzycie:
`
 builder.Services.AddSingleton<Class>();
 builder.Services.AddSingleton<Object>();
`
`
    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();
            builder
                .UseMauiApp<App>()
                .ConfigureFonts(fonts =>
                {
                    fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
                });

            // Add device-specific services used by the MAUIAdvancePasswordGenerator.Shared project
            builder.Services.AddSingleton<IFormFactor, FormFactor>();
            builder.Services.AddMauiBlazorWebView();

            builder.Services.AddSingleton<Words>();
            builder.Services.AddSingleton<IWordStorageService, Words>();
            builder.Services.AddTransient<PasswordGenerator>();
#if DEBUG
            builder.Services.AddBlazorWebViewDeveloperTools();
            builder.Logging.AddDebug();
#endif

            return builder.Build();
        }
    }
}
`

