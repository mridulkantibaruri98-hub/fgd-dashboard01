# FGD-1 Operations Dashboard

Created by **Mridul Kanti Baruri** · Employee ID 109384 · Operation Department

**Website:** https://mridulkantibaruri98-hub.github.io/fgd-dashboard01/

- **Everyone** opens the link and views the dashboard. There's no login, and they can't change anything.
- **The FGD control room engineer** updates the data with the **Update data · Control room** button on the website.
- **The owner (Mridul)** manages the website and the access key.

## What is in this repository

| File | What it does |
|---|---|
| `index.html` | The dashboard page |
| `data/dashboard-data.xlsx` | The published data. The website reads this file every time someone opens it |
| `README.md` | These instructions |

---

## 1. Owner: create the access key (one time, then once a year)

The access key is what allows the control room to publish data from the website. Only people who have the key can update the data.

1. On GitHub, click your profile picture (top right) → **Settings**.
2. In the left menu, scroll down and click **Developer settings** → **Personal access tokens** → **Fine-grained tokens**.
3. Click **Generate new token** and fill in:
   - **Token name:** `FGD dashboard upload`
   - **Expiration:** choose **Custom** and pick a date one year from today
   - **Repository access:** **Only select repositories** → choose **fgd-dashboard01**
   - **Permissions** → **Repository permissions** → **Contents:** **Read and write**
4. Click **Generate token** and **copy the key** (it starts with `github_pat_`). GitHub shows it only once.
5. Give the key to the FGD control room engineers privately, in person or by direct message. Never post it in a group or put it on the website.

**If the key leaks or someone leaves:** go to the same **Fine-grained tokens** page, click the token → **Delete**, then generate a new key and share it again.
**Before the expiry date:** generate a new key and give it to the control room. The website says "The access key is wrong or has expired" once the old one stops working.

---

## 2. Control room engineer: daily data update

Do this after the day's entries are complete in the Excel sheet.

1. Fill in the day's figures in the Excel sheet as usual. Don't rename sheets or move columns. The file can have any name.
2. Open the website: **https://mridulkantibaruri98-hub.github.io/fgd-dashboard01/**
3. Click **Update data · Control room** (top right).
4. **First time only:** enter **your name** (for example `Rahul Das (FGD Control Room)`) and the **access key**, and keep **Remember my name and key on this computer** ticked. On a shared control room PC, use a name like `FGD Control Room – Shift A`.
5. Click **Choose File** and pick the Excel file. The website checks it and shows **"✓ read correctly · data filled through (date)"**.
6. Check the **Note** (for example `Data up to 11-Oct-2026`) and click **Publish to website**.
7. The message **"Published"** appears. Everyone who opens or refreshes the website sees the new data within 1–2 minutes. The top right shows **"Data uploaded by (your name) · date and time · note"**.

If it shows **"The access key is wrong or has expired"**, ask the owner for the new key. Click **Use a different name or key** in the update box to enter it.

**Undo a wrong upload:** upload the previous correct Excel file the same way. GitHub also keeps every earlier version: in the repository, open **data** → `dashboard-data.xlsx` → **History**.

---

## 3. Keep the Excel layout the same

The dashboard reads these sheets and columns, the same as your Excel dashboard formulas:

- **DAILY**: date in column B; SOx Units 1–3 in C–E; opacity Units 1–3 in F–H; load Units 1–3 in I–K
- **COMMON**: date in B; APC daily C; APC monthly D; water F; gypsum produced G; gypsum sold H; gypsum trucks I; limestone received J; limestone trucks K; limestone consumed L; wet ball mill hours M; dewatering hours N; DG set YES/NO O
- **AVAILABILITY**: date in B; availability hours Units 1–3 in C–E; monthly availability Units 1–3 in I–K
- **DEFECT**: department names in A2:A7, defect counts in B2:B7

Renaming a sheet or moving a column will break the matching figure. Adding new rows (new dates) is fine. If a sheet is missing, the website refuses to publish the file and says which sheet is missing.

---

## Good to know

- **The data is public.** Anyone with the link can see the figures, and anyone who finds the repository can download the Excel file. Don't put confidential information in it.
- **Keep the access key secret.** Anyone who has it can replace the data.
- The website shows who **uploaded** the data. It can't show who is **viewing**, because there's no login. For visitor counts, open the repository → **Insights** → **Traffic** (owner only).
- The page needs internet access to load its charts and fonts.
- **Owner fallback:** you can still upload directly on GitHub: **data** folder → **Add file** → **Upload files** → a file named exactly `dashboard-data.xlsx` → **Commit changes**.
