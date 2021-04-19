---
title: Attribut Search-Flags
description: Contient un ensemble d’indicateurs qui spécifient des informations de recherche et d’indexation pour un attribut.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Search-Flags
- Schéma AD de l’attribut searchFlags
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106530819"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="684eb-105">Attribut Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-105">Search-Flags attribute</span></span>

<span data-ttu-id="684eb-106">Contient un ensemble d’indicateurs qui spécifient des informations de recherche et d’indexation pour un attribut.</span><span class="sxs-lookup"><span data-stu-id="684eb-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="684eb-107">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="684eb-107">See Remarks.</span></span>



| <span data-ttu-id="684eb-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-108">Entry</span></span> | <span data-ttu-id="684eb-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="684eb-110">CN</span><span class="sxs-lookup"><span data-stu-id="684eb-110">CN</span></span>                | <span data-ttu-id="684eb-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-111">Search-Flags</span></span>                         |
| <span data-ttu-id="684eb-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="684eb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="684eb-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="684eb-113">searchFlags</span></span>                          |
| <span data-ttu-id="684eb-114">Taille</span><span class="sxs-lookup"><span data-stu-id="684eb-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="684eb-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="684eb-115">Update Privilege</span></span>  | <span data-ttu-id="684eb-116">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="684eb-116">Schema administrator</span></span>                 |
| <span data-ttu-id="684eb-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="684eb-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="684eb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-118">Attribute-Id</span></span>      | <span data-ttu-id="684eb-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="684eb-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="684eb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="684eb-120">System-Id-Guid</span></span>    | <span data-ttu-id="684eb-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="684eb-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="684eb-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="684eb-122">Syntax</span></span>            | [<span data-ttu-id="684eb-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="684eb-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="684eb-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="684eb-124">Implementations</span></span>

-   [<span data-ttu-id="684eb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="684eb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="684eb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="684eb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="684eb-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="684eb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="684eb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="684eb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="684eb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="684eb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="684eb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="684eb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="684eb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="684eb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="684eb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="684eb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="684eb-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-133">Entry</span></span> | <span data-ttu-id="684eb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-136">MAPI-Id</span></span>                | <span data-ttu-id="684eb-137">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-137">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-138">System-Only</span></span>            | <span data-ttu-id="684eb-139">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-139">False</span></span>                                                    |
| <span data-ttu-id="684eb-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-140">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-141">True</span></span>                                                     |
| <span data-ttu-id="684eb-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-142">Is Indexed</span></span>             | <span data-ttu-id="684eb-143">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-143">False</span></span>                                                    |
| <span data-ttu-id="684eb-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-144">In Global Catalog</span></span>      | <span data-ttu-id="684eb-145">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-145">False</span></span>                                                    |
| <span data-ttu-id="684eb-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-150">Search-Flags</span></span>           | <span data-ttu-id="684eb-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-151">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-152">System-Flags</span></span>           | <span data-ttu-id="684eb-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-153">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-154">Classes used in</span></span>        | [<span data-ttu-id="684eb-155">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="684eb-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="684eb-156">Windows Server 2003</span></span>



| <span data-ttu-id="684eb-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-157">Entry</span></span> | <span data-ttu-id="684eb-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-160">MAPI-Id</span></span>                | <span data-ttu-id="684eb-161">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-161">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-162">System-Only</span></span>            | <span data-ttu-id="684eb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-163">False</span></span>                                                    |
| <span data-ttu-id="684eb-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-165">True</span></span>                                                     |
| <span data-ttu-id="684eb-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-166">Is Indexed</span></span>             | <span data-ttu-id="684eb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-167">False</span></span>                                                    |
| <span data-ttu-id="684eb-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-168">In Global Catalog</span></span>      | <span data-ttu-id="684eb-169">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-169">False</span></span>                                                    |
| <span data-ttu-id="684eb-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-174">Search-Flags</span></span>           | <span data-ttu-id="684eb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-175">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-176">System-Flags</span></span>           | <span data-ttu-id="684eb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-177">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-178">Classes used in</span></span>        | [<span data-ttu-id="684eb-179">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="684eb-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="684eb-180">ADAM</span></span>



| <span data-ttu-id="684eb-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-181">Entry</span></span> | <span data-ttu-id="684eb-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-184">MAPI-Id</span></span>                | <span data-ttu-id="684eb-185">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-185">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-186">System-Only</span></span>            | <span data-ttu-id="684eb-187">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-187">False</span></span>                                                    |
| <span data-ttu-id="684eb-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-189">True</span></span>                                                     |
| <span data-ttu-id="684eb-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-190">Is Indexed</span></span>             | <span data-ttu-id="684eb-191">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-191">False</span></span>                                                    |
| <span data-ttu-id="684eb-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-192">In Global Catalog</span></span>      | <span data-ttu-id="684eb-193">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-193">False</span></span>                                                    |
| <span data-ttu-id="684eb-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-198">Search-Flags</span></span>           | <span data-ttu-id="684eb-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-199">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-200">System-Flags</span></span>           | <span data-ttu-id="684eb-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-201">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-202">Classes used in</span></span>        | [<span data-ttu-id="684eb-203">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="684eb-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="684eb-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="684eb-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-205">Entry</span></span> | <span data-ttu-id="684eb-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-208">MAPI-Id</span></span>                | <span data-ttu-id="684eb-209">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-209">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-210">System-Only</span></span>            | <span data-ttu-id="684eb-211">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-211">False</span></span>                                                    |
| <span data-ttu-id="684eb-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-212">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-213">True</span></span>                                                     |
| <span data-ttu-id="684eb-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-214">Is Indexed</span></span>             | <span data-ttu-id="684eb-215">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-215">False</span></span>                                                    |
| <span data-ttu-id="684eb-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-216">In Global Catalog</span></span>      | <span data-ttu-id="684eb-217">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-217">False</span></span>                                                    |
| <span data-ttu-id="684eb-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-222">Search-Flags</span></span>           | <span data-ttu-id="684eb-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-223">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-224">System-Flags</span></span>           | <span data-ttu-id="684eb-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-225">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-226">Classes used in</span></span>        | [<span data-ttu-id="684eb-227">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="684eb-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="684eb-228">Windows Server 2008</span></span>



| <span data-ttu-id="684eb-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-229">Entry</span></span> | <span data-ttu-id="684eb-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-232">MAPI-Id</span></span>                | <span data-ttu-id="684eb-233">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-233">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-234">System-Only</span></span>            | <span data-ttu-id="684eb-235">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-235">False</span></span>                                                    |
| <span data-ttu-id="684eb-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-236">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-237">True</span></span>                                                     |
| <span data-ttu-id="684eb-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-238">Is Indexed</span></span>             | <span data-ttu-id="684eb-239">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-239">False</span></span>                                                    |
| <span data-ttu-id="684eb-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-240">In Global Catalog</span></span>      | <span data-ttu-id="684eb-241">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-241">False</span></span>                                                    |
| <span data-ttu-id="684eb-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-246">Search-Flags</span></span>           | <span data-ttu-id="684eb-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-247">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-248">System-Flags</span></span>           | <span data-ttu-id="684eb-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-249">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-250">Classes used in</span></span>        | [<span data-ttu-id="684eb-251">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="684eb-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="684eb-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="684eb-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-253">Entry</span></span> | <span data-ttu-id="684eb-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-256">MAPI-Id</span></span>                | <span data-ttu-id="684eb-257">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-257">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-258">System-Only</span></span>            | <span data-ttu-id="684eb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-259">False</span></span>                                                    |
| <span data-ttu-id="684eb-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-260">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-261">True</span></span>                                                     |
| <span data-ttu-id="684eb-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-262">Is Indexed</span></span>             | <span data-ttu-id="684eb-263">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-263">False</span></span>                                                    |
| <span data-ttu-id="684eb-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-264">In Global Catalog</span></span>      | <span data-ttu-id="684eb-265">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-265">False</span></span>                                                    |
| <span data-ttu-id="684eb-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-270">Search-Flags</span></span>           | <span data-ttu-id="684eb-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-271">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-272">System-Flags</span></span>           | <span data-ttu-id="684eb-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-273">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-274">Classes used in</span></span>        | [<span data-ttu-id="684eb-275">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="684eb-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="684eb-276">Windows Server 2012</span></span>



| <span data-ttu-id="684eb-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="684eb-277">Entry</span></span> | <span data-ttu-id="684eb-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="684eb-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="684eb-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="684eb-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="684eb-280">MAPI-Id</span></span>                | <span data-ttu-id="684eb-281">0x812D</span><span class="sxs-lookup"><span data-stu-id="684eb-281">0x812D</span></span>                                                   |
| <span data-ttu-id="684eb-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="684eb-282">System-Only</span></span>            | <span data-ttu-id="684eb-283">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-283">False</span></span>                                                    |
| <span data-ttu-id="684eb-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="684eb-284">Is-Single-Valued</span></span>       | <span data-ttu-id="684eb-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="684eb-285">True</span></span>                                                     |
| <span data-ttu-id="684eb-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="684eb-286">Is Indexed</span></span>             | <span data-ttu-id="684eb-287">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-287">False</span></span>                                                    |
| <span data-ttu-id="684eb-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="684eb-288">In Global Catalog</span></span>      | <span data-ttu-id="684eb-289">Faux</span><span class="sxs-lookup"><span data-stu-id="684eb-289">False</span></span>                                                    |
| <span data-ttu-id="684eb-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="684eb-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="684eb-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="684eb-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="684eb-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="684eb-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="684eb-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="684eb-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-294">Search-Flags</span></span>           | <span data-ttu-id="684eb-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="684eb-295">0x00000000</span></span>                                               |
| <span data-ttu-id="684eb-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="684eb-296">System-Flags</span></span>           | <span data-ttu-id="684eb-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="684eb-297">0x00000010</span></span>                                               |
| <span data-ttu-id="684eb-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="684eb-298">Classes used in</span></span>        | [<span data-ttu-id="684eb-299">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="684eb-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="684eb-300">Notes</span><span class="sxs-lookup"><span data-stu-id="684eb-300">Remarks</span></span>

<span data-ttu-id="684eb-301">Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="684eb-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="684eb-302">Valeur</span><span class="sxs-lookup"><span data-stu-id="684eb-302">Value</span></span>            | <span data-ttu-id="684eb-303">Description</span><span class="sxs-lookup"><span data-stu-id="684eb-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="684eb-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="684eb-304">1 (0x00000001)</span></span>   | <span data-ttu-id="684eb-305">Créez un index pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="684eb-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="684eb-306">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="684eb-306">2 (0x00000002)</span></span>   | <span data-ttu-id="684eb-307">Créez un index pour l’attribut dans chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="684eb-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="684eb-308">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="684eb-308">4 (0x00000004)</span></span>   | <span data-ttu-id="684eb-309">Ajoutez cet attribut à l’ensemble de résolution de noms ambigus (ANR).</span><span class="sxs-lookup"><span data-stu-id="684eb-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="684eb-310">Cela permet de rechercher un objet lorsque seules des informations partielles sont fournies.</span><span class="sxs-lookup"><span data-stu-id="684eb-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="684eb-311">Par exemple, si le filtre LDAP est (ANR = JEFF), la recherche trouvera chaque objet dont le prénom, le nom, l’adresse de messagerie ou un autre attribut ANR est égal à JEFF.</span><span class="sxs-lookup"><span data-stu-id="684eb-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="684eb-312">Le bit 0 doit être défini pour que cet index prenne effet.</span><span class="sxs-lookup"><span data-stu-id="684eb-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="684eb-313">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="684eb-313">8 (0x00000008)</span></span>   | <span data-ttu-id="684eb-314">Conservez cet attribut dans l’objet tombstone pour les objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="684eb-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="684eb-315">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="684eb-315">16 (0x00000010)</span></span>  | <span data-ttu-id="684eb-316">Copiez la valeur de cet attribut lorsque l’objet est copié.</span><span class="sxs-lookup"><span data-stu-id="684eb-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="684eb-317">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="684eb-317">32 (0x00000020)</span></span>  | <span data-ttu-id="684eb-318">Créez un index de tuple pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="684eb-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="684eb-319">Cela permet d’améliorer les recherches où le caractère générique apparaît au début de la chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="684eb-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="684eb-320">Par exemple, (SN = \* mith).</span><span class="sxs-lookup"><span data-stu-id="684eb-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="684eb-321">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="684eb-321">64(0x00000040)</span></span>   | <span data-ttu-id="684eb-322">Prise en charge à partir d’ADAM.</span><span class="sxs-lookup"><span data-stu-id="684eb-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="684eb-323">Crée un index pour aider de manière considérable les performances VLV sur les attributs arbitraires.</span><span class="sxs-lookup"><span data-stu-id="684eb-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="684eb-324">128 (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="684eb-324">128 (0x00000080)</span></span> | <span data-ttu-id="684eb-325">Marquez l’attribut comme confidentiel.</span><span class="sxs-lookup"><span data-stu-id="684eb-325">Mark attribute as confidential.</span></span> <span data-ttu-id="684eb-326">Ignoré pour les attributs de schéma de base (systemFlags = 0x10).</span><span class="sxs-lookup"><span data-stu-id="684eb-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="684eb-327">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="684eb-327">64 (0x00000040)</span></span>  | <span data-ttu-id="684eb-328">Prise en charge à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="684eb-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="684eb-329">Créez un index pour améliorer les performances de recherche VLV sur cet attribut.</span><span class="sxs-lookup"><span data-stu-id="684eb-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





