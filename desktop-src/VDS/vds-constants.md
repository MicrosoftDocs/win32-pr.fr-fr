---
description: Constantes VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523430"
---
# <a name="vds-constants"></a><span data-ttu-id="7a59a-103">Constantes VDS</span><span class="sxs-lookup"><span data-stu-id="7a59a-103">VDS Constants</span></span>

<span data-ttu-id="7a59a-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a59a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="7a59a-105">Les constantes VDS sont classées comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a59a-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="7a59a-106">Constantes d’état d’objet</span><span class="sxs-lookup"><span data-stu-id="7a59a-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="7a59a-107">Constantes d’indicateurs automagic</span><span class="sxs-lookup"><span data-stu-id="7a59a-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="7a59a-108">Constantes diverses</span><span class="sxs-lookup"><span data-stu-id="7a59a-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="7a59a-109">Constantes d’état d’objet</span><span class="sxs-lookup"><span data-stu-id="7a59a-109">Object Status Constants</span></span>



| <span data-ttu-id="7a59a-110">Constante</span><span class="sxs-lookup"><span data-stu-id="7a59a-110">Constant</span></span>           | <span data-ttu-id="7a59a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a59a-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="7a59a-112">ÉTAT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="7a59a-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="7a59a-113">0</span><span class="sxs-lookup"><span data-stu-id="7a59a-113">0</span></span>     |
| <span data-ttu-id="7a59a-114">ÉTAT \_ en ligne</span><span class="sxs-lookup"><span data-stu-id="7a59a-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="7a59a-115">1</span><span class="sxs-lookup"><span data-stu-id="7a59a-115">1</span></span>     |
| <span data-ttu-id="7a59a-116">ÉTAT \_ non \_ prêt</span><span class="sxs-lookup"><span data-stu-id="7a59a-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="7a59a-117">2</span><span class="sxs-lookup"><span data-stu-id="7a59a-117">2</span></span>     |
| <span data-ttu-id="7a59a-118">ÉTAT \_ aucun \_ support</span><span class="sxs-lookup"><span data-stu-id="7a59a-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="7a59a-119">3</span><span class="sxs-lookup"><span data-stu-id="7a59a-119">3</span></span>     |
| <span data-ttu-id="7a59a-120">ÉTAT \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="7a59a-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="7a59a-121">4</span><span class="sxs-lookup"><span data-stu-id="7a59a-121">4</span></span>     |
| <span data-ttu-id="7a59a-122">échec de l’état \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="7a59a-123">5</span><span class="sxs-lookup"><span data-stu-id="7a59a-123">5</span></span>     |
| <span data-ttu-id="7a59a-124">ÉTAT \_ manquant</span><span class="sxs-lookup"><span data-stu-id="7a59a-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="7a59a-125">6</span><span class="sxs-lookup"><span data-stu-id="7a59a-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="7a59a-126">Constantes d’indicateurs automagic</span><span class="sxs-lookup"><span data-stu-id="7a59a-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="7a59a-127">Constante</span><span class="sxs-lookup"><span data-stu-id="7a59a-127">Constant</span></span>                               | <span data-ttu-id="7a59a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a59a-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="7a59a-129">MOSTLYREADS de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="7a59a-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="7a59a-130">0x0002L</span></span> |
| <span data-ttu-id="7a59a-131">OPTIMIZEFORSEQUENTIALREADS de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="7a59a-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="7a59a-132">0x0004L</span></span> |
| <span data-ttu-id="7a59a-133">OPTIMIZEFORSEQUENTIALWRITES de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="7a59a-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="7a59a-134">0x0008L</span></span> |
| <span data-ttu-id="7a59a-135">REMAPENABLED de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="7a59a-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="7a59a-136">0x0020L</span></span> |
| <span data-ttu-id="7a59a-137">WRITETHROUGHCACHINGENABLED de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="7a59a-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="7a59a-138">0x0040L</span></span> |
| <span data-ttu-id="7a59a-139">HARDWARECHECKSUMENABLED de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="7a59a-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="7a59a-140">0x0080L</span></span> |
| <span data-ttu-id="7a59a-141">ISYANKABLE de l' \_ indicateur VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="7a59a-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="7a59a-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="7a59a-143">Constantes diverses</span><span class="sxs-lookup"><span data-stu-id="7a59a-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="7a59a-144">Constante</span><span class="sxs-lookup"><span data-stu-id="7a59a-144">Constant</span></span>                     | <span data-ttu-id="7a59a-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a59a-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="7a59a-146">\_priorité de \_ reconstruction \_ minimale de VDS</span><span class="sxs-lookup"><span data-stu-id="7a59a-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="7a59a-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="7a59a-147">0x0001L</span></span>    |
| <span data-ttu-id="7a59a-148">\_ \_ informations sur le numéro d’unité logique VDS \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="7a59a-149">1</span><span class="sxs-lookup"><span data-stu-id="7a59a-149">1</span></span>          |
| <span data-ttu-id="7a59a-150">longueur maximale du \_ nom d’ordinateur \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="7a59a-151">15</span><span class="sxs-lookup"><span data-stu-id="7a59a-151">15</span></span>         |
| <span data-ttu-id="7a59a-152">\_longueur max PROVIDERNAME \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="7a59a-153">200</span><span class="sxs-lookup"><span data-stu-id="7a59a-153">200</span></span>        |
| <span data-ttu-id="7a59a-154">longueur maximale de \_ VERSIONSTRING \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="7a59a-155">16</span><span class="sxs-lookup"><span data-stu-id="7a59a-155">16</span></span>         |
| <span data-ttu-id="7a59a-156">lettre de lecteur \_ \_ prop</span><span class="sxs-lookup"><span data-stu-id="7a59a-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="7a59a-157">N/A</span><span class="sxs-lookup"><span data-stu-id="7a59a-157">N/A</span></span>        |
| <span data-ttu-id="7a59a-158">\_taille de \_ nom \_ FS max.</span><span class="sxs-lookup"><span data-stu-id="7a59a-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="7a59a-159">8</span><span class="sxs-lookup"><span data-stu-id="7a59a-159">8</span></span>          |
| <span data-ttu-id="7a59a-160">\_idx de membre non valide \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="7a59a-161">Égale</span><span class="sxs-lookup"><span data-stu-id="7a59a-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="7a59a-162">longueur du nom de la \_ partition GPT \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a59a-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="7a59a-163">36</span><span class="sxs-lookup"><span data-stu-id="7a59a-163">36</span></span>         |
| <span data-ttu-id="7a59a-164">\_chemin d’accès maximal</span><span class="sxs-lookup"><span data-stu-id="7a59a-164">MAX\_PATH</span></span>                    | <span data-ttu-id="7a59a-165">260</span><span class="sxs-lookup"><span data-stu-id="7a59a-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7a59a-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a59a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a59a-167">Référence VDS</span><span class="sxs-lookup"><span data-stu-id="7a59a-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
