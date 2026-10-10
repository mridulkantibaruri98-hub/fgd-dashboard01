# FGD-1 Operations Dashboard

Created by **Mridul Kanti Baruri** · Employee ID 109384 · Operation Department

A web dashboard for FGD-1 (Units 1–3). It reads the Excel file in `data/` every time someone opens the page, so updating that one file updates the dashboard for everyone.

## What is in this folder

| File | What it does |
|---|---|
| `index.html` | The dashboard page |
| `data/dashboard-data.xlsx` | The data. Replace this file to update the dashboard |
| `README.md` | These instructions |

## Launch the website (one time, about 5 minutes)

1. Go to **https://github.com** and sign in. If you don't have an account, click **Sign up** and create a free one.
2. Click **+** (top right) → **New repository**.
   - Repository name: `fgd-dashboard`
   - Choose **Public** (free GitHub Pages needs a public repository)
   - Click **Create repository**.
3. On the new repository page, click the link **uploading an existing file**.
4. Unzip the folder you received. Drag **`index.html`**, **`README.md`** and the whole **`data`** folder into the upload box. Use Chrome or Edge so the folder uploads with its contents.
5. Scroll down and click **Commit changes**.
6. Click **Settings** (top of the repository) → **Pages** (left menu).
   - Under **Build and deployment**, set **Source** to **Deploy from a branch**.
   - Set **Branch** to **main** and the folder to **/ (root)**, then click **Save**.
7. Wait 1–2 minutes, then refresh the Pages screen. Your link appears at the top:

   **`https://YOUR-GITHUB-USERNAME.github.io/fgd-dashboard/`**

   Share this link with anyone. It opens on any phone or computer, with no login.

## Give the FGD control room engineer update access (one time)

The website owner does this once for each engineer who will update the data.

1. The engineer creates a free GitHub account at **https://github.com** and sends you their **GitHub username**.
2. In the `fgd-dashboard` repository, click **Settings** → **Collaborators** → **Add people**.
3. Type the engineer's username, select them, and click **Add to repository**.
4. The engineer opens the invitation email from GitHub (or https://github.com/notifications) and clicks **Accept invitation**.

To remove someone later, go to the same **Collaborators** page and click **Remove**.

Everyone else can only view the website. Only you and the collaborators you add can change the data.

## Daily data update: control room engineer

Do this after the day's entries are complete in the Excel sheet.

1. Fill in the day's figures in the Excel sheet as usual. Don't rename sheets or move columns.
2. Save the file and **rename it to `dashboard-data.xlsx`** (exactly this name, all lowercase).
3. Open **https://github.com/OWNER-USERNAME/fgd-dashboard** and sign in.
4. Click the **data** folder.
5. Click **Add file** → **Upload files** → drag in `dashboard-data.xlsx`.
6. In the box at the bottom, type a short note such as `Data up to 11-Oct-2026`, then click **Commit changes**.
7. After 1–2 minutes, open the website and check that the top right shows today's update time and the latest date with data.

The website shows **"Could not find data/dashboard-data.xlsx"** if the file name is wrong. Upload it again with the exact name.

**Undo a wrong upload:** open the **data** folder → click `dashboard-data.xlsx` → **History**. Download the previous good version, then upload it again with the steps above.

## Keep the Excel layout the same

The dashboard reads these sheets and columns, the same as your Excel dashboard formulas:

- **DAILY**: date in column B; SOx Units 1–3 in C–E; opacity Units 1–3 in F–H; load Units 1–3 in I–K
- **COMMON**: date in B; APC daily C; APC monthly D; water F; gypsum produced G; gypsum sold H; gypsum trucks I; limestone received J; limestone trucks K; limestone consumed L; wet ball mill hours M; dewatering hours N; DG set YES/NO O
- **AVAILABILITY**: date in B; availability hours Units 1–3 in C–E; monthly availability Units 1–3 in I–K
- **DEFECT**: department names in A2:A7, defect counts in B2:B7

Renaming a sheet or moving a column will break the matching figure. Adding new rows (new dates) is fine.

## Good to know

- **The data is public.** Anyone with the link can see the figures, and anyone who finds the repository can download the Excel file. Don't put confidential information in it.
- The page needs internet access to load its charts and fonts.
- Opening `index.html` by double-clicking it on your computer won't load the data. Use the GitHub Pages link, or click **Load workbook** on the page to preview a file in your own browser only.
