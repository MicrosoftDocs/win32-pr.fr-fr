---
title: MS-WMI-attribut de requête
description: Une seule requête WQL.
ms.assetid: 3fb594fc-d160-4807-a019-3dec56d2262b
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de requête MS-WMI
- msWMI-schéma Active Directory d’attribut de requête
topic_type:
- apiref
api_name:
- ms-WMI-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5bb5376cf957d46894c6fa2c59016564d28dfb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845390"
---
# <a name="ms-wmi-query-attribute"></a><span data-ttu-id="44474-105">MS-WMI-attribut de requête</span><span class="sxs-lookup"><span data-stu-id="44474-105">ms-WMI-Query attribute</span></span>

<span data-ttu-id="44474-106">Une seule requête WQL.</span><span class="sxs-lookup"><span data-stu-id="44474-106">A single WQL query.</span></span>



| <span data-ttu-id="44474-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-107">Entry</span></span> | <span data-ttu-id="44474-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="44474-109">CN</span><span class="sxs-lookup"><span data-stu-id="44474-109">CN</span></span>                | <span data-ttu-id="44474-110">MS-WMI-requête</span><span class="sxs-lookup"><span data-stu-id="44474-110">ms-WMI-Query</span></span>                                |
| <span data-ttu-id="44474-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="44474-111">Ldap-Display-Name</span></span> | <span data-ttu-id="44474-112">msWMI-requête</span><span class="sxs-lookup"><span data-stu-id="44474-112">msWMI-Query</span></span>                                 |
| <span data-ttu-id="44474-113">Taille</span><span class="sxs-lookup"><span data-stu-id="44474-113">Size</span></span>              | <span data-ttu-id="44474-114">Moins de 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="44474-114">Less than 250 characters.</span></span>                   |
| <span data-ttu-id="44474-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="44474-115">Update Privilege</span></span>  | <span data-ttu-id="44474-116">Administrateur stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="44474-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="44474-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="44474-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="44474-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="44474-118">Attribute-Id</span></span>      | <span data-ttu-id="44474-119">1.2.840.113556.1.4.1642</span><span class="sxs-lookup"><span data-stu-id="44474-119">1.2.840.113556.1.4.1642</span></span>                     |
| <span data-ttu-id="44474-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="44474-120">System-Id-Guid</span></span>    | <span data-ttu-id="44474-121">65fff93e-35e3-45a3-85ae-876c6718297f</span><span class="sxs-lookup"><span data-stu-id="44474-121">65fff93e-35e3-45a3-85ae-876c6718297f</span></span>        |
| <span data-ttu-id="44474-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44474-122">Syntax</span></span>            | [<span data-ttu-id="44474-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="44474-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="44474-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="44474-124">Implementations</span></span>

-   [<span data-ttu-id="44474-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="44474-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="44474-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="44474-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="44474-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="44474-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="44474-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="44474-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="44474-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="44474-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="44474-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44474-130">Windows Server 2003</span></span>



| <span data-ttu-id="44474-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-131">Entry</span></span> | <span data-ttu-id="44474-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="44474-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="44474-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44474-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="44474-135">System-Only</span></span>            | <span data-ttu-id="44474-136">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-136">False</span></span>                                          |
| <span data-ttu-id="44474-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="44474-137">Is-Single-Valued</span></span>       | <span data-ttu-id="44474-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="44474-138">True</span></span>                                           |
| <span data-ttu-id="44474-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="44474-139">Is Indexed</span></span>             | <span data-ttu-id="44474-140">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-140">False</span></span>                                          |
| <span data-ttu-id="44474-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44474-141">In Global Catalog</span></span>      | <span data-ttu-id="44474-142">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-142">False</span></span>                                          |
| <span data-ttu-id="44474-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="44474-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="44474-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="44474-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="44474-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44474-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="44474-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44474-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="44474-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-147">Search-Flags</span></span>           | <span data-ttu-id="44474-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44474-148">0x00000000</span></span>                                     |
| <span data-ttu-id="44474-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-149">System-Flags</span></span>           | <span data-ttu-id="44474-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44474-150">0x00000010</span></span>                                     |
| <span data-ttu-id="44474-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="44474-151">Classes used in</span></span>        | [<span data-ttu-id="44474-152">**MS-WMI-règle**</span><span class="sxs-lookup"><span data-stu-id="44474-152">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="44474-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44474-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="44474-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-154">Entry</span></span> | <span data-ttu-id="44474-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="44474-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="44474-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44474-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="44474-158">System-Only</span></span>            | <span data-ttu-id="44474-159">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-159">False</span></span>                                          |
| <span data-ttu-id="44474-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="44474-160">Is-Single-Valued</span></span>       | <span data-ttu-id="44474-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="44474-161">True</span></span>                                           |
| <span data-ttu-id="44474-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="44474-162">Is Indexed</span></span>             | <span data-ttu-id="44474-163">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-163">False</span></span>                                          |
| <span data-ttu-id="44474-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44474-164">In Global Catalog</span></span>      | <span data-ttu-id="44474-165">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-165">False</span></span>                                          |
| <span data-ttu-id="44474-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="44474-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="44474-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="44474-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="44474-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44474-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="44474-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44474-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="44474-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-170">Search-Flags</span></span>           | <span data-ttu-id="44474-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44474-171">0x00000000</span></span>                                     |
| <span data-ttu-id="44474-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-172">System-Flags</span></span>           | <span data-ttu-id="44474-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44474-173">0x00000010</span></span>                                     |
| <span data-ttu-id="44474-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="44474-174">Classes used in</span></span>        | [<span data-ttu-id="44474-175">**MS-WMI-règle**</span><span class="sxs-lookup"><span data-stu-id="44474-175">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="44474-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44474-176">Windows Server 2008</span></span>



| <span data-ttu-id="44474-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-177">Entry</span></span> | <span data-ttu-id="44474-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="44474-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="44474-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44474-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="44474-181">System-Only</span></span>            | <span data-ttu-id="44474-182">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-182">False</span></span>                                          |
| <span data-ttu-id="44474-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="44474-183">Is-Single-Valued</span></span>       | <span data-ttu-id="44474-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="44474-184">True</span></span>                                           |
| <span data-ttu-id="44474-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="44474-185">Is Indexed</span></span>             | <span data-ttu-id="44474-186">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-186">False</span></span>                                          |
| <span data-ttu-id="44474-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44474-187">In Global Catalog</span></span>      | <span data-ttu-id="44474-188">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-188">False</span></span>                                          |
| <span data-ttu-id="44474-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="44474-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="44474-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="44474-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="44474-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44474-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="44474-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44474-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="44474-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-193">Search-Flags</span></span>           | <span data-ttu-id="44474-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44474-194">0x00000000</span></span>                                     |
| <span data-ttu-id="44474-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-195">System-Flags</span></span>           | <span data-ttu-id="44474-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44474-196">0x00000010</span></span>                                     |
| <span data-ttu-id="44474-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="44474-197">Classes used in</span></span>        | [<span data-ttu-id="44474-198">**MS-WMI-règle**</span><span class="sxs-lookup"><span data-stu-id="44474-198">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="44474-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44474-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="44474-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-200">Entry</span></span> | <span data-ttu-id="44474-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="44474-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="44474-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44474-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="44474-204">System-Only</span></span>            | <span data-ttu-id="44474-205">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-205">False</span></span>                                          |
| <span data-ttu-id="44474-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="44474-206">Is-Single-Valued</span></span>       | <span data-ttu-id="44474-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="44474-207">True</span></span>                                           |
| <span data-ttu-id="44474-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="44474-208">Is Indexed</span></span>             | <span data-ttu-id="44474-209">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-209">False</span></span>                                          |
| <span data-ttu-id="44474-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44474-210">In Global Catalog</span></span>      | <span data-ttu-id="44474-211">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-211">False</span></span>                                          |
| <span data-ttu-id="44474-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="44474-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="44474-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="44474-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="44474-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44474-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="44474-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44474-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="44474-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-216">Search-Flags</span></span>           | <span data-ttu-id="44474-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44474-217">0x00000000</span></span>                                     |
| <span data-ttu-id="44474-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-218">System-Flags</span></span>           | <span data-ttu-id="44474-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44474-219">0x00000010</span></span>                                     |
| <span data-ttu-id="44474-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="44474-220">Classes used in</span></span>        | [<span data-ttu-id="44474-221">**MS-WMI-règle**</span><span class="sxs-lookup"><span data-stu-id="44474-221">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="44474-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44474-222">Windows Server 2012</span></span>



| <span data-ttu-id="44474-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="44474-223">Entry</span></span> | <span data-ttu-id="44474-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="44474-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="44474-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="44474-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44474-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="44474-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="44474-227">System-Only</span></span>            | <span data-ttu-id="44474-228">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-228">False</span></span>                                          |
| <span data-ttu-id="44474-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="44474-229">Is-Single-Valued</span></span>       | <span data-ttu-id="44474-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="44474-230">True</span></span>                                           |
| <span data-ttu-id="44474-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="44474-231">Is Indexed</span></span>             | <span data-ttu-id="44474-232">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-232">False</span></span>                                          |
| <span data-ttu-id="44474-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44474-233">In Global Catalog</span></span>      | <span data-ttu-id="44474-234">Faux</span><span class="sxs-lookup"><span data-stu-id="44474-234">False</span></span>                                          |
| <span data-ttu-id="44474-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="44474-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="44474-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="44474-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="44474-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44474-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="44474-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44474-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="44474-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-239">Search-Flags</span></span>           | <span data-ttu-id="44474-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44474-240">0x00000000</span></span>                                     |
| <span data-ttu-id="44474-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44474-241">System-Flags</span></span>           | <span data-ttu-id="44474-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44474-242">0x00000010</span></span>                                     |
| <span data-ttu-id="44474-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="44474-243">Classes used in</span></span>        | [<span data-ttu-id="44474-244">**MS-WMI-règle**</span><span class="sxs-lookup"><span data-stu-id="44474-244">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



 

 





