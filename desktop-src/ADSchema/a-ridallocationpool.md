---
title: RID-allocation-attribut de pool
description: Un pool qui a été préalablement récupéré pour être utilisé par le gestionnaire RID lorsque le pool d’allocation RID précédent a été utilisé.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- RID-allocation-schéma Active Directory d’attribut de pool
- Schéma AD de l’attribut rIDAllocationPool
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515498"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="7cb1c-105">RID-allocation-attribut de pool</span><span class="sxs-lookup"><span data-stu-id="7cb1c-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="7cb1c-106">Un pool qui a été préalablement récupéré pour être utilisé par le gestionnaire RID lorsque le pool d’allocation RID précédent a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="7cb1c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-107">Entry</span></span> | <span data-ttu-id="7cb1c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7cb1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7cb1c-109">CN</span></span>                | <span data-ttu-id="7cb1c-110">RID-allocation-pool</span><span class="sxs-lookup"><span data-stu-id="7cb1c-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="7cb1c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7cb1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7cb1c-112">rIDAllocationPool</span><span class="sxs-lookup"><span data-stu-id="7cb1c-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="7cb1c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7cb1c-113">Size</span></span>              | <span data-ttu-id="7cb1c-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="7cb1c-114">8 bytes</span></span>                              |
| <span data-ttu-id="7cb1c-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7cb1c-115">Update Privilege</span></span>  | <span data-ttu-id="7cb1c-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7cb1c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7cb1c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7cb1c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-118">Attribute-Id</span></span>      | <span data-ttu-id="7cb1c-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="7cb1c-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="7cb1c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7cb1c-120">System-Id-Guid</span></span>    | <span data-ttu-id="7cb1c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7cb1c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="7cb1c-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb1c-122">Syntax</span></span>            | [<span data-ttu-id="7cb1c-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7cb1c-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7cb1c-124">Implementations</span></span>

-   [<span data-ttu-id="7cb1c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7cb1c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7cb1c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7cb1c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7cb1c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7cb1c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7cb1c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7cb1c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7cb1c-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-132">Entry</span></span> | <span data-ttu-id="7cb1c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-136">System-Only</span></span>            | <span data-ttu-id="7cb1c-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-137">True</span></span>                                   |
| <span data-ttu-id="7cb1c-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-139">True</span></span>                                   |
| <span data-ttu-id="7cb1c-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-140">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-141">False</span></span>                                  |
| <span data-ttu-id="7cb1c-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-142">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-143">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-143">False</span></span>                                  |
| <span data-ttu-id="7cb1c-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-148">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-149">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-150">System-Flags</span></span>           | <span data-ttu-id="7cb1c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-151">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-152">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-153">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7cb1c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7cb1c-154">Windows Server 2003</span></span>



| <span data-ttu-id="7cb1c-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-155">Entry</span></span> | <span data-ttu-id="7cb1c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-159">System-Only</span></span>            | <span data-ttu-id="7cb1c-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-160">True</span></span>                                   |
| <span data-ttu-id="7cb1c-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-162">True</span></span>                                   |
| <span data-ttu-id="7cb1c-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-163">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-164">False</span></span>                                  |
| <span data-ttu-id="7cb1c-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-165">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-166">False</span></span>                                  |
| <span data-ttu-id="7cb1c-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-171">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-172">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-173">System-Flags</span></span>           | <span data-ttu-id="7cb1c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-174">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-175">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-176">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7cb1c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7cb1c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7cb1c-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-178">Entry</span></span> | <span data-ttu-id="7cb1c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-182">System-Only</span></span>            | <span data-ttu-id="7cb1c-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-183">True</span></span>                                   |
| <span data-ttu-id="7cb1c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-185">True</span></span>                                   |
| <span data-ttu-id="7cb1c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-186">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-187">False</span></span>                                  |
| <span data-ttu-id="7cb1c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-188">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-189">False</span></span>                                  |
| <span data-ttu-id="7cb1c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-194">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-195">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-196">System-Flags</span></span>           | <span data-ttu-id="7cb1c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-197">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-198">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-199">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7cb1c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cb1c-200">Windows Server 2008</span></span>



| <span data-ttu-id="7cb1c-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-201">Entry</span></span> | <span data-ttu-id="7cb1c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-205">System-Only</span></span>            | <span data-ttu-id="7cb1c-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-206">True</span></span>                                   |
| <span data-ttu-id="7cb1c-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-208">True</span></span>                                   |
| <span data-ttu-id="7cb1c-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-209">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-210">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-210">False</span></span>                                  |
| <span data-ttu-id="7cb1c-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-211">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-212">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-212">False</span></span>                                  |
| <span data-ttu-id="7cb1c-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-217">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-218">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-219">System-Flags</span></span>           | <span data-ttu-id="7cb1c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-220">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-221">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-222">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7cb1c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cb1c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7cb1c-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-224">Entry</span></span> | <span data-ttu-id="7cb1c-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-228">System-Only</span></span>            | <span data-ttu-id="7cb1c-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-229">True</span></span>                                   |
| <span data-ttu-id="7cb1c-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-231">True</span></span>                                   |
| <span data-ttu-id="7cb1c-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-232">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-233">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-233">False</span></span>                                  |
| <span data-ttu-id="7cb1c-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-234">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-235">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-235">False</span></span>                                  |
| <span data-ttu-id="7cb1c-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-240">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-241">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-242">System-Flags</span></span>           | <span data-ttu-id="7cb1c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-243">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-244">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-245">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7cb1c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7cb1c-246">Windows Server 2012</span></span>



| <span data-ttu-id="7cb1c-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb1c-247">Entry</span></span> | <span data-ttu-id="7cb1c-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb1c-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="7cb1c-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb1c-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb1c-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="7cb1c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb1c-251">System-Only</span></span>            | <span data-ttu-id="7cb1c-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-252">True</span></span>                                   |
| <span data-ttu-id="7cb1c-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb1c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb1c-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb1c-254">True</span></span>                                   |
| <span data-ttu-id="7cb1c-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb1c-255">Is Indexed</span></span>             | <span data-ttu-id="7cb1c-256">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-256">False</span></span>                                  |
| <span data-ttu-id="7cb1c-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb1c-257">In Global Catalog</span></span>      | <span data-ttu-id="7cb1c-258">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb1c-258">False</span></span>                                  |
| <span data-ttu-id="7cb1c-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb1c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb1c-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb1c-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="7cb1c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb1c-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb1c-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="7cb1c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-263">Search-Flags</span></span>           | <span data-ttu-id="7cb1c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb1c-264">0x00000000</span></span>                             |
| <span data-ttu-id="7cb1c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb1c-265">System-Flags</span></span>           | <span data-ttu-id="7cb1c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb1c-266">0x00000010</span></span>                             |
| <span data-ttu-id="7cb1c-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb1c-267">Classes used in</span></span>        | [<span data-ttu-id="7cb1c-268">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





