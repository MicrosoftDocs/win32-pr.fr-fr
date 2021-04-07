---
title: RID-Previous-allocation-attribut pool
description: Contient le pool d’identificateurs relatifs (RID) à partir duquel un contrôleur de domaine est alloué.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory RID-Previous-allocation-pool Attribute
- Schéma AD de l’attribut rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844938"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="8db4f-105">RID-Previous-allocation-attribut pool</span><span class="sxs-lookup"><span data-stu-id="8db4f-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="8db4f-106">L’attribut **RID-Previous-allocation-pool** contient le pool d’identificateurs relatifs (RID) à partir duquel un contrôleur de domaine est alloué.</span><span class="sxs-lookup"><span data-stu-id="8db4f-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="8db4f-107">Cet attribut est une valeur de huit octets qui contient une paire d’entiers de 4 octets qui représentent les valeurs de début et de fin du pool RID.</span><span class="sxs-lookup"><span data-stu-id="8db4f-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="8db4f-108">La valeur de départ est dans les quatre octets inférieurs et la valeur de fin se trouve dans les quatre octets supérieurs.</span><span class="sxs-lookup"><span data-stu-id="8db4f-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="8db4f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-109">Entry</span></span> | <span data-ttu-id="8db4f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8db4f-111">CN</span><span class="sxs-lookup"><span data-stu-id="8db4f-111">CN</span></span>                | <span data-ttu-id="8db4f-112">RID-précédent-allocation-pool</span><span class="sxs-lookup"><span data-stu-id="8db4f-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="8db4f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8db4f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8db4f-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="8db4f-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="8db4f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="8db4f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="8db4f-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8db4f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8db4f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8db4f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8db4f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-118">Attribute-Id</span></span>      | <span data-ttu-id="8db4f-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="8db4f-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="8db4f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8db4f-120">System-Id-Guid</span></span>    | <span data-ttu-id="8db4f-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="8db4f-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="8db4f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8db4f-122">Syntax</span></span>            | [<span data-ttu-id="8db4f-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="8db4f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8db4f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8db4f-124">Implementations</span></span>

-   [<span data-ttu-id="8db4f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8db4f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8db4f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8db4f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8db4f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8db4f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8db4f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8db4f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8db4f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8db4f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8db4f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8db4f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8db4f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8db4f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8db4f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-132">Entry</span></span> | <span data-ttu-id="8db4f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-136">System-Only</span></span>            | <span data-ttu-id="8db4f-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-137">True</span></span>                                   |
| <span data-ttu-id="8db4f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-139">True</span></span>                                   |
| <span data-ttu-id="8db4f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-140">Is Indexed</span></span>             | <span data-ttu-id="8db4f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-141">False</span></span>                                  |
| <span data-ttu-id="8db4f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-142">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-143">False</span></span>                                  |
| <span data-ttu-id="8db4f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-148">Search-Flags</span></span>           | <span data-ttu-id="8db4f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-149">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-150">System-Flags</span></span>           | <span data-ttu-id="8db4f-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-151">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-152">Classes used in</span></span>        | [<span data-ttu-id="8db4f-153">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8db4f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8db4f-154">Windows Server 2003</span></span>



| <span data-ttu-id="8db4f-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-155">Entry</span></span> | <span data-ttu-id="8db4f-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-159">System-Only</span></span>            | <span data-ttu-id="8db4f-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-160">True</span></span>                                   |
| <span data-ttu-id="8db4f-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-162">True</span></span>                                   |
| <span data-ttu-id="8db4f-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-163">Is Indexed</span></span>             | <span data-ttu-id="8db4f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-164">False</span></span>                                  |
| <span data-ttu-id="8db4f-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-165">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-166">False</span></span>                                  |
| <span data-ttu-id="8db4f-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-171">Search-Flags</span></span>           | <span data-ttu-id="8db4f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-172">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-173">System-Flags</span></span>           | <span data-ttu-id="8db4f-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-174">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-175">Classes used in</span></span>        | [<span data-ttu-id="8db4f-176">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8db4f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8db4f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8db4f-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-178">Entry</span></span> | <span data-ttu-id="8db4f-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-182">System-Only</span></span>            | <span data-ttu-id="8db4f-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-183">True</span></span>                                   |
| <span data-ttu-id="8db4f-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-185">True</span></span>                                   |
| <span data-ttu-id="8db4f-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-186">Is Indexed</span></span>             | <span data-ttu-id="8db4f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-187">False</span></span>                                  |
| <span data-ttu-id="8db4f-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-188">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-189">False</span></span>                                  |
| <span data-ttu-id="8db4f-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-194">Search-Flags</span></span>           | <span data-ttu-id="8db4f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-195">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-196">System-Flags</span></span>           | <span data-ttu-id="8db4f-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-197">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-198">Classes used in</span></span>        | [<span data-ttu-id="8db4f-199">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8db4f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8db4f-200">Windows Server 2008</span></span>



| <span data-ttu-id="8db4f-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-201">Entry</span></span> | <span data-ttu-id="8db4f-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-205">System-Only</span></span>            | <span data-ttu-id="8db4f-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-206">True</span></span>                                   |
| <span data-ttu-id="8db4f-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-208">True</span></span>                                   |
| <span data-ttu-id="8db4f-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-209">Is Indexed</span></span>             | <span data-ttu-id="8db4f-210">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-210">False</span></span>                                  |
| <span data-ttu-id="8db4f-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-211">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-212">False</span></span>                                  |
| <span data-ttu-id="8db4f-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-217">Search-Flags</span></span>           | <span data-ttu-id="8db4f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-218">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-219">System-Flags</span></span>           | <span data-ttu-id="8db4f-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-220">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-221">Classes used in</span></span>        | [<span data-ttu-id="8db4f-222">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8db4f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8db4f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8db4f-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-224">Entry</span></span> | <span data-ttu-id="8db4f-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-228">System-Only</span></span>            | <span data-ttu-id="8db4f-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-229">True</span></span>                                   |
| <span data-ttu-id="8db4f-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-231">True</span></span>                                   |
| <span data-ttu-id="8db4f-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-232">Is Indexed</span></span>             | <span data-ttu-id="8db4f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-233">False</span></span>                                  |
| <span data-ttu-id="8db4f-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-234">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-235">False</span></span>                                  |
| <span data-ttu-id="8db4f-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-240">Search-Flags</span></span>           | <span data-ttu-id="8db4f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-241">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-242">System-Flags</span></span>           | <span data-ttu-id="8db4f-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-243">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-244">Classes used in</span></span>        | [<span data-ttu-id="8db4f-245">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8db4f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8db4f-246">Windows Server 2012</span></span>



| <span data-ttu-id="8db4f-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="8db4f-247">Entry</span></span> | <span data-ttu-id="8db4f-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db4f-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="8db4f-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8db4f-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8db4f-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="8db4f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8db4f-251">System-Only</span></span>            | <span data-ttu-id="8db4f-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-252">True</span></span>                                   |
| <span data-ttu-id="8db4f-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8db4f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8db4f-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="8db4f-254">True</span></span>                                   |
| <span data-ttu-id="8db4f-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8db4f-255">Is Indexed</span></span>             | <span data-ttu-id="8db4f-256">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-256">False</span></span>                                  |
| <span data-ttu-id="8db4f-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8db4f-257">In Global Catalog</span></span>      | <span data-ttu-id="8db4f-258">Faux</span><span class="sxs-lookup"><span data-stu-id="8db4f-258">False</span></span>                                  |
| <span data-ttu-id="8db4f-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8db4f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8db4f-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8db4f-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="8db4f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8db4f-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8db4f-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="8db4f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-263">Search-Flags</span></span>           | <span data-ttu-id="8db4f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8db4f-264">0x00000000</span></span>                             |
| <span data-ttu-id="8db4f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8db4f-265">System-Flags</span></span>           | <span data-ttu-id="8db4f-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8db4f-266">0x00000011</span></span>                             |
| <span data-ttu-id="8db4f-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8db4f-267">Classes used in</span></span>        | [<span data-ttu-id="8db4f-268">**RID-définir**</span><span class="sxs-lookup"><span data-stu-id="8db4f-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





