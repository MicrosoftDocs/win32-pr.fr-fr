---
title: Attribut Object-Count
description: Quota de fichiers suivi pour un volume donné.
ms.assetid: 22900e97-d3d3-49cc-a2c3-1f557fe383b1
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Count
- Schéma AD de l’attribut objectCount
topic_type:
- apiref
api_name:
- Object-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9a93f4f84a9fb01922659bddd6b9fc1982e58e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844986"
---
# <a name="object-count-attribute"></a><span data-ttu-id="a0180-105">Attribut Object-Count</span><span class="sxs-lookup"><span data-stu-id="a0180-105">Object-Count attribute</span></span>

<span data-ttu-id="a0180-106">Quota de fichiers suivi pour un volume donné.</span><span class="sxs-lookup"><span data-stu-id="a0180-106">Tracked file quota for a given volume.</span></span>



| <span data-ttu-id="a0180-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-107">Entry</span></span> | <span data-ttu-id="a0180-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a0180-109">CN</span><span class="sxs-lookup"><span data-stu-id="a0180-109">CN</span></span>                | <span data-ttu-id="a0180-110">Object-Count</span><span class="sxs-lookup"><span data-stu-id="a0180-110">Object-Count</span></span>                         |
| <span data-ttu-id="a0180-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a0180-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a0180-112">objectCount</span><span class="sxs-lookup"><span data-stu-id="a0180-112">objectCount</span></span>                          |
| <span data-ttu-id="a0180-113">Taille</span><span class="sxs-lookup"><span data-stu-id="a0180-113">Size</span></span>              | <span data-ttu-id="a0180-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="a0180-114">4 bytes</span></span>                              |
| <span data-ttu-id="a0180-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a0180-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a0180-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a0180-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a0180-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-117">Attribute-Id</span></span>      | <span data-ttu-id="a0180-118">1.2.840.113556.1.4.506</span><span class="sxs-lookup"><span data-stu-id="a0180-118">1.2.840.113556.1.4.506</span></span>               |
| <span data-ttu-id="a0180-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a0180-119">System-Id-Guid</span></span>    | <span data-ttu-id="a0180-120">34aaa216-b699-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a0180-120">34aaa216-b699-11d0-afee-0000f80367c1</span></span> |
| <span data-ttu-id="a0180-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0180-121">Syntax</span></span>            | [<span data-ttu-id="a0180-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a0180-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a0180-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a0180-123">Implementations</span></span>

-   [<span data-ttu-id="a0180-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a0180-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a0180-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0180-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0180-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0180-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0180-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0180-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0180-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0180-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0180-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0180-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a0180-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0180-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a0180-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-131">Entry</span></span> | <span data-ttu-id="a0180-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-132">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-133">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-134">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-135">System-Only</span></span>            | <span data-ttu-id="a0180-136">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-136">False</span></span>                                                          |
| <span data-ttu-id="a0180-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-138">True</span></span>                                                           |
| <span data-ttu-id="a0180-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-139">Is Indexed</span></span>             | <span data-ttu-id="a0180-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-140">False</span></span>                                                          |
| <span data-ttu-id="a0180-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-141">In Global Catalog</span></span>      | <span data-ttu-id="a0180-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-142">False</span></span>                                                          |
| <span data-ttu-id="a0180-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-144">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-145">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-146">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-147">Search-Flags</span></span>           | <span data-ttu-id="a0180-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-148">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-149">System-Flags</span></span>           | <span data-ttu-id="a0180-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-150">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-151">Classes used in</span></span>        | [<span data-ttu-id="a0180-152">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-152">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a0180-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0180-153">Windows Server 2003</span></span>



| <span data-ttu-id="a0180-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-154">Entry</span></span> | <span data-ttu-id="a0180-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-155">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-156">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-157">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-158">System-Only</span></span>            | <span data-ttu-id="a0180-159">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-159">False</span></span>                                                          |
| <span data-ttu-id="a0180-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-161">True</span></span>                                                           |
| <span data-ttu-id="a0180-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-162">Is Indexed</span></span>             | <span data-ttu-id="a0180-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-163">False</span></span>                                                          |
| <span data-ttu-id="a0180-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-164">In Global Catalog</span></span>      | <span data-ttu-id="a0180-165">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-165">False</span></span>                                                          |
| <span data-ttu-id="a0180-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-167">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-168">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-169">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-170">Search-Flags</span></span>           | <span data-ttu-id="a0180-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-171">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-172">System-Flags</span></span>           | <span data-ttu-id="a0180-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-173">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-174">Classes used in</span></span>        | [<span data-ttu-id="a0180-175">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-175">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0180-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0180-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0180-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-177">Entry</span></span> | <span data-ttu-id="a0180-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-178">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-179">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-180">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-181">System-Only</span></span>            | <span data-ttu-id="a0180-182">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-182">False</span></span>                                                          |
| <span data-ttu-id="a0180-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-184">True</span></span>                                                           |
| <span data-ttu-id="a0180-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-185">Is Indexed</span></span>             | <span data-ttu-id="a0180-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-186">False</span></span>                                                          |
| <span data-ttu-id="a0180-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-187">In Global Catalog</span></span>      | <span data-ttu-id="a0180-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-188">False</span></span>                                                          |
| <span data-ttu-id="a0180-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-190">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-191">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-192">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-193">Search-Flags</span></span>           | <span data-ttu-id="a0180-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-194">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-195">System-Flags</span></span>           | <span data-ttu-id="a0180-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-196">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-197">Classes used in</span></span>        | [<span data-ttu-id="a0180-198">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-198">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0180-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0180-199">Windows Server 2008</span></span>



| <span data-ttu-id="a0180-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-200">Entry</span></span> | <span data-ttu-id="a0180-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-201">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-202">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-203">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-204">System-Only</span></span>            | <span data-ttu-id="a0180-205">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-205">False</span></span>                                                          |
| <span data-ttu-id="a0180-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-207">True</span></span>                                                           |
| <span data-ttu-id="a0180-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-208">Is Indexed</span></span>             | <span data-ttu-id="a0180-209">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-209">False</span></span>                                                          |
| <span data-ttu-id="a0180-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-210">In Global Catalog</span></span>      | <span data-ttu-id="a0180-211">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-211">False</span></span>                                                          |
| <span data-ttu-id="a0180-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-213">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-214">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-215">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-216">Search-Flags</span></span>           | <span data-ttu-id="a0180-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-217">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-218">System-Flags</span></span>           | <span data-ttu-id="a0180-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-219">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-220">Classes used in</span></span>        | [<span data-ttu-id="a0180-221">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-221">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0180-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0180-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0180-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-223">Entry</span></span> | <span data-ttu-id="a0180-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-224">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-225">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-226">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-227">System-Only</span></span>            | <span data-ttu-id="a0180-228">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-228">False</span></span>                                                          |
| <span data-ttu-id="a0180-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-230">True</span></span>                                                           |
| <span data-ttu-id="a0180-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-231">Is Indexed</span></span>             | <span data-ttu-id="a0180-232">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-232">False</span></span>                                                          |
| <span data-ttu-id="a0180-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-233">In Global Catalog</span></span>      | <span data-ttu-id="a0180-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-234">False</span></span>                                                          |
| <span data-ttu-id="a0180-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-236">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-237">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-238">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-239">Search-Flags</span></span>           | <span data-ttu-id="a0180-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-240">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-241">System-Flags</span></span>           | <span data-ttu-id="a0180-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-242">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-243">Classes used in</span></span>        | [<span data-ttu-id="a0180-244">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-244">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0180-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0180-245">Windows Server 2012</span></span>



| <span data-ttu-id="a0180-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="a0180-246">Entry</span></span> | <span data-ttu-id="a0180-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0180-247">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0180-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a0180-248">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0180-249">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="a0180-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0180-250">System-Only</span></span>            | <span data-ttu-id="a0180-251">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-251">False</span></span>                                                          |
| <span data-ttu-id="a0180-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a0180-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a0180-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="a0180-253">True</span></span>                                                           |
| <span data-ttu-id="a0180-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a0180-254">Is Indexed</span></span>             | <span data-ttu-id="a0180-255">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-255">False</span></span>                                                          |
| <span data-ttu-id="a0180-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a0180-256">In Global Catalog</span></span>      | <span data-ttu-id="a0180-257">Faux</span><span class="sxs-lookup"><span data-stu-id="a0180-257">False</span></span>                                                          |
| <span data-ttu-id="a0180-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a0180-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0180-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a0180-259">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="a0180-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0180-260">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0180-261">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="a0180-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-262">Search-Flags</span></span>           | <span data-ttu-id="a0180-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0180-263">0x00000000</span></span>                                                     |
| <span data-ttu-id="a0180-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0180-264">System-Flags</span></span>           | <span data-ttu-id="a0180-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0180-265">0x00000010</span></span>                                                     |
| <span data-ttu-id="a0180-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a0180-266">Classes used in</span></span>        | [<span data-ttu-id="a0180-267">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="a0180-267">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





