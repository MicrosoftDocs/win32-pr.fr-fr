---
title: Attribut FRS-version-GUID
description: Si elle est présente, la modification de cette valeur indique qu’une modification de configuration a été apportée à ce jeu de réplicas.
ms.assetid: 27cd68c5-a8aa-4c14-bf1d-0eb7c4d9cca5
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory FRS-version-GUID Attribute
- Schéma AD de l’attribut fRSVersionGUID
topic_type:
- apiref
api_name:
- FRS-Version-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12cfadd1086fbb8ee79bafb8d0ee5f947ff503e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519929"
---
# <a name="frs-version-guid-attribute"></a><span data-ttu-id="c39a9-105">Attribut FRS-version-GUID</span><span class="sxs-lookup"><span data-stu-id="c39a9-105">FRS-Version-GUID attribute</span></span>

<span data-ttu-id="c39a9-106">Si elle est présente, la modification de cette valeur indique qu’une modification de configuration a été apportée à ce jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="c39a9-106">If present, changing this value indicates a configuration change has been made on this replica set.</span></span>



| <span data-ttu-id="c39a9-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-107">Entry</span></span> | <span data-ttu-id="c39a9-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c39a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="c39a9-109">CN</span></span>                | <span data-ttu-id="c39a9-110">FRS-version-GUID</span><span class="sxs-lookup"><span data-stu-id="c39a9-110">FRS-Version-GUID</span></span>                                      |
| <span data-ttu-id="c39a9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c39a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c39a9-112">fRSVersionGUID</span><span class="sxs-lookup"><span data-stu-id="c39a9-112">fRSVersionGUID</span></span>                                        |
| <span data-ttu-id="c39a9-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c39a9-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c39a9-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c39a9-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c39a9-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c39a9-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c39a9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-116">Attribute-Id</span></span>      | <span data-ttu-id="c39a9-117">1.2.840.113556.1.4.43</span><span class="sxs-lookup"><span data-stu-id="c39a9-117">1.2.840.113556.1.4.43</span></span>                                 |
| <span data-ttu-id="c39a9-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c39a9-118">System-Id-Guid</span></span>    | <span data-ttu-id="c39a9-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c39a9-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span></span>                  |
| <span data-ttu-id="c39a9-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c39a9-120">Syntax</span></span>            | [<span data-ttu-id="c39a9-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c39a9-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c39a9-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c39a9-122">Implementations</span></span>

-   [<span data-ttu-id="c39a9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c39a9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c39a9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c39a9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c39a9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c39a9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c39a9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c39a9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c39a9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c39a9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c39a9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c39a9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c39a9-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c39a9-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c39a9-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-130">Entry</span></span> | <span data-ttu-id="c39a9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-134">System-Only</span></span>            | <span data-ttu-id="c39a9-135">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-135">False</span></span>                                                     |
| <span data-ttu-id="c39a9-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-137">True</span></span>                                                      |
| <span data-ttu-id="c39a9-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-138">Is Indexed</span></span>             | <span data-ttu-id="c39a9-139">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-139">False</span></span>                                                     |
| <span data-ttu-id="c39a9-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-140">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-141">False</span></span>                                                     |
| <span data-ttu-id="c39a9-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-144">Range-Lower</span></span>            | <span data-ttu-id="c39a9-145">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-145">16</span></span>                                                        |
| <span data-ttu-id="c39a9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-146">Range-Upper</span></span>            | <span data-ttu-id="c39a9-147">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-147">16</span></span>                                                        |
| <span data-ttu-id="c39a9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-148">Search-Flags</span></span>           | <span data-ttu-id="c39a9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-149">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-150">System-Flags</span></span>           | <span data-ttu-id="c39a9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-151">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-152">Classes used in</span></span>        | [<span data-ttu-id="c39a9-153">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c39a9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c39a9-154">Windows Server 2003</span></span>



| <span data-ttu-id="c39a9-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-155">Entry</span></span> | <span data-ttu-id="c39a9-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-159">System-Only</span></span>            | <span data-ttu-id="c39a9-160">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-160">False</span></span>                                                     |
| <span data-ttu-id="c39a9-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-162">True</span></span>                                                      |
| <span data-ttu-id="c39a9-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-163">Is Indexed</span></span>             | <span data-ttu-id="c39a9-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-164">False</span></span>                                                     |
| <span data-ttu-id="c39a9-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-165">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-166">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-166">False</span></span>                                                     |
| <span data-ttu-id="c39a9-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-169">Range-Lower</span></span>            | <span data-ttu-id="c39a9-170">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-170">16</span></span>                                                        |
| <span data-ttu-id="c39a9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-171">Range-Upper</span></span>            | <span data-ttu-id="c39a9-172">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-172">16</span></span>                                                        |
| <span data-ttu-id="c39a9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-173">Search-Flags</span></span>           | <span data-ttu-id="c39a9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-174">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-175">System-Flags</span></span>           | <span data-ttu-id="c39a9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-176">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-177">Classes used in</span></span>        | [<span data-ttu-id="c39a9-178">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c39a9-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c39a9-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c39a9-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-180">Entry</span></span> | <span data-ttu-id="c39a9-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-184">System-Only</span></span>            | <span data-ttu-id="c39a9-185">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-185">False</span></span>                                                     |
| <span data-ttu-id="c39a9-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-187">True</span></span>                                                      |
| <span data-ttu-id="c39a9-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-188">Is Indexed</span></span>             | <span data-ttu-id="c39a9-189">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-189">False</span></span>                                                     |
| <span data-ttu-id="c39a9-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-190">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-191">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-191">False</span></span>                                                     |
| <span data-ttu-id="c39a9-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-194">Range-Lower</span></span>            | <span data-ttu-id="c39a9-195">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-195">16</span></span>                                                        |
| <span data-ttu-id="c39a9-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-196">Range-Upper</span></span>            | <span data-ttu-id="c39a9-197">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-197">16</span></span>                                                        |
| <span data-ttu-id="c39a9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-198">Search-Flags</span></span>           | <span data-ttu-id="c39a9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-199">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-200">System-Flags</span></span>           | <span data-ttu-id="c39a9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-201">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-202">Classes used in</span></span>        | [<span data-ttu-id="c39a9-203">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c39a9-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c39a9-204">Windows Server 2008</span></span>



| <span data-ttu-id="c39a9-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-205">Entry</span></span> | <span data-ttu-id="c39a9-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-209">System-Only</span></span>            | <span data-ttu-id="c39a9-210">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-210">False</span></span>                                                     |
| <span data-ttu-id="c39a9-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-212">True</span></span>                                                      |
| <span data-ttu-id="c39a9-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-213">Is Indexed</span></span>             | <span data-ttu-id="c39a9-214">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-214">False</span></span>                                                     |
| <span data-ttu-id="c39a9-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-215">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-216">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-216">False</span></span>                                                     |
| <span data-ttu-id="c39a9-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-219">Range-Lower</span></span>            | <span data-ttu-id="c39a9-220">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-220">16</span></span>                                                        |
| <span data-ttu-id="c39a9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-221">Range-Upper</span></span>            | <span data-ttu-id="c39a9-222">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-222">16</span></span>                                                        |
| <span data-ttu-id="c39a9-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-223">Search-Flags</span></span>           | <span data-ttu-id="c39a9-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-224">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-225">System-Flags</span></span>           | <span data-ttu-id="c39a9-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-226">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-227">Classes used in</span></span>        | [<span data-ttu-id="c39a9-228">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c39a9-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c39a9-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c39a9-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-230">Entry</span></span> | <span data-ttu-id="c39a9-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-234">System-Only</span></span>            | <span data-ttu-id="c39a9-235">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-235">False</span></span>                                                     |
| <span data-ttu-id="c39a9-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-237">True</span></span>                                                      |
| <span data-ttu-id="c39a9-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-238">Is Indexed</span></span>             | <span data-ttu-id="c39a9-239">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-239">False</span></span>                                                     |
| <span data-ttu-id="c39a9-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-240">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-241">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-241">False</span></span>                                                     |
| <span data-ttu-id="c39a9-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-244">Range-Lower</span></span>            | <span data-ttu-id="c39a9-245">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-245">16</span></span>                                                        |
| <span data-ttu-id="c39a9-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-246">Range-Upper</span></span>            | <span data-ttu-id="c39a9-247">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-247">16</span></span>                                                        |
| <span data-ttu-id="c39a9-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-248">Search-Flags</span></span>           | <span data-ttu-id="c39a9-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-249">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-250">System-Flags</span></span>           | <span data-ttu-id="c39a9-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-251">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-252">Classes used in</span></span>        | [<span data-ttu-id="c39a9-253">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c39a9-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c39a9-254">Windows Server 2012</span></span>



| <span data-ttu-id="c39a9-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="c39a9-255">Entry</span></span> | <span data-ttu-id="c39a9-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="c39a9-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c39a9-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c39a9-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39a9-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c39a9-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39a9-259">System-Only</span></span>            | <span data-ttu-id="c39a9-260">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-260">False</span></span>                                                     |
| <span data-ttu-id="c39a9-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c39a9-261">Is-Single-Valued</span></span>       | <span data-ttu-id="c39a9-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="c39a9-262">True</span></span>                                                      |
| <span data-ttu-id="c39a9-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c39a9-263">Is Indexed</span></span>             | <span data-ttu-id="c39a9-264">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-264">False</span></span>                                                     |
| <span data-ttu-id="c39a9-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c39a9-265">In Global Catalog</span></span>      | <span data-ttu-id="c39a9-266">Faux</span><span class="sxs-lookup"><span data-stu-id="c39a9-266">False</span></span>                                                     |
| <span data-ttu-id="c39a9-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c39a9-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39a9-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c39a9-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c39a9-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39a9-269">Range-Lower</span></span>            | <span data-ttu-id="c39a9-270">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-270">16</span></span>                                                        |
| <span data-ttu-id="c39a9-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39a9-271">Range-Upper</span></span>            | <span data-ttu-id="c39a9-272">16</span><span class="sxs-lookup"><span data-stu-id="c39a9-272">16</span></span>                                                        |
| <span data-ttu-id="c39a9-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-273">Search-Flags</span></span>           | <span data-ttu-id="c39a9-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39a9-274">0x00000000</span></span>                                                |
| <span data-ttu-id="c39a9-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39a9-275">System-Flags</span></span>           | <span data-ttu-id="c39a9-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39a9-276">0x00000010</span></span>                                                |
| <span data-ttu-id="c39a9-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c39a9-277">Classes used in</span></span>        | [<span data-ttu-id="c39a9-278">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="c39a9-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





