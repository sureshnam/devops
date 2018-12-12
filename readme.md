# Waymo Models, Graphs and Artifacts 

## Setup
```
# Install git lfs for debian (Full instructions is here https://github.com/git-lfs/git-lfs/wiki/Installation )
echo 'deb http://http.debian.net/debian wheezy-backports main' > /etc/apt/sources.list.d/wheezy-backports-main.list
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
git lfs install

```
















































## How to manage `nnpi-transformer` and `ngraph` repos for standalone build

- Clone `nnpi-transformer` and build following the instructions above
- `ngraph` repo will be located at `nnpi-transformer/build/ngraph/src/ext_ngraph`
- In `ngraph` repo, we can make modifications, and perform git operations
- In `nnpi-transformer` repo, the build scripts will pick up the changes inside `ngraph` repo

## Code formatting before checkin any code changes

Format code with the format specified with `.clang-format`. Go to Root folder of the repo and give following commands
```
./maint/apply-code-format.sh
./maint/check-code-format.sh
