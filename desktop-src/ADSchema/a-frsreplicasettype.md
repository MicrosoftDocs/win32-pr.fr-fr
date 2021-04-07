---
title: Attribut FRS-Replica-Set-type
description: Il s’agit d’un code qui indique s’il s’agit d’un jeu de réplicas Sysvol, d’un jeu de réplicas DFS ou d’un autre jeu de réplicas.
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory FRS-Replica-Set-type
- Schéma AD de l’attribut fRSReplicaSetType
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844661"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="89f11-105">Attribut FRS-Replica-Set-type</span><span class="sxs-lookup"><span data-stu-id="89f11-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="89f11-106">Il s’agit d’un code qui indique s’il s’agit d’un jeu de réplicas Sysvol, d’un jeu de réplicas DFS ou d’un autre jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="89f11-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="89f11-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-107">Entry</span></span> | <span data-ttu-id="89f11-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="89f11-109">CN</span><span class="sxs-lookup"><span data-stu-id="89f11-109">CN</span></span>                | <span data-ttu-id="89f11-110">FRS-Replica-Set-type</span><span class="sxs-lookup"><span data-stu-id="89f11-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="89f11-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="89f11-111">Ldap-Display-Name</span></span> | <span data-ttu-id="89f11-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="89f11-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="89f11-113">Taille</span><span class="sxs-lookup"><span data-stu-id="89f11-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="89f11-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="89f11-114">Update Privilege</span></span>  | <span data-ttu-id="89f11-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="89f11-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="89f11-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="89f11-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="89f11-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-117">Attribute-Id</span></span>      | <span data-ttu-id="89f11-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="89f11-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="89f11-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="89f11-119">System-Id-Guid</span></span>    | <span data-ttu-id="89f11-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="89f11-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="89f11-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89f11-121">Syntax</span></span>            | [<span data-ttu-id="89f11-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="89f11-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="89f11-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="89f11-123">Implementations</span></span>

-   [<span data-ttu-id="89f11-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="89f11-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="89f11-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="89f11-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="89f11-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="89f11-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="89f11-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="89f11-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="89f11-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="89f11-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="89f11-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="89f11-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="89f11-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89f11-130">Windows 2000 Server</span></span>



| <span data-ttu-id="89f11-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-131">Entry</span></span> | <span data-ttu-id="89f11-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-135">System-Only</span></span>            | <span data-ttu-id="89f11-136">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-136">False</span></span>                                                     |
| <span data-ttu-id="89f11-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-137">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-138">True</span></span>                                                      |
| <span data-ttu-id="89f11-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-139">Is Indexed</span></span>             | <span data-ttu-id="89f11-140">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-140">False</span></span>                                                     |
| <span data-ttu-id="89f11-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-141">In Global Catalog</span></span>      | <span data-ttu-id="89f11-142">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-142">False</span></span>                                                     |
| <span data-ttu-id="89f11-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-147">Search-Flags</span></span>           | <span data-ttu-id="89f11-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-148">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-149">System-Flags</span></span>           | <span data-ttu-id="89f11-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-150">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-151">Classes used in</span></span>        | [<span data-ttu-id="89f11-152">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="89f11-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89f11-153">Windows Server 2003</span></span>



| <span data-ttu-id="89f11-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-154">Entry</span></span> | <span data-ttu-id="89f11-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-158">System-Only</span></span>            | <span data-ttu-id="89f11-159">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-159">False</span></span>                                                     |
| <span data-ttu-id="89f11-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-160">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-161">True</span></span>                                                      |
| <span data-ttu-id="89f11-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-162">Is Indexed</span></span>             | <span data-ttu-id="89f11-163">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-163">False</span></span>                                                     |
| <span data-ttu-id="89f11-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-164">In Global Catalog</span></span>      | <span data-ttu-id="89f11-165">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-165">False</span></span>                                                     |
| <span data-ttu-id="89f11-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-170">Search-Flags</span></span>           | <span data-ttu-id="89f11-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-171">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-172">System-Flags</span></span>           | <span data-ttu-id="89f11-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-173">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-174">Classes used in</span></span>        | [<span data-ttu-id="89f11-175">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="89f11-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="89f11-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="89f11-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-177">Entry</span></span> | <span data-ttu-id="89f11-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-181">System-Only</span></span>            | <span data-ttu-id="89f11-182">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-182">False</span></span>                                                     |
| <span data-ttu-id="89f11-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-183">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-184">True</span></span>                                                      |
| <span data-ttu-id="89f11-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-185">Is Indexed</span></span>             | <span data-ttu-id="89f11-186">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-186">False</span></span>                                                     |
| <span data-ttu-id="89f11-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-187">In Global Catalog</span></span>      | <span data-ttu-id="89f11-188">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-188">False</span></span>                                                     |
| <span data-ttu-id="89f11-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-193">Search-Flags</span></span>           | <span data-ttu-id="89f11-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-194">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-195">System-Flags</span></span>           | <span data-ttu-id="89f11-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-196">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-197">Classes used in</span></span>        | [<span data-ttu-id="89f11-198">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="89f11-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f11-199">Windows Server 2008</span></span>



| <span data-ttu-id="89f11-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-200">Entry</span></span> | <span data-ttu-id="89f11-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-204">System-Only</span></span>            | <span data-ttu-id="89f11-205">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-205">False</span></span>                                                     |
| <span data-ttu-id="89f11-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-206">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-207">True</span></span>                                                      |
| <span data-ttu-id="89f11-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-208">Is Indexed</span></span>             | <span data-ttu-id="89f11-209">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-209">False</span></span>                                                     |
| <span data-ttu-id="89f11-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-210">In Global Catalog</span></span>      | <span data-ttu-id="89f11-211">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-211">False</span></span>                                                     |
| <span data-ttu-id="89f11-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-216">Search-Flags</span></span>           | <span data-ttu-id="89f11-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-217">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-218">System-Flags</span></span>           | <span data-ttu-id="89f11-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-219">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-220">Classes used in</span></span>        | [<span data-ttu-id="89f11-221">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="89f11-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89f11-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="89f11-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-223">Entry</span></span> | <span data-ttu-id="89f11-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-227">System-Only</span></span>            | <span data-ttu-id="89f11-228">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-228">False</span></span>                                                     |
| <span data-ttu-id="89f11-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-229">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-230">True</span></span>                                                      |
| <span data-ttu-id="89f11-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-231">Is Indexed</span></span>             | <span data-ttu-id="89f11-232">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-232">False</span></span>                                                     |
| <span data-ttu-id="89f11-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-233">In Global Catalog</span></span>      | <span data-ttu-id="89f11-234">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-234">False</span></span>                                                     |
| <span data-ttu-id="89f11-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-239">Search-Flags</span></span>           | <span data-ttu-id="89f11-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-240">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-241">System-Flags</span></span>           | <span data-ttu-id="89f11-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-242">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-243">Classes used in</span></span>        | [<span data-ttu-id="89f11-244">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="89f11-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89f11-245">Windows Server 2012</span></span>



| <span data-ttu-id="89f11-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-246">Entry</span></span> | <span data-ttu-id="89f11-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f11-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89f11-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="89f11-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89f11-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="89f11-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="89f11-250">System-Only</span></span>            | <span data-ttu-id="89f11-251">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-251">False</span></span>                                                     |
| <span data-ttu-id="89f11-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="89f11-252">Is-Single-Valued</span></span>       | <span data-ttu-id="89f11-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="89f11-253">True</span></span>                                                      |
| <span data-ttu-id="89f11-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="89f11-254">Is Indexed</span></span>             | <span data-ttu-id="89f11-255">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-255">False</span></span>                                                     |
| <span data-ttu-id="89f11-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="89f11-256">In Global Catalog</span></span>      | <span data-ttu-id="89f11-257">Faux</span><span class="sxs-lookup"><span data-stu-id="89f11-257">False</span></span>                                                     |
| <span data-ttu-id="89f11-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="89f11-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="89f11-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="89f11-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="89f11-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89f11-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89f11-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="89f11-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-262">Search-Flags</span></span>           | <span data-ttu-id="89f11-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89f11-263">0x00000000</span></span>                                                |
| <span data-ttu-id="89f11-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89f11-264">System-Flags</span></span>           | <span data-ttu-id="89f11-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89f11-265">0x00000010</span></span>                                                |
| <span data-ttu-id="89f11-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="89f11-266">Classes used in</span></span>        | [<span data-ttu-id="89f11-267">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="89f11-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





