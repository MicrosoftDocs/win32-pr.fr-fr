---
title: RID-available-attribut de pool
description: Espace à partir duquel les pools RID sont alloués.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID-available-Schema AD, attribut de pool
- Schéma AD de l’attribut rIDAvailablePool
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104200621"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="d38e1-105">RID-available-attribut de pool</span><span class="sxs-lookup"><span data-stu-id="d38e1-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="d38e1-106">Espace à partir duquel les pools RID sont alloués.</span><span class="sxs-lookup"><span data-stu-id="d38e1-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="d38e1-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-107">Entry</span></span> | <span data-ttu-id="d38e1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d38e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="d38e1-109">CN</span></span>                | <span data-ttu-id="d38e1-110">RID-available-pool</span><span class="sxs-lookup"><span data-stu-id="d38e1-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="d38e1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d38e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d38e1-112">rIDAvailablePool</span><span class="sxs-lookup"><span data-stu-id="d38e1-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="d38e1-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d38e1-113">Size</span></span>              | <span data-ttu-id="d38e1-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="d38e1-114">8 bytes</span></span>                              |
| <span data-ttu-id="d38e1-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d38e1-115">Update Privilege</span></span>  | <span data-ttu-id="d38e1-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="d38e1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d38e1-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d38e1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d38e1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-118">Attribute-Id</span></span>      | <span data-ttu-id="d38e1-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="d38e1-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="d38e1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d38e1-120">System-Id-Guid</span></span>    | <span data-ttu-id="d38e1-121">66171888-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="d38e1-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="d38e1-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d38e1-122">Syntax</span></span>            | [<span data-ttu-id="d38e1-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="d38e1-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d38e1-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d38e1-124">Implementations</span></span>

-   [<span data-ttu-id="d38e1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d38e1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d38e1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d38e1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d38e1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d38e1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d38e1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d38e1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d38e1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d38e1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d38e1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d38e1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d38e1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d38e1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d38e1-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-132">Entry</span></span> | <span data-ttu-id="d38e1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-136">System-Only</span></span>            | <span data-ttu-id="d38e1-137">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-137">False</span></span>                                          |
| <span data-ttu-id="d38e1-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-139">True</span></span>                                           |
| <span data-ttu-id="d38e1-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-140">Is Indexed</span></span>             | <span data-ttu-id="d38e1-141">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-141">False</span></span>                                          |
| <span data-ttu-id="d38e1-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-142">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-143">False</span></span>                                          |
| <span data-ttu-id="d38e1-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-148">Search-Flags</span></span>           | <span data-ttu-id="d38e1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-149">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-150">System-Flags</span></span>           | <span data-ttu-id="d38e1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-151">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-152">Classes used in</span></span>        | [<span data-ttu-id="d38e1-153">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d38e1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d38e1-154">Windows Server 2003</span></span>



| <span data-ttu-id="d38e1-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-155">Entry</span></span> | <span data-ttu-id="d38e1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-159">System-Only</span></span>            | <span data-ttu-id="d38e1-160">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-160">False</span></span>                                          |
| <span data-ttu-id="d38e1-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-162">True</span></span>                                           |
| <span data-ttu-id="d38e1-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-163">Is Indexed</span></span>             | <span data-ttu-id="d38e1-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-164">False</span></span>                                          |
| <span data-ttu-id="d38e1-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-165">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-166">False</span></span>                                          |
| <span data-ttu-id="d38e1-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-171">Search-Flags</span></span>           | <span data-ttu-id="d38e1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-172">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-173">System-Flags</span></span>           | <span data-ttu-id="d38e1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-174">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-175">Classes used in</span></span>        | [<span data-ttu-id="d38e1-176">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d38e1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d38e1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d38e1-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-178">Entry</span></span> | <span data-ttu-id="d38e1-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-182">System-Only</span></span>            | <span data-ttu-id="d38e1-183">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-183">False</span></span>                                          |
| <span data-ttu-id="d38e1-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-185">True</span></span>                                           |
| <span data-ttu-id="d38e1-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-186">Is Indexed</span></span>             | <span data-ttu-id="d38e1-187">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-187">False</span></span>                                          |
| <span data-ttu-id="d38e1-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-188">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-189">False</span></span>                                          |
| <span data-ttu-id="d38e1-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-194">Search-Flags</span></span>           | <span data-ttu-id="d38e1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-195">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-196">System-Flags</span></span>           | <span data-ttu-id="d38e1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-197">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-198">Classes used in</span></span>        | [<span data-ttu-id="d38e1-199">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d38e1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d38e1-200">Windows Server 2008</span></span>



| <span data-ttu-id="d38e1-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-201">Entry</span></span> | <span data-ttu-id="d38e1-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-205">System-Only</span></span>            | <span data-ttu-id="d38e1-206">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-206">False</span></span>                                          |
| <span data-ttu-id="d38e1-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-208">True</span></span>                                           |
| <span data-ttu-id="d38e1-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-209">Is Indexed</span></span>             | <span data-ttu-id="d38e1-210">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-210">False</span></span>                                          |
| <span data-ttu-id="d38e1-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-211">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-212">False</span></span>                                          |
| <span data-ttu-id="d38e1-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-217">Search-Flags</span></span>           | <span data-ttu-id="d38e1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-218">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-219">System-Flags</span></span>           | <span data-ttu-id="d38e1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-220">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-221">Classes used in</span></span>        | [<span data-ttu-id="d38e1-222">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d38e1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d38e1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d38e1-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-224">Entry</span></span> | <span data-ttu-id="d38e1-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-228">System-Only</span></span>            | <span data-ttu-id="d38e1-229">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-229">False</span></span>                                          |
| <span data-ttu-id="d38e1-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-231">True</span></span>                                           |
| <span data-ttu-id="d38e1-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-232">Is Indexed</span></span>             | <span data-ttu-id="d38e1-233">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-233">False</span></span>                                          |
| <span data-ttu-id="d38e1-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-234">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-235">False</span></span>                                          |
| <span data-ttu-id="d38e1-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-240">Search-Flags</span></span>           | <span data-ttu-id="d38e1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-241">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-242">System-Flags</span></span>           | <span data-ttu-id="d38e1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-243">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-244">Classes used in</span></span>        | [<span data-ttu-id="d38e1-245">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d38e1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d38e1-246">Windows Server 2012</span></span>



| <span data-ttu-id="d38e1-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="d38e1-247">Entry</span></span> | <span data-ttu-id="d38e1-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38e1-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d38e1-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d38e1-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d38e1-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d38e1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d38e1-251">System-Only</span></span>            | <span data-ttu-id="d38e1-252">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-252">False</span></span>                                          |
| <span data-ttu-id="d38e1-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d38e1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d38e1-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="d38e1-254">True</span></span>                                           |
| <span data-ttu-id="d38e1-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d38e1-255">Is Indexed</span></span>             | <span data-ttu-id="d38e1-256">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-256">False</span></span>                                          |
| <span data-ttu-id="d38e1-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d38e1-257">In Global Catalog</span></span>      | <span data-ttu-id="d38e1-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d38e1-258">False</span></span>                                          |
| <span data-ttu-id="d38e1-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d38e1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d38e1-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d38e1-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d38e1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d38e1-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d38e1-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d38e1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-263">Search-Flags</span></span>           | <span data-ttu-id="d38e1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d38e1-264">0x00000000</span></span>                                     |
| <span data-ttu-id="d38e1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d38e1-265">System-Flags</span></span>           | <span data-ttu-id="d38e1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d38e1-266">0x00000010</span></span>                                     |
| <span data-ttu-id="d38e1-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d38e1-267">Classes used in</span></span>        | [<span data-ttu-id="d38e1-268">**Gestionnaire RID**</span><span class="sxs-lookup"><span data-stu-id="d38e1-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 





