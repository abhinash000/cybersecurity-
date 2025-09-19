
# 🔥 FAKEBANK HEIST – Offensive Security Lab

<p align="center">
  <img src="assets/banner-glitch.gif" alt="FakeBank Heist Banner" width="700">
</p>

> 💻 A cyberpunk-style walkthrough for an **Offensive Security** exercise.  
> 🕶️ Discover hidden paths, exploit a banking portal, and learn responsibly.

---

## 🌟 Overview
This lab teaches:
- Directory brute-forcing with `gobuster`.
- Exploiting a vulnerable banking transfer page.
- Documenting your result.

> ⚠️ **Legal Notice:** Run these steps only inside labs you own or are authorized to test.

---

## 🗺️ Step 1 – Reconnaissance
![Recon Screenshot](assets/1.png)


Target host:
```

[http://fakebank.thm](http://fakebank.thm)

````

Before starting:
- [ ] Add `fakebank.thm` to `/etc/hosts` (point to your lab IP).
- [ ] Open your terminal — neon green theme optional 😉

---

## 🔍 Step 2 – Directory Hunt
Run:

```bash
gobuster dir -u http://fakebank/ -w wordlist.txt
````

✅ **Expected output:**

```
/images
/bank-transfer
```

> 💡 If you don’t see these, try another wordlist.

---

## 💳 Step 3 – Transfer Mission

![Portal Screenshot](assets/2.png)

Go to:

```
http://fakebank.thm/bank-transfer/
```

🎯 **Objective:**
Move **\$2000** from account `2276` → `8881`.

---

## 📈 Step 4 – Verify & Log

![Balance Screenshot](assets/3.png)

Check your account page and note:

```text
💰 New Balance: ____________________
```

---

## ✅ Progress Tracker

| Step | Task                     | Status |
| ---- | ------------------------ | ------ |
| 1    | Set up lab & hosts file  | ⬜      |
| 2    | Run gobuster & find dirs | ⬜      |
| 3    | Access transfer portal   | ⬜      |
| 4    | Transfer funds           | ⬜      |
| 5    | Record balance           | ⬜      |

---

## 🧭 Tips & Gotchas

* DNS issues? Double-check `/etc/hosts` or your lab’s IP mapping.
* No transfer form? Ensure you typed the URL exactly.

---

## 🎯 Wrap-Up

By completing this, you’ve:

* ✅ Practiced **directory brute-forcing**
* ✅ Exploited a vulnerable endpoint (legally!)
* ✅ Learned how to document findings with style.

---

## 📜 License

MIT License – for educational purposes only.

````

---

### How to use it

1. On your repo ([`cybersecurity-`](https://github.com/abhinash000/cybersecurity-)), create a folder called `assets/`.
2. Add your glitch images:
   - `banner-glitch.gif`
   - `recon-glitch.png`
   - `transfer-glitch.gif`
   - `balance-glitch.png`
3. Create a new file `README.md` in the repo root → paste the content above.
4. Commit & push:
   ```bash
   git add README.md assets/
   git commit -m "Add stylish README with glitch images"
   git push origin main
````

After that, your repo’s front page will show the banner, screenshots, and interactive checklist.

Would you like me to generate and send you this `README.md` as a downloadable file so you can upload it directly?
