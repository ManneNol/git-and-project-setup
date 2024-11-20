## Att arbeta med datorns konsol
### Olika specialkaraktärer och deras betydelser
- ~ = home-folder, beroende på OS. 
    - Windows: `C:\Users\<username>\`
    - Linux: `/home/<username>/`

### Olika kommandon
- cd = då hamnar jag i min home folder (~)

## Git
Git är en source code manager som vi ofta använder i vår vardag när vi arbetar
med kod. 

### Läs mer
- [Hur git ser på filer](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)
- [Grundläggande vim kommandon för git commit](TODO(manuel): lägg till länk här)

### Clone 
givet att jag är i ~/repos/
`$ git clone git@github.com:<repo-owner>/<repo-name>.git` gör följande:
1. se ifall ett projekt med `<repo-name>` finns på github med ägaren `<repo-owner>` och ifall vi får hämta den koden
2. skapa en lokal folder som heter `<repo-name>` i min ~/repos/ folder
3. gör den foldern till ett git repo (git init)
4. sätt ssh adressen som remote med namnet origin (`git remote add origin git@github.com:<repo-owner>/<repo-name>`)
5. gör en git pull på huvudbranchen (git pull)

#### Hur relaterar detta till git pull?
Git pull är två kommandon i ett.
1. `$ git fetch` (kollar i vår remote om det finns några förändringar)
2. `$ git merge origin/main` (kombinera vår lokala branch med vår remote branch)

#### Tips and tricks

- `<namn-på-remote>` = origin
- `<git-server-domain>` = github.com
- `<repo-owner>` = manuelnoltorp
- `<repo-name>` = git-and-project-setup
- `[local-folder-name]` = lektion-git-del-2

`git remote add <namn-på-remote> git@<git-server-domain>:<repo-owner>/<repo-name>.git`
`git remote add origin git@github.com:mannenol/git-and-project-setup.git`

`git clone git@github.com:<repo-owner>/<repo-name>.git [local-folder-name]`
`git clone git@github.com:mannenol/git-and-project-setup.git`

### Githubs relation till Git
Git är en SCM (source control manager) som kan användas lokalst eller i ett
distribuerat system. 

Github är en git-server med andra verktyg som vi använder för att synka våra
lokala git repositories med varandra


