---
description: La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme Msimsp.exe pour appeler UiCreatePatchPackage dans Patchwiz.dll. Msimsp.exe et PatchWiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Génération d’un package de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952297"
---
# <a name="generating-a-patch-package"></a><span data-ttu-id="ea771-104">Génération d’un package de correctifs</span><span class="sxs-lookup"><span data-stu-id="ea771-104">Generating a Patch Package</span></span>

<span data-ttu-id="ea771-105">La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) pour appeler [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) dans [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="ea771-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="ea771-106">Msimsp.exe et PatchWiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ea771-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="ea771-107">L’exemple de ligne de commande suivant utilise Msimsp.exe et le fichier. PCP créé lors de la [création d’un fichier de propriétés de création de correctifs](creating-a-patch-creation-properties-file.md) pour générer l’exemple de package de correctif MNP2000. msp.</span><span class="sxs-lookup"><span data-stu-id="ea771-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="ea771-108">**Msimsp.exe-s C : \\ Remarque \_ installer \\ Patch Patch \\ MNP2000. PCP-p C : \\ Remarque \_ installer \\ patch \\ MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="ea771-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="ea771-109">Un outil de création de correctif créé peut générer le package de correctifs en appelant [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) comme suit.</span><span class="sxs-lookup"><span data-stu-id="ea771-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="ea771-110">Continuer</span><span class="sxs-lookup"><span data-stu-id="ea771-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



