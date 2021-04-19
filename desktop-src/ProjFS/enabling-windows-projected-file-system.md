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
# <a name="enabling-windows-projected-file-system"></a>Activation du système de fichiers projetés Windows

ProjFS est fourni avec Windows en tant que composant facultatif.  Pour qu’un fournisseur puisse l’utiliser, il doit être activé.  Vous pouvez utiliser <!--the GUI or--> PowerShell pour activer ProjFS.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Comment activer ProjFS à l’aide de PowerShell

Pour utiliser PowerShell pour activer ProjFS, utilisez l' `Enable-WindowsOptionalFeature` applet de commande dans une fenêtre PowerShell avec élévation de privilèges :

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Redémarrez l’ordinateur si le Enable-WindowsOptionalFeature rapports `RestartNeeded: True` .
