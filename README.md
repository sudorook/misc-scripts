# Miscellaneous scripts

| Script             | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- |
| `add-subtitles`    | embed srt files into video                                             |
| `allow-ip`         | add rule to routing table for an IP address (e.g. a local printer)     |
| `alphabetize`      | sorts line alphabetically and deletes repeats                          |
| `archive`          | tar a directory and output to ~/Desktop with a unique filename         |
| `backup`           | backup home directory to external drive (up to 2 backups at once)      |
| `battery-notify`   | use `notify-send` to display when the battery level is too high or low |
| `cleanup`          | wrapper script for cleanup programs                                    |
| `clipify`          | cut clips out of videos                                                |
| `copy-playlist`    | copy files in a playlist (e.g. m3u) to a destination directory         |
| `count-commits`    | count commits made by an author over specified period of time          |
| `count-lines`      | count number of lines in all files in directory                        |
| `coverart`         | embeds or remove images in audio files                                 |
| `cryptdir`         | wrapper for mounting/unmounting fs-level encrypted directories         |
| `decode-base64`    | detect and convert base64 text in emails to UTF-8                      |
| `delete-swp`       | clear sw[a-p] files in directory (Vim backups)                         |
| `drop-caches`      | clear system cache                                                     |
| `dump-streams`     | copy container streams into one file each                              |
| `embed-script`     | combine executable script and source dependencies into one file        |
| `encfs-decrypt`    | mount and decrypt an EncFS-encrypted directory                         |
| `encfs-encrypt`    | (re)encrypt directory with EncFS                                       |
| `epub-convert`     | `ebook-convert` wrapper to convert azw3 and mobi files to ePub         |
| `epub-fixup`       | disable `text-align: justify` and hardcoded colors in EPUB files       |
| `extract-audio`    | extract audio track from video                                         |
| `extract-subs`     | extract all subtitle streams from video                                |
| `format`           | format source code with language-specific tools                        |
| `gen-playlist`     | generate playlists based on beets database                             |
| `get-song`         | download song (audio) from URL and set ID3v2 metadata                  |
| `get-webseries`    | `youtube-dl` wrapper to download web series / playlists / etc.         |
| `gifify`           | generate a GIF from part of a video                                    |
| `git-archive`      | simple wrapper for git archive                                         |
| `git-clone-all`    | clone all repositories of a GitHub user/organization                   |
| `git-gc`           | prune orphaned objects and force garbage collection                    |
| `git-init`         | wrapper script for initializing a Git repo and setting the metadata    |
| `git-partial-push` | push commits up to a given date                                        |
| `join-vids`        | concatenate videos                                                     |
| `kvm-clear`        | clear out shared KVM directory                                         |
| `kvm-cp`           | copy file to shared KVM directory                                      |
| `kvm-ls`           | list files in shared KVM directory                                     |
| `kvm-mv`           | move file to shared KVM directory                                      |
| `list-ass-fonts`   | list all the fonts referenced in a subtitle file or directory          |
| `make-watch`       | re-run `make` when files changes are written                           |
| `mpv-play`         | play media above a duration cutoff                                     |
| `mpv-ssh`          | search remote directories over SSH and pipe as playlist to mpv         |
| `nm-ovpn-delete`   | delete OpenVPN connections via `nmcli`                                 |
| `nm-ovpn-import`   | `nmcli` wrapper for importing an OpenVPN configuration file            |
| `nm-wg-delete`     | delete all WireGuard connection definitions using Network Manager      |
| `nm-wg-import`     | import a WireGuard configuration file using Network Manager            |
| `ova-to-qcow2`     | convert an OVA virtual disk image to QCOW2                             |
| `pdf-fixup`        | fix up the metadata in PDF files (newlines in tags, covers, etc.)      |
| `pdf-split`        | extract range of pages from a PDF                                      |
| `ping-test`        | use `ping` to estimate network speed                                   |
| `print-colors`     | print terminal colors                                                  |
| `print-fontstring` | generate the FFmpeg format string to embed fonts in a container        |
| `quickdate`        | wrapper for generating date strings based on a specified offset        |
| `rank-mirrorlist`  | rank all servers listed in /etc/pacman.d/mirrorlist                    |
| `rate-song`        | write song rating metadata to beets database                           |
| `reencode`         | convert video's encoding                                               |
| `rename-user`      | rename an existing user and migrate all files, symlinks, etc.          |
| `render`           | compile LaTeX, RMarkdown and Julia Markdown files to PDF               |
| `restart-network`  | restart network connection (for getting new MAC address)               |
| `rmlink`           | delete symlink and the file it references                              |
| `rotate`           | rotate the screen with `xrandr` and switch background theme            |
| `scourify`         | wrapper to scour for simplifying SVG files                             |
| `search-docs`      | find documents, with option to pin to ~/Desktop and ~/Sync             |
| `seek-and-destroy` | find and delete pesky dotfiles and dot-directories                     |
| `set-gdm-theme`    | overwrite the GDM theme with the CSS in the current GTK theme          |
| `set-replaygain`   | compute replay gain for directory of audio files                       |
| `shrink-vm`        | resize a qcow2 image                                                   |
| `split-cue`        | use a CUE file to split a single large audio file into MP3 components  |
| `strip-audio`      | use `ffmpeg` to strip metadata from FLAC and MP3 files                 |
| `strip-metadata`   | remove metadata from MKV and MP4 containers and streams                |
| `strip-yaml`       | strip YAML front matter from text file                                 |
| `swapfile`         | create or destroy swapfile                                             |
| `swap-symlink`     | switch around a symlink and its reference location                     |
| `switch-theme`     | switch GTK or icon theme (and edit Vim/UI settings accordingly)        |
| `torrentstat-sync` | synchronize statistics between Transmission and qBittorrent            |
| `upgrade`          | upgrade system, AUR, Zsh plugins, and Julia packages                   |
| `vidname-cleanup`  | use regex to clean up file names                                       |
| `vpn-killswitch`   | add `iptables` rules to block networking if VPN connection is lost     |
| `wget-mirror`      | `wget` wrapper to create local mirror of website                       |
| `whattodo`         | find all to-do lists and print them in the terminal                    |
| `write-entry`      | write a entry into your log                                            |

## Globals

The `globals` file contains global variables that need to be set before running
specific scripts.

| Variable          | Description                                     | Required By                                     |
| ----------------- | ----------------------------------------------- | ----------------------------------------------- |
| archivedir        | destination for archive files                   | `archive`                                       |
| backup1           | path to backup destination device               | `backup`                                        |
| backup2           | path of device to mirror backup1                | `backup`                                        |
| calibrelibrarydir | path to Calibre library directory               | `search-docs`                                   |
| kvmdir            | directory containing KVM images                 | `backup`                                        |
| kvmshare          | shared (host <--> guest) KVM directory          | `kvm-clear`, `kvm-cp`, `kvm-ls`, `kvm-mv`       |
| vboxdir           | directory with VirtualBox configs and images    | `backup`                                        |
| encryptpath       | encrypted EncFS store (source)                  | `cryptdir`                                      |
| decryptpath       | decrypted EncFS store (destination)             | `cryptdir`                                      |
| gtkdir            | directory that contains sources for GTK themes  | `upgrade`                                       |
| plasmadir         | directory containing Plasma themes source repos | `upgrade`                                       |
| icondir           | directory that contains sources for icon themes | `upgrade`                                       |
| thunderbirddir    | path to Thunderbird profile directory           | `upgrade`                                       |
| zshdir            | where Zsh themes are downloaded                 | `upgrade`                                       |
| pkgbuilddir       | where AUR pkgbuilds are stored                  | `seek-and-destroy`, `upgrade`                   |
| projectdir        | directory containing Git repos and projects     | `count-commits`, `seek-and-destroy`, `whattodo` |
| musicdir          | directory containing music files                | `copy-playlist`                                 |
| videodir          | directory for video files                       | `get-webseries`                                 |
| ignoreprojectdirs | list of directories in projectdir to ignore     | `whattodo`                                      |
| zoterodatadir     | location of Zotero data (not config) directory  | `search-docs`                                   |
