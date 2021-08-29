# Arch MBP iso

This symlink is needed so mkarchiso will be able to use local packages. You can remove it after building.

```sh
sudo ln -s $PWD/airootfs/usr/local/repo /usr/local/repo
sudo mkarchiso -v -C pacman.conf -A linux-mbp -L LINUX-MBP -w /tmp/work -o out .
```
After mkarchiso finishes, the iso will be in `./out/`. You can delete the `/tmp/work` directory once it's finished.

The message of the day (/etc/motd) has instructions on getting wifi working, but I don't know if it'll work for MBA8,1/2.
