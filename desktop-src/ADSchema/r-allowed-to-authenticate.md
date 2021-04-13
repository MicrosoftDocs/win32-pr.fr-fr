---
title: Autorisé à authentifier à droite étendu
description: Les contrôles de droits d’accès du contrôle qui peuvent s’authentifier auprès d’un ordinateur ou d’un service particulier.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Autorisé à authentifier le schéma AD droit étendu
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480445"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="4ae3d-104">Autorisé à authentifier à droite étendu</span><span class="sxs-lookup"><span data-stu-id="4ae3d-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="4ae3d-105">Les contrôles de droits d’accès du contrôle qui peuvent s’authentifier auprès d’un ordinateur ou d’un service particulier.</span><span class="sxs-lookup"><span data-stu-id="4ae3d-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="4ae3d-106">Elle réside en fait sur les objets ordinateur, utilisateur et InetOrgPerson.</span><span class="sxs-lookup"><span data-stu-id="4ae3d-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="4ae3d-107">Il est également applicable sur l’objet de domaine si l’accès est autorisé pour l’ensemble du domaine.</span><span class="sxs-lookup"><span data-stu-id="4ae3d-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="4ae3d-108">Il peut être appliqué aux unités d’organisation pour permettre aux utilisateurs de définir des ACE pouvant être héritées sur les unités d’organisation qui contiennent un ensemble d’objets utilisateur ou ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4ae3d-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="4ae3d-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-109">Entry</span></span> | <span data-ttu-id="4ae3d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="4ae3d-111">CN</span><span class="sxs-lookup"><span data-stu-id="4ae3d-111">CN</span></span>           | <span data-ttu-id="4ae3d-112">Autorisé à s’authentifier</span><span class="sxs-lookup"><span data-stu-id="4ae3d-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="4ae3d-113">Display-Name</span><span class="sxs-lookup"><span data-stu-id="4ae3d-113">Display-Name</span></span> | <span data-ttu-id="4ae3d-114">Autorisé à s’authentifier</span><span class="sxs-lookup"><span data-stu-id="4ae3d-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="4ae3d-115">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-115">Rights-GUID</span></span>  | <span data-ttu-id="4ae3d-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="4ae3d-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="4ae3d-117">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4ae3d-117">Implementations</span></span>

-   [<span data-ttu-id="4ae3d-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ae3d-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ae3d-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ae3d-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ae3d-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4ae3d-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ae3d-123">Windows Server 2003</span></span>



| <span data-ttu-id="4ae3d-124">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-124">Entry</span></span> | <span data-ttu-id="4ae3d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae3d-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4ae3d-126">Applies-To</span></span>              | [<span data-ttu-id="4ae3d-127">**Computer**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4ae3d-128">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="4ae3d-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="4ae3d-130">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-130">Localization-Display-ID</span></span> | <span data-ttu-id="4ae3d-131">65</span><span class="sxs-lookup"><span data-stu-id="4ae3d-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ae3d-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ae3d-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ae3d-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-133">Entry</span></span> | <span data-ttu-id="4ae3d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae3d-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4ae3d-135">Applies-To</span></span>              | [<span data-ttu-id="4ae3d-136">**Computer**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4ae3d-137">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="4ae3d-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="4ae3d-139">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-139">Localization-Display-ID</span></span> | <span data-ttu-id="4ae3d-140">65</span><span class="sxs-lookup"><span data-stu-id="4ae3d-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="4ae3d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ae3d-141">Windows Server 2008</span></span>



| <span data-ttu-id="4ae3d-142">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-142">Entry</span></span> | <span data-ttu-id="4ae3d-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae3d-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4ae3d-144">Applies-To</span></span>              | [<span data-ttu-id="4ae3d-145">**Computer**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4ae3d-146">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="4ae3d-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="4ae3d-148">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-148">Localization-Display-ID</span></span> | <span data-ttu-id="4ae3d-149">65</span><span class="sxs-lookup"><span data-stu-id="4ae3d-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ae3d-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ae3d-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ae3d-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-151">Entry</span></span> | <span data-ttu-id="4ae3d-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae3d-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4ae3d-153">Applies-To</span></span>              | [<span data-ttu-id="4ae3d-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4ae3d-155">**ms-DS-Managed-service-account**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="4ae3d-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="4ae3d-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="4ae3d-158">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-158">Localization-Display-ID</span></span> | <span data-ttu-id="4ae3d-159">65</span><span class="sxs-lookup"><span data-stu-id="4ae3d-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="4ae3d-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ae3d-160">Windows Server 2012</span></span>



| <span data-ttu-id="4ae3d-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae3d-161">Entry</span></span> | <span data-ttu-id="4ae3d-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae3d-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae3d-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4ae3d-163">Applies-To</span></span>              | [<span data-ttu-id="4ae3d-164">**Computer**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4ae3d-165">**ms-DS-Managed-service-account**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="4ae3d-166">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="4ae3d-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4ae3d-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="4ae3d-168">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="4ae3d-168">Localization-Display-ID</span></span> | <span data-ttu-id="4ae3d-169">65</span><span class="sxs-lookup"><span data-stu-id="4ae3d-169">65</span></span>                                                                                                                                                                                                               |



 

 





