---
description: Microsoft Windows Installer accepte une Uniform Resource Locator (URL) comme source valide d’un correctif.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Téléchargement et installation d’un correctif à partir d’Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091461"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Téléchargement et installation d’un correctif à partir d’Internet

Microsoft Windows Installer accepte une Uniform Resource Locator (URL) comme source valide d’un [correctif](patch-packages.md). Pour installer un correctif situé sur un serveur Web à https://MyWeb/MyPatch.msp l’adresse, utilisez la ligne de commande suivante :

**msiexec/p https://MyWeb/MyPatch.msp**

Pour éviter des résultats inattendus, ne lancez pas un correctif en cliquant sur le lien de la page Web qui indique l’URL du fichier correctif. Vous pouvez également installer un correctif à l’aide d’un script similaire à ce qui suit :


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



Notez que, étant donné que l’objet [**installer**](installer-object.md) n’est pas marqué comme [SafeForScripting](safeforscripting.md) sur l’ordinateur de l’utilisateur, les utilisateurs doivent ajuster les paramètres de sécurité de leur navigateur pour que l’exemple fonctionne correctement.

pour plus d’informations, consultez [instructions pour la création d’Installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Packages de correctifs](patch-packages.md)
</dt> <dt>

[Création d’un package de correctifs](creating-a-patch-package.md)
</dt> <dt>

[Mise à jour corrective des applications personnalisées](patching-customized-applications.md)
</dt> <dt>

[Téléchargement d’une installation à partir d’Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



