---
title: attribut ms-DS-KrbTgt-Link
description: Utilisé avec les contrôleurs de domaine en lecture seule pour définir le \_ compte krbtgt xxxx correspondant à chaque RODC.
ms.assetid: 08c3e50f-7f2a-4746-86b6-77780316679c
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de lien ms-DS-KrbTgt
- Schéma Active Directory de l’attribut msDS-KrbTgtLink
topic_type:
- apiref
api_name:
- ms-DS-KrbTgt-Link
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcf8ddfee6f15532e4dad91fc1e34e1f136ea99b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845486"
---
# <a name="ms-ds-krbtgt-link-attribute"></a><span data-ttu-id="50476-105">attribut ms-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="50476-105">ms-DS-KrbTgt-Link attribute</span></span>

<span data-ttu-id="50476-106">Utilisé avec les contrôleurs de domaine en lecture seule pour définir le \_ compte krbtgt xxxx correspondant à chaque RODC.</span><span class="sxs-lookup"><span data-stu-id="50476-106">Used with RODCs to define which krbtgt\_XXXX account corresponds to each RODC.</span></span>



| <span data-ttu-id="50476-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="50476-107">Entry</span></span> | <span data-ttu-id="50476-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="50476-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="50476-109">CN</span><span class="sxs-lookup"><span data-stu-id="50476-109">CN</span></span>                | <span data-ttu-id="50476-110">ms-DS-KrbTgt-lien</span><span class="sxs-lookup"><span data-stu-id="50476-110">ms-DS-KrbTgt-Link</span></span>                       |
| <span data-ttu-id="50476-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="50476-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50476-112">msDS-KrbTgtLink</span><span class="sxs-lookup"><span data-stu-id="50476-112">msDS-KrbTgtLink</span></span>                         |
| <span data-ttu-id="50476-113">Taille</span><span class="sxs-lookup"><span data-stu-id="50476-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="50476-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="50476-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="50476-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="50476-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="50476-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50476-116">Attribute-Id</span></span>      | <span data-ttu-id="50476-117">1.2.840.113556.1.4.1923</span><span class="sxs-lookup"><span data-stu-id="50476-117">1.2.840.113556.1.4.1923</span></span>                 |
| <span data-ttu-id="50476-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="50476-118">System-Id-Guid</span></span>    | <span data-ttu-id="50476-119">778ff5c9-6f4e-4b74-856a-d68383313910</span><span class="sxs-lookup"><span data-stu-id="50476-119">778ff5c9-6f4e-4b74-856a-d68383313910</span></span>    |
| <span data-ttu-id="50476-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50476-120">Syntax</span></span>            | [<span data-ttu-id="50476-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="50476-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="50476-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="50476-122">Implementations</span></span>

-   [<span data-ttu-id="50476-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50476-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50476-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50476-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50476-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50476-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="50476-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50476-126">Windows Server 2008</span></span>



| <span data-ttu-id="50476-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="50476-127">Entry</span></span> | <span data-ttu-id="50476-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="50476-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="50476-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="50476-129">Link-Id</span></span>                | <span data-ttu-id="50476-130">2100</span><span class="sxs-lookup"><span data-stu-id="50476-130">2100</span></span>                                      |
| <span data-ttu-id="50476-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50476-131">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="50476-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="50476-132">System-Only</span></span>            | <span data-ttu-id="50476-133">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-133">False</span></span>                                     |
| <span data-ttu-id="50476-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="50476-134">Is-Single-Valued</span></span>       | <span data-ttu-id="50476-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="50476-135">True</span></span>                                      |
| <span data-ttu-id="50476-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="50476-136">Is Indexed</span></span>             | <span data-ttu-id="50476-137">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-137">False</span></span>                                     |
| <span data-ttu-id="50476-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="50476-138">In Global Catalog</span></span>      | <span data-ttu-id="50476-139">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-139">False</span></span>                                     |
| <span data-ttu-id="50476-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="50476-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="50476-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="50476-141">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="50476-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50476-142">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="50476-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50476-143">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="50476-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-144">Search-Flags</span></span>           | <span data-ttu-id="50476-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50476-145">0x00000000</span></span>                                |
| <span data-ttu-id="50476-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-146">System-Flags</span></span>           | <span data-ttu-id="50476-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50476-147">0x00000010</span></span>                                |
| <span data-ttu-id="50476-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="50476-148">Classes used in</span></span>        | [<span data-ttu-id="50476-149">**Computer**</span><span class="sxs-lookup"><span data-stu-id="50476-149">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50476-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50476-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50476-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="50476-151">Entry</span></span> | <span data-ttu-id="50476-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="50476-152">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="50476-153">ID de lien</span><span class="sxs-lookup"><span data-stu-id="50476-153">Link-Id</span></span>                | <span data-ttu-id="50476-154">2100</span><span class="sxs-lookup"><span data-stu-id="50476-154">2100</span></span>                                      |
| <span data-ttu-id="50476-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50476-155">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="50476-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="50476-156">System-Only</span></span>            | <span data-ttu-id="50476-157">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-157">False</span></span>                                     |
| <span data-ttu-id="50476-158">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="50476-158">Is-Single-Valued</span></span>       | <span data-ttu-id="50476-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="50476-159">True</span></span>                                      |
| <span data-ttu-id="50476-160">Est indexé</span><span class="sxs-lookup"><span data-stu-id="50476-160">Is Indexed</span></span>             | <span data-ttu-id="50476-161">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-161">False</span></span>                                     |
| <span data-ttu-id="50476-162">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="50476-162">In Global Catalog</span></span>      | <span data-ttu-id="50476-163">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-163">False</span></span>                                     |
| <span data-ttu-id="50476-164">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="50476-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="50476-165">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="50476-165">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="50476-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50476-166">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="50476-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50476-167">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="50476-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-168">Search-Flags</span></span>           | <span data-ttu-id="50476-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50476-169">0x00000000</span></span>                                |
| <span data-ttu-id="50476-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-170">System-Flags</span></span>           | <span data-ttu-id="50476-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50476-171">0x00000010</span></span>                                |
| <span data-ttu-id="50476-172">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="50476-172">Classes used in</span></span>        | [<span data-ttu-id="50476-173">**Computer**</span><span class="sxs-lookup"><span data-stu-id="50476-173">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50476-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50476-174">Windows Server 2012</span></span>



| <span data-ttu-id="50476-175">Entrée</span><span class="sxs-lookup"><span data-stu-id="50476-175">Entry</span></span> | <span data-ttu-id="50476-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="50476-176">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="50476-177">ID de lien</span><span class="sxs-lookup"><span data-stu-id="50476-177">Link-Id</span></span>                | <span data-ttu-id="50476-178">2100</span><span class="sxs-lookup"><span data-stu-id="50476-178">2100</span></span>                                      |
| <span data-ttu-id="50476-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50476-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="50476-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="50476-180">System-Only</span></span>            | <span data-ttu-id="50476-181">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-181">False</span></span>                                     |
| <span data-ttu-id="50476-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="50476-182">Is-Single-Valued</span></span>       | <span data-ttu-id="50476-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="50476-183">True</span></span>                                      |
| <span data-ttu-id="50476-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="50476-184">Is Indexed</span></span>             | <span data-ttu-id="50476-185">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-185">False</span></span>                                     |
| <span data-ttu-id="50476-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="50476-186">In Global Catalog</span></span>      | <span data-ttu-id="50476-187">Faux</span><span class="sxs-lookup"><span data-stu-id="50476-187">False</span></span>                                     |
| <span data-ttu-id="50476-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="50476-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="50476-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="50476-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="50476-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50476-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="50476-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50476-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="50476-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-192">Search-Flags</span></span>           | <span data-ttu-id="50476-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50476-193">0x00000000</span></span>                                |
| <span data-ttu-id="50476-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50476-194">System-Flags</span></span>           | <span data-ttu-id="50476-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50476-195">0x00000010</span></span>                                |
| <span data-ttu-id="50476-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="50476-196">Classes used in</span></span>        | [<span data-ttu-id="50476-197">**Computer**</span><span class="sxs-lookup"><span data-stu-id="50476-197">**Computer**</span></span>](c-computer.md)<br/> |



 

 





