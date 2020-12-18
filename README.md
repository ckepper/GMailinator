# GMailinator

Adds Gmail-esque keyboard shorcuts to Mail.app.  This is still very much a work
in progress.

Tested with Mail for OS X Cataina.

## Supported Shortcuts

| Key    | Action                         |
| :----: | ------------------------------ |
| #      | Delete                         |
| /      | Mailbox search                 |
| !      | Toggle message as Junk         |
| c      | Compose new message            |
| e, y   | Archive                        |
| f      | Forward message                |
| G      | Go to the last message         |
| g      | Go to the first message        |
| j      | Go to next message/thread      |
| k      | Go to previous message/thread  |
| l      | Move to folder (opens dialog)  |
| o      | Open selected message          |
| R      | Reply All                      |
| r      | Reply                          |
| s      | Flag                           |
| u      | Mark message as read           |
| U      | Mark message as unread         |
| v      | View raw message dialog        |
| z      | Undo                           |

## How to install

1. Grab the latest build from Github releases
2. Unzip to ~/Library/Mail/Bundles
3. Enable Mail.app plugins:
       `defaults write com.apple.mail EnableBundles -bool true`

## How to install (Mojave onwards)
1. Build the project or download it from Github releases
2. In the Finder, open /tmp/Gmailinator and ~/Library/Mail/Bundles
3. Copy the GMailinator.mailbundle folder from /tmp/Gmailinator to ~/Library/Mail/Bundles
4. In mail, open Preferences -> General -> Manage Plug-ins, and enable Gmailinator.
5. You will be prompted to restart Mail

### Add Gatekeeper Exception (Big Sur onwards)

The following command will tell Gatekeeper to allow the plug-in to be enabled:

`spctl --add /tmp/GMailinator/GMailinator.mailbundle`

## Credits

A lot of this was built with heavy use of of the
[BindDeleteKeyToArchive](https://github.com/benlenarts/BindDeleteKeyToArchive)
project by Ben Lenarts.  The Xcode project and interface skeleton were
all from that project, and for the most part, renamed.  I added the keybinding code.

A lot of the code is also either copied in whole, or modified from the
Nostalgy4Mail.app project, by [Hajo Nils
Krabbenhöft](https://github.com/fxtentacle/Nostalgy-4-Mail.app), and
subsequently by [Jelmer van der
Linde](https://github.com/jelmervdl/Nostalgy-4-Mail.app). I've added support
for ARC (turns out there were quite a few leaks), and prettied-up (imho) the
move-to-folder dialog.

Other references:

- [Rui Carmo's PyObjC vim keybinding script](http://taoofmac.com/space/blog/2011/08/13/2110)
