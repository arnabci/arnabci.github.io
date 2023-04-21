This is my blog!


Customize the _config.yml:

1. Added my URL in ```url``` section and kept ```baseurl``` empty.

2. Save!


To enable automatic deployment:

1. Click on Actions tab and Enable GitHub Actions; do not worry about creating any workflows as everything has already been set for you.

2. Go to ```Settings -> Actions -> General -> Workflow``` permissions, and give Read and write permissions to GitHub Actions.

3. Make any other changes to your webpage, commit, and push. This will automatically trigger the Deploy action. I just made a change into the README.md file.

4. Wait for a few minutes and let the action complete. You can see the progress in the Actions tab. If completed successfully, in addition to the ```main``` branch, your repository should now have a newly built ```gh-pages``` branch.

5. Finally, in the Settings of your repository, in the Pages section, set the branch to ```gh-pages``` and NOT to ```main```.


To start re-editing thee blog:

1. Install Jekyll.

```
sudo dnf install ruby rubygems ruby-devel gcc gcc-c++ rpm-build
```
```
sudo gem install jekyll bundler
```
```
jekyll -v
```

2. Install Bundle.
```
sudo bundle install
```

3. Start the server offline by going into the blog directory.
```
bundle exec jekyll serve
```

GIT auto-commit:

1. Check if GIT is installed.
```
git version
```

2. If not already present, create a ```.git-credentials``` file in the ```~/``` directory.
```
nano .git-credentials
```

3. Add the following line into the ```.git-credentials``` file.
```
https://<github-user>:<unique-access-token>@github.com
```

4. Run the below commands to make sure caching is enabled.
```
git config --global credential.helper store
```
```
git config --global credential.helper cache
```