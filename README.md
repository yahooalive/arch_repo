# arch_repo

links like shown in arch doc won't work.
rename `arch_repo.db.tar.gz` and `arch_repo.files.tar.gz` to `arch_repo.db` and `arch_repo.files` after adding/removing packets.

## Links

- [db url](https://github.com/yahooalive/arch_repo/main/x86_64/arch_repo.db)
- [arch doc](https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository)
- [Arch Linux repository on github](https://www.arcolinuxiso.com/how-to-create-your-own-online-arch-linux-repository-on-github-and-use-it-on-any-arcolinux/)

## Commands

```sh
rm -r x86_64
mkdir x86_64
cd gnome-shell-extension-gsconnect-47
makepkg -f
mv *.tar.zst ../x86_64
cd ../imdb-tools
makepkg -f
mv *.tar.zst ../x86_64
cd ../x86_64
repo-add arch_repo.db.tar.gz *.tar.zst
mv arch_repo.db.tar.gz arch_repo.db
mv arch_repo.files.tar.gz arch_repo.files
```
