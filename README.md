i# Linux Lab1

--USAGE--------------------------------
Run the install file which will give permissions for Dlorg and also activate it. Dlorg will then create folders in your $HOME/Downloads for all your files and will check if the folders exists, if not re-build them and then filter all files into their correct folder.


Dlorg works in the following way
- We check if there are folders in $HOME/Downloads if there aren't any folders we create new once.
(Each folder is independent and we can add more folders afterwards if we want to).
- We  then check all files in $HOME/Downloads for file names backwards starting from the last . which gives us each file type.
- Each file type is assigned to a folder and more types can be added afterwards if needed.
- All of this happens in a While loop that restarts every 5 seconds meaning our Downloads folder will always sort all files into the correct folders.

!! A problem is that it currently replaces files of the same name in all folders which could be fixed if needed. !!






# För att kunna sortera filer in i mappar så krävs det att vi skapar en kod som tillåter dessa saker

# - Skapa mappar i en specific path.
# - Se om mapparna vi skapar redan finns
# - Sortera alla filer in i de olika mapparna och göra det lätt för oss att kunna lägga in flera fil typer om vi behöver kunna itirera.


# Med den tanken så börjar vi med att skapa en VIM som med kod vet att den ska städa den normala Downloads mappen
# Den ska
# - Checka om det finns folders som delar samma namn som den ska skapa
# - Om det fins mappar med de namnen skapa inte nya annars skapa nya
# Sortera alla filer till rätt map


# Swap
[._]*.s[a-v][a-z]
# comment out the next line if you don't need vector files
!*.svg
[._]*.sw[a-p]
[._]s[a-rt-v][a-z]
[._]ss[a-gi-z]
[._]sw[a-p]

# Session
Session.vim
Sessionx.vim

# Temporary
.netrwhist
*~
# Auto-generated tag files
tags
# Persistent undo
[._]*.un~

