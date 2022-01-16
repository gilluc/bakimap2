# bakimap2
Python code to backup your IMAP accounts (really working and really FREE and opensource).
Bakimap2 is mainly bakimap with IMAP accounts details read from a json file.
By default, bakimap2.py reads bakimap2.json.
You can put another json file instead of bakimap2.json in command line parameter like :
```
D:\GILLES\CIMAP>py bakimap2.py another_file.json
```
Example of first run output :
```
D:\GILLES\CIMAP>py bakimap2.py
Loading details from bakimap2.json
--------------------------------------------------------------
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
--------------------------------------------------------------
Server : imap.you.com, Account : you@you.com, Mode : NEW
Found folders:
        Spam
        Sent
        INBOX
Folder : INBOX
        44 messages found
        44 messages saved
--------------------------------------------------------------
D:\GILLES\CIMAP>
```

# more?
just go to gilluc/bakimap!

# dependency
```
pip install IMAPClient
```

# now it's up to you
After downloading bakimap.py, you have to set some parameters in bakimap2.json (as usual) before using it!
Remember : 
- "NEW" backup mode only saves new messages from last run (like incremental backup) : recommended!
- "RESET" backup mode delete existing saved messages and saves all messages found on IMAP host to mirror the folders account (mainly for me when testing)

```
{
    "imap_accounts": [
        {
            "HOST"     : "imap.me.com",
            "USERNAME" : "me@me.com",
            "PASSWORD" : "$$##$$",
            "FOLDERS"  : [ { "name": "INBOX" }, { "name": "Sent" } ],
            "BACKUP"   : "NEW"
        },
        {
            "HOST"     : "imap.you.com",
            "USERNAME" : "you@you.com",
            "PASSWORD" : "$$##$$",
            "FOLDERS"  : [ { "name": "INBOX" } ],
            "BACKUP"   : "NEW"
        }
    ]
}
```
