SolarSquare Presales Dashboard — GitHub Pages package

FILES
- index.html: self-contained dashboard with the requested username/password screen.

DEPLOYMENT
1. Create a GitHub repository.
2. Upload index.html to the repository root (top level, not inside another folder).
3. Open repository Settings → Pages.
4. Under Build and deployment, choose Deploy from a branch.
5. Select branch main and folder /(root), then Save.
6. When deployment completes, open the site URL shown in Settings → Pages.

IMPORTANT SECURITY NOTE
The requested admin/admin screen is only a basic client-side gate. The username and password are present in the downloaded page's JavaScript and can be discovered by anyone. The dashboard also downloads its data from a publicly published Google Sheets CSV URL, which can be opened directly without logging in. GitHub Pages serves public static content; this login does NOT secure confidential data or restrict who can access the CSV. Do not use this approach for sensitive/company-confidential data. Real access control requires server-side authentication and a private data source/API (for example, Supabase Auth with protected server-side/RLS access).

ABOUT THE OTHER UPLOADED FILES
The supplied HTML already contains all styling and both required JavaScript layers inline. It does not load app.js or style.css, and no calc.js file was supplied separately. Therefore those two files are intentionally not added to this deploy package, to avoid loading duplicate or mismatched code. They remain unchanged in the original upload.
