# bakimap2
Python code to backup your IMAP accounts (really working and really FREE and opensource)
Bakimap2 is mainly bakimap with IMAP accounts details read from a json file.
By default, bakimap2.py reads bakimap2.json.
You can put another json file instead of bakimap2.json in command line parameter like 
```
D:\GILLES\CIMAP>py bakimap2.py another_file.json
```
First execution output:
```
D:\GILLES\CIMAP>py bakimap2.py
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
----------------------------------------
Server : imap.you.com, Account : you@you.com, Mode : NEW
Found folders:
        Spam
        Sent
        INBOX
Folder : INBOX
        44 messages found
        44 messages saved
----------------------------------------
D:\GILLES\CIMAP>
```

# more?
just go to gilluc/bakimap!

# dependency
```
pip install IMAPClient
```

# now it's up to you
- after downloading bakimap.py, you have to set some parameters in bakimap2.json (as usual) before using it

```
```
