# lab04
export GITHUB_USERNAME=samchik7
export GITHUB_TOKEN=token




cd ${GITHUB_USERNAME}/workspace
pushd .
~/samchik7/workspace ~/samchik7/workspace
source scripts/activate




\curl -sSL https://get.rvm.io | bash -s -- --ignore-dotfiles
Turning on ignore dotfiles mode.
Downloading https://github.com/rvm/rvm/archive/master.tar.gz
Upgrading the RVM installation in /Users/sam/.rvm/
Upgrade of RVM in /Users/sam/.rvm/ is complete
. scripts/activate
rvm autolibs disable
rvm install ruby-2.4.2 # При вводе этой команды вдается ошибка,которую я никак не могу исправить
.....





git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab04
Cloning into 'projects/lab04'...
remote: Enumerating objects: 32, done.
remote: Counting objects: 100% (32/32), done.
remote: Compressing objects: 100% (21/21), done.
remote: Total 32 (delta 6), reused 28 (delta 5), pack-reused 0 (from 0)
Receiving objects: 100% (32/32), 11.64 KiB | 1.29 MiB/s, done.
Resolving deltas: 100% (6/6), done.
cd projects/lab04
git remote remove origin
git remote add origin https://github.com/${GITHUB_USERNAME}/lab04





$ cat > .travis.yml <<EOF
language: cpp
EOF




$ cat >> .travis.yml <<EOF

script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
EOF



$ cat >> .travis.yml <<EOF

addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
EOF





ex -sc '1i|<фрагмент_вставки_значка>' -cx README.md




it add .travis.yml
git add README.md
git commit -m"added CI"
[main e1f13db] added CI
2 files changed, 2 insertions(+)
create mode 100644 .travis.yml










