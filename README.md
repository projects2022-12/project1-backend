# project1-backend

# Info pagal kuri sukuriau API

https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-7.0&tabs=visual-studio-code

# .NET 7 Install

wget https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb

sudo dpkg -i packages-microsoft-prod.deb

sudo apt install -f

rm packages-microsoft-prod.deb

sudo apt-get update

sudo apt-get install -y dotnet-sdk-7.0

sudo apt-get install -y aspnetcore-runtime-7.0

## Patikrinti ar intaliuota .NET 7

dotnet --list-sdks

dotnet --list-runtimes

# Add NuGet packages, turbut reikia nepakenks

cd i folder kurame su ls matosi Program.cs, User.cs ir kiti failai ir folderiai.

dotnet add package Microsoft.EntityFrameworkCore.InMemory

dotnet add package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore

# Run backend

dotnet run


# API komandos, pas mane port 5126, jei kitaip tai visur si skaiciu pakeisk

# POST, komanda issaugo viena zmogu, veikia kaip registracija vieno userio

http://localhost:5126/useritems

JSON body:

{
  "UserName":"interUserName",
  "Email":"test@email.com",
  "Password":"nhustpfgha56"
}

# GET, komanda grazina visus su POST issaugotus userius

http://localhost:5126/useritems

JSON body:

Tuscias, jo nereikia.

Turetu grazinti runinus su GET request:

[
    {
        "id": 1,
        "userName": "interUserName",
        "email": "test@email.com",
        "password": "nhustpfgha56"
    }
]
