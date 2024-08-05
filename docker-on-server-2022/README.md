---
Created: 2024-07-27T08:43:12+05:30
Updated: 2024-08-05T12:14:52+05:30
Maintainer: Ibrar Ansari
---
# Install Docker on Server 2022 without enabling Virtualization in BIOS

### Step 1: Install DockerMsftProvider Module
```
Install-Module DockerMsftProvider -Force
```

### Step 2: Download Docker Installation Script
```
Invoke-WebRequest -UseBasicParsing "https://raw.githubusercontent.com/microsoft/Windows-Containers/Main/helpful_tools/Install-DockerCE/install-docker-ce.ps1" -o install-docker-ce.ps1
```

### Step 3: Execute the Installation Script
```
./install-docker-ce.ps1
```

#### Step 4: Verify Docker Installation
```
docker --version
```



### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)