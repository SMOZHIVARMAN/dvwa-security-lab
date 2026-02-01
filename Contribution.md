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
- 📊 Scores are cumulative across multiple merged PRs  

---

## 🧮 Scoring Rules (Strict & Location-Based)

### ✅ Base Contribution
- Every merged Pull Request earns **+10 points**

This applies to **any valid contribution**, including:
- New folders
- New experiments
- Code changes
- Documentation updates (outside bonus rules)

### 📄 Documentation Bonus (Strict Location Rules)

| Bonus Type | Points | Conditions |
|----------|--------|------------|
| Root `README.md` updated | +4 | Must be `README.md` in the **root of the repository** |
| Root `screenshots/` folder used | +5 | Files must be inside **root-level `screenshots/` only** |

⚠️ **Important Constraints**
- `experiments/hari/screenshots/` ❌ does NOT count
- `docs/README.md` ❌ does NOT count
- `readme/` folder ❌ does NOT count
- Only **exact paths** listed above earn bonus points

### 📊 Scoring Examples

| Change Made | Points |
|------------|--------|
| Any PR merged | 10 |
| Edit root `README.md` | 14 |
| Add image to root `screenshots/` | 15 |
| New folder + files (anywhere else) | 10 |
| `experiments/demo/screenshots/img.png` | 10 |

---

## 🚫 Penalties

| Violation | Penalty |
|---------|---------|
| Fake, copied, or misleading content | −10 |
| Spam or empty Pull Request | −10 |

⚠️ Penalties subtract from existing score  
⚠️ Penalties are applied manually by the maintainer and are not automated.
⚠️ When a penalty applies, **no positive points are awarded for that PR**

---

## 👤 Contributor Responsibilities

As a contributor, you must:
- Follow ethical hacking principles
- Work **only on DVWA**
- Provide original, meaningful content
- Use a feature branch for all work
- Open Pull Requests to `main`

You must **not**:
- Edit `LEADERBOARD.md`
- Push directly to `main`
- Attempt to game the scoring system
- Submit fake or copied experiments

---

## 👨‍⚖️ Maintainer Responsibilities

The maintainer will:
- Review all submissions manually
- Verify DVWA-only testing
- Detect spam or invalid PRs
- Merge or reject Pull Requests

After merge, **GitHub Actions automatically updates the leaderboard**.

---

## 🚫 What Is NOT Allowed

To keep this project safe and ethical, the following are **strictly prohibited**:

- Attacks against real or external systems  
- Uploading malware, exploit kits, or hacking tools  
- Automated attacks on non-DVWA targets  
- Publishing real credentials or personal data  
- Internet-exposed or production deployments  

---

## 📁 Recommended Experiment Structure

Each experiment should follow this structure for clarity:

```text
Experiments/
└── vulnerability-name/
    ├── README.md
    └── screenshots/
        ├── payload.png
        ├── result.png
```

📌 **Note**: This structure is for documentation quality only.  
Only root-level README.md and screenshots/ affect leaderboard bonus points.

### 📝 Experiment README Guidelines

Each experiment README should include:

- **Objective**  
- **Environment** (OS, DVWA version)  
- **Steps Performed**  
- **Payload Used**  
- **Observation**  
- **Impact**  
- **Mitigation**  
- **Conclusion**

Missing sections may reduce review quality or lead to rejection.

---

## 🔀 How to Contribute (Step-by-Step)

1️⃣ **Fork this repository**  
```
   Click Fork on GitHub to create your own copy.
```
2️⃣ **Clone your fork**  
   ```bash
   git clone https://github.com/your-username/dvwa-security-lab.git
   cd dvwa-security-lab
   ```
3️⃣ Add upstream (recommended)

```
git remote add upstream https://github.com/SMOZHIVARMAN/dvwa-security-lab.git
git remote -v
```
4️⃣ Sync before starting

```
git checkout main
git pull upstream main
```
5️⃣ Create a feature branch

```
git checkout -b feature/your-feature-name
```
6️⃣ Make your changes
```
Follow all project rules and ethical guidelines.
```
7️⃣ Commit your changes

```
git commit -m "feat: add DVWA experiment"
```
Use clear, meaningful commit messages.

8️⃣ Push to your fork

```
git push origin feature/your-feature-name
```
9️⃣ Open a Pull Request
```
Base branch: main

Compare branch: your feature branch
```
📌 Leaderboard points are awarded only after merge.

🔐 Ethical Reminder
- By contributing, you agree that:

- All experiments are performed only on DVWA

- No real systems are attacked

- All content is for learning and defensive awareness

👥 Code of Conduct
- Be respectful

- Be constructive

- Help others learn

📬 Questions or Suggestions?
- Open an Issue

- Or submit a Pull Request

- Thank you for contributing to DVWA Security Lab 🚀
- Your work helps others learn security the right way.