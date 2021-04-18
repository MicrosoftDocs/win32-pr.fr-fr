---
title: Dernier attribut parent connu
description: Nom unique (DN) du dernier parent connu d’un objet orphelin.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- Dernier schéma AD de l’attribut parent connu
- Schéma AD de l’attribut lastKnownParent
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106519160"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="19f78-105">Dernier attribut parent connu</span><span class="sxs-lookup"><span data-stu-id="19f78-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="19f78-106">Nom unique (DN) du dernier parent connu d’un objet orphelin.</span><span class="sxs-lookup"><span data-stu-id="19f78-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="19f78-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-107">Entry</span></span> | <span data-ttu-id="19f78-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="19f78-109">CN</span><span class="sxs-lookup"><span data-stu-id="19f78-109">CN</span></span>                | <span data-ttu-id="19f78-110">Dernier-parent connu</span><span class="sxs-lookup"><span data-stu-id="19f78-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="19f78-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="19f78-111">Ldap-Display-Name</span></span> | <span data-ttu-id="19f78-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="19f78-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="19f78-113">Taille</span><span class="sxs-lookup"><span data-stu-id="19f78-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="19f78-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="19f78-114">Update Privilege</span></span>  | <span data-ttu-id="19f78-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="19f78-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="19f78-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="19f78-116">Update Frequency</span></span>  | <span data-ttu-id="19f78-117">Chaque fois qu’un objet est orphelin.</span><span class="sxs-lookup"><span data-stu-id="19f78-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="19f78-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-118">Attribute-Id</span></span>      | <span data-ttu-id="19f78-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="19f78-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="19f78-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19f78-120">System-Id-Guid</span></span>    | <span data-ttu-id="19f78-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="19f78-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="19f78-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19f78-122">Syntax</span></span>            | [<span data-ttu-id="19f78-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="19f78-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="19f78-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="19f78-124">Implementations</span></span>

-   [<span data-ttu-id="19f78-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19f78-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19f78-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19f78-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19f78-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="19f78-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="19f78-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19f78-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19f78-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19f78-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19f78-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19f78-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19f78-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19f78-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19f78-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19f78-132">Windows 2000 Server</span></span>



| <span data-ttu-id="19f78-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-133">Entry</span></span> | <span data-ttu-id="19f78-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-137">System-Only</span></span>            | <span data-ttu-id="19f78-138">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-138">False</span></span>                           |
| <span data-ttu-id="19f78-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-139">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-140">True</span></span>                            |
| <span data-ttu-id="19f78-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-141">Is Indexed</span></span>             | <span data-ttu-id="19f78-142">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-142">False</span></span>                           |
| <span data-ttu-id="19f78-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-143">In Global Catalog</span></span>      | <span data-ttu-id="19f78-144">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-144">False</span></span>                           |
| <span data-ttu-id="19f78-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-149">Search-Flags</span></span>           | <span data-ttu-id="19f78-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-150">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-151">System-Flags</span></span>           | <span data-ttu-id="19f78-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-152">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-153">Classes used in</span></span>        | [<span data-ttu-id="19f78-154">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19f78-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19f78-155">Windows Server 2003</span></span>



| <span data-ttu-id="19f78-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-156">Entry</span></span> | <span data-ttu-id="19f78-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-160">System-Only</span></span>            | <span data-ttu-id="19f78-161">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-161">False</span></span>                           |
| <span data-ttu-id="19f78-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-162">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-163">True</span></span>                            |
| <span data-ttu-id="19f78-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-164">Is Indexed</span></span>             | <span data-ttu-id="19f78-165">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-165">False</span></span>                           |
| <span data-ttu-id="19f78-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-166">In Global Catalog</span></span>      | <span data-ttu-id="19f78-167">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-167">False</span></span>                           |
| <span data-ttu-id="19f78-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-172">Search-Flags</span></span>           | <span data-ttu-id="19f78-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-173">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-174">System-Flags</span></span>           | <span data-ttu-id="19f78-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-175">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-176">Classes used in</span></span>        | [<span data-ttu-id="19f78-177">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="19f78-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="19f78-178">ADAM</span></span>



| <span data-ttu-id="19f78-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-179">Entry</span></span> | <span data-ttu-id="19f78-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-183">System-Only</span></span>            | <span data-ttu-id="19f78-184">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-184">False</span></span>                           |
| <span data-ttu-id="19f78-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-185">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-186">True</span></span>                            |
| <span data-ttu-id="19f78-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-187">Is Indexed</span></span>             | <span data-ttu-id="19f78-188">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-188">False</span></span>                           |
| <span data-ttu-id="19f78-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-189">In Global Catalog</span></span>      | <span data-ttu-id="19f78-190">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-190">False</span></span>                           |
| <span data-ttu-id="19f78-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-195">Search-Flags</span></span>           | <span data-ttu-id="19f78-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-196">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-197">System-Flags</span></span>           | <span data-ttu-id="19f78-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-198">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-199">Classes used in</span></span>        | [<span data-ttu-id="19f78-200">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19f78-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19f78-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19f78-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-202">Entry</span></span> | <span data-ttu-id="19f78-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-206">System-Only</span></span>            | <span data-ttu-id="19f78-207">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-207">False</span></span>                           |
| <span data-ttu-id="19f78-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-208">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-209">True</span></span>                            |
| <span data-ttu-id="19f78-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-210">Is Indexed</span></span>             | <span data-ttu-id="19f78-211">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-211">False</span></span>                           |
| <span data-ttu-id="19f78-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-212">In Global Catalog</span></span>      | <span data-ttu-id="19f78-213">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-213">False</span></span>                           |
| <span data-ttu-id="19f78-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-218">Search-Flags</span></span>           | <span data-ttu-id="19f78-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-219">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-220">System-Flags</span></span>           | <span data-ttu-id="19f78-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-221">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-222">Classes used in</span></span>        | [<span data-ttu-id="19f78-223">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19f78-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f78-224">Windows Server 2008</span></span>



| <span data-ttu-id="19f78-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-225">Entry</span></span> | <span data-ttu-id="19f78-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-229">System-Only</span></span>            | <span data-ttu-id="19f78-230">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-230">False</span></span>                           |
| <span data-ttu-id="19f78-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-231">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-232">True</span></span>                            |
| <span data-ttu-id="19f78-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-233">Is Indexed</span></span>             | <span data-ttu-id="19f78-234">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-234">False</span></span>                           |
| <span data-ttu-id="19f78-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-235">In Global Catalog</span></span>      | <span data-ttu-id="19f78-236">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-236">False</span></span>                           |
| <span data-ttu-id="19f78-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-241">Search-Flags</span></span>           | <span data-ttu-id="19f78-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-242">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-243">System-Flags</span></span>           | <span data-ttu-id="19f78-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-244">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-245">Classes used in</span></span>        | [<span data-ttu-id="19f78-246">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19f78-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19f78-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19f78-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-248">Entry</span></span> | <span data-ttu-id="19f78-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-252">System-Only</span></span>            | <span data-ttu-id="19f78-253">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-253">False</span></span>                           |
| <span data-ttu-id="19f78-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-254">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-255">True</span></span>                            |
| <span data-ttu-id="19f78-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-256">Is Indexed</span></span>             | <span data-ttu-id="19f78-257">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-257">False</span></span>                           |
| <span data-ttu-id="19f78-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-258">In Global Catalog</span></span>      | <span data-ttu-id="19f78-259">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-259">False</span></span>                           |
| <span data-ttu-id="19f78-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-264">Search-Flags</span></span>           | <span data-ttu-id="19f78-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-265">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-266">System-Flags</span></span>           | <span data-ttu-id="19f78-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-267">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-268">Classes used in</span></span>        | [<span data-ttu-id="19f78-269">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19f78-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19f78-270">Windows Server 2012</span></span>



| <span data-ttu-id="19f78-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="19f78-271">Entry</span></span> | <span data-ttu-id="19f78-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="19f78-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f78-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="19f78-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f78-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="19f78-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f78-275">System-Only</span></span>            | <span data-ttu-id="19f78-276">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-276">False</span></span>                           |
| <span data-ttu-id="19f78-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="19f78-277">Is-Single-Valued</span></span>       | <span data-ttu-id="19f78-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="19f78-278">True</span></span>                            |
| <span data-ttu-id="19f78-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="19f78-279">Is Indexed</span></span>             | <span data-ttu-id="19f78-280">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-280">False</span></span>                           |
| <span data-ttu-id="19f78-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="19f78-281">In Global Catalog</span></span>      | <span data-ttu-id="19f78-282">Faux</span><span class="sxs-lookup"><span data-stu-id="19f78-282">False</span></span>                           |
| <span data-ttu-id="19f78-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="19f78-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f78-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="19f78-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f78-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f78-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f78-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f78-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f78-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-287">Search-Flags</span></span>           | <span data-ttu-id="19f78-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f78-288">0x00000000</span></span>                      |
| <span data-ttu-id="19f78-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f78-289">System-Flags</span></span>           | <span data-ttu-id="19f78-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f78-290">0x00000010</span></span>                      |
| <span data-ttu-id="19f78-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="19f78-291">Classes used in</span></span>        | [<span data-ttu-id="19f78-292">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="19f78-292">**Top**</span></span>](c-top.md)<br/> |



 

 





