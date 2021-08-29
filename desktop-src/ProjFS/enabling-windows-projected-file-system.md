---
title: activation d’Windows système de fichiers projeté
description: Décrit comment activer ProjFS sur Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: ca891b9b7f89b3722ea9db1c606961d4ba47f0a1a1d05d1bebc2951c68e00f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031259"
---
# <a name="enabling-windows-projected-file-system"></a>activation d’Windows système de fichiers projeté

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
