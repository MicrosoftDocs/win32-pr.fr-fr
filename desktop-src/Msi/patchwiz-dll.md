---
description: Pour générer un package de correctifs, il est recommandé d’utiliser un outil de création de correctifs comme Msimsp.exe et Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210769"
---
# <a name="patchwizdll"></a><span data-ttu-id="b128b-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="b128b-103">Patchwiz.dll</span></span>

<span data-ttu-id="b128b-104">Pour générer un package de correctifs, il est recommandé d’utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) et Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="b128b-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="b128b-105">Patchwiz.dll version 4,0 est compatible avec les packages et les correctifs qui ont été créés à l’aide de versions antérieures du Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="b128b-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="b128b-106">L’outil Patchwiz.dll est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="b128b-107">Patchwiz.dll version 4,0 a une nouvelle fonction, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), qui étend les fonctionnalités de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="b128b-108">Ces fonctions prennent un fichier de propriétés de création de correctifs (fichier. PCP) et génèrent un [package de correctifs](patch-packages.md)du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="b128b-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="b128b-109">Le fichier. PCP est un fichier de base de données binaire avec le même format qu’une base de données Windows Installer (fichier. msi), mais avec un schéma de base de données différent.</span><span class="sxs-lookup"><span data-stu-id="b128b-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="b128b-110">Par conséquent, un fichier. PCP peut être créé à l’aide des mêmes outils que ceux utilisés pour une base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="b128b-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="b128b-111">Vous pouvez créer un fichier. PCP à l’aide d’un éditeur de tables comme [Orca.exe](orca-exe.md) pour entrer des informations dans la base de données Blank. PCP fournie avec le kit de développement logiciel (SDK) Windows Installer, template. PCP.</span><span class="sxs-lookup"><span data-stu-id="b128b-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="b128b-112">Pour plus d’informations, consultez [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="b128b-113">Les tables de base de données suivantes sont requises dans chaque fichier. PCP :</span><span class="sxs-lookup"><span data-stu-id="b128b-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="b128b-114">Table Properties (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-115">Table ImageFamilies (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-116">Table UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-117">Table TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="b128b-118">Les tables de base de données suivantes sont facultatives :</span><span class="sxs-lookup"><span data-stu-id="b128b-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="b128b-119">UpgradedFiles \_ OptionalData, table (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-120">Table FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-121">TargetFiles \_ OptionalData, table (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-122">Table ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="b128b-123">Table UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="b128b-124">Le tableau suivant est requis dans les fichiers. PCP qui ont un MinimumRequiredMsiVersion égal à 300 dans le tableau des [Propriétés](properties-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="b128b-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="b128b-125">Table PatchMetadata (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b128b-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="b128b-126">La table est facultative si MinimumRequiredMsiVersion n’est pas égal à 300.</span><span class="sxs-lookup"><span data-stu-id="b128b-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="b128b-127">La version de Patchwiz.dll publiée avec Windows Installer 3,0 peut générer automatiquement des informations de séquencement de correctifs et les ajouter à la [table MsiPatchSequence](msipatchsequence-table.md) d’un nouveau correctif.</span><span class="sxs-lookup"><span data-stu-id="b128b-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="b128b-128">La [table PatchSequence](patchsequence-table--patchwiz-dll-.md) peut être utilisée pour ajouter manuellement des informations de séquencement de correctifs à la table MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="b128b-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="b128b-129">Pour plus d’informations, consultez [génération d’informations sur les séquences de correctifs](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="b128b-130">À partir de Patchwiz.dll version 2,0, vous pouvez augmenter la vitesse de création des correctifs suivants à l’aide de [la mise en cache des informations sur les correctifs (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="b128b-131">L’utilisation de symboles publics pour vos fichiers binaires image de mise à niveau et cible peut réduire d’environ une demi-taille des correctifs binaires.</span><span class="sxs-lookup"><span data-stu-id="b128b-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="b128b-132">Pour plus d’informations, consultez [utilisation de symboles pour réduire la taille des correctifs binaires](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="b128b-133">Vous pouvez spécifier que certaines régions du fichier cible soient conservées lors de la mise à jour corrective et que les informations contenues dans ces régions soient conservées.</span><span class="sxs-lookup"><span data-stu-id="b128b-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="b128b-134">Pour plus d’informations, consultez Mise à [jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="b128b-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b128b-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b128b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b128b-136">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="b128b-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



