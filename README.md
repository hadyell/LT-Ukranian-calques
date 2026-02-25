# 📝 LT-Ukranian-calques - Local Ukrainian Text Checker

[![Download LT-Ukranian-calques](https://img.shields.io/badge/Download-LT--Ukranian--calques-blue?style=for-the-badge)](https://github.com/hadyell/LT-Ukranian-calques/releases)

---

## 🚀 What is LT-Ukranian-calques?

LT-Ukranian-calques is a local tool that helps you check Ukrainian text for common mistakes. It spots Russian borrowings, awkward translations, stylistic problems, and agreement errors in writing. This tool uses special rules based on Ukrainian language studies to make your text sound more natural.

You don’t need to be a programmer to use it. The tool runs inside a small program called Docker, but don’t worry – this guide will help you set it up step by step.

---

## 💻 System Requirements

Before you start, make sure your computer meets these basic needs:

- Operating system: Windows 10/11, macOS, or most modern Linux distributions.
- At least 4 GB of RAM.
- Around 1 GB free disk space.
- Internet access to download installation files.
- Permissions to install and run software on your computer.

You will also need to install Docker, a program that runs software inside containers. It works like a virtual box for running apps safely.

---

## 📥 Download & Install

### Step 1: Visit the download page

Click the big button below to open the official download page for LT-Ukranian-calques:

[![Download LT-Ukranian-calques](https://img.shields.io/badge/Download-LT--Ukranian--calques-blue?style=for-the-badge)](https://github.com/hadyell/LT-Ukranian-calques/releases)

On this page, look for the latest release. You will find files to download and detailed notes.

### Step 2: Download Docker

If you don’t have Docker installed, get it here:

- [Docker for Windows](https://docs.docker.com/docker-for-windows/install/)
- [Docker for macOS](https://docs.docker.com/docker-for-mac/install/)
- [Docker for Linux](https://docs.docker.com/engine/install/)

Follow the instructions on Docker’s site to install it.

### Step 3: Download LT-Ukranian-calques files

On the GitHub release page, download the whole project archive or the Docker Compose file if offered. This file contains instructions to set up LT-Ukranian-calques automatically.

---

## ⚙️ How to Set Up and Run

Once you have Docker and the LT-Ukranian-calques files on your computer, follow these steps:

### Step 1: Open your command prompt or terminal

- On Windows: Press `Win + R`, type `cmd`, then press Enter.
- On macOS: Open Finder > Applications > Utilities > Terminal.
- On Linux: Open your preferred terminal app.

Navigate to the folder where you saved LT-Ukranian-calques. Use the command:

```bash
cd path/to/your/downloaded/folder
```

Replace `path/to/your/downloaded/folder` with the actual folder path.

### Step 2: Start the LT-Ukranian-calques server

Run this command:

```bash
docker compose up -d --build
```

This command builds and starts the tool inside Docker on your computer. The `-d` option runs it in the background.

### Step 3: Check if LT-Ukranian-calques is working

Run the test script by typing:

```bash
./test.sh
```

This script runs a quick check to make sure the Ukrainian language rules are applied correctly. If you see messages about Russian borrowings or style issues, the tool is working.

---

## 🧰 About LT-Ukranian-calques

This project contains special rules designed to catch common problems in Ukrainian writing. The rules come from research on Ukrainian texts and language corpora.

The project has these main parts:

- **Dockerfile**: Builds the custom Docker image with the rules.
- **docker-compose.yml**: Configures the whole server setup.
- **test.sh**: Helps you test that rules are loaded properly.
- **rules/**: Folder with rule files.
  - `grammar-fluency-ua.xml`: Contains 132 rules targeting borrowings, style, flow, and agreement.
  - `agreement-yi.xml`: Includes 44 rules focused on agreement between particles and grammar.

---

## 🖥️ How to Use LT-Ukranian-calques

LT-Ukranian-calques runs as a server on your computer. To use it:

1. Run the server following the setup steps above.
2. Find a way to send your Ukrainian text to the server for checking.

You can use this with a browser extension that connects to your local server. The extension sends your text and receives error messages based on the rules.

---

## 🌐 Browser Integration (Optional)

If you want to check text inside your web browser while typing:

1. Find a LanguageTool-compatible browser extension (often available for Chrome, Firefox).
2. Configure the extension to point to your local server:
   - URL: `http://localhost:8081` (the default LT-Ukranian-calques server address)
3. Now the extension will use the custom Ukrainian rules from your local tool.

---

## 🤔 FAQ

**Q: What if Docker commands fail?**  
A: Make sure Docker is installed and running. You might need administrator rights.

**Q: Can I use LT-Ukranian-calques on any Ukrainian text?**  
A: Yes, it checks text for style, errors, and borrowed words typically found in everyday writing.

**Q: How do I stop the server?**  
A: Run `docker compose down` in the same folder to stop and remove the running container.

---

## 📚 More Information

This tool is based on Ukrainian linguistic research. It uses a collection of 176 rules focused on improving Ukrainian writing style and accuracy.

For technical details, explore the `rules/` folder and the configuration files. They control how the tool detects different language issues.

---

## 🔗 Useful Links

- [Download LT-Ukranian-calques Releases](https://github.com/hadyell/LT-Ukranian-calques/releases)  
  Visit this page to download the latest files.

- [UA-GEC Corpus on GitHub](https://github.com/grammarly/ua-gec)  
  The research dataset behind the rules.

- [Docker Documentation](https://docs.docker.com/get-started/)  
  Learn more about how Docker works.

---

## 📄 License

This project uses open-source licenses. Check the repository for full license details.