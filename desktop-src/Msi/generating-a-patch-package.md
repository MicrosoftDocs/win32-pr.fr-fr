---
description: La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme Msimsp.exe pour appeler UiCreatePatchPackage dans Patchwiz.dll. Msimsp.exe et PatchWiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Génération d’un package de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581429"
---
# <a name="generating-a-patch-package"></a>Génération d’un package de correctifs

La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) pour appeler [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) dans [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe et PatchWiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer.

L’exemple de ligne de commande suivant utilise Msimsp.exe et le fichier. PCP créé lors de la [création d’un fichier de propriétés de création de correctifs](creating-a-patch-creation-properties-file.md) pour générer l’exemple de package de correctif MNP2000. msp.

**Msimsp.exe-s C : \\ Remarque \_ installer \\ Patch Patch \\ MNP2000. PCP-p C : \\ Remarque \_ installer \\ patch \\ MNP2000. msp**

Un outil de création de correctif créé peut générer le package de correctifs en appelant [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) comme suit.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continuer](applying-a-patch-package-to-a-local-installation.md)

 

 



