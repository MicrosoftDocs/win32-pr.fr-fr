---
title: RID-used-pool (attribut)
description: Pools RID qui ont été utilisés par un contrôleur de périphérique.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut RID-used-pool
- Schéma AD de l’attribut rIDUsedPool
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107572"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="fed5a-105">RID-used-pool (attribut)</span><span class="sxs-lookup"><span data-stu-id="fed5a-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="fed5a-106">Pools RID qui ont été utilisés par un contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="fed5a-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="fed5a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-107">Entry</span></span> | <span data-ttu-id="fed5a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fed5a-109">CN</span><span class="sxs-lookup"><span data-stu-id="fed5a-109">CN</span></span>                | <span data-ttu-id="fed5a-110">RID-used-pool</span><span class="sxs-lookup"><span data-stu-id="fed5a-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="fed5a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fed5a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fed5a-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="fed5a-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="fed5a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="fed5a-113">Size</span></span>              | <span data-ttu-id="fed5a-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="fed5a-114">8 bytes</span></span>                              |
| <span data-ttu-id="fed5a-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="fed5a-115">Update Privilege</span></span>  | <span data-ttu-id="fed5a-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="fed5a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="fed5a-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="fed5a-117">Update Frequency</span></span>  | <span data-ttu-id="fed5a-118">À chaque fois qu’un pool RID est vidé.</span><span class="sxs-lookup"><span data-stu-id="fed5a-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="fed5a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-119">Attribute-Id</span></span>      | <span data-ttu-id="fed5a-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="fed5a-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="fed5a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fed5a-121">System-Id-Guid</span></span>    | <span data-ttu-id="fed5a-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="fed5a-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="fed5a-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fed5a-123">Syntax</span></span>            | [<span data-ttu-id="fed5a-124">**Défini**</span><span class="sxs-lookup"><span data-stu-id="fed5a-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="fed5a-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="fed5a-125">Implementations</span></span>

-   [<span data-ttu-id="fed5a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fed5a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fed5a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fed5a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fed5a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fed5a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fed5a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fed5a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fed5a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fed5a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fed5a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fed5a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fed5a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fed5a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fed5a-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-133">Entry</span></span> | <span data-ttu-id="fed5a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-137">System-Only</span></span>            | <span data-ttu-id="fed5a-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-138">True</span></span>                                   |
| <span data-ttu-id="fed5a-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-140">True</span></span>                                   |
| <span data-ttu-id="fed5a-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-141">Is Indexed</span></span>             | <span data-ttu-id="fed5a-142">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-142">False</span></span>                                  |
| <span data-ttu-id="fed5a-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-143">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-144">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-144">False</span></span>                                  |
| <span data-ttu-id="fed5a-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-149">Search-Flags</span></span>           | <span data-ttu-id="fed5a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-150">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-151">System-Flags</span></span>           | <span data-ttu-id="fed5a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-152">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-153">Classes used in</span></span>        | [<span data-ttu-id="fed5a-154">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fed5a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed5a-155">Windows Server 2003</span></span>



| <span data-ttu-id="fed5a-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-156">Entry</span></span> | <span data-ttu-id="fed5a-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-160">System-Only</span></span>            | <span data-ttu-id="fed5a-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-161">True</span></span>                                   |
| <span data-ttu-id="fed5a-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-163">True</span></span>                                   |
| <span data-ttu-id="fed5a-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-164">Is Indexed</span></span>             | <span data-ttu-id="fed5a-165">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-165">False</span></span>                                  |
| <span data-ttu-id="fed5a-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-166">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-167">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-167">False</span></span>                                  |
| <span data-ttu-id="fed5a-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-172">Search-Flags</span></span>           | <span data-ttu-id="fed5a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-173">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-174">System-Flags</span></span>           | <span data-ttu-id="fed5a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-175">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-176">Classes used in</span></span>        | [<span data-ttu-id="fed5a-177">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fed5a-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fed5a-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fed5a-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-179">Entry</span></span> | <span data-ttu-id="fed5a-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-183">System-Only</span></span>            | <span data-ttu-id="fed5a-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-184">True</span></span>                                   |
| <span data-ttu-id="fed5a-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-186">True</span></span>                                   |
| <span data-ttu-id="fed5a-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-187">Is Indexed</span></span>             | <span data-ttu-id="fed5a-188">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-188">False</span></span>                                  |
| <span data-ttu-id="fed5a-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-189">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-190">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-190">False</span></span>                                  |
| <span data-ttu-id="fed5a-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-195">Search-Flags</span></span>           | <span data-ttu-id="fed5a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-196">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-197">System-Flags</span></span>           | <span data-ttu-id="fed5a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-198">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-199">Classes used in</span></span>        | [<span data-ttu-id="fed5a-200">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fed5a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fed5a-201">Windows Server 2008</span></span>



| <span data-ttu-id="fed5a-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-202">Entry</span></span> | <span data-ttu-id="fed5a-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-206">System-Only</span></span>            | <span data-ttu-id="fed5a-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-207">True</span></span>                                   |
| <span data-ttu-id="fed5a-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-209">True</span></span>                                   |
| <span data-ttu-id="fed5a-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-210">Is Indexed</span></span>             | <span data-ttu-id="fed5a-211">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-211">False</span></span>                                  |
| <span data-ttu-id="fed5a-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-212">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-213">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-213">False</span></span>                                  |
| <span data-ttu-id="fed5a-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-218">Search-Flags</span></span>           | <span data-ttu-id="fed5a-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-219">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-220">System-Flags</span></span>           | <span data-ttu-id="fed5a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-221">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-222">Classes used in</span></span>        | [<span data-ttu-id="fed5a-223">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fed5a-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fed5a-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fed5a-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-225">Entry</span></span> | <span data-ttu-id="fed5a-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-229">System-Only</span></span>            | <span data-ttu-id="fed5a-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-230">True</span></span>                                   |
| <span data-ttu-id="fed5a-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-232">True</span></span>                                   |
| <span data-ttu-id="fed5a-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-233">Is Indexed</span></span>             | <span data-ttu-id="fed5a-234">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-234">False</span></span>                                  |
| <span data-ttu-id="fed5a-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-235">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-236">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-236">False</span></span>                                  |
| <span data-ttu-id="fed5a-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-241">Search-Flags</span></span>           | <span data-ttu-id="fed5a-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-242">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-243">System-Flags</span></span>           | <span data-ttu-id="fed5a-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-244">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-245">Classes used in</span></span>        | [<span data-ttu-id="fed5a-246">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fed5a-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fed5a-247">Windows Server 2012</span></span>



| <span data-ttu-id="fed5a-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed5a-248">Entry</span></span> | <span data-ttu-id="fed5a-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed5a-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="fed5a-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fed5a-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fed5a-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="fed5a-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fed5a-252">System-Only</span></span>            | <span data-ttu-id="fed5a-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-253">True</span></span>                                   |
| <span data-ttu-id="fed5a-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fed5a-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fed5a-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed5a-255">True</span></span>                                   |
| <span data-ttu-id="fed5a-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fed5a-256">Is Indexed</span></span>             | <span data-ttu-id="fed5a-257">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-257">False</span></span>                                  |
| <span data-ttu-id="fed5a-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fed5a-258">In Global Catalog</span></span>      | <span data-ttu-id="fed5a-259">Faux</span><span class="sxs-lookup"><span data-stu-id="fed5a-259">False</span></span>                                  |
| <span data-ttu-id="fed5a-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fed5a-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fed5a-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fed5a-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="fed5a-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fed5a-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fed5a-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="fed5a-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-264">Search-Flags</span></span>           | <span data-ttu-id="fed5a-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fed5a-265">0x00000000</span></span>                             |
| <span data-ttu-id="fed5a-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fed5a-266">System-Flags</span></span>           | <span data-ttu-id="fed5a-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fed5a-267">0x00000010</span></span>                             |
| <span data-ttu-id="fed5a-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fed5a-268">Classes used in</span></span>        | [<span data-ttu-id="fed5a-269">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="fed5a-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





