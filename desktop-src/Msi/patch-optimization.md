---
description: Windows Installer pouvez optimiser la mise à jour corrective pour réduire le temps nécessaire à l’application des correctifs pour les applications installées.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Optimisation des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864078"
---
# <a name="patch-optimization"></a><span data-ttu-id="9e840-103">Optimisation des correctifs</span><span class="sxs-lookup"><span data-stu-id="9e840-103">Patch Optimization</span></span>

<span data-ttu-id="9e840-104">Windows Installer pouvez optimiser la mise à jour corrective pour réduire le temps nécessaire à l’application des correctifs pour les applications installées.</span><span class="sxs-lookup"><span data-stu-id="9e840-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="9e840-105">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9e840-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="9e840-106">Pour les versions de Windows Installer publiées avant Windows Installer 3,0, la mise à jour corrective exécute une installation de réparation complète de l’application, ce qui peut prendre beaucoup plus de temps.</span><span class="sxs-lookup"><span data-stu-id="9e840-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="9e840-107">**Windows Installer 3,0 et versions ultérieures :** Le processus de mise à jour corrective modifie uniquement les parties d’une application qui sont modifiées par un correctif.</span><span class="sxs-lookup"><span data-stu-id="9e840-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="9e840-108">**Windows Installer 3,1 et versions ultérieures :** À partir de Windows Installer 3,1, l’optimisation des correctifs exige que la propriété OptimizedInstallMode de tous les correctifs de la transaction soit définie sur 1 (un) dans la [table MsiPatchMetadata](msipatchmetadata-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e840-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="9e840-109">Si un correctif modifie uniquement les tables suivantes, Windows Installer 3,0 ou une version ultérieure ignore les actions associées à toutes les autres tables, même si ces actions sont répertoriées dans les tables de séquence du package d’installation d’application d’origine (fichier. msi).</span><span class="sxs-lookup"><span data-stu-id="9e840-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="9e840-110">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="9e840-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="9e840-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="9e840-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="9e840-112">Condition</span><span class="sxs-lookup"><span data-stu-id="9e840-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="9e840-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="9e840-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="9e840-114">File</span><span class="sxs-lookup"><span data-stu-id="9e840-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="9e840-115">FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="9e840-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="9e840-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="9e840-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="9e840-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="9e840-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="9e840-118">Média</span><span class="sxs-lookup"><span data-stu-id="9e840-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="9e840-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="9e840-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="9e840-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="9e840-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="9e840-121">MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="9e840-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="9e840-122">MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="9e840-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="9e840-123">MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="9e840-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="9e840-124">MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="9e840-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="9e840-125">Patch</span><span class="sxs-lookup"><span data-stu-id="9e840-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="9e840-126">PatchPackage</span><span class="sxs-lookup"><span data-stu-id="9e840-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="9e840-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="9e840-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="9e840-128">Registre</span><span class="sxs-lookup"><span data-stu-id="9e840-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="9e840-129">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="9e840-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="9e840-130">Exportation</span><span class="sxs-lookup"><span data-stu-id="9e840-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="9e840-131">\_Colonnes</span><span class="sxs-lookup"><span data-stu-id="9e840-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="9e840-132">\_Stockages</span><span class="sxs-lookup"><span data-stu-id="9e840-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="9e840-133">\_Flux</span><span class="sxs-lookup"><span data-stu-id="9e840-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="9e840-134">\_Tables</span><span class="sxs-lookup"><span data-stu-id="9e840-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="9e840-135">\_Table TransformView</span><span class="sxs-lookup"><span data-stu-id="9e840-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="9e840-136">\_Validation</span><span class="sxs-lookup"><span data-stu-id="9e840-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="9e840-137">Pour désactiver l’option d’optimisation des correctifs, utilisez la stratégie [DisableFlyWeightPatching](disableflyweightpatching.md) .</span><span class="sxs-lookup"><span data-stu-id="9e840-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 



