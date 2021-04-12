---
title: Attribut System-Flags
description: Valeur entière qui contient des indicateurs qui définissent des propriétés supplémentaires de la classe.
ms.assetid: ce24322c-fb01-462a-aefe-cb422851f782
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut System-Flags
- Schéma Active Directory de l’attribut systemFlags
topic_type:
- apiref
api_name:
- System-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34bf4286cbdadc84bf340eea3f6cbec741c7920
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480221"
---
# <a name="system-flags-attribute"></a><span data-ttu-id="187ad-105">Attribut System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-105">System-Flags attribute</span></span>

<span data-ttu-id="187ad-106">Valeur entière qui contient des indicateurs qui définissent des propriétés supplémentaires de la classe.</span><span class="sxs-lookup"><span data-stu-id="187ad-106">An integer value that contains flags that define additional properties of the class.</span></span> <span data-ttu-id="187ad-107">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="187ad-107">See Remarks.</span></span>



| <span data-ttu-id="187ad-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-108">Entry</span></span> | <span data-ttu-id="187ad-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="187ad-110">CN</span><span class="sxs-lookup"><span data-stu-id="187ad-110">CN</span></span>                | <span data-ttu-id="187ad-111">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-111">System-Flags</span></span>                                   |
| <span data-ttu-id="187ad-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="187ad-112">Ldap-Display-Name</span></span> | <span data-ttu-id="187ad-113">systemFlags</span><span class="sxs-lookup"><span data-stu-id="187ad-113">systemFlags</span></span>                                    |
| <span data-ttu-id="187ad-114">Taille</span><span class="sxs-lookup"><span data-stu-id="187ad-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="187ad-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="187ad-115">Update Privilege</span></span>  | <span data-ttu-id="187ad-116">Cette valeur est définie par l’administrateur de schéma.</span><span class="sxs-lookup"><span data-stu-id="187ad-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="187ad-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="187ad-117">Update Frequency</span></span>  | <span data-ttu-id="187ad-118">Chaque fois que l’état de l’objet change.</span><span class="sxs-lookup"><span data-stu-id="187ad-118">Whenever the state of the object changes.</span></span>      |
| <span data-ttu-id="187ad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-119">Attribute-Id</span></span>      | <span data-ttu-id="187ad-120">1.2.840.113556.1.4.375</span><span class="sxs-lookup"><span data-stu-id="187ad-120">1.2.840.113556.1.4.375</span></span>                         |
| <span data-ttu-id="187ad-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="187ad-121">System-Id-Guid</span></span>    | <span data-ttu-id="187ad-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="187ad-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span></span>           |
| <span data-ttu-id="187ad-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="187ad-123">Syntax</span></span>            | [<span data-ttu-id="187ad-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="187ad-124">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="187ad-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="187ad-125">Implementations</span></span>

-   [<span data-ttu-id="187ad-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="187ad-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="187ad-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="187ad-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="187ad-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="187ad-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="187ad-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="187ad-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="187ad-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="187ad-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="187ad-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="187ad-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="187ad-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="187ad-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="187ad-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="187ad-133">Windows 2000 Server</span></span>



| <span data-ttu-id="187ad-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-134">Entry</span></span> | <span data-ttu-id="187ad-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-138">System-Only</span></span>            | <span data-ttu-id="187ad-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-139">True</span></span>                            |
| <span data-ttu-id="187ad-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-140">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-141">True</span></span>                            |
| <span data-ttu-id="187ad-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-142">Is Indexed</span></span>             | <span data-ttu-id="187ad-143">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-143">False</span></span>                           |
| <span data-ttu-id="187ad-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-144">In Global Catalog</span></span>      | <span data-ttu-id="187ad-145">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-145">False</span></span>                           |
| <span data-ttu-id="187ad-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-150">Search-Flags</span></span>           | <span data-ttu-id="187ad-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-151">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-152">System-Flags</span></span>           | <span data-ttu-id="187ad-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-153">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-154">Classes used in</span></span>        | [<span data-ttu-id="187ad-155">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="187ad-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="187ad-156">Windows Server 2003</span></span>



| <span data-ttu-id="187ad-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-157">Entry</span></span> | <span data-ttu-id="187ad-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-161">System-Only</span></span>            | <span data-ttu-id="187ad-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-162">True</span></span>                            |
| <span data-ttu-id="187ad-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-163">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-164">True</span></span>                            |
| <span data-ttu-id="187ad-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-165">Is Indexed</span></span>             | <span data-ttu-id="187ad-166">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-166">False</span></span>                           |
| <span data-ttu-id="187ad-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-167">In Global Catalog</span></span>      | <span data-ttu-id="187ad-168">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-168">False</span></span>                           |
| <span data-ttu-id="187ad-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-173">Search-Flags</span></span>           | <span data-ttu-id="187ad-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-174">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-175">System-Flags</span></span>           | <span data-ttu-id="187ad-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-176">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-177">Classes used in</span></span>        | [<span data-ttu-id="187ad-178">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="187ad-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="187ad-179">ADAM</span></span>



| <span data-ttu-id="187ad-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-180">Entry</span></span> | <span data-ttu-id="187ad-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-184">System-Only</span></span>            | <span data-ttu-id="187ad-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-185">True</span></span>                            |
| <span data-ttu-id="187ad-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-186">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-187">True</span></span>                            |
| <span data-ttu-id="187ad-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-188">Is Indexed</span></span>             | <span data-ttu-id="187ad-189">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-189">False</span></span>                           |
| <span data-ttu-id="187ad-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-190">In Global Catalog</span></span>      | <span data-ttu-id="187ad-191">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-191">False</span></span>                           |
| <span data-ttu-id="187ad-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-196">Search-Flags</span></span>           | <span data-ttu-id="187ad-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-197">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-198">System-Flags</span></span>           | <span data-ttu-id="187ad-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-199">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-200">Classes used in</span></span>        | [<span data-ttu-id="187ad-201">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="187ad-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="187ad-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="187ad-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-203">Entry</span></span> | <span data-ttu-id="187ad-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-207">System-Only</span></span>            | <span data-ttu-id="187ad-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-208">True</span></span>                            |
| <span data-ttu-id="187ad-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-209">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-210">True</span></span>                            |
| <span data-ttu-id="187ad-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-211">Is Indexed</span></span>             | <span data-ttu-id="187ad-212">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-212">False</span></span>                           |
| <span data-ttu-id="187ad-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-213">In Global Catalog</span></span>      | <span data-ttu-id="187ad-214">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-214">False</span></span>                           |
| <span data-ttu-id="187ad-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-219">Search-Flags</span></span>           | <span data-ttu-id="187ad-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-220">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-221">System-Flags</span></span>           | <span data-ttu-id="187ad-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-222">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-223">Classes used in</span></span>        | [<span data-ttu-id="187ad-224">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="187ad-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="187ad-225">Windows Server 2008</span></span>



| <span data-ttu-id="187ad-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-226">Entry</span></span> | <span data-ttu-id="187ad-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-230">System-Only</span></span>            | <span data-ttu-id="187ad-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-231">True</span></span>                            |
| <span data-ttu-id="187ad-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-232">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-233">True</span></span>                            |
| <span data-ttu-id="187ad-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-234">Is Indexed</span></span>             | <span data-ttu-id="187ad-235">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-235">False</span></span>                           |
| <span data-ttu-id="187ad-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-236">In Global Catalog</span></span>      | <span data-ttu-id="187ad-237">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-237">False</span></span>                           |
| <span data-ttu-id="187ad-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-242">Search-Flags</span></span>           | <span data-ttu-id="187ad-243">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-243">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-244">System-Flags</span></span>           | <span data-ttu-id="187ad-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-245">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-246">Classes used in</span></span>        | [<span data-ttu-id="187ad-247">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="187ad-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="187ad-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="187ad-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-249">Entry</span></span> | <span data-ttu-id="187ad-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-253">System-Only</span></span>            | <span data-ttu-id="187ad-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-254">True</span></span>                            |
| <span data-ttu-id="187ad-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-255">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-256">True</span></span>                            |
| <span data-ttu-id="187ad-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-257">Is Indexed</span></span>             | <span data-ttu-id="187ad-258">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-258">False</span></span>                           |
| <span data-ttu-id="187ad-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-259">In Global Catalog</span></span>      | <span data-ttu-id="187ad-260">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-260">False</span></span>                           |
| <span data-ttu-id="187ad-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-265">Search-Flags</span></span>           | <span data-ttu-id="187ad-266">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-266">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-267">System-Flags</span></span>           | <span data-ttu-id="187ad-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-268">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-269">Classes used in</span></span>        | [<span data-ttu-id="187ad-270">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="187ad-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="187ad-271">Windows Server 2012</span></span>



| <span data-ttu-id="187ad-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="187ad-272">Entry</span></span> | <span data-ttu-id="187ad-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="187ad-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="187ad-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187ad-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="187ad-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="187ad-276">System-Only</span></span>            | <span data-ttu-id="187ad-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-277">True</span></span>                            |
| <span data-ttu-id="187ad-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="187ad-278">Is-Single-Valued</span></span>       | <span data-ttu-id="187ad-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="187ad-279">True</span></span>                            |
| <span data-ttu-id="187ad-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="187ad-280">Is Indexed</span></span>             | <span data-ttu-id="187ad-281">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-281">False</span></span>                           |
| <span data-ttu-id="187ad-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="187ad-282">In Global Catalog</span></span>      | <span data-ttu-id="187ad-283">Faux</span><span class="sxs-lookup"><span data-stu-id="187ad-283">False</span></span>                           |
| <span data-ttu-id="187ad-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="187ad-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="187ad-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="187ad-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="187ad-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187ad-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="187ad-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187ad-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="187ad-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-288">Search-Flags</span></span>           | <span data-ttu-id="187ad-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="187ad-289">0x00000008</span></span>                      |
| <span data-ttu-id="187ad-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187ad-290">System-Flags</span></span>           | <span data-ttu-id="187ad-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187ad-291">0x00000010</span></span>                      |
| <span data-ttu-id="187ad-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="187ad-292">Classes used in</span></span>        | [<span data-ttu-id="187ad-293">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="187ad-293">**Top**</span></span>](c-top.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="187ad-294">Notes</span><span class="sxs-lookup"><span data-stu-id="187ad-294">Remarks</span></span>

<span data-ttu-id="187ad-295">Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="187ad-295">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="187ad-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="187ad-296">Value</span></span>                   | <span data-ttu-id="187ad-297">Description</span><span class="sxs-lookup"><span data-stu-id="187ad-297">Description</span></span>                                                                                                                                                                                                                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187ad-298">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="187ad-298">1 (0x00000001)</span></span>          | <span data-ttu-id="187ad-299">Lorsqu’il est appliqué à un attribut, l’attribut n’est pas répliqué. Lorsqu’il est appliqué à un objet [**Cross-Ref**](c-crossref.md) , le contexte d’appellation est dans NTDS.</span><span class="sxs-lookup"><span data-stu-id="187ad-299">When applied to an attribute, the attribute will not be replicated.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is in NTDS.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="187ad-300">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="187ad-300">2 (0x00000002)</span></span>          | <span data-ttu-id="187ad-301">Lorsqu’il est appliqué à un attribut, l’attribut est répliqué dans le catalogue global. Lorsqu’il est appliqué à un objet [**Cross-Ref**](c-crossref.md) , le contexte d’appellation est un domaine.</span><span class="sxs-lookup"><span data-stu-id="187ad-301">When applied to an attribute, the attribute will be replicated to the global catalog.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is a domain.</span></span><br/>                                                                                                       |
| <span data-ttu-id="187ad-302">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="187ad-302">4 (0x00000004)</span></span>          | <span data-ttu-id="187ad-303">Lorsqu’il est appliqué à un attribut, l’attribut est construit.</span><span class="sxs-lookup"><span data-stu-id="187ad-303">When applied to an attribute, the attribute is constructed.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="187ad-304">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="187ad-304">16 (0x00000010)</span></span>         | <span data-ttu-id="187ad-305">Lorsqu’il est défini, indique que l’objet est un objet de catégorie 1.</span><span class="sxs-lookup"><span data-stu-id="187ad-305">When set, indicates the object is a category 1 object.</span></span> <span data-ttu-id="187ad-306">Un objet catégorie 1 est une classe ou un attribut inclus dans le schéma de base inclus dans le système.</span><span class="sxs-lookup"><span data-stu-id="187ad-306">A category 1 object is a class or attribute that is included in the base schema included with the system.</span></span>                                                                                                                                |
| <span data-ttu-id="187ad-307">33554432 (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-307">33554432 (0x02000000)</span></span>   | <span data-ttu-id="187ad-308">L’objet n’est pas déplacé vers le conteneur objets supprimés lorsqu’il est supprimé.</span><span class="sxs-lookup"><span data-stu-id="187ad-308">The object is not moved to the Deleted Objects container when it is deleted.</span></span> <span data-ttu-id="187ad-309">Elle sera supprimée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="187ad-309">It will be deleted immediately.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="187ad-310">67108864 (0x04000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-310">67108864 (0x04000000)</span></span>   | <span data-ttu-id="187ad-311">L’objet ne peut pas être déplacé.</span><span class="sxs-lookup"><span data-stu-id="187ad-311">The object cannot be moved.</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="187ad-312">134217728 (0x08000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-312">134217728 (0x08000000)</span></span>  | <span data-ttu-id="187ad-313">L’objet ne peut pas être renommé.</span><span class="sxs-lookup"><span data-stu-id="187ad-313">The object cannot be renamed.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="187ad-314">268435456 (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-314">268435456 (0x10000000)</span></span>  | <span data-ttu-id="187ad-315">Pour les objets de la partition de configuration, si cet indicateur est défini, l’objet peut être déplacé avec des restrictions ; dans le cas contraire, l’objet ne peut pas être déplacé.</span><span class="sxs-lookup"><span data-stu-id="187ad-315">For objects in the configuration partition, if this flag is set, the object can be moved with restrictions; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="187ad-316">Par défaut, cet indicateur n’est pas défini sur les nouveaux objets créés sous la partition de configuration.</span><span class="sxs-lookup"><span data-stu-id="187ad-316">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="187ad-317">Cet indicateur ne peut être défini qu’au moment de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="187ad-317">This flag can only be set during object creation.</span></span> |
| <span data-ttu-id="187ad-318">536870912 (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-318">536870912 (0x20000000)</span></span>  | <span data-ttu-id="187ad-319">Pour les objets de la partition de configuration, si cet indicateur est défini, l’objet peut être déplacé. dans le cas contraire, l’objet ne peut pas être déplacé.</span><span class="sxs-lookup"><span data-stu-id="187ad-319">For objects in the configuration partition, if this flag is set, the object can be moved; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="187ad-320">Par défaut, cet indicateur n’est pas défini sur les nouveaux objets créés sous la partition de configuration.</span><span class="sxs-lookup"><span data-stu-id="187ad-320">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="187ad-321">Cet indicateur ne peut être défini qu’au moment de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="187ad-321">This flag can only be set during object creation.</span></span>                   |
| <span data-ttu-id="187ad-322">1073741824 (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-322">1073741824 (0x40000000)</span></span> | <span data-ttu-id="187ad-323">Pour les objets de la partition de configuration, si cet indicateur est défini, l’objet peut être renommé ; dans le cas contraire, l’objet ne peut pas être renommé.</span><span class="sxs-lookup"><span data-stu-id="187ad-323">For objects in the configuration partition, if this flag is set, the object can be renamed; otherwise, the object cannot be renamed.</span></span> <span data-ttu-id="187ad-324">Par défaut, cet indicateur n’est pas défini sur les nouveaux objets créés sous la partition de configuration.</span><span class="sxs-lookup"><span data-stu-id="187ad-324">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="187ad-325">Cet indicateur ne peut être défini qu’au moment de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="187ad-325">This flag can only be set during object creation.</span></span>               |
| <span data-ttu-id="187ad-326">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="187ad-326">2147483648 (0x80000000)</span></span> | <span data-ttu-id="187ad-327">Impossible de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="187ad-327">The object cannot be deleted.</span></span>                                                                                                                                                                                                                                                                   |



 

 

 





