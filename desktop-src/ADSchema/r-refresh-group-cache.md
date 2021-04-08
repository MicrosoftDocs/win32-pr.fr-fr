---
title: Actualiser-groupe-à droite étendu
description: Il ne s’agit pas d’une ouverture de session GC. Aucune ouverture de session de catalogue global ne s’appuie sur les appartenances aux groupes de mise en cache, et ce droit d’accès de contrôle est utilisé pour accorder aux administrateurs et aux opérateurs des droits d’autorisation pour provoquer une actualisation immédiate du cache, en contactant un GC disponible.
ms.assetid: 1db49a92-ccf8-4087-ac79-f4c1bcea6aa4
ms.tgt_platform: multiple
keywords:
- 'Actualiser : schéma AD droit étendu du cache de groupe'
topic_type:
- apiref
api_name:
- Refresh-Group-Cache
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb576b5ef2310bceedb632a3b1ab8453b4d435e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844621"
---
# <a name="refresh-group-cache-extended-right"></a><span data-ttu-id="ee637-105">Actualiser-groupe-à droite étendu</span><span class="sxs-lookup"><span data-stu-id="ee637-105">Refresh-Group-Cache extended right</span></span>

<span data-ttu-id="ee637-106">Il ne s’agit pas d’une ouverture de session GC.</span><span class="sxs-lookup"><span data-stu-id="ee637-106">This is for no GC logon.</span></span> <span data-ttu-id="ee637-107">Aucune ouverture de session de catalogue global ne s’appuie sur les appartenances aux groupes de mise en cache, et ce droit d’accès de contrôle est utilisé pour accorder aux administrateurs et aux opérateurs des droits d’autorisation pour provoquer une actualisation immédiate du cache, en contactant un GC disponible.</span><span class="sxs-lookup"><span data-stu-id="ee637-107">No GC logon relies on caching group memberships, and this control access right is used to grant administrators and operators permission rights to cause an immediate refresh of the cache, contacting an available GC.</span></span>



| <span data-ttu-id="ee637-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-108">Entry</span></span> | <span data-ttu-id="ee637-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-109">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="ee637-110">CN</span><span class="sxs-lookup"><span data-stu-id="ee637-110">CN</span></span>           | <span data-ttu-id="ee637-111">Actualiser-groupe-cache</span><span class="sxs-lookup"><span data-stu-id="ee637-111">Refresh-Group-Cache</span></span>                  |
| <span data-ttu-id="ee637-112">Display-Name</span><span class="sxs-lookup"><span data-stu-id="ee637-112">Display-Name</span></span> | <span data-ttu-id="ee637-113">Actualiser le cache de groupe pour les ouvertures de session</span><span class="sxs-lookup"><span data-stu-id="ee637-113">Refresh Group Cache for Logons</span></span>       |
| <span data-ttu-id="ee637-114">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="ee637-114">Rights-GUID</span></span>  | <span data-ttu-id="ee637-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span><span class="sxs-lookup"><span data-stu-id="ee637-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span></span> |



## <a name="implementations"></a><span data-ttu-id="ee637-116">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ee637-116">Implementations</span></span>

-   [<span data-ttu-id="ee637-117">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee637-117">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee637-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee637-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee637-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee637-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee637-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee637-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee637-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee637-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ee637-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee637-122">Windows Server 2003</span></span>



| <span data-ttu-id="ee637-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-123">Entry</span></span> | <span data-ttu-id="ee637-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-124">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ee637-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ee637-125">Applies-To</span></span>              | [<span data-ttu-id="ee637-126">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ee637-126">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="ee637-127">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="ee637-127">Localization-Display-ID</span></span> | <span data-ttu-id="ee637-128">56</span><span class="sxs-lookup"><span data-stu-id="ee637-128">56</span></span>                                       |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee637-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee637-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee637-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-130">Entry</span></span> | <span data-ttu-id="ee637-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-131">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ee637-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ee637-132">Applies-To</span></span>              | [<span data-ttu-id="ee637-133">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ee637-133">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="ee637-134">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="ee637-134">Localization-Display-ID</span></span> | <span data-ttu-id="ee637-135">56</span><span class="sxs-lookup"><span data-stu-id="ee637-135">56</span></span>                                       |



## <a name="windows-server-2008"></a><span data-ttu-id="ee637-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee637-136">Windows Server 2008</span></span>



| <span data-ttu-id="ee637-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-137">Entry</span></span> | <span data-ttu-id="ee637-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-138">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ee637-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ee637-139">Applies-To</span></span>              | [<span data-ttu-id="ee637-140">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ee637-140">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="ee637-141">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="ee637-141">Localization-Display-ID</span></span> | <span data-ttu-id="ee637-142">56</span><span class="sxs-lookup"><span data-stu-id="ee637-142">56</span></span>                                       |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee637-143">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee637-143">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee637-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-144">Entry</span></span> | <span data-ttu-id="ee637-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-145">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ee637-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ee637-146">Applies-To</span></span>              | [<span data-ttu-id="ee637-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ee637-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="ee637-148">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="ee637-148">Localization-Display-ID</span></span> | <span data-ttu-id="ee637-149">56</span><span class="sxs-lookup"><span data-stu-id="ee637-149">56</span></span>                                       |



## <a name="windows-server-2012"></a><span data-ttu-id="ee637-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee637-150">Windows Server 2012</span></span>



| <span data-ttu-id="ee637-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee637-151">Entry</span></span> | <span data-ttu-id="ee637-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee637-152">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ee637-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ee637-153">Applies-To</span></span>              | [<span data-ttu-id="ee637-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ee637-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="ee637-155">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="ee637-155">Localization-Display-ID</span></span> | <span data-ttu-id="ee637-156">56</span><span class="sxs-lookup"><span data-stu-id="ee637-156">56</span></span>                                       |



 

 





