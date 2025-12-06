<h2 align="center">🚀 Gensyn RL-SWARM Node — Ultimate Easy Guide (All Issues Fixed)</h2>

## ⚙️ Hardware Requirements

> ### 📝 Overview  
> Your hardware requirements depend on the **swarm type** and **model size** you choose.  
> - For **low hardware**, use **Qwen 0.5B / 1.5B** + **GSM8K**  
> - For **high hardware**, use **Qwen 7B / 32B / 72B** + **DAPO-Math 17K**  
>  
> Choose according to the details below:

---

> ## 🟩 Small Model (0.5B / 1.5B) — GSM8K Dataset  
> For users with mid-level hardware.

### 📌 Minimum VPS Requirements
> - **32 GB RAM**  
> - **8 vCPU**  
> - **200 GB Storage**  
> - Best for **default (0.5B) training**

### 🖥️ CPU Requirements
> - **ARM64** or **x86_64 CPU**  
> - Minimum **32GB RAM**  
> - ⚠️ **Note:** Running extra applications during training may cause a crash.

### 🎮 GPU Requirements (CUDA Supported)
> - **RTX 3090**  
> - **RTX 4090**  
> - **A100**  
> - **H100**

---

> ## 🟦 Big Model (7B / 32B / 72B) — DAPO-Math 17K Dataset  
> For users with powerful hardware.

### 🔥 Recommended GPUs
> - **NVIDIA A100 (80GB)**  
> - **NVIDIA H100 (80GB)**  

---

## 🖥️ Node Setup Guide

> ## 🔐 1. Open Your VPS  
> Connect to your server:
```bash
ssh username@ip
```
# 🚀 RL-SWARM Installation & Setup Guide

A complete step-by-step guide to run RL-SWARM on Linux (VPS/WSL) or Mac.

---

## 🛠️ 1. Installation & Setup

Run the following commands step-by-step on your terminal.

1. **Install `sudo`**
```bash
apt update && apt install -y sudo
```
2. **Install other dependencies**
```bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git lsof nano unzip iproute2 build-essential gcc g++
```

3. **Create a `screen` session**
```bash
screen -S gensyn
```
4. **Clone official `rl-swarm` repo**
```
git clone https://github.com/gensyn-ai/rl-swarm.git && cd rl-swarm
```
5. **Run the swarm**
```
python3 -m venv .venv
. .venv/bin/activate
./run_rl_swarm.sh
```
![image](https://github.com/user-attachments/assets/40d07439-ffd1-4207-9e51-fabc3fdbb8aa)

- After sometimes, u will see something like this if your running it on Linux system, so here follow the next step
- * Now it will promt you to login: Follow: [1️⃣ How to Login or access  http://localhost:3000/ in VPS? 📶](https://github.com/Mayankgg01/Gensyn-ai-Rl-Swarm_Guide?tab=readme-ov-file#1%EF%B8%8F%E2%83%A3-how-to-login-or-access--httplocalhost3000-in-vps-)

* Now It will promt `Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]` Enter `N`

* Now It will promt `>> Enter the name of the model you want to use in huggingface repo/name format, or press [Enter] to use the default model.`  press `Enter` & get defalut model: 

---❗ If U put model manually then it can be cause of terminated❗--- So better to use Default:

------>>>If u want to select the model then choose between them:
## 5️⃣ Choose customised model's


<pre>

 Gensyn/Qwen2.5-0.5B-Instruct

 Qwen/Qwen3-0.6B

 nvidia/AceInstruct-1.5B

 dnotitia/Smoothie-Qwen3-1.7B

 Gensyn/Qwen2.5-1.5B-Instruct

</pre>

Models (CodeZero):
   - **Qwen2.5-Coder-0.5B-Instruct** — Solver role (Recommended Choose This)  
   - **Qwen2.5-Coder-1.5B-Instruct** — Evaluator (frozen)  

Currently, we are running **CodeZero** on the Gensyn Testnet. 

Its Done ✅

# NEXT


# Detach & Attach from screen

`ctrl` `A` `D` To Detach from screen 

* Attach with previous screen:

```
screen -r gensyn
```



## 1️⃣ How to Login or access  http://localhost:3000/ in VPS? 📶

* Open a new Terminal and login ur vps 

* Allow Incoming connection on VPS

```
sudo apt install ufw -y
sudo ufw allow 22
sudo ufw allow 3000/tcp
```

* Enable ufw

```
sudo ufw enable
```

* Install cloudflared on the VPS

```
wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb
````

```
sudo dpkg -i cloudflared-linux-amd64.deb
```

* Check version

```
cloudflared --version
```

* Make sure your Node is running on port 3000 in Previous Screen

* Run the tunnel command

```
cloudflared tunnel --url http://localhost:3000
```

* Access the Link from your local machine

    
    ![image](https://github.com/user-attachments/assets/c5bdfec5-123d-4625-8da8-f46269700950)

* Now follow Login!
 
* Done!✅



