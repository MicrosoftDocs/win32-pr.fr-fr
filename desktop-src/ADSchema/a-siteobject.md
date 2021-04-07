---
title: Attribut Site-Object
description: Nom unique du site auquel appartient ce sous-réseau.
ms.assetid: 4533c742-4276-48df-b0cd-7ba1641737a7
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Site-Object
- Schéma AD de l’attribut siteObject
topic_type:
- apiref
api_name:
- Site-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac43fb4ee0718aec855de4b7eb251a5d67c1a5fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845294"
---
# <a name="site-object-attribute"></a><span data-ttu-id="601d8-105">Attribut Site-Object</span><span class="sxs-lookup"><span data-stu-id="601d8-105">Site-Object attribute</span></span>

<span data-ttu-id="601d8-106">Nom unique du site auquel appartient ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="601d8-106">The distinguished name for the site to which this subnet belongs.</span></span>



| <span data-ttu-id="601d8-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-107">Entry</span></span> | <span data-ttu-id="601d8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="601d8-109">CN</span><span class="sxs-lookup"><span data-stu-id="601d8-109">CN</span></span>                | <span data-ttu-id="601d8-110">Site-Object</span><span class="sxs-lookup"><span data-stu-id="601d8-110">Site-Object</span></span>                             |
| <span data-ttu-id="601d8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="601d8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="601d8-112">siteObject</span><span class="sxs-lookup"><span data-stu-id="601d8-112">siteObject</span></span>                              |
| <span data-ttu-id="601d8-113">Taille</span><span class="sxs-lookup"><span data-stu-id="601d8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="601d8-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="601d8-114">Update Privilege</span></span>  | <span data-ttu-id="601d8-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="601d8-115">Domain administrator</span></span>                    |
| <span data-ttu-id="601d8-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="601d8-116">Update Frequency</span></span>  | <span data-ttu-id="601d8-117">Chaque fois qu’un site est créé.</span><span class="sxs-lookup"><span data-stu-id="601d8-117">Whenever a site is created.</span></span>             |
| <span data-ttu-id="601d8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-118">Attribute-Id</span></span>      | <span data-ttu-id="601d8-119">1.2.840.113556.1.4.512</span><span class="sxs-lookup"><span data-stu-id="601d8-119">1.2.840.113556.1.4.512</span></span>                  |
| <span data-ttu-id="601d8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="601d8-120">System-Id-Guid</span></span>    | <span data-ttu-id="601d8-121">3e10944c-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="601d8-121">3e10944c-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="601d8-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="601d8-122">Syntax</span></span>            | [<span data-ttu-id="601d8-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="601d8-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="601d8-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="601d8-124">Implementations</span></span>

-   [<span data-ttu-id="601d8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="601d8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="601d8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="601d8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="601d8-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="601d8-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="601d8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="601d8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="601d8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="601d8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="601d8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="601d8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="601d8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="601d8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="601d8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="601d8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="601d8-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-133">Entry</span></span> | <span data-ttu-id="601d8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-135">Link-Id</span></span>                | <span data-ttu-id="601d8-136">46</span><span class="sxs-lookup"><span data-stu-id="601d8-136">46</span></span>                                    |
| <span data-ttu-id="601d8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-138">System-Only</span></span>            | <span data-ttu-id="601d8-139">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-139">False</span></span>                                 |
| <span data-ttu-id="601d8-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-141">True</span></span>                                  |
| <span data-ttu-id="601d8-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-142">Is Indexed</span></span>             | <span data-ttu-id="601d8-143">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-143">False</span></span>                                 |
| <span data-ttu-id="601d8-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-144">In Global Catalog</span></span>      | <span data-ttu-id="601d8-145">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-145">False</span></span>                                 |
| <span data-ttu-id="601d8-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-150">Search-Flags</span></span>           | <span data-ttu-id="601d8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-151">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-152">System-Flags</span></span>           | <span data-ttu-id="601d8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-153">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-154">Classes used in</span></span>        | [<span data-ttu-id="601d8-155">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-155">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="601d8-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="601d8-156">Windows Server 2003</span></span>



| <span data-ttu-id="601d8-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-157">Entry</span></span> | <span data-ttu-id="601d8-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-159">Link-Id</span></span>                | <span data-ttu-id="601d8-160">46</span><span class="sxs-lookup"><span data-stu-id="601d8-160">46</span></span>                                    |
| <span data-ttu-id="601d8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-162">System-Only</span></span>            | <span data-ttu-id="601d8-163">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-163">False</span></span>                                 |
| <span data-ttu-id="601d8-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-165">True</span></span>                                  |
| <span data-ttu-id="601d8-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-166">Is Indexed</span></span>             | <span data-ttu-id="601d8-167">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-167">False</span></span>                                 |
| <span data-ttu-id="601d8-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-168">In Global Catalog</span></span>      | <span data-ttu-id="601d8-169">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-169">False</span></span>                                 |
| <span data-ttu-id="601d8-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-174">Search-Flags</span></span>           | <span data-ttu-id="601d8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-175">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-176">System-Flags</span></span>           | <span data-ttu-id="601d8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-177">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-178">Classes used in</span></span>        | [<span data-ttu-id="601d8-179">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-179">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="adam"></a><span data-ttu-id="601d8-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="601d8-180">ADAM</span></span>



| <span data-ttu-id="601d8-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-181">Entry</span></span> | <span data-ttu-id="601d8-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-183">Link-Id</span></span>                | <span data-ttu-id="601d8-184">46</span><span class="sxs-lookup"><span data-stu-id="601d8-184">46</span></span>                                    |
| <span data-ttu-id="601d8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-186">System-Only</span></span>            | <span data-ttu-id="601d8-187">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-187">False</span></span>                                 |
| <span data-ttu-id="601d8-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-189">True</span></span>                                  |
| <span data-ttu-id="601d8-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-190">Is Indexed</span></span>             | <span data-ttu-id="601d8-191">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-191">False</span></span>                                 |
| <span data-ttu-id="601d8-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-192">In Global Catalog</span></span>      | <span data-ttu-id="601d8-193">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-193">False</span></span>                                 |
| <span data-ttu-id="601d8-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-198">Search-Flags</span></span>           | <span data-ttu-id="601d8-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-199">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-200">System-Flags</span></span>           | <span data-ttu-id="601d8-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-201">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-202">Classes used in</span></span>        | [<span data-ttu-id="601d8-203">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="601d8-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="601d8-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="601d8-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-205">Entry</span></span> | <span data-ttu-id="601d8-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-207">Link-Id</span></span>                | <span data-ttu-id="601d8-208">46</span><span class="sxs-lookup"><span data-stu-id="601d8-208">46</span></span>                                    |
| <span data-ttu-id="601d8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-210">System-Only</span></span>            | <span data-ttu-id="601d8-211">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-211">False</span></span>                                 |
| <span data-ttu-id="601d8-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-213">True</span></span>                                  |
| <span data-ttu-id="601d8-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-214">Is Indexed</span></span>             | <span data-ttu-id="601d8-215">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-215">False</span></span>                                 |
| <span data-ttu-id="601d8-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-216">In Global Catalog</span></span>      | <span data-ttu-id="601d8-217">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-217">False</span></span>                                 |
| <span data-ttu-id="601d8-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-222">Search-Flags</span></span>           | <span data-ttu-id="601d8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-223">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-224">System-Flags</span></span>           | <span data-ttu-id="601d8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-225">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-226">Classes used in</span></span>        | [<span data-ttu-id="601d8-227">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-227">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="601d8-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="601d8-228">Windows Server 2008</span></span>



| <span data-ttu-id="601d8-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-229">Entry</span></span> | <span data-ttu-id="601d8-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-231">Link-Id</span></span>                | <span data-ttu-id="601d8-232">46</span><span class="sxs-lookup"><span data-stu-id="601d8-232">46</span></span>                                    |
| <span data-ttu-id="601d8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-234">System-Only</span></span>            | <span data-ttu-id="601d8-235">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-235">False</span></span>                                 |
| <span data-ttu-id="601d8-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-237">True</span></span>                                  |
| <span data-ttu-id="601d8-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-238">Is Indexed</span></span>             | <span data-ttu-id="601d8-239">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-239">False</span></span>                                 |
| <span data-ttu-id="601d8-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-240">In Global Catalog</span></span>      | <span data-ttu-id="601d8-241">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-241">False</span></span>                                 |
| <span data-ttu-id="601d8-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-246">Search-Flags</span></span>           | <span data-ttu-id="601d8-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-247">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-248">System-Flags</span></span>           | <span data-ttu-id="601d8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-249">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-250">Classes used in</span></span>        | [<span data-ttu-id="601d8-251">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-251">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="601d8-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="601d8-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="601d8-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-253">Entry</span></span> | <span data-ttu-id="601d8-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-255">Link-Id</span></span>                | <span data-ttu-id="601d8-256">46</span><span class="sxs-lookup"><span data-stu-id="601d8-256">46</span></span>                                    |
| <span data-ttu-id="601d8-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-258">System-Only</span></span>            | <span data-ttu-id="601d8-259">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-259">False</span></span>                                 |
| <span data-ttu-id="601d8-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-260">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-261">True</span></span>                                  |
| <span data-ttu-id="601d8-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-262">Is Indexed</span></span>             | <span data-ttu-id="601d8-263">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-263">False</span></span>                                 |
| <span data-ttu-id="601d8-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-264">In Global Catalog</span></span>      | <span data-ttu-id="601d8-265">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-265">False</span></span>                                 |
| <span data-ttu-id="601d8-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-270">Search-Flags</span></span>           | <span data-ttu-id="601d8-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-271">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-272">System-Flags</span></span>           | <span data-ttu-id="601d8-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-273">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-274">Classes used in</span></span>        | [<span data-ttu-id="601d8-275">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-275">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="601d8-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="601d8-276">Windows Server 2012</span></span>



| <span data-ttu-id="601d8-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="601d8-277">Entry</span></span> | <span data-ttu-id="601d8-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="601d8-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="601d8-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="601d8-279">Link-Id</span></span>                | <span data-ttu-id="601d8-280">46</span><span class="sxs-lookup"><span data-stu-id="601d8-280">46</span></span>                                    |
| <span data-ttu-id="601d8-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="601d8-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="601d8-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="601d8-282">System-Only</span></span>            | <span data-ttu-id="601d8-283">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-283">False</span></span>                                 |
| <span data-ttu-id="601d8-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="601d8-284">Is-Single-Valued</span></span>       | <span data-ttu-id="601d8-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="601d8-285">True</span></span>                                  |
| <span data-ttu-id="601d8-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="601d8-286">Is Indexed</span></span>             | <span data-ttu-id="601d8-287">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-287">False</span></span>                                 |
| <span data-ttu-id="601d8-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="601d8-288">In Global Catalog</span></span>      | <span data-ttu-id="601d8-289">Faux</span><span class="sxs-lookup"><span data-stu-id="601d8-289">False</span></span>                                 |
| <span data-ttu-id="601d8-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="601d8-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="601d8-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="601d8-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="601d8-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="601d8-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="601d8-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="601d8-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="601d8-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-294">Search-Flags</span></span>           | <span data-ttu-id="601d8-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="601d8-295">0x00000000</span></span>                            |
| <span data-ttu-id="601d8-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="601d8-296">System-Flags</span></span>           | <span data-ttu-id="601d8-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="601d8-297">0x00000010</span></span>                            |
| <span data-ttu-id="601d8-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="601d8-298">Classes used in</span></span>        | [<span data-ttu-id="601d8-299">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="601d8-299">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





