# Miscellaneous scripts

Scripts that help maintain my sanity.

| Title            | Description                                                          |
| :---:            | :---:                                                                |
| add-cover        | embeds images in audio files                                         |
| add-song         | just edits a list of songs                                           |
| add-subtitles    | embed srt files into video                                           |
| allow-ip         | add rule to routing table for an IP address (e.g. a local printer)   |
| alphabetize      | sorts line alphabetically and deletes repeats                        |
| archive          | tar a directory and output to ~/Desktop with a unique filename       |
| backup           | backup home directory to external drive (up to 2 backups at once)    |
| battery-notify   | use notify-send to display when the battery level is too high or low |
| clipify          | cut clips out of videos                                              |
| copy-playist     | copy files in a playlist (e.g. m3u) to a destination directory       |
| count-commits    | count commits made by an author over specified period of time        |
| count-lines      | count number of lines in all files in directory                      |
| decrypt-secrets  | decrypt an encfs-encrypted folder                                    |
| delete-swp       | clear sw[a-p] files in directory (vim backups)                       |
| drop-caches      | clear system cache                                                   |
| encrypt-secrets  | (re)encrypt directory with encfs                                     |
| extract-audio    | extract audio track from video                                       |
| format           | format source code with language-specific tools                      |
| gen-playlist     | generate playlists based on beets database                           |
| get-song         | download song (audio) from url and set id3v2 metadata                |
| get-webseries    | youtube-dl wrapper to download web series / playlists / etc.         |
| gifify           | generate a gif from part of a video                                  |
| join-vids        | concatenate videos                                                   |
| kvm-clear        | clear out shared kvm directory                                       |
| kvm-cp           | copy file to shared kvm directory                                    |
| kvm-ls           | list files in shared kvm directory                                   |
| kvm-mv           | move file to shared kvm directory                                    |
| pdfsplit         | extract range of pages from a pdf                                    |
| print-colors     | print terminal colors                                                |
| rate-song        | write song rating metadata to beets database                         |
| reencode         | convert video's encoding                                             |
| rename-user      | rename an existing user and migrate all files, symlinks, etc.        |
| render           | compile LaTeX, RMarkdown and Julia Markdown files to PDF             |
| restart-network  | restart network connection (for getting new mac address)             |
| seek-and-destroy | find and delete pesky dotfiles and dotdirectories                    |
| set-gdm-theme    | overwrite the gdm theme with the css in the current gtk theme        |
| shrink-vm        | resize a qcow2 image                                                 |
| switch-theme     | switch gtk or icon theme (and edit vim/ui settings accordingly)      |
| upgrade          | upgrade system, aur, zsh plugins, and julia packages                 |
| vidname-cleanup  | use regex to clean up file names                                     |
| whattodo         | find all todo lists and print them in the terminal                   |
| write-entry      | write a entry into your log                                          |


## Globals

The `globals` file contains global variables that need to be set before running
specific scripts.

| Variable          | Description                                     | Required By                             |
| :---:             | :---:                                           | :---:                                   |
| archivedir           | destination for archive files                | archive                                 |
| backup1           | path to backup destination device               | backup                                  |
| backup2           | path of device to mirror backup1                | backup                                  |
| kvmdir            | directory containing kvm images                 | backup                                  |
| kvmshare          | shared (host<->guest) kvm directory             | kvm-clear,kvm-cp,kvm-ls,kvm-mv          |
| vboxdir           | directory with VirtualBox configs and images    | backup                                  |
| encryptpath       | encrypted encfs store (source)                  | decrypt-secrets,encrypt-secrets         |
| decryptpath       | decrypted encfs store (destination)             | decrypt-secrets,encrypt-secrets         |
| gtkdir            | directory that contains sources for gtk themes  | upgrade                                 |
| icondir           | directory that contains sources for icon themes | upgrade                                 |
| thunderbirddir    | directory containing thunderbird profile        | upgrade                                 |
| zshdir            | where zsh themes are downloaded                 | upgrade                                 |
| pkgbuilddir       | where AUR pkgbuilds are stored                  | seek-and-destroy,upgrade                |
| projectdir        | directory containing git repos and projects     | count-commits,seek-and-destroy,whattodo |
| musicdir          | directory containing music files in playlists   | copy-playlist                           |
| ignoreprojectdirs | list of directories in projectdir to ignore     | whattodo                                |
