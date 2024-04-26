# ![logo](src/icons/48x48.png) WhatsApp in Sidebar

![Mozilla Add-on](https://img.shields.io/amo/v/{2b38cb05-9cff-44a7-b9f1-7cc575afab8a})
![Add-on rating](https://img.shields.io/amo/rating/{2b38cb05-9cff-44a7-b9f1-7cc575afab8a})
![Add-on downloads](https://img.shields.io/amo/dw/{2b38cb05-9cff-44a7-b9f1-7cc575afab8a})
![Add-on users](https://img.shields.io/amo/users/{2b38cb05-9cff-44a7-b9f1-7cc575afab8a})
![License](https://img.shields.io/github/license/semanticdata/firefox-new-tab-notes)

A Firefox extension to open WhatsApp Web within the Firefox sidebar. This extension adds a new section to the sidebar which contains the WhatsApp web app. It also adds a shortcut, and a button toggle within the toolbar.

[![Get the Addon](https://raw.githubusercontent.com/semanticdata/text-revealer-firefox-extension/master/firefox.png)](https://addons.mozilla.org/en-US/firefox/addon/whatsapp-in-sidebar/)

## Usage

1. Toggle the sidebar by pressing _`Alt+Shift+W`_. This shortcut can be changed by going to _`Add-ons` → `WhatsApp in Sidebar` → `Options`_.
2. If you prefer buttons over shortcuts, there is a toolbar button you can press to toggle the sidebar.

## How to Unlock Firefox Sidebar Width

The sidebar's width is _locked by default_ in Firefox. Unfortunately, the sidebar is very restrictive and I can only do so much to enhance the functionality of this extension. I put together a step-by-step guide on how to unlock it.

### Step-by-Step Instructions

1. In a new tab, navigate to `about:support`.
2. Under _Application Basics_, find _Profile Folder_.
3. Locate and click the `Open Folder` button next to it. It will be next to an address similar to: `%appdata%\Mozilla\Firefox\Profiles\{profile-id}.default`.
4. Inside your Firefox _Profile Folder_, create a new folder named: `chrome`.
5. Inside the newly created chrome folder, create a new file named: `userChrome.css`.
6. Copy the following code, paste as content and save:

```css
#sidebar-box {
  max-width: 40% !important;
  min-width: 300px !important;
}
```

7. Finally, in a new tab, navigate to `about:config` and search for `toolkit.legacyUserProfileCustomizations.stylesheets` and change it to `true`.
8. Restart Firefox and test it out!

### Notes

- You can find the canonical publication for the guide on my [Blog](https://miguelpimentel.do/unlock-firefox-sidebar/).  
- I also have instructions in Spanish in this GitHub [Gist](https://gist.github.com/semanticdata/ee0bca4f3617241aa98da114653c0b08#file-instrucciones-md).

## ⚠ Disclaimer

This extension is an independent project, has no relationship, and is not affiliated to WhatsApp or Meta in any way. This extension is primarily for personal use; a personal project if you will. This add-on _only_ launches their web app in the sidebar. WhatsApp™ is a registered trademark of Meta.

## 💜 Acknowledgments

Icons used for all my extensions are part of [UXWing](https://uxwing.com/)'s collection. Take a look at their [license](https://uxwing.com/license).

## © License

Source code in this repository is available under the [MIT License](LICENSE).
