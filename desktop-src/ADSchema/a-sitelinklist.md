---
title: Attribut site-lien-liste
description: Liste des liens de sites associés à ce pont.
ms.assetid: 79ec0ae2-ceb3-4321-8b6d-ce5c3bda667a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut site-Link-List
- Schéma AD de l’attribut siteLinkList
topic_type:
- apiref
api_name:
- Site-Link-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e71284e4650a3cb146b1656c846483e33a6dd66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385423"
---
# <a name="site-link-list-attribute"></a><span data-ttu-id="ef918-105">Attribut site-lien-liste</span><span class="sxs-lookup"><span data-stu-id="ef918-105">Site-Link-List attribute</span></span>

<span data-ttu-id="ef918-106">Liste des liens de sites associés à ce pont.</span><span class="sxs-lookup"><span data-stu-id="ef918-106">List of site links that are associated with this bridge.</span></span>



| <span data-ttu-id="ef918-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-107">Entry</span></span> | <span data-ttu-id="ef918-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-108">Value</span></span> |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="ef918-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef918-109">CN</span></span>                | <span data-ttu-id="ef918-110">Site-lien-liste</span><span class="sxs-lookup"><span data-stu-id="ef918-110">Site-Link-List</span></span>                                               |
| <span data-ttu-id="ef918-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ef918-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef918-112">siteLinkList</span><span class="sxs-lookup"><span data-stu-id="ef918-112">siteLinkList</span></span>                                                 |
| <span data-ttu-id="ef918-113">Taille</span><span class="sxs-lookup"><span data-stu-id="ef918-113">Size</span></span>              | \-                                                           |
| <span data-ttu-id="ef918-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ef918-114">Update Privilege</span></span>  | <span data-ttu-id="ef918-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="ef918-115">Domain administrator</span></span>                                         |
| <span data-ttu-id="ef918-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ef918-116">Update Frequency</span></span>  | <span data-ttu-id="ef918-117">Chaque fois qu’un lien de site est ajouté ou supprimé du pont.</span><span class="sxs-lookup"><span data-stu-id="ef918-117">Whenever a site link is added to or removed from the bridge.</span></span> |
| <span data-ttu-id="ef918-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-118">Attribute-Id</span></span>      | <span data-ttu-id="ef918-119">1.2.840.113556.1.4.822</span><span class="sxs-lookup"><span data-stu-id="ef918-119">1.2.840.113556.1.4.822</span></span>                                       |
| <span data-ttu-id="ef918-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ef918-120">System-Id-Guid</span></span>    | <span data-ttu-id="ef918-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ef918-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span></span>                         |
| <span data-ttu-id="ef918-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef918-122">Syntax</span></span>            | [<span data-ttu-id="ef918-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ef918-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                      |



## <a name="implementations"></a><span data-ttu-id="ef918-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ef918-124">Implementations</span></span>

-   [<span data-ttu-id="ef918-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef918-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef918-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef918-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef918-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ef918-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ef918-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef918-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef918-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef918-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef918-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef918-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef918-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef918-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef918-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef918-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ef918-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-133">Entry</span></span> | <span data-ttu-id="ef918-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-134">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-135">Link-Id</span></span>                | <span data-ttu-id="ef918-136">142</span><span class="sxs-lookup"><span data-stu-id="ef918-136">142</span></span>                                                     |
| <span data-ttu-id="ef918-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-137">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-138">System-Only</span></span>            | <span data-ttu-id="ef918-139">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-139">False</span></span>                                                   |
| <span data-ttu-id="ef918-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-141">False</span></span>                                                   |
| <span data-ttu-id="ef918-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-142">Is Indexed</span></span>             | <span data-ttu-id="ef918-143">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-143">False</span></span>                                                   |
| <span data-ttu-id="ef918-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-144">In Global Catalog</span></span>      | <span data-ttu-id="ef918-145">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-145">False</span></span>                                                   |
| <span data-ttu-id="ef918-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-147">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-148">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-149">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-150">Search-Flags</span></span>           | <span data-ttu-id="ef918-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-151">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-152">System-Flags</span></span>           | <span data-ttu-id="ef918-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-153">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-154">Classes used in</span></span>        | [<span data-ttu-id="ef918-155">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-155">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef918-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef918-156">Windows Server 2003</span></span>



| <span data-ttu-id="ef918-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-157">Entry</span></span> | <span data-ttu-id="ef918-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-158">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-159">Link-Id</span></span>                | <span data-ttu-id="ef918-160">142</span><span class="sxs-lookup"><span data-stu-id="ef918-160">142</span></span>                                                     |
| <span data-ttu-id="ef918-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-161">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-162">System-Only</span></span>            | <span data-ttu-id="ef918-163">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-163">False</span></span>                                                   |
| <span data-ttu-id="ef918-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-165">False</span></span>                                                   |
| <span data-ttu-id="ef918-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-166">Is Indexed</span></span>             | <span data-ttu-id="ef918-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-167">False</span></span>                                                   |
| <span data-ttu-id="ef918-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-168">In Global Catalog</span></span>      | <span data-ttu-id="ef918-169">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-169">False</span></span>                                                   |
| <span data-ttu-id="ef918-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-171">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-172">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-173">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-174">Search-Flags</span></span>           | <span data-ttu-id="ef918-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-175">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-176">System-Flags</span></span>           | <span data-ttu-id="ef918-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-177">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-178">Classes used in</span></span>        | [<span data-ttu-id="ef918-179">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-179">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ef918-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="ef918-180">ADAM</span></span>



| <span data-ttu-id="ef918-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-181">Entry</span></span> | <span data-ttu-id="ef918-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-182">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-183">Link-Id</span></span>                | <span data-ttu-id="ef918-184">142</span><span class="sxs-lookup"><span data-stu-id="ef918-184">142</span></span>                                                     |
| <span data-ttu-id="ef918-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-185">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-186">System-Only</span></span>            | <span data-ttu-id="ef918-187">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-187">False</span></span>                                                   |
| <span data-ttu-id="ef918-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-189">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-189">False</span></span>                                                   |
| <span data-ttu-id="ef918-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-190">Is Indexed</span></span>             | <span data-ttu-id="ef918-191">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-191">False</span></span>                                                   |
| <span data-ttu-id="ef918-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-192">In Global Catalog</span></span>      | <span data-ttu-id="ef918-193">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-193">False</span></span>                                                   |
| <span data-ttu-id="ef918-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-195">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-196">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-197">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-198">Search-Flags</span></span>           | <span data-ttu-id="ef918-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-199">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-200">System-Flags</span></span>           | <span data-ttu-id="ef918-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-201">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-202">Classes used in</span></span>        | [<span data-ttu-id="ef918-203">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-203">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef918-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef918-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef918-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-205">Entry</span></span> | <span data-ttu-id="ef918-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-206">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-207">Link-Id</span></span>                | <span data-ttu-id="ef918-208">142</span><span class="sxs-lookup"><span data-stu-id="ef918-208">142</span></span>                                                     |
| <span data-ttu-id="ef918-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-209">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-210">System-Only</span></span>            | <span data-ttu-id="ef918-211">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-211">False</span></span>                                                   |
| <span data-ttu-id="ef918-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-213">False</span></span>                                                   |
| <span data-ttu-id="ef918-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-214">Is Indexed</span></span>             | <span data-ttu-id="ef918-215">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-215">False</span></span>                                                   |
| <span data-ttu-id="ef918-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-216">In Global Catalog</span></span>      | <span data-ttu-id="ef918-217">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-217">False</span></span>                                                   |
| <span data-ttu-id="ef918-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-219">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-220">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-221">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-222">Search-Flags</span></span>           | <span data-ttu-id="ef918-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-223">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-224">System-Flags</span></span>           | <span data-ttu-id="ef918-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-225">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-226">Classes used in</span></span>        | [<span data-ttu-id="ef918-227">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-227">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef918-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef918-228">Windows Server 2008</span></span>



| <span data-ttu-id="ef918-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-229">Entry</span></span> | <span data-ttu-id="ef918-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-230">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-231">Link-Id</span></span>                | <span data-ttu-id="ef918-232">142</span><span class="sxs-lookup"><span data-stu-id="ef918-232">142</span></span>                                                     |
| <span data-ttu-id="ef918-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-233">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-234">System-Only</span></span>            | <span data-ttu-id="ef918-235">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-235">False</span></span>                                                   |
| <span data-ttu-id="ef918-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-236">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-237">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-237">False</span></span>                                                   |
| <span data-ttu-id="ef918-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-238">Is Indexed</span></span>             | <span data-ttu-id="ef918-239">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-239">False</span></span>                                                   |
| <span data-ttu-id="ef918-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-240">In Global Catalog</span></span>      | <span data-ttu-id="ef918-241">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-241">False</span></span>                                                   |
| <span data-ttu-id="ef918-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-243">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-244">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-245">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-246">Search-Flags</span></span>           | <span data-ttu-id="ef918-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-247">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-248">System-Flags</span></span>           | <span data-ttu-id="ef918-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-249">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-250">Classes used in</span></span>        | [<span data-ttu-id="ef918-251">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-251">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef918-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef918-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef918-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-253">Entry</span></span> | <span data-ttu-id="ef918-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-254">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-255">Link-Id</span></span>                | <span data-ttu-id="ef918-256">142</span><span class="sxs-lookup"><span data-stu-id="ef918-256">142</span></span>                                                     |
| <span data-ttu-id="ef918-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-257">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-258">System-Only</span></span>            | <span data-ttu-id="ef918-259">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-259">False</span></span>                                                   |
| <span data-ttu-id="ef918-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-260">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-261">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-261">False</span></span>                                                   |
| <span data-ttu-id="ef918-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-262">Is Indexed</span></span>             | <span data-ttu-id="ef918-263">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-263">False</span></span>                                                   |
| <span data-ttu-id="ef918-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-264">In Global Catalog</span></span>      | <span data-ttu-id="ef918-265">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-265">False</span></span>                                                   |
| <span data-ttu-id="ef918-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-267">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-268">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-269">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-270">Search-Flags</span></span>           | <span data-ttu-id="ef918-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-271">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-272">System-Flags</span></span>           | <span data-ttu-id="ef918-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-273">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-274">Classes used in</span></span>        | [<span data-ttu-id="ef918-275">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-275">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef918-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef918-276">Windows Server 2012</span></span>



| <span data-ttu-id="ef918-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef918-277">Entry</span></span> | <span data-ttu-id="ef918-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-278">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef918-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef918-279">Link-Id</span></span>                | <span data-ttu-id="ef918-280">142</span><span class="sxs-lookup"><span data-stu-id="ef918-280">142</span></span>                                                     |
| <span data-ttu-id="ef918-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef918-281">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="ef918-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef918-282">System-Only</span></span>            | <span data-ttu-id="ef918-283">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-283">False</span></span>                                                   |
| <span data-ttu-id="ef918-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef918-284">Is-Single-Valued</span></span>       | <span data-ttu-id="ef918-285">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-285">False</span></span>                                                   |
| <span data-ttu-id="ef918-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef918-286">Is Indexed</span></span>             | <span data-ttu-id="ef918-287">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-287">False</span></span>                                                   |
| <span data-ttu-id="ef918-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef918-288">In Global Catalog</span></span>      | <span data-ttu-id="ef918-289">Faux</span><span class="sxs-lookup"><span data-stu-id="ef918-289">False</span></span>                                                   |
| <span data-ttu-id="ef918-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef918-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef918-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef918-291">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="ef918-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef918-292">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef918-293">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="ef918-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-294">Search-Flags</span></span>           | <span data-ttu-id="ef918-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef918-295">0x00000000</span></span>                                              |
| <span data-ttu-id="ef918-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef918-296">System-Flags</span></span>           | <span data-ttu-id="ef918-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef918-297">0x00000010</span></span>                                              |
| <span data-ttu-id="ef918-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef918-298">Classes used in</span></span>        | [<span data-ttu-id="ef918-299">**Site-lien-pont**</span><span class="sxs-lookup"><span data-stu-id="ef918-299">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



 

 





