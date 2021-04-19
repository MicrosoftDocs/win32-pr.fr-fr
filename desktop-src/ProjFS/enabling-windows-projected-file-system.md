---
title: Activation du système de fichiers projetés Windows
description: Décrit comment activer ProjFS sur Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2019
ms.locfileid: "106510585"
---
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="495be-103">Activation du système de fichiers projetés Windows</span><span class="sxs-lookup"><span data-stu-id="495be-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="495be-104">ProjFS est fourni avec Windows en tant que composant facultatif.</span><span class="sxs-lookup"><span data-stu-id="495be-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="495be-105">Pour qu’un fournisseur puisse l’utiliser, il doit être activé.</span><span class="sxs-lookup"><span data-stu-id="495be-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="495be-106">Vous pouvez utiliser</span><span class="sxs-lookup"><span data-stu-id="495be-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="495be-107">PowerShell pour activer ProjFS.</span><span class="sxs-lookup"><span data-stu-id="495be-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="495be-108">Comment activer ProjFS à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="495be-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="495be-109">Pour utiliser PowerShell pour activer ProjFS, utilisez l' `Enable-WindowsOptionalFeature` applet de commande dans une fenêtre PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="495be-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="495be-110">Redémarrez l’ordinateur si le Enable-WindowsOptionalFeature rapports `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="495be-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
