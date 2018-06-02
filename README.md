# iOS-Backuper
Backup Your Phone Manually

## Dependency
Rsync (Get it from Cydia)

## Usage
1. Put files on /var/mobile
2. Run Command

(Backup)
```
cd /var/mobile && sh ./backup.sh
```

(Restore)
```
cd /var/mobile && sh ./restore.sh
```

## Explanation
To add files on backup list, you need to edit backuplist.lst.
Moreover, you have to add all directories that path to the file.

Once you added the path, you don't need to rewrite. 

If you want to backup preference files of "Asktocall", add the line like bottom.
```
+ /private/
+ /private/var/
+ /private/var/mobile/
+ /private/var/mobile/Library/
+ /private/var/mobile/Library/Preferences/
+ /private/var/mobile/Library/Preferences/me.deVbug.AskToCall.plist
```

"+" means that script will backup file (or folder), and "-" means excluding the directory.

To backup entire folder you want, add the line like bottom.
```
+ /private/var/**
```

## Thanks
Tools4hack (Original Script)
