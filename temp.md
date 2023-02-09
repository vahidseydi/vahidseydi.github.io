jekyll serve

git add -u
git commit -a -m ...
git push

jekyll build
cd \_site/  
git remote set-url origin https://github.com/vahidseydi/vahidseydi.github.io.git
git add .
