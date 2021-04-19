---
title: Attribut From-Entry
description: Il s’agit d’un attribut construit qui a la valeur TRUE si l’objet est accessible en écriture et FALSe s’il est en lecture seule, par exemple, une instance de réplica GC.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut From-Entry
- Schéma AD de l’attribut fromEntry
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106532058"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="1fa03-105">Attribut From-Entry</span><span class="sxs-lookup"><span data-stu-id="1fa03-105">From-Entry attribute</span></span>

<span data-ttu-id="1fa03-106">Il s’agit d’un attribut construit qui a la **valeur true** si l’objet est accessible en écriture et **false** s’il est en lecture seule, par exemple, une instance de réplica gc.</span><span class="sxs-lookup"><span data-stu-id="1fa03-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="1fa03-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-107">Entry</span></span> | <span data-ttu-id="1fa03-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1fa03-109">CN</span><span class="sxs-lookup"><span data-stu-id="1fa03-109">CN</span></span>                | <span data-ttu-id="1fa03-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="1fa03-110">From-Entry</span></span>                           |
| <span data-ttu-id="1fa03-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1fa03-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1fa03-112">fromEntry</span><span class="sxs-lookup"><span data-stu-id="1fa03-112">fromEntry</span></span>                            |
| <span data-ttu-id="1fa03-113">Taille</span><span class="sxs-lookup"><span data-stu-id="1fa03-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="1fa03-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="1fa03-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1fa03-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="1fa03-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1fa03-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-116">Attribute-Id</span></span>      | <span data-ttu-id="1fa03-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="1fa03-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="1fa03-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1fa03-118">System-Id-Guid</span></span>    | <span data-ttu-id="1fa03-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="1fa03-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="1fa03-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fa03-120">Syntax</span></span>            | [<span data-ttu-id="1fa03-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1fa03-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="1fa03-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="1fa03-122">Implementations</span></span>

-   [<span data-ttu-id="1fa03-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1fa03-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1fa03-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1fa03-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1fa03-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1fa03-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1fa03-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1fa03-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1fa03-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1fa03-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1fa03-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1fa03-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1fa03-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1fa03-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1fa03-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fa03-130">Windows 2000 Server</span></span>



| <span data-ttu-id="1fa03-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-131">Entry</span></span> | <span data-ttu-id="1fa03-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-135">System-Only</span></span>            | <span data-ttu-id="1fa03-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-136">True</span></span>                            |
| <span data-ttu-id="1fa03-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-138">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-138">False</span></span>                           |
| <span data-ttu-id="1fa03-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-139">Is Indexed</span></span>             | <span data-ttu-id="1fa03-140">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-140">False</span></span>                           |
| <span data-ttu-id="1fa03-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-141">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-142">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-142">False</span></span>                           |
| <span data-ttu-id="1fa03-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-147">Search-Flags</span></span>           | <span data-ttu-id="1fa03-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-148">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-149">System-Flags</span></span>           | <span data-ttu-id="1fa03-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-150">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-151">Classes used in</span></span>        | [<span data-ttu-id="1fa03-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1fa03-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fa03-153">Windows Server 2003</span></span>



| <span data-ttu-id="1fa03-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-154">Entry</span></span> | <span data-ttu-id="1fa03-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-158">System-Only</span></span>            | <span data-ttu-id="1fa03-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-159">True</span></span>                            |
| <span data-ttu-id="1fa03-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-160">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-161">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-161">False</span></span>                           |
| <span data-ttu-id="1fa03-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-162">Is Indexed</span></span>             | <span data-ttu-id="1fa03-163">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-163">False</span></span>                           |
| <span data-ttu-id="1fa03-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-164">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-165">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-165">False</span></span>                           |
| <span data-ttu-id="1fa03-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-170">Search-Flags</span></span>           | <span data-ttu-id="1fa03-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-171">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-172">System-Flags</span></span>           | <span data-ttu-id="1fa03-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-173">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-174">Classes used in</span></span>        | [<span data-ttu-id="1fa03-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1fa03-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="1fa03-176">ADAM</span></span>



| <span data-ttu-id="1fa03-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-177">Entry</span></span> | <span data-ttu-id="1fa03-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-181">System-Only</span></span>            | <span data-ttu-id="1fa03-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-182">True</span></span>                            |
| <span data-ttu-id="1fa03-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-183">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-184">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-184">False</span></span>                           |
| <span data-ttu-id="1fa03-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-185">Is Indexed</span></span>             | <span data-ttu-id="1fa03-186">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-186">False</span></span>                           |
| <span data-ttu-id="1fa03-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-187">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-188">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-188">False</span></span>                           |
| <span data-ttu-id="1fa03-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-193">Search-Flags</span></span>           | <span data-ttu-id="1fa03-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-194">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-195">System-Flags</span></span>           | <span data-ttu-id="1fa03-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-196">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-197">Classes used in</span></span>        | [<span data-ttu-id="1fa03-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1fa03-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1fa03-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1fa03-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-200">Entry</span></span> | <span data-ttu-id="1fa03-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-204">System-Only</span></span>            | <span data-ttu-id="1fa03-205">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-205">True</span></span>                            |
| <span data-ttu-id="1fa03-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-206">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-207">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-207">False</span></span>                           |
| <span data-ttu-id="1fa03-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-208">Is Indexed</span></span>             | <span data-ttu-id="1fa03-209">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-209">False</span></span>                           |
| <span data-ttu-id="1fa03-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-210">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-211">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-211">False</span></span>                           |
| <span data-ttu-id="1fa03-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-216">Search-Flags</span></span>           | <span data-ttu-id="1fa03-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-217">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-218">System-Flags</span></span>           | <span data-ttu-id="1fa03-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-219">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-220">Classes used in</span></span>        | [<span data-ttu-id="1fa03-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1fa03-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fa03-222">Windows Server 2008</span></span>



| <span data-ttu-id="1fa03-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-223">Entry</span></span> | <span data-ttu-id="1fa03-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-227">System-Only</span></span>            | <span data-ttu-id="1fa03-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-228">True</span></span>                            |
| <span data-ttu-id="1fa03-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-229">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-230">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-230">False</span></span>                           |
| <span data-ttu-id="1fa03-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-231">Is Indexed</span></span>             | <span data-ttu-id="1fa03-232">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-232">False</span></span>                           |
| <span data-ttu-id="1fa03-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-233">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-234">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-234">False</span></span>                           |
| <span data-ttu-id="1fa03-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-239">Search-Flags</span></span>           | <span data-ttu-id="1fa03-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-240">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-241">System-Flags</span></span>           | <span data-ttu-id="1fa03-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-242">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-243">Classes used in</span></span>        | [<span data-ttu-id="1fa03-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1fa03-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fa03-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1fa03-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-246">Entry</span></span> | <span data-ttu-id="1fa03-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-250">System-Only</span></span>            | <span data-ttu-id="1fa03-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-251">True</span></span>                            |
| <span data-ttu-id="1fa03-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-252">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-253">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-253">False</span></span>                           |
| <span data-ttu-id="1fa03-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-254">Is Indexed</span></span>             | <span data-ttu-id="1fa03-255">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-255">False</span></span>                           |
| <span data-ttu-id="1fa03-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-256">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-257">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-257">False</span></span>                           |
| <span data-ttu-id="1fa03-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-262">Search-Flags</span></span>           | <span data-ttu-id="1fa03-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-263">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-264">System-Flags</span></span>           | <span data-ttu-id="1fa03-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-265">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-266">Classes used in</span></span>        | [<span data-ttu-id="1fa03-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1fa03-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fa03-268">Windows Server 2012</span></span>



| <span data-ttu-id="1fa03-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="1fa03-269">Entry</span></span> | <span data-ttu-id="1fa03-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa03-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fa03-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1fa03-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fa03-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fa03-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fa03-273">System-Only</span></span>            | <span data-ttu-id="1fa03-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="1fa03-274">True</span></span>                            |
| <span data-ttu-id="1fa03-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1fa03-275">Is-Single-Valued</span></span>       | <span data-ttu-id="1fa03-276">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-276">False</span></span>                           |
| <span data-ttu-id="1fa03-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1fa03-277">Is Indexed</span></span>             | <span data-ttu-id="1fa03-278">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-278">False</span></span>                           |
| <span data-ttu-id="1fa03-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1fa03-279">In Global Catalog</span></span>      | <span data-ttu-id="1fa03-280">Faux</span><span class="sxs-lookup"><span data-stu-id="1fa03-280">False</span></span>                           |
| <span data-ttu-id="1fa03-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1fa03-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fa03-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1fa03-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fa03-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fa03-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fa03-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fa03-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fa03-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-285">Search-Flags</span></span>           | <span data-ttu-id="1fa03-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fa03-286">0x00000000</span></span>                      |
| <span data-ttu-id="1fa03-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fa03-287">System-Flags</span></span>           | <span data-ttu-id="1fa03-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1fa03-288">0x08000014</span></span>                      |
| <span data-ttu-id="1fa03-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1fa03-289">Classes used in</span></span>        | [<span data-ttu-id="1fa03-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1fa03-290">**Top**</span></span>](c-top.md)<br/> |



 

 





