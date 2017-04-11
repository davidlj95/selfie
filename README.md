# Selfie
An ASCII-version selfie of myself, presented using a little Jekyll website that includes the text file


## How-to
How can you do the same? Easily explained in 13 steps!
### Requirements
 - `Git` knowledge basics
 - `HTML5, CSS3` knowledge basics
 - `Jekyll` to test the website locally
 - `An Android phone` to use the application
1. **Downloaded _AsciiCam_ Android application:**
   [_AsciiCam_ in the _Google Play Store_](https://play.google.com/store/apps/details?id=com.dozingcatsoftware.asciicam)
   I've found [this](https://itunes.apple.com/us/app/ascii-camera/id659908678?mt=8) for _iPhone_ but not tested it
2. **Took a selfie**
   Using default camera application on my Xiaomi Redmi Note 4 (no filters ;))
3. **Imported the recently taken selfie**
   Using the button with an _a_ letter in the right bar of the _AsciiCam_ application
4. **Exported the picture to my personal Google Drive**
   Using the `Share Picture -> Share Text` option and then `Save to Google Drive` from the _Android UI_
5. **Created a basic _Jekyll_ site**
   Using the following commands:
   1. Create the project folder
      `jekyll new selfie`
   2. Change into the project folder
      `cd selfie`
   3. Created `_config.yml`, `_layouts/default.html`, `_includes/head.html`, `_includes/content.html`, modified `index.html` and added some assets (a _CSS_ file and some _favicons_ with its browser-specific definitions)
      - Using sources from [uab.codes](https://www.uab.codes) website as a template
      - In `_includes/content.html` the key is to include the text photo as a block of text:
      ```html
      <pre>{% include photo.txt %}</pre>
      ```
6. **Copied the photo as text to the `_includes` folder and `assets/txt` folder**
   To the `_includes` folder so the text can be included using _Jekyll_ and to the `assets/txt` folder so it lives online as a separated text resource
7. **Created a _Git_ repository, and added main files**
   To create an empty _Git_ repository:
   `git init .`
   Then added some files:
    - `.gitignore` (_Jekyll template from [GitHub gitignores](https://raw.githubusercontent.com/github/gitignore/master/Jekyll.gitignore)_)
    - `.gitattributes` to always checkout the same UNIX-like EOL
    - `README.md` describing the steps to create the project
    - `LICENSE` the license of the project
    - `CNAME` file to set a custom domain to the _GitHub Pages_ project

   Added and commited those files:
   `git add .git* README.md CNAME && git commit -m "Initial commit"`
8. **Add the project files too**
   Commit the project files
   `git add * && git commit -m "First site"`
9. **Created an empty repository in GitHub**
   Using the GitHub website. I create one named `selfie`, without including a `README` or `LICENSE` to create an empty repo
10. **Added a remote**
   Set a git remote
   `git remote add github git@github.com:davidlj95/selfie`
11. **Push changes to the remote**
   `git push -u github master`
12. **Set the project as a _GitHub Pages_ project**
    In the repository settings page in _GitHub_, section _GitHub Pages_, select `master` as _Source_ and `Save`
13. **Enjoy it**
