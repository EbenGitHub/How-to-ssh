# How-to-ssh
1. Create an SSH key in your local terminal
```bash
ssh-keygen -t ed25519 -C "yshmarov@gmail.com"
```
> Just hit enter, `do not enter any password`.
2. Start ssh agent, “Use” the generated key (in my case id_ed25519):
```bash
eval `ssh-agent -s`
ssh-add ~/.ssh/id_ed25519.pub
```
3. Open the key file
```bash
cat ~/.ssh/id_ed25519.pub
```
4. Copy everything from the file
5. Paste the key to github SSH creator, give it any name
6. Check if you are connected to github. Console:
```bash
ssh -T git@github.com
```
7. Connect to remote repo via SSH
```bash
git remote -v
```
```bash
https://[github]/USERNAME/REPOSITORY.git
```
```bash
git@github.com:USERNAME/REPOSITORY.git
```
```bash
git push
```
8. Configure your git if you have not done yet
```bash
git config --global user.name "Yaro"
git config --global user.email yshmarov@gmail.com
```
