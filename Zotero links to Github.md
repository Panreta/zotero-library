Sometimes, we want the pdf we drag into the local Zotero can be also put to Github.
For it not only give a remote repo. to store our pdf, but also can let our repo. looks more active :)
# 1. **Install Better BibTeX in Zotero**

1. Open Zotero
2. Go to **Tools** → **Add-ons**
3. Click the gear icon (⚙️) → **Install Add-on From File**
4. Download Better BibTeX from: [https://github.com/retorquere/zotero-better-bibtex/releases/latest](https://github.com/retorquere/zotero-better-bibtex/releases/latest)
5. Install the `.xpi` file
6. Restart Zotero

#  2. Set up automatic export

1. In Zotero, right-click "My Library"(or a collection)
2. Select **Export Library...**
3. Format: Choose **Better BibTeX** or **Better BibLaTeX**
4. ✅ Check **"Keep updated"**
5. Save to a folder path you want to put your .bib

Typically, .bib is the content of the papers you restore into Zotero in the academic form, arranged in json structure.

# 3.Create auto-sync script

If you don't want to write bash code to push every time, I definitely recommend a .bat here:

```bash
@echo off  
cd "your local path of the folder"
git add "My Library.bib "
git commit -m "Auto-update: %date% %time%" 
git push
```

"echo off" here means do not show the code out, @ means even for "echo off" it doesn't need to be shown on your screen. Technically, this file just works efficiently in silence.(Thank it!)

I didn't mention to create a repo. on Github here cuz you can search it out everywhere. And the info. of which repo. are pushing to is stored into .git in your folder.

---


So now, every time you put pdf into your Zotero, click sync.bat, it will send .bib immediately onto your Github repo