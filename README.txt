Marksheet Management System — GitHub Pages

Files
- index.html: the complete static website
- logo.jpg: default school result-sheet logo
- sidebar.jpg: image shown at the bottom of the left menu
- developer.png: developer profile image shown in the Developer panel

Publish
1. Create a GitHub repository and upload these four files to its root folder.
2. In the repository, open Settings > Pages.
3. Choose Deploy from a branch, select the main branch and / (root), then save.
4. Open the Pages URL GitHub provides.

The app automatically saves its data in browser storage (local storage and IndexedDB), including unfinished student drafts. Browser storage is tied to that browser/device, so use Backup > Download full JSON backup regularly as an independent copy.

Subject Management
- Open the Subject Management menu to configure each class separately.
- Add, edit, disable or delete subjects; set full and pass marks; choose Compulsory, Optional or Extra.
- Play, Nursery, KG, primary, secondary and higher secondary classes start with different editable subject lists.
- Class subject configurations are included in JSON, Excel and Google Drive backups.

Data transfer
- Use Data Transfer to download a JSON package, share it from a supported phone/browser, or import it on another device.
- For web-to-phone transfer, show the QR on the web page and scan each frame with the phone camera; the phone opens the site and stages the data there. Then choose Merge or Replace on the phone.
- Merge skips duplicate/incomplete student rows and can apply the incoming class-wise subject settings. Replace first downloads a copy of the current database.
- The phone uses its built-in camera to open each QR link; the website itself does not need camera access. For same-Wi-Fi transfer, serve the site on the PC and use its LAN URL (for example, http://192.168.1.x/index.html) in Data Transfer. A file:// page is local to one device and cannot be opened by another.
- QR generation and file sharing need an internet connection to load the app libraries and share support.
- This static website has no central server, so devices exchange data through a transfer file, QR frames, or the configured Google Drive backup.

Online backup
- The Backup page supports Google Drive. Publish the app on HTTPS first; Google sign-in will not work from a file:// URL.
- Configure Google Drive API and a Web application OAuth client in Google Cloud. Add the exact GitHub Pages URL as an authorized JavaScript origin, then paste the client ID into Backup > Online backup.
- Sign in and choose Back up now, or enable automatic backup while connected. The sign-in token is kept only in the current browser session.
- Other cloud providers need their own OAuth/app setup; a static website cannot securely connect to every account or service automatically.

The app loads chart, PDF, Excel and export libraries from public CDNs, so those features need an internet connection.
