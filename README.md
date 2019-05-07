# Cordova crypt file plugin
HTML source file is encrypted at build, and decrypted at run.  
https://www.npmjs.com/package/cordova-plugin-cryptx-file

## Add Plugin
`cordova plugin add cordova-plugin-cryptx-file`

## Encrypt
`cordova build [ios / android]`

## Decrypt
`cordova emulate [ios / android]`  
or  
`cordova run [ios / android]`  

## Encryption subjects.

### Default

* .html
* .htm
* .js
* .css
* .png
* .jpg
* .ogg

### Edit subjects

You can specify the encryption subjects by editing `plugin.xml`.

**plugins/cordova-plugin-cryptx-file/plugin.xml**

```
<cryptfiles>
    <include>
        <file regex="\.(htm|html|js|css)$" />
    </include>
    <exclude>
        <file regex="exclude_file\.js$" />
    </exclude>
</cryptfiles>
```

Specify the target file as a regular expression.


## Supported platforms
* iOS
* Android
* CrossWalk

## Before reporting your issue
Use this URL https://github.com/tkyaji/cordova-plugin-crypt-file

## Based on the original cordova-crypt-file created by tkyaji

https://github.com/tkyaji/cordova-plugin-crypt-file

## License
Apache version 2.0
