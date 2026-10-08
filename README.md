# Linux Lab1
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

