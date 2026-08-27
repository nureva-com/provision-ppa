# provision-ppa

PPA repository for provision system packages to be used in a RPi Secure Boot Provisioner system.

## Usage

To use this PPA:

```bash
curl -s --compressed "https://nureva-com.github.io/provision-ppa/KEY.gpg" | gpg --dearmor | sudo tee /usr/share/keyrings/nureva-provision-archive-keyring.gpg
sudo curl -s --compressed -o /etc/apt/sources.list.d/nureva-provision.list "https://nureva-com.github.io/provision-ppa/nureva-provisio<n.list"
sudo apt update
sudo apt-get install -y <package from this repository>
```

## Updating/adding new Packages to the PPA

Put your new .deb files inside the git repo and run `./bin/generate.sh` to
update the files. Then commit and push to repo.
