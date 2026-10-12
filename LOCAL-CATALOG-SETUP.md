# Local catalog management

The local catalog backend uses Python 3's standard library and SQLite; it needs no package installation or internet connection.

1. Double-click `start-local.bat`. It starts the local server in a minimized window, waits for it to respond, and opens the admin page; if the server is already running, it simply opens the page. Keep the minimized server window open while using the site.
2. Open `http://127.0.0.1:8765` and select **Admin Login** in the header, or go directly to `http://127.0.0.1:8765/admin`.
3. Sign in to the Owner account with username `adminowner` and the current owner password. The password is stored as a salted hash in the local database.
4. Add or edit a listing, select its storefront section, and optionally upload an image. Use JPEG, PNG, WEBP, or GIF images up to 8 MB.
5. Open `http://127.0.0.1:8765` to view the storefront. Visible catalog changes appear in the selected section.

The admin page offers separate **Owner's Sign in** and **Developer Sign in** options. Owner sign-in uses username `adminowner` and the current Owner password. Developer sign-in uses username `Ebenezer` and password `iyanuoluwa200`. Both roles can manage the catalog; buyers cannot read or change admin listings without an authenticated session.

Owner passwords cannot be reset from this local admin page. Keep the current Owner credentials safe. Do not expose this backend to the public internet.

The first startup imports the current phone, laptop, gadget, repair, and spare-part listings into the editable catalog. Data is stored in `catalog.sqlite3`; uploaded images are stored in `uploads`. Keep both safe when backing up the site.

This development setup binds only to `127.0.0.1`, so it is available on this computer and is not a public website or a shared online admin system. Online use requires hosting and additional deployment security.
