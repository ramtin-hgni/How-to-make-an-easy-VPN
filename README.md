# 🚀 Create Your Own Cloudflare Worker VPN

A simple, step-by-step guide to setting up your very own VPN using Cloudflare Workers. Perfect for bypassing restrictions and securing your connection!

## 📋 Table of Contents
- [Prerequisites](#prerequisites)
- [Setup Guide](#setup-guide)
- [Configuration](#configuration)
- [Optimization](#optimization)
- [Limitations](#limitations)
- [Credits](#credits)

---

## 📌 Prerequisites

Before you begin, make sure you have:
- A valid email address (Gmail recommended)
- A device with internet access
- [V2RayNG]([https://play.google.com/store/apps/details?id=com.v2ray.ang](https://github.com/2dust/v2rayng)) (for Android) or any V2Ray-compatible client

---

## 🔧 Setup Guide

### Step 1: Create a New Email
Start by creating a new email account on your device. Gmail is recommended for reliability.

### Step 2: Sign Up for Cloudflare
1. Open your browser and go to [Cloudflare](https://cloudflare.com)
2. Click on **Sign Up** and use your newly created email
3. Complete the registration process

![cf page](https://github.com/ramtin-hgni/How-to-make-an-easy-VPN/blob/3718776358f2bbdf5330874c5b4f9ad3a525d3c6/Screenshot%202026-09-03%20181512.png)

### Step 3: Access Workers & Pages
- Once logged in, type **"Workers & Pages"** in the top-left search bar
- Click on the result to navigate to the Workers dashboard

![](https://github.com/ramtin-hgni/How-to-make-an-easy-VPN/blob/bf460b399f9fe2c8f64ea13f45fdb3c660d084ba/Screenshot%202026-09-03%20183721.png)

![](https://github.com/ramtin-hgni/How-to-make-an-easy-VPN/blob/d89324fb87d926bc6e621e147d4ae079262a338d/Screenshot%202026-09-03%20181629.png)

### Step 4: Create Your Worker
1. Click the **"Create application"** button
2. Select **"Start with Hello World!"**
3. Hit the **Deploy** button

![](https://github.com/ramtin-hgni/How-to-make-an-easy-VPN/blob/48d0664443849bea3aab64cf0100148026045257/Screenshot%202026-09-03%20182028.png)

### Step 5: Paste the Code
Now you'll need to replace the default code with the VPN script:

![Codes](https://github.com/ramtin-hgni/How-to-make-an-easy-VPN/blob/d97645c7fb1e5f924eae342c582795ba9c13bcf1/code.md)

1. Go to the **Edit code** section of your Worker
2. Paste the entire code from the repository
3. Click **Deploy** again

### Step 6: Generate Your UUID
1. Open a new browser tab and search for **"UUID Generator"**
2. Or directly visit: [UUID Generator](https://www.uuidgenerator.net/)
3. Copy the generated UUID code

### Step 7: Configure Environment Variables
1. Return to your Cloudflare Worker Overview page
2. Click on **"Settings"** in the top bar
3. Select **"Add variables"**
4. Create a new variable:
   - **Name:** `UUID`
   - **Value:** Paste your generated UUID
5. Click **Add** to save

### Step 8: Set Compatibility Date
1. Scroll down to the **Runtime** section
2. Locate **Compatibility date**
3. Set it to `2026-01-13` or a later date
4. Save the changes

---

## 📱 Configuration

### Setting Up V2RayNG

1. Copy your Worker Address (e.g., `your-worker-name.workers.dev`)
2. Open **V2RayNG** on your device
3. Go to **"Servers"** → **"Add [VLESS] Server"**
4. Fill in the details:

| Field | Value |
|-------|-------|
| Alias | Anything you like |
| Address | `104.25.96.193` or any other CF IP |
| Port | `443` |
| UUID | Your Generated UUID |
| Encryption | `none` |
| Transport protocol | `ws` |
| Camouflage type | `none` |
| Camouflage domain(host) | `your-worker-name.workers.dev` |
| Path | `/?ed=2048` |
| Security | `tls` |
| SNI | `your-worker-name.workers.dev` |
| AllowInssecure | `false` |

⚠️ remember paste worker address like this: (`your-worker-name.workers.dev`) not this: (`your-worker-name.workers.dev/`) or this: (`https://your-worker-name.workers.dev/`)

5. Click **Confirm** to save the configuration

---

## ⚡ Optimization Tips

### Find the Best Cloudflare IP

1. Download **CF Scanner** (a tool to find optimal Cloudflare IPs)
2. Paste your V2Ray configuration URL into the scanner
3. Start the scan to find the best-performing IPs for your ISP
4. Copy the high-speed results and update your V2Ray configuration

---

## ⚠️ Limitations

Before using this VPN, be aware of these important limitations:

- ❌ **Not suitable for gaming** - No UDP support
- ❌ **Not for trading** - Unstable for financial applications
- 🔄 **IP changes daily** - Your IP rotates regularly
- 👥 **Limited sharing** - Only 3-4 people can use the same config
- 📊 **Daily limit** - 100,000 requests per day maximum

---

## 🙏 Credits

Special thanks to [zizifn](https://github.com/zizifn) for providing the core code that makes this possible!

---

## 📝 License

This guide is for educational purposes only. Use at your own risk. Please respect Cloudflare's Terms of Service.

---

**Happy Browsing! 🎉**
