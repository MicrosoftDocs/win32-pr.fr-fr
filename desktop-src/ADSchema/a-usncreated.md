---
title: Attribut USN-Created
description: Numéro de séquence de mise à jour (USN) affecté lors de la création de l’objet. Voir aussi USN-changed.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut USN-Created
- Schéma AD de l’attribut uSNCreated
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106511991"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="7836a-106">Attribut USN-Created</span><span class="sxs-lookup"><span data-stu-id="7836a-106">USN-Created attribute</span></span>

<span data-ttu-id="7836a-107">Numéro de séquence de mise à jour (USN) affecté lors de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7836a-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="7836a-108">Voir aussi [**USN-Changed**](a-usnchanged.md).</span><span class="sxs-lookup"><span data-stu-id="7836a-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="7836a-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-109">Entry</span></span> | <span data-ttu-id="7836a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7836a-111">CN</span><span class="sxs-lookup"><span data-stu-id="7836a-111">CN</span></span>                | <span data-ttu-id="7836a-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="7836a-112">USN-Created</span></span>                          |
| <span data-ttu-id="7836a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7836a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7836a-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="7836a-114">uSNCreated</span></span>                           |
| <span data-ttu-id="7836a-115">Taille</span><span class="sxs-lookup"><span data-stu-id="7836a-115">Size</span></span>              | <span data-ttu-id="7836a-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="7836a-116">8 bytes</span></span>                              |
| <span data-ttu-id="7836a-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7836a-117">Update Privilege</span></span>  | <span data-ttu-id="7836a-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="7836a-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="7836a-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7836a-119">Update Frequency</span></span>  | <span data-ttu-id="7836a-120">Lorsque l’objet est créé.</span><span class="sxs-lookup"><span data-stu-id="7836a-120">When the object is created.</span></span>          |
| <span data-ttu-id="7836a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-121">Attribute-Id</span></span>      | <span data-ttu-id="7836a-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="7836a-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="7836a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7836a-123">System-Id-Guid</span></span>    | <span data-ttu-id="7836a-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7836a-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7836a-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7836a-125">Syntax</span></span>            | [<span data-ttu-id="7836a-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="7836a-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7836a-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7836a-127">Implementations</span></span>

-   [<span data-ttu-id="7836a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7836a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7836a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7836a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7836a-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7836a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7836a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7836a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7836a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7836a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7836a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7836a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7836a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7836a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7836a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7836a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="7836a-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-136">Entry</span></span> | <span data-ttu-id="7836a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-139">MAPI-Id</span></span>                | <span data-ttu-id="7836a-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-140">0x8154</span></span>                          |
| <span data-ttu-id="7836a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-141">System-Only</span></span>            | <span data-ttu-id="7836a-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-142">True</span></span>                            |
| <span data-ttu-id="7836a-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-144">True</span></span>                            |
| <span data-ttu-id="7836a-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-145">Is Indexed</span></span>             | <span data-ttu-id="7836a-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-146">True</span></span>                            |
| <span data-ttu-id="7836a-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-147">In Global Catalog</span></span>      | <span data-ttu-id="7836a-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-148">True</span></span>                            |
| <span data-ttu-id="7836a-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-153">Search-Flags</span></span>           | <span data-ttu-id="7836a-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-154">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-155">System-Flags</span></span>           | <span data-ttu-id="7836a-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-156">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-157">Classes used in</span></span>        | [<span data-ttu-id="7836a-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7836a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7836a-159">Windows Server 2003</span></span>



| <span data-ttu-id="7836a-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-160">Entry</span></span> | <span data-ttu-id="7836a-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-163">MAPI-Id</span></span>                | <span data-ttu-id="7836a-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-164">0x8154</span></span>                          |
| <span data-ttu-id="7836a-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-165">System-Only</span></span>            | <span data-ttu-id="7836a-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-166">True</span></span>                            |
| <span data-ttu-id="7836a-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-167">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-168">True</span></span>                            |
| <span data-ttu-id="7836a-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-169">Is Indexed</span></span>             | <span data-ttu-id="7836a-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-170">True</span></span>                            |
| <span data-ttu-id="7836a-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-171">In Global Catalog</span></span>      | <span data-ttu-id="7836a-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-172">True</span></span>                            |
| <span data-ttu-id="7836a-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-177">Search-Flags</span></span>           | <span data-ttu-id="7836a-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-178">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-179">System-Flags</span></span>           | <span data-ttu-id="7836a-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-180">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-181">Classes used in</span></span>        | [<span data-ttu-id="7836a-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7836a-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="7836a-183">ADAM</span></span>



| <span data-ttu-id="7836a-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-184">Entry</span></span> | <span data-ttu-id="7836a-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-187">MAPI-Id</span></span>                | <span data-ttu-id="7836a-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-188">0x8154</span></span>                          |
| <span data-ttu-id="7836a-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-189">System-Only</span></span>            | <span data-ttu-id="7836a-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-190">True</span></span>                            |
| <span data-ttu-id="7836a-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-191">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-192">True</span></span>                            |
| <span data-ttu-id="7836a-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-193">Is Indexed</span></span>             | <span data-ttu-id="7836a-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-194">True</span></span>                            |
| <span data-ttu-id="7836a-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-195">In Global Catalog</span></span>      | <span data-ttu-id="7836a-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-196">True</span></span>                            |
| <span data-ttu-id="7836a-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-201">Search-Flags</span></span>           | <span data-ttu-id="7836a-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-202">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-203">System-Flags</span></span>           | <span data-ttu-id="7836a-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-204">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-205">Classes used in</span></span>        | [<span data-ttu-id="7836a-206">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7836a-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7836a-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7836a-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-208">Entry</span></span> | <span data-ttu-id="7836a-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-211">MAPI-Id</span></span>                | <span data-ttu-id="7836a-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-212">0x8154</span></span>                          |
| <span data-ttu-id="7836a-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-213">System-Only</span></span>            | <span data-ttu-id="7836a-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-214">True</span></span>                            |
| <span data-ttu-id="7836a-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-215">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-216">True</span></span>                            |
| <span data-ttu-id="7836a-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-217">Is Indexed</span></span>             | <span data-ttu-id="7836a-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-218">True</span></span>                            |
| <span data-ttu-id="7836a-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-219">In Global Catalog</span></span>      | <span data-ttu-id="7836a-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-220">True</span></span>                            |
| <span data-ttu-id="7836a-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-225">Search-Flags</span></span>           | <span data-ttu-id="7836a-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-226">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-227">System-Flags</span></span>           | <span data-ttu-id="7836a-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-228">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-229">Classes used in</span></span>        | [<span data-ttu-id="7836a-230">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7836a-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7836a-231">Windows Server 2008</span></span>



| <span data-ttu-id="7836a-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-232">Entry</span></span> | <span data-ttu-id="7836a-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-235">MAPI-Id</span></span>                | <span data-ttu-id="7836a-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-236">0x8154</span></span>                          |
| <span data-ttu-id="7836a-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-237">System-Only</span></span>            | <span data-ttu-id="7836a-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-238">True</span></span>                            |
| <span data-ttu-id="7836a-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-239">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-240">True</span></span>                            |
| <span data-ttu-id="7836a-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-241">Is Indexed</span></span>             | <span data-ttu-id="7836a-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-242">True</span></span>                            |
| <span data-ttu-id="7836a-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-243">In Global Catalog</span></span>      | <span data-ttu-id="7836a-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-244">True</span></span>                            |
| <span data-ttu-id="7836a-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-249">Search-Flags</span></span>           | <span data-ttu-id="7836a-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-250">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-251">System-Flags</span></span>           | <span data-ttu-id="7836a-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-252">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-253">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-253">Classes used in</span></span>        | [<span data-ttu-id="7836a-254">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7836a-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7836a-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7836a-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-256">Entry</span></span> | <span data-ttu-id="7836a-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-258">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-259">MAPI-Id</span></span>                | <span data-ttu-id="7836a-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-260">0x8154</span></span>                          |
| <span data-ttu-id="7836a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-261">System-Only</span></span>            | <span data-ttu-id="7836a-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-262">True</span></span>                            |
| <span data-ttu-id="7836a-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-264">True</span></span>                            |
| <span data-ttu-id="7836a-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-265">Is Indexed</span></span>             | <span data-ttu-id="7836a-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-266">True</span></span>                            |
| <span data-ttu-id="7836a-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-267">In Global Catalog</span></span>      | <span data-ttu-id="7836a-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-268">True</span></span>                            |
| <span data-ttu-id="7836a-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-273">Search-Flags</span></span>           | <span data-ttu-id="7836a-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-274">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-275">System-Flags</span></span>           | <span data-ttu-id="7836a-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-276">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-277">Classes used in</span></span>        | [<span data-ttu-id="7836a-278">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7836a-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7836a-279">Windows Server 2012</span></span>



| <span data-ttu-id="7836a-280">Entrée</span><span class="sxs-lookup"><span data-stu-id="7836a-280">Entry</span></span> | <span data-ttu-id="7836a-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="7836a-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7836a-282">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7836a-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7836a-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7836a-283">MAPI-Id</span></span>                | <span data-ttu-id="7836a-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="7836a-284">0x8154</span></span>                          |
| <span data-ttu-id="7836a-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="7836a-285">System-Only</span></span>            | <span data-ttu-id="7836a-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-286">True</span></span>                            |
| <span data-ttu-id="7836a-287">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7836a-287">Is-Single-Valued</span></span>       | <span data-ttu-id="7836a-288">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-288">True</span></span>                            |
| <span data-ttu-id="7836a-289">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7836a-289">Is Indexed</span></span>             | <span data-ttu-id="7836a-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-290">True</span></span>                            |
| <span data-ttu-id="7836a-291">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7836a-291">In Global Catalog</span></span>      | <span data-ttu-id="7836a-292">Vrai</span><span class="sxs-lookup"><span data-stu-id="7836a-292">True</span></span>                            |
| <span data-ttu-id="7836a-293">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7836a-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="7836a-294">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7836a-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7836a-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7836a-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7836a-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7836a-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7836a-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-297">Search-Flags</span></span>           | <span data-ttu-id="7836a-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7836a-298">0x00000009</span></span>                      |
| <span data-ttu-id="7836a-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7836a-299">System-Flags</span></span>           | <span data-ttu-id="7836a-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7836a-300">0x00000013</span></span>                      |
| <span data-ttu-id="7836a-301">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7836a-301">Classes used in</span></span>        | [<span data-ttu-id="7836a-302">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7836a-302">**Top**</span></span>](c-top.md)<br/> |



 

 





