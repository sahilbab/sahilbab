mkdir TestRepo
cd TestRepo
git init

echo "This is the initial version of the article." > ARTICLE
git add ARTICLE
git commit -m "Initial commit: Add ARTICLE file"

echo "Adding more content to the article in the master branch." >> ARTICLE
git add ARTICLE
git commit -m "Update ARTICLE with additional content in master branch"


git branch feature-branch
git checkout feature-branch

echo "This is content added specifically in feature-branch." >> ARTICLE
git add ARTICLE
git commit -m "Add branch-specific content to ARTICLE in feature-branch"


git checkout master
git diff master feature-branch


git merge feature-branch

git status
git log --oneline
