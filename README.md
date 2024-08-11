all dependencies+libraries+main app for kdenlive ubuntu arm64 can be using in repos
# getting the file
so now you can either get the file from releases but that is the old version and not recommended and will not work 
the recommended way is by cloning the repository and making the file so doing this is very easy just
```sh
git clone https://github.com/capt-dev/kdenlive-all-debs.git
```
to clone the repository you might also need to install the git package if it's not already installed 
after cloning the repository go into it
```sh
cd kdenlive-all-debs
```
probably expected that and now
```sh
cat kdenlive_part_* > kdenlive.tar.xz
```
and you got the file
for easier file getting
```sh
git clone https://github.com/capt-dev/kdenlive-all-debs.git && cd kdenlive-all-debs && cat kdenlive_part_* > kdenlive.tar.xz
```
you should now see the file...,to get a folder with all the dependencies extracted from the .tar.xz do
```sh
mkdir -p <name_of_folder> # replace <name_of_folder> with the desired name of folder with all dependencies
```
after this do
```sh
tar -xf kdenlive.tar.xz -C <name_of_folder>
```
they should make it so there are thousands of .deb files in the folder also if you want to install all of them in arm64 ubuntu you can do 
```sh
dpkg --force-all -i *.deb # this command expects that you are in the directory with all the dependency and app and libraries
```
the --force-all flag is needed because a lot of dependencies/libraries/applications are installed before their dependency/libraries required
