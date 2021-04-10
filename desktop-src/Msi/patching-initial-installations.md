---
description: Un correctif Windows Installer (MSP) peut être appliqué lors de l’installation d’une application pour la première fois à l’aide de la propriété PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Mise à jour corrective des installations initiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953077"
---
# <a name="patching-initial-installations"></a><span data-ttu-id="56515-103">Mise à jour corrective des installations initiales</span><span class="sxs-lookup"><span data-stu-id="56515-103">Patching Initial Installations</span></span>

<span data-ttu-id="56515-104">Un correctif Windows Installer (MSP) peut être appliqué lors de l’installation d’une application pour la première fois à l’aide de la propriété [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="56515-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="56515-105">Pour appliquer un correctif lors de la première installation de l’application, vous devez définir la propriété [**patch**](patch.md) sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56515-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="56515-106">Spécifiez le chemin d’accès complet au correctif sur la ligne de commande en tant que paire propriété-valeur « PATCH = {*path to patch*} ».</span><span class="sxs-lookup"><span data-stu-id="56515-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="56515-107">Notez que la spécification de la propriété [**patch**](patch.md) sur la ligne de commande remplace les vérifications d’applicabilité des correctifs effectuées lors de l’utilisation de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou de l' [option de ligne de commande](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="56515-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="56515-108">Si un correctif est appliqué à l’aide de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou de l' [option de ligne de commande](command-line-options.md)/p, le programme d’installation compare les applications actuellement installées sur l’ordinateur à la liste des codes de produit éligibles pour recevoir le correctif dans la propriété Résumé du [**modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="56515-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="56515-109">Lorsque vous définissez la propriété [**patch**](patch.md) sur la ligne de commande pour installer lors de la première installation, les applications éligibles pour recevoir le correctif sont déterminées par des conditions de validation sur les transformations incorporées dans le package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="56515-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="56515-110">La méthode recommandée pour générer un package de correctif consiste à utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) et [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="56515-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="56515-111">Les conditions de validation des transformations dans le correctif proviennent de la colonne ProductValidateFlags de la table [TargetImages](targetimages-table-patchwiz-dll-.md) du fichier de propriétés de création de correctifs (. PCP).</span><span class="sxs-lookup"><span data-stu-id="56515-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="56515-112">Le correctif peut être appliqué lors de la première installation de l’application par une ligne de commande, une autre application ou un script.</span><span class="sxs-lookup"><span data-stu-id="56515-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="56515-113">L’exemple suivant illustre la première mise à jour corrective à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56515-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="56515-114">**msiexec/i** *package.msi* **patch =**_"c : \\ Directory \\ patch. msp"_</span><span class="sxs-lookup"><span data-stu-id="56515-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="56515-115">L’exemple suivant illustre la mise à jour corrective initiale à partir d’une autre application.</span><span class="sxs-lookup"><span data-stu-id="56515-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="56515-116">L’exemple suivant illustre la mise à jour corrective initiale à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="56515-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="56515-117">\* \* Windows Installer 3,0 et versions ultérieures : \* \*</span><span class="sxs-lookup"><span data-stu-id="56515-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="56515-118">À partir de Windows Installer version 3,0, plusieurs correctifs peuvent être appliqués lors de l’installation d’une application pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="56515-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="56515-119">Définissez la propriété [**patch**](patch.md) sur une liste délimitée par des points-virgules des chemins d’accès complets des correctifs.</span><span class="sxs-lookup"><span data-stu-id="56515-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="56515-120">L’exemple suivant illustre la première mise à jour corrective de plusieurs correctifs à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56515-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="56515-121">**msiexec/i** *package.msi* **patch =**_"c : \\ Directory \\ patch. msp ; c : \\ répertoire \\ patch2. msp ; c : \\ Directory \\ patch3. msp"_</span><span class="sxs-lookup"><span data-stu-id="56515-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



