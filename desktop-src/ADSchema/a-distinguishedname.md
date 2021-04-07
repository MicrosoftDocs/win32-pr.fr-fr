---
title: Obj-Dist-Name (attribut)
description: Identique au nom unique d’un objet. Utilisé par Exchange.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Obj-Dist-Name
- Schéma AD attribut distinguishedName
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844682"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="b1729-106">Obj-Dist-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="b1729-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="b1729-107">Identique au nom unique d’un objet.</span><span class="sxs-lookup"><span data-stu-id="b1729-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="b1729-108">Utilisé par Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1729-108">Used by Exchange.</span></span>



| <span data-ttu-id="b1729-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-109">Entry</span></span> | <span data-ttu-id="b1729-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b1729-111">CN</span><span class="sxs-lookup"><span data-stu-id="b1729-111">CN</span></span>                | <span data-ttu-id="b1729-112">Obj-Dist-Name</span><span class="sxs-lookup"><span data-stu-id="b1729-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="b1729-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1729-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b1729-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="b1729-114">distinguishedName</span></span>                       |
| <span data-ttu-id="b1729-115">Taille</span><span class="sxs-lookup"><span data-stu-id="b1729-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="b1729-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b1729-116">Update Privilege</span></span>  | <span data-ttu-id="b1729-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="b1729-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="b1729-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b1729-118">Update Frequency</span></span>  | <span data-ttu-id="b1729-119">À chaque fois qu’un objet est créé ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="b1729-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="b1729-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-120">Attribute-Id</span></span>      | <span data-ttu-id="b1729-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="b1729-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="b1729-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1729-122">System-Id-Guid</span></span>    | <span data-ttu-id="b1729-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b1729-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="b1729-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1729-124">Syntax</span></span>            | [<span data-ttu-id="b1729-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b1729-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b1729-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b1729-126">Implementations</span></span>

-   [<span data-ttu-id="b1729-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1729-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1729-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1729-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1729-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b1729-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1729-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1729-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1729-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1729-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1729-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1729-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1729-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1729-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1729-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1729-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b1729-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-135">Entry</span></span> | <span data-ttu-id="b1729-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-138">MAPI-Id</span></span>                | <span data-ttu-id="b1729-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-139">0x803C</span></span>                          |
| <span data-ttu-id="b1729-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-140">System-Only</span></span>            | <span data-ttu-id="b1729-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-141">True</span></span>                            |
| <span data-ttu-id="b1729-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-143">True</span></span>                            |
| <span data-ttu-id="b1729-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-144">Is Indexed</span></span>             | <span data-ttu-id="b1729-145">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-145">False</span></span>                           |
| <span data-ttu-id="b1729-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-146">In Global Catalog</span></span>      | <span data-ttu-id="b1729-147">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-147">True</span></span>                            |
| <span data-ttu-id="b1729-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-152">Search-Flags</span></span>           | <span data-ttu-id="b1729-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-153">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-154">System-Flags</span></span>           | <span data-ttu-id="b1729-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-155">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-156">Classes used in</span></span>        | [<span data-ttu-id="b1729-157">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1729-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1729-158">Windows Server 2003</span></span>



| <span data-ttu-id="b1729-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-159">Entry</span></span> | <span data-ttu-id="b1729-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-162">MAPI-Id</span></span>                | <span data-ttu-id="b1729-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-163">0x803C</span></span>                          |
| <span data-ttu-id="b1729-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-164">System-Only</span></span>            | <span data-ttu-id="b1729-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-165">True</span></span>                            |
| <span data-ttu-id="b1729-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-167">True</span></span>                            |
| <span data-ttu-id="b1729-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-168">Is Indexed</span></span>             | <span data-ttu-id="b1729-169">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-169">False</span></span>                           |
| <span data-ttu-id="b1729-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-170">In Global Catalog</span></span>      | <span data-ttu-id="b1729-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-171">True</span></span>                            |
| <span data-ttu-id="b1729-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-176">Search-Flags</span></span>           | <span data-ttu-id="b1729-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-177">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-178">System-Flags</span></span>           | <span data-ttu-id="b1729-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-179">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-180">Classes used in</span></span>        | [<span data-ttu-id="b1729-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b1729-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="b1729-182">ADAM</span></span>



| <span data-ttu-id="b1729-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-183">Entry</span></span> | <span data-ttu-id="b1729-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-186">MAPI-Id</span></span>                | <span data-ttu-id="b1729-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-187">0x803C</span></span>                          |
| <span data-ttu-id="b1729-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-188">System-Only</span></span>            | <span data-ttu-id="b1729-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-189">True</span></span>                            |
| <span data-ttu-id="b1729-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-190">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-191">True</span></span>                            |
| <span data-ttu-id="b1729-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-192">Is Indexed</span></span>             | <span data-ttu-id="b1729-193">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-193">False</span></span>                           |
| <span data-ttu-id="b1729-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-194">In Global Catalog</span></span>      | <span data-ttu-id="b1729-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-195">True</span></span>                            |
| <span data-ttu-id="b1729-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-200">Search-Flags</span></span>           | <span data-ttu-id="b1729-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-201">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-202">System-Flags</span></span>           | <span data-ttu-id="b1729-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-203">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-204">Classes used in</span></span>        | [<span data-ttu-id="b1729-205">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1729-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1729-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1729-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-207">Entry</span></span> | <span data-ttu-id="b1729-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-210">MAPI-Id</span></span>                | <span data-ttu-id="b1729-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-211">0x803C</span></span>                          |
| <span data-ttu-id="b1729-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-212">System-Only</span></span>            | <span data-ttu-id="b1729-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-213">True</span></span>                            |
| <span data-ttu-id="b1729-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-214">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-215">True</span></span>                            |
| <span data-ttu-id="b1729-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-216">Is Indexed</span></span>             | <span data-ttu-id="b1729-217">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-217">False</span></span>                           |
| <span data-ttu-id="b1729-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-218">In Global Catalog</span></span>      | <span data-ttu-id="b1729-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-219">True</span></span>                            |
| <span data-ttu-id="b1729-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-224">Search-Flags</span></span>           | <span data-ttu-id="b1729-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-225">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-226">System-Flags</span></span>           | <span data-ttu-id="b1729-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-227">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-228">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-228">Classes used in</span></span>        | [<span data-ttu-id="b1729-229">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1729-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1729-230">Windows Server 2008</span></span>



| <span data-ttu-id="b1729-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-231">Entry</span></span> | <span data-ttu-id="b1729-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-234">MAPI-Id</span></span>                | <span data-ttu-id="b1729-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-235">0x803C</span></span>                          |
| <span data-ttu-id="b1729-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-236">System-Only</span></span>            | <span data-ttu-id="b1729-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-237">True</span></span>                            |
| <span data-ttu-id="b1729-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-238">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-239">True</span></span>                            |
| <span data-ttu-id="b1729-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-240">Is Indexed</span></span>             | <span data-ttu-id="b1729-241">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-241">False</span></span>                           |
| <span data-ttu-id="b1729-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-242">In Global Catalog</span></span>      | <span data-ttu-id="b1729-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-243">True</span></span>                            |
| <span data-ttu-id="b1729-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-248">Search-Flags</span></span>           | <span data-ttu-id="b1729-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-249">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-250">System-Flags</span></span>           | <span data-ttu-id="b1729-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-251">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-252">Classes used in</span></span>        | [<span data-ttu-id="b1729-253">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1729-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1729-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1729-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-255">Entry</span></span> | <span data-ttu-id="b1729-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-258">MAPI-Id</span></span>                | <span data-ttu-id="b1729-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-259">0x803C</span></span>                          |
| <span data-ttu-id="b1729-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-260">System-Only</span></span>            | <span data-ttu-id="b1729-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-261">True</span></span>                            |
| <span data-ttu-id="b1729-262">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-262">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-263">True</span></span>                            |
| <span data-ttu-id="b1729-264">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-264">Is Indexed</span></span>             | <span data-ttu-id="b1729-265">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-265">False</span></span>                           |
| <span data-ttu-id="b1729-266">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-266">In Global Catalog</span></span>      | <span data-ttu-id="b1729-267">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-267">True</span></span>                            |
| <span data-ttu-id="b1729-268">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-269">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-272">Search-Flags</span></span>           | <span data-ttu-id="b1729-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-273">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-274">System-Flags</span></span>           | <span data-ttu-id="b1729-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-275">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-276">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-276">Classes used in</span></span>        | [<span data-ttu-id="b1729-277">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1729-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1729-278">Windows Server 2012</span></span>



| <span data-ttu-id="b1729-279">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1729-279">Entry</span></span> | <span data-ttu-id="b1729-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1729-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1729-281">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1729-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1729-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1729-282">MAPI-Id</span></span>                | <span data-ttu-id="b1729-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="b1729-283">0x803C</span></span>                          |
| <span data-ttu-id="b1729-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1729-284">System-Only</span></span>            | <span data-ttu-id="b1729-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-285">True</span></span>                            |
| <span data-ttu-id="b1729-286">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1729-286">Is-Single-Valued</span></span>       | <span data-ttu-id="b1729-287">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-287">True</span></span>                            |
| <span data-ttu-id="b1729-288">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1729-288">Is Indexed</span></span>             | <span data-ttu-id="b1729-289">Faux</span><span class="sxs-lookup"><span data-stu-id="b1729-289">False</span></span>                           |
| <span data-ttu-id="b1729-290">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1729-290">In Global Catalog</span></span>      | <span data-ttu-id="b1729-291">Vrai</span><span class="sxs-lookup"><span data-stu-id="b1729-291">True</span></span>                            |
| <span data-ttu-id="b1729-292">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1729-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1729-293">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1729-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1729-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1729-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1729-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1729-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1729-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-296">Search-Flags</span></span>           | <span data-ttu-id="b1729-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1729-297">0x00000008</span></span>                      |
| <span data-ttu-id="b1729-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1729-298">System-Flags</span></span>           | <span data-ttu-id="b1729-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b1729-299">0x00000013</span></span>                      |
| <span data-ttu-id="b1729-300">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1729-300">Classes used in</span></span>        | [<span data-ttu-id="b1729-301">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="b1729-301">**Top**</span></span>](c-top.md)<br/> |



 

 





