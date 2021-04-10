---
title: Fonctions ADSI
description: Active Directory interfaces de service exposent les fonctions d’assistance suivantes aux clients qui n’utilisent pas Automation.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, référence, fonctions
- function ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309262"
---
# <a name="adsi-functions"></a><span data-ttu-id="81cc4-105">Fonctions ADSI</span><span class="sxs-lookup"><span data-stu-id="81cc4-105">ADSI Functions</span></span>

<span data-ttu-id="81cc4-106">Active Directory interfaces de service exposent les fonctions d’assistance suivantes aux clients qui n’utilisent pas Automation.</span><span class="sxs-lookup"><span data-stu-id="81cc4-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="81cc4-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="81cc4-107">Function</span></span>                                           | <span data-ttu-id="81cc4-108">Description</span><span class="sxs-lookup"><span data-stu-id="81cc4-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81cc4-109">**ADsBuildEnumerator**</span><span class="sxs-lookup"><span data-stu-id="81cc4-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="81cc4-110">Crée un objet énumérateur pour l’objet conteneur ADSI spécifié.</span><span class="sxs-lookup"><span data-stu-id="81cc4-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="81cc4-111">**ADsBuildVarArrayInt**</span><span class="sxs-lookup"><span data-stu-id="81cc4-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="81cc4-112">Génère un tableau de variant à partir d’un tableau de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="81cc4-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="81cc4-113">**ADsBuildVarArrayStr**</span><span class="sxs-lookup"><span data-stu-id="81cc4-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="81cc4-114">Génère un tableau de variant à partir d’un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="81cc4-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="81cc4-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="81cc4-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="81cc4-116">Convertit un objet blob de données binaires au format approprié pour un filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="81cc4-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="81cc4-117">**ADsEnumerateNext**</span><span class="sxs-lookup"><span data-stu-id="81cc4-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="81cc4-118">Remplit un tableau de variants avec les éléments récupérés à partir de l’objet énumérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="81cc4-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="81cc4-119">**ADsFreeEnumerator**</span><span class="sxs-lookup"><span data-stu-id="81cc4-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="81cc4-120">Libère un objet énumérateur créé précédemment par [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span><span class="sxs-lookup"><span data-stu-id="81cc4-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="81cc4-121">**ADsGetLastError**</span><span class="sxs-lookup"><span data-stu-id="81cc4-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="81cc4-122">Récupère la dernière valeur de code d’erreur du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="81cc4-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="81cc4-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="81cc4-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="81cc4-124">Crée une liaison avec un objet ADSI à l’aide des informations d’identification actuelles.</span><span class="sxs-lookup"><span data-stu-id="81cc4-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="81cc4-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="81cc4-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="81cc4-126">Crée une liaison avec un objet ADSI à l’aide des informations d’identification spécifiées</span><span class="sxs-lookup"><span data-stu-id="81cc4-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="81cc4-127">**ADsSetLastError**</span><span class="sxs-lookup"><span data-stu-id="81cc4-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="81cc4-128">Définit la valeur du code d’erreur du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="81cc4-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="81cc4-129">**AllocADsMem**</span><span class="sxs-lookup"><span data-stu-id="81cc4-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="81cc4-130">Alloue un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="81cc4-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="81cc4-131">**AllocADsStr**</span><span class="sxs-lookup"><span data-stu-id="81cc4-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="81cc4-132">Alloue de la mémoire pour une chaîne donnée.</span><span class="sxs-lookup"><span data-stu-id="81cc4-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="81cc4-133">**FreeADsMem**</span><span class="sxs-lookup"><span data-stu-id="81cc4-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="81cc4-134">Libère la mémoire allouée par [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span><span class="sxs-lookup"><span data-stu-id="81cc4-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="81cc4-135">**FreeADsStr**</span><span class="sxs-lookup"><span data-stu-id="81cc4-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="81cc4-136">Libère la mémoire allouée pour la chaîne donnée.</span><span class="sxs-lookup"><span data-stu-id="81cc4-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="81cc4-137">**ReallocADsMem**</span><span class="sxs-lookup"><span data-stu-id="81cc4-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="81cc4-138">Affecte le contenu de mémoire existant à un emplacement de mémoire nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="81cc4-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="81cc4-139">**ReallocADsStr**</span><span class="sxs-lookup"><span data-stu-id="81cc4-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="81cc4-140">Remplace une chaîne existante par une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="81cc4-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="81cc4-141">Les fonctions ADSI suivantes sont obsolètes.</span><span class="sxs-lookup"><span data-stu-id="81cc4-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="81cc4-142">Fonction</span><span class="sxs-lookup"><span data-stu-id="81cc4-142">Function</span></span>                                                  | <span data-ttu-id="81cc4-143">Description</span><span class="sxs-lookup"><span data-stu-id="81cc4-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="81cc4-144">**AdsFreeAllErrorRecords**</span><span class="sxs-lookup"><span data-stu-id="81cc4-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="81cc4-145">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-145">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-146">**AdsDecodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="81cc4-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="81cc4-147">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-147">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-148">**PropVariantToAdsType**</span><span class="sxs-lookup"><span data-stu-id="81cc4-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="81cc4-149">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-149">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-150">**AdsTypeToPropVariant**</span><span class="sxs-lookup"><span data-stu-id="81cc4-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="81cc4-151">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-151">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-152">**AdsFreeAdsValues**</span><span class="sxs-lookup"><span data-stu-id="81cc4-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="81cc4-153">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-153">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-154">**InitAdsMem**</span><span class="sxs-lookup"><span data-stu-id="81cc4-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="81cc4-155">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-155">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-156">**AssertAdsmemLeaks**</span><span class="sxs-lookup"><span data-stu-id="81cc4-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="81cc4-157">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-157">Obsolete.</span></span>   |
| [<span data-ttu-id="81cc4-158">**DumpMemorytracker**</span><span class="sxs-lookup"><span data-stu-id="81cc4-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="81cc4-159">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="81cc4-159">Obsolete.</span></span>   |



 

 

 




