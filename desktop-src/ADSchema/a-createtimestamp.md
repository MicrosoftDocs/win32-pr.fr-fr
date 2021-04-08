---
title: Attribut d’horodatage de création
description: Date à laquelle cet objet a été créé. Cette valeur est répliquée.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut de création d’horodateur
- Schéma AD de l’attribut createTimeStamp
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745268"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="2e817-106">Attribut d’horodatage de création</span><span class="sxs-lookup"><span data-stu-id="2e817-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="2e817-107">Date à laquelle cet objet a été créé.</span><span class="sxs-lookup"><span data-stu-id="2e817-107">The date when this object was created.</span></span> <span data-ttu-id="2e817-108">Cette valeur est répliquée.</span><span class="sxs-lookup"><span data-stu-id="2e817-108">This value is replicated.</span></span>



| <span data-ttu-id="2e817-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-109">Entry</span></span> | <span data-ttu-id="2e817-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="2e817-111">CN</span><span class="sxs-lookup"><span data-stu-id="2e817-111">CN</span></span>                | <span data-ttu-id="2e817-112">Date et heure de création</span><span class="sxs-lookup"><span data-stu-id="2e817-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="2e817-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e817-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2e817-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="2e817-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="2e817-115">Taille</span><span class="sxs-lookup"><span data-stu-id="2e817-115">Size</span></span>              | <span data-ttu-id="2e817-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="2e817-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="2e817-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2e817-117">Update Privilege</span></span>  | <span data-ttu-id="2e817-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="2e817-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="2e817-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2e817-119">Update Frequency</span></span>  | <span data-ttu-id="2e817-120">Lorsque l’objet est créé.</span><span class="sxs-lookup"><span data-stu-id="2e817-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="2e817-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-121">Attribute-Id</span></span>      | <span data-ttu-id="2e817-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="2e817-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="2e817-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e817-123">System-Id-Guid</span></span>    | <span data-ttu-id="2e817-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="2e817-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="2e817-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e817-125">Syntax</span></span>            | [<span data-ttu-id="2e817-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="2e817-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="2e817-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2e817-127">Implementations</span></span>

-   [<span data-ttu-id="2e817-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e817-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e817-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e817-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e817-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2e817-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2e817-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e817-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e817-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e817-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e817-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e817-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e817-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e817-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e817-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e817-135">Windows 2000 Server</span></span>



| <span data-ttu-id="2e817-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-136">Entry</span></span> | <span data-ttu-id="2e817-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-140">System-Only</span></span>            | <span data-ttu-id="2e817-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-141">True</span></span>                            |
| <span data-ttu-id="2e817-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-143">True</span></span>                            |
| <span data-ttu-id="2e817-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-144">Is Indexed</span></span>             | <span data-ttu-id="2e817-145">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-145">False</span></span>                           |
| <span data-ttu-id="2e817-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-146">In Global Catalog</span></span>      | <span data-ttu-id="2e817-147">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-147">False</span></span>                           |
| <span data-ttu-id="2e817-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-152">Search-Flags</span></span>           | <span data-ttu-id="2e817-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-153">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-154">System-Flags</span></span>           | <span data-ttu-id="2e817-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-155">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-156">Classes used in</span></span>        | [<span data-ttu-id="2e817-157">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e817-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e817-158">Windows Server 2003</span></span>



| <span data-ttu-id="2e817-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-159">Entry</span></span> | <span data-ttu-id="2e817-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-163">System-Only</span></span>            | <span data-ttu-id="2e817-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-164">True</span></span>                            |
| <span data-ttu-id="2e817-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-166">True</span></span>                            |
| <span data-ttu-id="2e817-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-167">Is Indexed</span></span>             | <span data-ttu-id="2e817-168">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-168">False</span></span>                           |
| <span data-ttu-id="2e817-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-169">In Global Catalog</span></span>      | <span data-ttu-id="2e817-170">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-170">False</span></span>                           |
| <span data-ttu-id="2e817-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-175">Search-Flags</span></span>           | <span data-ttu-id="2e817-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-176">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-177">System-Flags</span></span>           | <span data-ttu-id="2e817-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-178">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-179">Classes used in</span></span>        | [<span data-ttu-id="2e817-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2e817-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="2e817-181">ADAM</span></span>



| <span data-ttu-id="2e817-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-182">Entry</span></span> | <span data-ttu-id="2e817-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-186">System-Only</span></span>            | <span data-ttu-id="2e817-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-187">True</span></span>                            |
| <span data-ttu-id="2e817-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-189">True</span></span>                            |
| <span data-ttu-id="2e817-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-190">Is Indexed</span></span>             | <span data-ttu-id="2e817-191">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-191">False</span></span>                           |
| <span data-ttu-id="2e817-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-192">In Global Catalog</span></span>      | <span data-ttu-id="2e817-193">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-193">False</span></span>                           |
| <span data-ttu-id="2e817-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-198">Search-Flags</span></span>           | <span data-ttu-id="2e817-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-199">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-200">System-Flags</span></span>           | <span data-ttu-id="2e817-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-201">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-202">Classes used in</span></span>        | [<span data-ttu-id="2e817-203">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e817-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e817-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e817-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-205">Entry</span></span> | <span data-ttu-id="2e817-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-209">System-Only</span></span>            | <span data-ttu-id="2e817-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-210">True</span></span>                            |
| <span data-ttu-id="2e817-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-212">True</span></span>                            |
| <span data-ttu-id="2e817-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-213">Is Indexed</span></span>             | <span data-ttu-id="2e817-214">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-214">False</span></span>                           |
| <span data-ttu-id="2e817-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-215">In Global Catalog</span></span>      | <span data-ttu-id="2e817-216">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-216">False</span></span>                           |
| <span data-ttu-id="2e817-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-221">Search-Flags</span></span>           | <span data-ttu-id="2e817-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-222">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-223">System-Flags</span></span>           | <span data-ttu-id="2e817-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-224">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-225">Classes used in</span></span>        | [<span data-ttu-id="2e817-226">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e817-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e817-227">Windows Server 2008</span></span>



| <span data-ttu-id="2e817-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-228">Entry</span></span> | <span data-ttu-id="2e817-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-232">System-Only</span></span>            | <span data-ttu-id="2e817-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-233">True</span></span>                            |
| <span data-ttu-id="2e817-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-235">True</span></span>                            |
| <span data-ttu-id="2e817-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-236">Is Indexed</span></span>             | <span data-ttu-id="2e817-237">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-237">False</span></span>                           |
| <span data-ttu-id="2e817-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-238">In Global Catalog</span></span>      | <span data-ttu-id="2e817-239">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-239">False</span></span>                           |
| <span data-ttu-id="2e817-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-244">Search-Flags</span></span>           | <span data-ttu-id="2e817-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-245">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-246">System-Flags</span></span>           | <span data-ttu-id="2e817-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-247">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-248">Classes used in</span></span>        | [<span data-ttu-id="2e817-249">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e817-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e817-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e817-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-251">Entry</span></span> | <span data-ttu-id="2e817-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-255">System-Only</span></span>            | <span data-ttu-id="2e817-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-256">True</span></span>                            |
| <span data-ttu-id="2e817-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-257">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-258">True</span></span>                            |
| <span data-ttu-id="2e817-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-259">Is Indexed</span></span>             | <span data-ttu-id="2e817-260">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-260">False</span></span>                           |
| <span data-ttu-id="2e817-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-261">In Global Catalog</span></span>      | <span data-ttu-id="2e817-262">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-262">False</span></span>                           |
| <span data-ttu-id="2e817-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-267">Search-Flags</span></span>           | <span data-ttu-id="2e817-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-268">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-269">System-Flags</span></span>           | <span data-ttu-id="2e817-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-270">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-271">Classes used in</span></span>        | [<span data-ttu-id="2e817-272">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e817-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e817-273">Windows Server 2012</span></span>



| <span data-ttu-id="2e817-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="2e817-274">Entry</span></span> | <span data-ttu-id="2e817-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2e817-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2e817-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e817-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2e817-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e817-278">System-Only</span></span>            | <span data-ttu-id="2e817-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-279">True</span></span>                            |
| <span data-ttu-id="2e817-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2e817-280">Is-Single-Valued</span></span>       | <span data-ttu-id="2e817-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="2e817-281">True</span></span>                            |
| <span data-ttu-id="2e817-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2e817-282">Is Indexed</span></span>             | <span data-ttu-id="2e817-283">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-283">False</span></span>                           |
| <span data-ttu-id="2e817-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2e817-284">In Global Catalog</span></span>      | <span data-ttu-id="2e817-285">Faux</span><span class="sxs-lookup"><span data-stu-id="2e817-285">False</span></span>                           |
| <span data-ttu-id="2e817-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2e817-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e817-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2e817-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2e817-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e817-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2e817-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e817-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2e817-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-290">Search-Flags</span></span>           | <span data-ttu-id="2e817-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e817-291">0x00000000</span></span>                      |
| <span data-ttu-id="2e817-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e817-292">System-Flags</span></span>           | <span data-ttu-id="2e817-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2e817-293">0x08000014</span></span>                      |
| <span data-ttu-id="2e817-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2e817-294">Classes used in</span></span>        | [<span data-ttu-id="2e817-295">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="2e817-295">**Top**</span></span>](c-top.md)<br/> |



 

 





