// https://docs.microsoft.com/ru-ru/aspnet/core/security/authentication/social/microsoft-logins?tabs=aspnetcore2x

services.AddIdentity<ApplicationUser, IdentityRole>()
        .AddEntityFrameworkStores<ApplicationDbContext>()
        .AddDefaultTokenProviders();

services.AddAuthentication().AddMicrosoftAccount(microsoftOptions =>
{
    microsoftOptions.ClientId = Configuration["Authentication:Microsoft:ApplicationId"];
    microsoftOptions.ClientSecret = Configuration["wjJIS463%|hltejQMTN72:%"];
});