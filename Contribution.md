# 🤝 Contributing to DVWA Security Lab

Thank you for your interest in contributing to the **DVWA Security Lab** project.

This repository is created **strictly for educational and ethical security learning purposes**.  
All contributions must follow responsible disclosure and ethical hacking principles.

---

## 📌 Purpose of This Project

The goal of this project is to:
- Help learners understand common web vulnerabilities
- Practice attacks in a **controlled and legal environment**
- Document security experiments clearly for academic and learning use
- Encourage **high-quality contributions** through a transparent leaderboard system

---

## 🏆 Leaderboard & Scoring System

This project maintains a **community leaderboard** to recognize meaningful contributions.

### Important Rules
- ✅ Only **merged Pull Requests** are scored  
- 🤖 Scores are calculated **automatically using GitHub Actions**  
- 🚫 Contributors **must not edit `LEADERBOARD.md` manually**  

---

## 🧮 Scoring Rules

### ✅ Base Submission
- Merged Pull Request: **+2 points**

### 🔐 DVWA Security Level  
(The level must be clearly mentioned in `README.md`)

| Level | Points |
|-------|--------|
| Low   | +2     |
| Medium| +3     |
| High  | +4     |
| Impossible | +5  |

> 📌 Security level is verified and labeled by the maintainer.

### 📄 Documentation Quality

| Requirement | Points |
|-------------|--------|
| `README.md` present | +4 |
| `screenshots/` folder with valid images | +5 |

### 🚫 Penalties (Strict)

| Violation | Penalty |
|-----------|---------|
| Fake / copied / misleading submission | **−10** |
| Spam or empty Pull Request | **−10** |

⚠️ Penalties subtract from existing score.  
⚠️ If a penalty is applied, **no positive points are added** for that submission.

---

## 🏷️ Pull Request Labels (Very Important)

Labels are **applied only by the maintainer after manual review**.  
They are used by GitHub Actions to calculate scores.

### 🔐 Security Level Labels
- `level:low`
- `level:medium`
- `level:high`
- `level:impossible`

### 🚫 Penalty Label
- `fake`

📌 Contributors **must not** apply labels themselves.

---

## 👤 Contributor Responsibilities

As a contributor, you must:
- Follow the required folder structure
- Include clear and original documentation
- Mention the DVWA security level in `README.md`
- Submit honest, DVWA-only experiments
- Open a Pull Request from a feature branch

You must **not**:
- Edit the leaderboard
- Push directly to `main`
- Apply labels
- Submit copied or fake content

---

## 👨‍⚖️ Maintainer Responsibilities

The maintainer will:
- Review all submissions manually
- Verify DVWA-only testing
- Decide the security level
- Apply appropriate labels
- Detect fake or invalid submissions
- Merge or reject Pull Requests

After merge, **GitHub Actions automatically updates the leaderboard**.

---

## 🚫 What Is NOT Allowed

To keep this project safe and ethical, the following are **strictly prohibited**:

- Attacks against real or external systems  
- Uploading exploit tools, malware, or hacking frameworks  
- Automated attacks on non-DVWA targets  
- Publishing real credentials or personal data  
- Internet-exposed or production deployments  

---

## 📁 Required Folder Structure

Each experiment must follow **exactly** this structure:


```text
Experiments/
└── vulnerability-name/
    ├── README.md
    └── screenshots/
        ├── input.png
        ├── payload.png
        └── result.png
```


### ❗ Submissions not following this structure may be rejected or penalized.

## 📝 Experiment README Guidelines
Each README.md must include:

- **Objective** – What vulnerability is tested

- **Environment** – OS, DVWA version, security level

- **Steps Performed** – Clear numbered steps

- **Payload Used** – Input or exploit string

- **Screenshots Reference** – Mention screenshots folder

- **Observation** – What happened

- **Impact** – Security risk explained

- **Mitigation** – How to prevent the vulnerability

- **Conclusion** – Summary of the experiment

Missing sections may reduce score.

## 📸 Screenshot Guidelines
- Use clear names (payload.png, result.png)
- Avoid duplicates or unnecessary images
- Do not include personal information
- Screenshots must clearly show the outcome

---

## 🔀 How to Contribute (Step-by-Step)


1️⃣ **Fork this repository**

   Click Fork on GitHub to create your own copy.

2️⃣ **Clone your fork**  
```
git clone https://github.com/your-username/dvwa-security-lab.git
cd dvwa-security-lab
```


3️⃣ **Add the original repository as upstream (Recommended)** 
``` 
git remote add upstream https://github.com/SMOZHIVARMAN/dvwa-security-lab.git
```

Verify:
```
git remote -v
```


4️⃣ **Sync with upstream before starting work**  
```
git checkout main
git pull upstream main
```

5️⃣ **Create a feature branch**  
```
git checkout -b feature/your-feature-name
```


6️⃣ **Make your changes**  
```
 Follow all project rules and folder structure.
```
7️⃣ **Commit your changes**  
```
git commit -m "feat: add SQL Injection experiment (high)"
```
Use clear, meaningful commit messages.

8️⃣ **Push to your fork** 
``` 
git push origin feature/your-feature-name
```


9️⃣ **Open a Pull Request**  
- Base branch: `main`
- Compare branch: your feature branch

📌 Leaderboard points are awarded automatically after PR review and merge.

---

## 🔐 Ethical Reminder

By contributing, you agree that:

- All experiments are performed only on DVWA
- No real systems are attacked
- All content is for learning and defensive awareness

---

## 👥 Code of Conduct

- Be respectful and constructive
- Provide helpful feedback
- Avoid offensive or abusive language

---

## 📬 Questions or Suggestions?

- Open an [Issue](https://github.com/SMOZHIVARMAN/dvwa-security-lab/issues)
- Or submit a Pull Request

Thank you for helping improve the DVWA Security Lab 🚀  
Your contribution helps others learn security the right way.

---
