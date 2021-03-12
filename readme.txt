1.CREATE SLN File
dotnew new SLN

2.CREATE API
DOTNET NEW WEBAPI -o FOLDERNAME
3.ADD API TO SLN
DOTNET SLN ADD API
4.dev-certs
dotnet dev-certs https -t
5.in folder API
dotnet tool list -g
dotnet tool install --global dotnet-ef --version 5.0.4
from nuget Galley

6. db migration
dotnet ef migrations add InitialCrate -o Data/Migrations
and should be install Microsoft.EntityFrameworkCore.Design

7.dotnet ef database update

skinet folder
8.dotnet new classlib -o Core

9.dotnet new classlib -o Infrastructure

10.dotnet sln add Infrastructure/

11.dotnet sln add Core/

into API folder
12.dotnet add reference ../Infrastructure

into Infrastructure
13.dotnet add reference ../Core
into skinet
14.dotnet restore


15. dotnet ef database drop -p Infrastructure -s API
16. dotnet ef migrations remove -p Infrastructure -s API
17. dotnet ef migrations add InitialCreate -p Infrastructure -s API -o Data/Migrations