---
description: Pour reproduire l’exemple de package de correctifs, vous avez besoin d’un outil logiciel permettant de créer et de modifier un package de correctifs Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Création d’un fichier de propriétés de création de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522461"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="2bcaf-103">Création d’un fichier de propriétés de création de correctifs</span><span class="sxs-lookup"><span data-stu-id="2bcaf-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="2bcaf-104">Pour reproduire l’exemple de package de correctifs, vous avez besoin d’un outil logiciel permettant de créer et de modifier un package de correctifs Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="2bcaf-105">Plusieurs outils de création de packages de correctifs sont disponibles auprès des éditeurs de logiciels indépendants.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="2bcaf-106">L’exemple décrit dans les sections suivantes utilise une Windows Installer éditeur de base de données appelé Orca pour créer un fichier de propriétés de création de correctifs (extension. PCP).</span><span class="sxs-lookup"><span data-stu-id="2bcaf-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="2bcaf-107">Le fichier. PCP peut être utilisé avec les utilitaires [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) pour générer un package de correctifs Windows Installer (extension. msp).</span><span class="sxs-lookup"><span data-stu-id="2bcaf-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="2bcaf-108">Orca, Msimsp.exe et Patchwiz.dll sont fournis dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaf-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="2bcaf-109">Un fichier de propriétés de création de correctifs vide, template. PCP, est également fourni avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="2bcaf-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="2bcaf-110">Effectuez une copie de template. PCP et renommez cette copie MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="2bcaf-111">Utilisez Orca ou un autre éditeur de base de données pour entrer les données suivantes dans la table Properties de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="2bcaf-112">La table propriétés contient des paramètres globaux pour le package correctif.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="2bcaf-113">Tableau des propriétés</span><span class="sxs-lookup"><span data-stu-id="2bcaf-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="2bcaf-114">Nom</span><span class="sxs-lookup"><span data-stu-id="2bcaf-114">Name</span></span>                               | <span data-ttu-id="2bcaf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bcaf-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="2bcaf-116">AllowProductCodeMismatches</span><span class="sxs-lookup"><span data-stu-id="2bcaf-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="2bcaf-117">1</span><span class="sxs-lookup"><span data-stu-id="2bcaf-117">1</span></span>                                      |
| <span data-ttu-id="2bcaf-118">AllowProductVersionMajorMismatches</span><span class="sxs-lookup"><span data-stu-id="2bcaf-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="2bcaf-119">1</span><span class="sxs-lookup"><span data-stu-id="2bcaf-119">1</span></span>                                      |
| <span data-ttu-id="2bcaf-120">ApiPatchingSymbolFlags</span><span class="sxs-lookup"><span data-stu-id="2bcaf-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="2bcaf-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bcaf-121">0x00000000</span></span>                             |
| <span data-ttu-id="2bcaf-122">DontRemoveTempFolderWhenFinished</span><span class="sxs-lookup"><span data-stu-id="2bcaf-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="2bcaf-123">1</span><span class="sxs-lookup"><span data-stu-id="2bcaf-123">1</span></span>                                      |
| <span data-ttu-id="2bcaf-124">IncludeWholeFilesOnly</span><span class="sxs-lookup"><span data-stu-id="2bcaf-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="2bcaf-125">0</span><span class="sxs-lookup"><span data-stu-id="2bcaf-125">0</span></span>                                      |
| <span data-ttu-id="2bcaf-126">ListOfPatchGUIDsToReplace</span><span class="sxs-lookup"><span data-stu-id="2bcaf-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="2bcaf-127">ListOfTargetProductCodes</span><span class="sxs-lookup"><span data-stu-id="2bcaf-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="2bcaf-128">PatchGUID</span><span class="sxs-lookup"><span data-stu-id="2bcaf-128">PatchGUID</span></span>                          | <span data-ttu-id="2bcaf-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="2bcaf-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="2bcaf-130">PatchOutputPath</span><span class="sxs-lookup"><span data-stu-id="2bcaf-130">PatchOutputPath</span></span>                    | <span data-ttu-id="2bcaf-131">c : \\ sortie. msp</span><span class="sxs-lookup"><span data-stu-id="2bcaf-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="2bcaf-132">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="2bcaf-132">PatchSourceList</span></span>                    | <span data-ttu-id="2bcaf-133">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="2bcaf-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="2bcaf-134">Utilisez l’éditeur de base de données pour entrer les données suivantes dans la table ImageFamilies de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="2bcaf-135">La table ImageFamilies contient des informations à ajouter à la [table multimédia](media-table.md) lors de la mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="2bcaf-136">Table ImageFamilies</span><span class="sxs-lookup"><span data-stu-id="2bcaf-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="2bcaf-137">Famille</span><span class="sxs-lookup"><span data-stu-id="2bcaf-137">Family</span></span>  | <span data-ttu-id="2bcaf-138">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="2bcaf-138">MediaSrcPropName</span></span> | <span data-ttu-id="2bcaf-139">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="2bcaf-139">MediaDiskId</span></span> | <span data-ttu-id="2bcaf-140">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="2bcaf-140">FileSequenceStart</span></span> | <span data-ttu-id="2bcaf-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="2bcaf-141">DiskPrompt</span></span> | <span data-ttu-id="2bcaf-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="2bcaf-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="2bcaf-143">MNPapps</span><span class="sxs-lookup"><span data-stu-id="2bcaf-143">MNPapps</span></span> | <span data-ttu-id="2bcaf-144">MNPSrcPropName</span><span class="sxs-lookup"><span data-stu-id="2bcaf-144">MNPSrcPropName</span></span>   | <span data-ttu-id="2bcaf-145">2</span><span class="sxs-lookup"><span data-stu-id="2bcaf-145">2</span></span>           | <span data-ttu-id="2bcaf-146">1 000</span><span class="sxs-lookup"><span data-stu-id="2bcaf-146">1000</span></span>              |            |             |



 

<span data-ttu-id="2bcaf-147">Entrez les données suivantes dans la table UpgradedImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="2bcaf-148">La table UpgradedImages contient des informations sur l’image mise à niveau que vous avez créée lors de la [planification d’un correctif logiciel de petite mise à jour](planning-a-small-update-patch.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaf-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="2bcaf-149">Table UpgradedImages</span><span class="sxs-lookup"><span data-stu-id="2bcaf-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="2bcaf-150">Upgraded</span><span class="sxs-lookup"><span data-stu-id="2bcaf-150">Upgraded</span></span>   | <span data-ttu-id="2bcaf-151">MsiPath</span><span class="sxs-lookup"><span data-stu-id="2bcaf-151">MsiPath</span></span>                                           | <span data-ttu-id="2bcaf-152">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="2bcaf-152">PatchMsiPath</span></span> | <span data-ttu-id="2bcaf-153">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="2bcaf-153">SymbolPaths</span></span> | <span data-ttu-id="2bcaf-154">Famille</span><span class="sxs-lookup"><span data-stu-id="2bcaf-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="2bcaf-155">MNP \_ fixe</span><span class="sxs-lookup"><span data-stu-id="2bcaf-155">MNP\_fixed</span></span> | <span data-ttu-id="2bcaf-156">C : \\ Remarque le \_ correctif du programme d’installation a \\ \\ mis à niveau \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="2bcaf-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="2bcaf-157">MNPapps</span><span class="sxs-lookup"><span data-stu-id="2bcaf-157">MNPapps</span></span> |



 

<span data-ttu-id="2bcaf-158">Entrez les données suivantes dans la table TargetImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="2bcaf-159">La table TargetImages contient des informations sur l’image cible.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="2bcaf-160">Table TargetImages</span><span class="sxs-lookup"><span data-stu-id="2bcaf-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="2bcaf-161">Cible</span><span class="sxs-lookup"><span data-stu-id="2bcaf-161">Target</span></span>     | <span data-ttu-id="2bcaf-162">MsiPath</span><span class="sxs-lookup"><span data-stu-id="2bcaf-162">MsiPath</span></span>                                         | <span data-ttu-id="2bcaf-163">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="2bcaf-163">SymbolPaths</span></span> | <span data-ttu-id="2bcaf-164">Upgraded</span><span class="sxs-lookup"><span data-stu-id="2bcaf-164">Upgraded</span></span>   | <span data-ttu-id="2bcaf-165">Commande</span><span class="sxs-lookup"><span data-stu-id="2bcaf-165">Order</span></span> | <span data-ttu-id="2bcaf-166">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="2bcaf-166">ProductValidateFlags</span></span> | <span data-ttu-id="2bcaf-167">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="2bcaf-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="2bcaf-168">\_Erreur MNP</span><span class="sxs-lookup"><span data-stu-id="2bcaf-168">MNP\_error</span></span> | <span data-ttu-id="2bcaf-169">C : \\ remarque \_MNP2000.msi de la cible de correctif du programme d’installation \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="2bcaf-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="2bcaf-170">MNP \_ fixe</span><span class="sxs-lookup"><span data-stu-id="2bcaf-170">MNP\_fixed</span></span> | <span data-ttu-id="2bcaf-171">1</span><span class="sxs-lookup"><span data-stu-id="2bcaf-171">1</span></span>     |                      | <span data-ttu-id="2bcaf-172">0</span><span class="sxs-lookup"><span data-stu-id="2bcaf-172">0</span></span>                     |



 

<span data-ttu-id="2bcaf-173">Pour l’exemple de package de correctifs, laissez les tableaux suivants dans MNP2000. PCP vide.</span><span class="sxs-lookup"><span data-stu-id="2bcaf-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="2bcaf-174">\_Table UpgradedFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="2bcaf-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="2bcaf-175">Table FamilyFileRanges</span><span class="sxs-lookup"><span data-stu-id="2bcaf-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="2bcaf-176">\_Table TargetFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="2bcaf-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="2bcaf-177">Table ExternalFiles</span><span class="sxs-lookup"><span data-stu-id="2bcaf-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="2bcaf-178">Table UpgradedFilesToIgnore</span><span class="sxs-lookup"><span data-stu-id="2bcaf-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="2bcaf-179">Continuer</span><span class="sxs-lookup"><span data-stu-id="2bcaf-179">Continue</span></span>](generating-a-patch-package.md)

 

 



