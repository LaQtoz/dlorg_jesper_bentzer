i# Linux Lab1

Linux Lab 1 — Downloads Organizer

#--Usage-------------------------

Run the install file. It will:

Create the required directories.
Copy dlorg to the user's local bin directory.
Give dlorg execute permissions.
Install the systemd service.
Enable and start the service.

Once installed, dlorg will organize files in:

$HOME/Downloads

It will make sure the required folders exist and then sort files into the appropriate folder based on their file extension.


#--How Dlorg Works-------------------------

Dlorg works in the following way:

We check whether the required folders exist in $HOME/Downloads. If they don't exist, we create them.
Each folder is independent, so additional folders and file types can be added later if needed.
We then check all files in $HOME/Downloads and extract the file extension by looking at the last . in the filename.
Each file extension is assigned to a destination folder.
The program runs inside a while loop and checks the Downloads folder every 5 seconds.
This means new files can be automatically sorted without having to manually run the program again.

The general process is:

Downloads
    ↓
Check that category folders exist
    ↓
Find files
    ↓
Get file extension
    ↓
Determine destination folder
    ↓
Move file
    ↓
Wait 5 seconds
    ↓
Repeat


#--Known Problem-------------------------

There is currently a problem when two files have the same name and are moved into the same destination folder.

For example:

Downloads/photo.jpg
Images/photo.jpg

If dlorg tries to move Downloads/photo.jpg into Images, the existing file can be replaced.

This means the program currently has the potential to overwrite files.

A future improvement would be to detect duplicate filenames and rename the new file instead, for example:

photo.jpg
photo_1.jpg
photo_2.jpg

This would allow the Downloads folder to remain clean without losing existing files.


#--Planering-------------------------
# För att kunna sortera filer in i mappar så krävs det att vi skapar en kod som tillåter dessa saker

# - Skapa mappar i en specific path.
# - Se om mapparna vi skapar redan finns
# - Sortera alla filer in i de olika mapparna och göra det lätt för oss att kunna lägga in flera fil typer om vi behöver kunna itirera.


# Med den tanken så börjar vi med att skapa en VIM som med kod vet att den ska städa den normala Downloads mappen
# Den ska
# - Checka om det finns folders som delar samma namn som den ska skapa
# - Om det fins mappar med de namnen skapa inte nya annars skapa nya
# Sortera alla filer till rätt map

