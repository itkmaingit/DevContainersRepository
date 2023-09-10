# OverView

This repository is for Docker development environments using the "Dev Containers" extension to VSCode. The repository contains various branches, each of which serves a different purpose (for example, the cpp branch is a sample for creating a Docker development environment for C++). The cpp branch is a sample for creating a Docker development environment for C++.

If you see a branch and want to set up a development environment, run the following command. For example, if you feel you want to clone the cpp branch, all you have to execute is

```bash
git clone -b cpp https://github.com/itkmaingit/DevContainersRepository.git
```

. After that, simply run `Dev Containers: Reopen in Container` on VSCode to complete the setup of the development environment.

## Caution

This repository includes .gitignore, but we don't add `.env` to .gitignore. So, you need to add `.env` for yourself.
