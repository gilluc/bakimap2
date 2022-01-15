# bakimap
Python code to backup your IMAP accounts (really working and really FREE and opensource)
```
D:\GILLES\CIMAP>py bakimap.py
Server : imap.me.com, Account : me@me.com, Mode : NEW
Found folders:
        Spam
        Objets envoyés
        Courrier indésirable
        Corbeille
        Brouillons
        Sent
        INBOX
Folder : INBOX
        106 messages found
        106 messages saved
Folder : Sent
        55 messages found
        55 messages saved
D:\GILLES\CIMAP>
```

# the story
I just wanted to learn Python and to use it on deep learning with TensorFlow.
The step was too large.
As i have another need, i decided to switch.
I didn't find any free opensource IMAP backup solution anywhere so i decided to build one.
Everyone is aware that IMAP acounts need to be backed up ;-)

# the needs
- i have several IMAP accounts by different hosting companies to backup
- i want to do it with Python
- i want to recreate the same folder tree in my local disk as the folders tree in my IMAP account
- as i want to run my script quite often, i need an INCREMENTAL backup
- i want to save every message as a EML text file to be able to open it with my text editor of choice or any EML viewer

# the result
- i built a Python script !
- the script can backup only one IMAP account with the choice of its folders
- for each IMAP account, i duplicate the script under another name ...
- the script creates a subfolder using the name of the account
- the script creates a subfolder for each IMAP folder in the account subfolder
- each message is a EML file
- the script uses SSL protocol
- you have the choice of INCREMENTAL backup (recommended) or complete REBUILD of account backup to mirror the IMAP server

# my tests
- i used Python 3.9 on Windows 10
- i tested several accounts on [PlanetHoster](https://www.planethoster.com/fr/Hebergements-World) and [Free.fr](https://assistance.free.fr/articles/605)
- i backuped hundreds of messages
- i verified the messages using [Notepad++](https://notepad-plus-plus.org/downloads/v8.2/) and two free EML viewers i just found :
- [dalecoop EML viewer](https://www.01net.com/telecharger/windows/Internet/internet_utlitaire/fiches/130608.html) is great to open EML file by double clic
- [mitec mail viewer](https://mitec.cz/mailview.html) is great to open a folder containing EML files

# dependency
```
pip install IMAPClient
```

# now it's up to you
- after downloading bakimap.py, you have to set some parameters (as usual) before using it

```
# params
HOST     = "imap.me.com"
USERNAME = "me@me.com"
PASSWORD = "$$##$$"
FOLDERS  = ["INBOX", "Sent"]        # folder list to backup
BACKUP   = "NEW"   # "NEW" to backup only new messages (INCREMENTAL, recommended) or "RESET" to backup all messages to match exactly what is in IMAP server
```
