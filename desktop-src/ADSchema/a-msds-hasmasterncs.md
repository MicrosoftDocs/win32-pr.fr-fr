---
title: attribut ms-DS-a-Master-NC
description: Contient les contextes d’attribution de noms détenus par un contrôleur de domaine. Cet attribut déconseillé a-Master-NC.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-a-Master-NC
- Schéma Active Directory de l’attribut msDS-hasMasterNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845490"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="17152-106">attribut ms-DS-a-Master-NC</span><span class="sxs-lookup"><span data-stu-id="17152-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="17152-107">Contient les contextes d’attribution de noms détenus par un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="17152-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="17152-108">Cet attribut déconseillé a-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="17152-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="17152-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-109">Entry</span></span> | <span data-ttu-id="17152-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="17152-111">CN</span><span class="sxs-lookup"><span data-stu-id="17152-111">CN</span></span>                | <span data-ttu-id="17152-112">ms-DS-a-Master-NC</span><span class="sxs-lookup"><span data-stu-id="17152-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="17152-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17152-113">Ldap-Display-Name</span></span> | <span data-ttu-id="17152-114">msDS-hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="17152-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="17152-115">Taille</span><span class="sxs-lookup"><span data-stu-id="17152-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="17152-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="17152-116">Update Privilege</span></span>  | <span data-ttu-id="17152-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="17152-117">This value is set by the system</span></span>         |
| <span data-ttu-id="17152-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="17152-118">Update Frequency</span></span>  | <span data-ttu-id="17152-119">À chaque fois qu’un nouveau contexte de nommage est créé.</span><span class="sxs-lookup"><span data-stu-id="17152-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="17152-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17152-120">Attribute-Id</span></span>      | <span data-ttu-id="17152-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="17152-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="17152-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17152-122">System-Id-Guid</span></span>    | <span data-ttu-id="17152-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="17152-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="17152-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17152-124">Syntax</span></span>            | [<span data-ttu-id="17152-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="17152-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="17152-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="17152-126">Implementations</span></span>

-   [<span data-ttu-id="17152-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17152-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17152-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="17152-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="17152-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17152-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17152-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17152-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17152-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17152-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17152-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17152-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="17152-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17152-133">Windows Server 2003</span></span>



| <span data-ttu-id="17152-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-134">Entry</span></span> | <span data-ttu-id="17152-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-136">Link-Id</span></span>                | <span data-ttu-id="17152-137">2036</span><span class="sxs-lookup"><span data-stu-id="17152-137">2036</span></span>                                     |
| <span data-ttu-id="17152-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-139">System-Only</span></span>            | <span data-ttu-id="17152-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-140">True</span></span>                                     |
| <span data-ttu-id="17152-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-141">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-142">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-142">False</span></span>                                    |
| <span data-ttu-id="17152-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-143">Is Indexed</span></span>             | <span data-ttu-id="17152-144">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-144">False</span></span>                                    |
| <span data-ttu-id="17152-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-145">In Global Catalog</span></span>      | <span data-ttu-id="17152-146">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-146">False</span></span>                                    |
| <span data-ttu-id="17152-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-151">Search-Flags</span></span>           | <span data-ttu-id="17152-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-152">0x00000000</span></span>                               |
| <span data-ttu-id="17152-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-153">System-Flags</span></span>           | <span data-ttu-id="17152-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-154">0x00000010</span></span>                               |
| <span data-ttu-id="17152-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-155">Classes used in</span></span>        | [<span data-ttu-id="17152-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="17152-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="17152-157">ADAM</span></span>



| <span data-ttu-id="17152-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-158">Entry</span></span> | <span data-ttu-id="17152-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-160">Link-Id</span></span>                | <span data-ttu-id="17152-161">2036</span><span class="sxs-lookup"><span data-stu-id="17152-161">2036</span></span>                                     |
| <span data-ttu-id="17152-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-163">System-Only</span></span>            | <span data-ttu-id="17152-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-164">True</span></span>                                     |
| <span data-ttu-id="17152-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-165">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-166">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-166">False</span></span>                                    |
| <span data-ttu-id="17152-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-167">Is Indexed</span></span>             | <span data-ttu-id="17152-168">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-168">False</span></span>                                    |
| <span data-ttu-id="17152-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-169">In Global Catalog</span></span>      | <span data-ttu-id="17152-170">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-170">False</span></span>                                    |
| <span data-ttu-id="17152-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-175">Search-Flags</span></span>           | <span data-ttu-id="17152-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-176">0x00000000</span></span>                               |
| <span data-ttu-id="17152-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-177">System-Flags</span></span>           | <span data-ttu-id="17152-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-178">0x00000010</span></span>                               |
| <span data-ttu-id="17152-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-179">Classes used in</span></span>        | [<span data-ttu-id="17152-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17152-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17152-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17152-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-182">Entry</span></span> | <span data-ttu-id="17152-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-184">Link-Id</span></span>                | <span data-ttu-id="17152-185">2036</span><span class="sxs-lookup"><span data-stu-id="17152-185">2036</span></span>                                     |
| <span data-ttu-id="17152-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-187">System-Only</span></span>            | <span data-ttu-id="17152-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-188">True</span></span>                                     |
| <span data-ttu-id="17152-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-189">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-190">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-190">False</span></span>                                    |
| <span data-ttu-id="17152-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-191">Is Indexed</span></span>             | <span data-ttu-id="17152-192">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-192">False</span></span>                                    |
| <span data-ttu-id="17152-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-193">In Global Catalog</span></span>      | <span data-ttu-id="17152-194">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-194">False</span></span>                                    |
| <span data-ttu-id="17152-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-199">Search-Flags</span></span>           | <span data-ttu-id="17152-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-200">0x00000000</span></span>                               |
| <span data-ttu-id="17152-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-201">System-Flags</span></span>           | <span data-ttu-id="17152-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-202">0x00000010</span></span>                               |
| <span data-ttu-id="17152-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-203">Classes used in</span></span>        | [<span data-ttu-id="17152-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17152-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17152-205">Windows Server 2008</span></span>



| <span data-ttu-id="17152-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-206">Entry</span></span> | <span data-ttu-id="17152-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-208">Link-Id</span></span>                | <span data-ttu-id="17152-209">2036</span><span class="sxs-lookup"><span data-stu-id="17152-209">2036</span></span>                                     |
| <span data-ttu-id="17152-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-211">System-Only</span></span>            | <span data-ttu-id="17152-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-212">True</span></span>                                     |
| <span data-ttu-id="17152-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-213">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-214">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-214">False</span></span>                                    |
| <span data-ttu-id="17152-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-215">Is Indexed</span></span>             | <span data-ttu-id="17152-216">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-216">False</span></span>                                    |
| <span data-ttu-id="17152-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-217">In Global Catalog</span></span>      | <span data-ttu-id="17152-218">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-218">False</span></span>                                    |
| <span data-ttu-id="17152-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-223">Search-Flags</span></span>           | <span data-ttu-id="17152-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-224">0x00000000</span></span>                               |
| <span data-ttu-id="17152-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-225">System-Flags</span></span>           | <span data-ttu-id="17152-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-226">0x00000010</span></span>                               |
| <span data-ttu-id="17152-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-227">Classes used in</span></span>        | [<span data-ttu-id="17152-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17152-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17152-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17152-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-230">Entry</span></span> | <span data-ttu-id="17152-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-232">Link-Id</span></span>                | <span data-ttu-id="17152-233">2036</span><span class="sxs-lookup"><span data-stu-id="17152-233">2036</span></span>                                     |
| <span data-ttu-id="17152-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-235">System-Only</span></span>            | <span data-ttu-id="17152-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-236">True</span></span>                                     |
| <span data-ttu-id="17152-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-237">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-238">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-238">False</span></span>                                    |
| <span data-ttu-id="17152-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-239">Is Indexed</span></span>             | <span data-ttu-id="17152-240">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-240">False</span></span>                                    |
| <span data-ttu-id="17152-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-241">In Global Catalog</span></span>      | <span data-ttu-id="17152-242">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-242">False</span></span>                                    |
| <span data-ttu-id="17152-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-247">Search-Flags</span></span>           | <span data-ttu-id="17152-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-248">0x00000000</span></span>                               |
| <span data-ttu-id="17152-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-249">System-Flags</span></span>           | <span data-ttu-id="17152-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-250">0x00000010</span></span>                               |
| <span data-ttu-id="17152-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-251">Classes used in</span></span>        | [<span data-ttu-id="17152-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17152-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17152-253">Windows Server 2012</span></span>



| <span data-ttu-id="17152-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="17152-254">Entry</span></span> | <span data-ttu-id="17152-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="17152-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="17152-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="17152-256">Link-Id</span></span>                | <span data-ttu-id="17152-257">2036</span><span class="sxs-lookup"><span data-stu-id="17152-257">2036</span></span>                                     |
| <span data-ttu-id="17152-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17152-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="17152-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="17152-259">System-Only</span></span>            | <span data-ttu-id="17152-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="17152-260">True</span></span>                                     |
| <span data-ttu-id="17152-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="17152-261">Is-Single-Valued</span></span>       | <span data-ttu-id="17152-262">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-262">False</span></span>                                    |
| <span data-ttu-id="17152-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="17152-263">Is Indexed</span></span>             | <span data-ttu-id="17152-264">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-264">False</span></span>                                    |
| <span data-ttu-id="17152-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="17152-265">In Global Catalog</span></span>      | <span data-ttu-id="17152-266">Faux</span><span class="sxs-lookup"><span data-stu-id="17152-266">False</span></span>                                    |
| <span data-ttu-id="17152-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="17152-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="17152-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="17152-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="17152-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17152-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="17152-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17152-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="17152-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-271">Search-Flags</span></span>           | <span data-ttu-id="17152-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17152-272">0x00000000</span></span>                               |
| <span data-ttu-id="17152-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17152-273">System-Flags</span></span>           | <span data-ttu-id="17152-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17152-274">0x00000010</span></span>                               |
| <span data-ttu-id="17152-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="17152-275">Classes used in</span></span>        | [<span data-ttu-id="17152-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="17152-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





