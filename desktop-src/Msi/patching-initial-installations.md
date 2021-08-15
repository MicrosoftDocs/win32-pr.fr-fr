---
description: un correctif Windows Installer (MSP) peut être appliqué lors de l’installation d’une application pour la première fois à l’aide de la propriété Patch.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Mise à jour corrective des installations initiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf89c3a83a6000a5716b5317a9fc2965562c217b110b020a2795573f8175235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377632"
---
# <a name="patching-initial-installations"></a>Mise à jour corrective des installations initiales

un correctif Windows Installer (MSP) peut être appliqué lors de l’installation d’une application pour la première fois à l’aide de la propriété [**Patch**](patch.md) .

Pour appliquer un correctif lors de la première installation de l’application, vous devez définir la propriété [**patch**](patch.md) sur la ligne de commande. Spécifiez le chemin d’accès complet au correctif sur la ligne de commande en tant que paire propriété-valeur « PATCH = {*path to patch*} ».

Notez que la spécification de la propriété [**patch**](patch.md) sur la ligne de commande remplace les vérifications d’applicabilité des correctifs effectuées lors de l’utilisation de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou de l' [option de ligne de commande](command-line-options.md)/p.

Si un correctif est appliqué à l’aide de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou de l' [option de ligne de commande](command-line-options.md)/p, le programme d’installation compare les applications actuellement installées sur l’ordinateur à la liste des codes de produit éligibles pour recevoir le correctif dans la propriété Résumé du [**modèle**](template-summary.md) .

Lorsque vous définissez la propriété [**patch**](patch.md) sur la ligne de commande pour installer lors de la première installation, les applications éligibles pour recevoir le correctif sont déterminées par des conditions de validation sur les transformations incorporées dans le package de correctifs. La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) et [PATCHWIZ.DLL](patchwiz-dll.md). Les conditions de validation des transformations dans le correctif proviennent de la colonne ProductValidateFlags de la table [TargetImages](targetimages-table-patchwiz-dll-.md) du fichier de propriétés de création de correctifs (. PCP).

Le correctif peut être appliqué lors de la première installation de l’application par une ligne de commande, une autre application ou un script.

L’exemple suivant illustre la première mise à jour corrective à partir de la ligne de commande.

**msiexec/i** *package.msi* **patch =**_"c : \\ Directory \\ patch. msp"_

L’exemple suivant illustre la mise à jour corrective initiale à partir d’une autre application.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

L’exemple suivant illustre la mise à jour corrective initiale à partir d’un script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3,0 et versions ultérieures : * *

à partir de Windows Installer version 3,0, plusieurs correctifs peuvent être appliqués lors de l’installation d’une application pour la première fois. Définissez la propriété [**patch**](patch.md) sur une liste délimitée par des points-virgules des chemins d’accès complets des correctifs. L’exemple suivant illustre la première mise à jour corrective de plusieurs correctifs à partir de la ligne de commande.

**msiexec/i** *package.msi* **patch =**_"c : \\ Directory \\ patch. msp ; c : \\ répertoire \\ patch2. msp ; c : \\ Directory \\ patch3. msp"_

 

 



