# Lab Setup

## Create Windows 11 VM in Azure Cloud

## Install Choco in powershell
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

## Exit powershell
```
exit
```

## Open powershell and install
```
choco install git -y
choco install googlechrome -y
choco install vscode -y
choco install python -y
choco install dotnetcore-sdk -y
choco install azure-cli -y
exit
```

## Clone Repos in another powershell
```
md c:\ai-102
cd c:\ai-102
git clone https://github.com/MicrosoftLearning/mslearn-ai-services
git clone https://github.com/MicrosoftLearning/mslearn-ai-vision
git clone https://github.com/MicrosoftLearning/mslearn-ai-language
git clone https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence
git clone https://github.com/MicrosoftLearning/mslearn-knowledge-mining/
git clone https://github.com/MicrosoftLearning/mslearn-openai
dir
```

## Connect to Azure CLI
```
az login -u u1@atingupta.xyz -p <password>
```

## Create SP
```
az ad sp create-for-rbac -n "api://ag-ai-services" --role owner --scopes subscriptions/c0cdfbe3-2e41-4bb3-a3d9-b40843a3c3f7/resourceGroups/rg-practice-ai-102
```

```
{
  "appId": "69bb7c51-f901-456b-ad19-83574a4fd128",
  "displayName": "api://ag-ai-services",
  "password": "APP_PASSWORD_TO_REPLACE",
  "tenant": "6bb2f9af-a0af-4c32-a5ec-5f7011d37551"
}
```

## Create Key Vault using Azure Portal

## Set permissions on Key Vault using Azure Portal
