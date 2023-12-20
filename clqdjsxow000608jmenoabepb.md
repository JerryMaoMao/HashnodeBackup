---
title: "Elegant Use of nvm for Node.js Management on Mac in 2024"
seoTitle: "Elegant Use of nvm for Node.js Management on Mac in 2024"
seoDescription: "However, with the long history of products, versioning becomes a common issue—some projects require new versions, while others need older ones."
datePublished: Wed Dec 20 2023 09:05:09 GMT+0000 (Coordinated Universal Time)
cuid: clqdjsxow000608jmenoabepb
slug: elegant-use-of-nvm-for-nodejs-management-on-mac-in-2024
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703062832173/e1fa8c98-7e9d-4dc5-96f6-bfe77188b9a3.png
tags: web-development, nodejs, webdev, typescript, macos, nvm

---

Node.js, as the foundation of frontend capabilities, is no longer just a "JS Server Runtime." Numerous tool libraries, local package management, mock environments, and more are built on Node.js, making it truly the infrastructure of the frontend world.

The flourishing ecosystem has made it essential for everyone to install Node.js when building frontend projects. However, with the long history of products, versioning becomes a common issue—some projects require new versions, while others need older ones. Managing multiple versions of Node.js has been a persistent challenge for developers.

Currently, the open-source tool nvm addresses this issue. With simple command-line usage, developers can quickly switch between different versions of Node.js, allowing them to focus on development rather than wasting time on environment configuration.

The predominant machines for frontend development are still Macbooks. Therefore, this article will explain how to elegantly install and use nvm on Mac to efficiently manage Node.js versions.

## Recommending an Open Source Project for Backend Development

[ILLA Cloud](https://illacloud.com?utm_source=hashnode) is an out-of-the-box low-code tool that enables the rapid construction of internal tools using simple JS, without the need to create new projects.

* Web & App Admin Panel
    
* Data Dashboard
    
* Customized B2B Tools
    

Compared to scenarios built with component libraries, ILLA Cloud allows for 10x faster construction of the mentioned tools. Additionally, ILLA Cloud supports collaboration among multiple users, facilitating teamwork for rapid customization of backend capabilities.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062875672/b8e7877a-ec0e-4b9a-9bd8-06ebd8d40f34.png align="center")

## Introduction to nvm

⏬ GitHub Repository: [https://github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm)

⭐ GitHub Stars: 72.4k

💪🏼 First Release Date: Dec 22, 2014

nvm is an open-source project that has been maintained for nearly 10 years. Positive reviews have kept this project robust and, through continuous maintenance, it has become a perfect solution for "Node.js version management."

## Installing nvm

Since we are using a Mac for development, I strongly recommend using [Homebrew](https://brew.sh) for package management and then using [Homebrew](https://brew.sh) to install nvm.

To install Homebrew, it is recommended to use the installation script. It requires minimal configuration and allows immediate use. Moreover, Homebrew makes it easy to uninstall repositories cleanly if needed.

```shell
> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Running this command will install the latest version of Homebrew, automatically handling the installation of Xcode Command Tools in the MacOS environment.

Of course, all of this is automated. Below is an installation process example.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062885850/15a2ed5a-9af6-484f-bc97-19a22f73b15a.png align="center")

After a short wait, we can proceed with the installation of nvm using the installed Homebrew.

```shell
> brew install nvm
```

After confirming agreement, nvm will be completely installed. If you decide you don't want it anymore, you can use the following command to uninstall:

```shell
# delete nvm if you don't need it.
> brew uninstall nvm
```

## Using nvm

Once nvm is installed, here are some commonly used commands to help you get started. These commands should fulfill your daily needs.

```shell
> nvm list
```

The "list" command displays various mainstream Node.js versions. You can install versions according to your needs, and it will also show the currently used Node.js version on your machine. It will display some codenames.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062893207/8b53a956-6e5f-4926-bb04-f872cd9d124f.png align="center")

For example, "lts/gallim" is the version name for Node.js v16. To install using this codename, nvm will automatically install the latest version of v16. It's quite convenient. You can also use this command to check the currently used version.

Another command allows you to check the current Node.js version:

```shell
> node --version
```

After entering this command, you can verify whether the Node.js version has been successfully switched.

```shell
> nvm install stable
```

The second command installs a specific Node.js version; "stable" refers to a specific version number. You can also use the codename for a particular version. For example, to install "Node.js 18," you would use "nvm install 18." Here, I'm installing the "stable" version. nvm will automatically determine the latest Stable version and install it for me. After successful installation, it will automatically switch to the installed version.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062901485/1129f00d-646d-491b-b6d4-0e8394dcdb27.png align="center")

Where there's an installation command, there's also an uninstallation command. Use:

```shell
> nvm uninstall stable
```

To delete the corresponding version.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062916580/6d8e90e7-7b4c-4759-ad01-36edfe311a04.png align="center")

Once you've learned how to install and uninstall, the next important step is version switching.

```shell
> nvm use stable
```

The "use" command allows you to quickly switch between Node.js versions currently in use. You can also use the "stable" codename. This way, you can quickly switch between versions for different projects.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703062917572/c7698cd6-b716-4483-b620-b0dad1352f21.png align="center")

## Conclusion

This article has explained the entire process for a beginner, from installing to using nvm. You can quickly try it out and better manage your Node.js versions.

Node.js version management is a long-discussed issue, and nvm is an excellent open-source project that effectively addresses this problem. Of course, no project is perfect. If you have other recommendations, feel free to leave a comment and let more people know about outstanding projects—that's the mission of open-source enthusiasts!