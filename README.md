# ⚡️ Virtual Environment Alias

**One Command to Set Up and Activate Your Python Virtual Environment**

This repository provides a simple PowerShell function to create a virtual environment, activate it, and install dependencies — all in a single command.

---

## 📂 What’s Inside

- `venvalias.ps1` — A PowerShell script defining the `Venv` function.

---

## ✅ How to Use

Follow these steps to add the `Venv` function to your PowerShell profile.

---

### 1️⃣ Clone or Copy

Clone this repo or open `venvalias.ps1` and copy its contents.

```bash
git clone https://github.com/bitsbuild/venv-setup-alias.git
````

---

### 2️⃣ Open Your PowerShell Profile

Open your PowerShell profile file in your default editor:

```powershell
notepad $PROFILE
```

> 📌 **Note:** If this file doesn’t exist, PowerShell will create it for you.

---

### 3️⃣ Add the Function

Paste the contents of `venvalias.ps1` into your profile.
Example:

```powershell
function Venv {
    python -m venv venv
    .\venv\Scripts\Activate.ps1
    pip install -r requirements.txt
}
```

---

### 4️⃣ Reload Your Profile

Apply the changes by reloading your profile:

```powershell
. $PROFILE
```

---

### 5️⃣ Use It

Inside your Python project folder, run:

```powershell
Venv
```

This will:

* Create a `venv` folder if it doesn’t exist.
* Activate the virtual environment.
* Install packages from `requirements.txt`.

---

## ⚙️ `.gitattributes`

To ensure GitHub detects this repo as **PowerShell**, add:

```
*.ps1 linguist-language=PowerShell
```

to your `.gitattributes` file.

---

## ⚠️ Execution Policy Note

If you see a security warning when trying to run `.ps1` scripts, you may need to allow script execution:

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

---

## 📝 License

MIT — use, modify, and share freely.
