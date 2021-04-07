---
title: Attribut When-Changed
description: Date à laquelle cet objet a été modifié pour la dernière fois. Cette valeur n’est pas répliquée et existe dans le catalogue global.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut When-Changed
- Schéma AD attribut whenChanged
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844538"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="1156f-106">Attribut When-Changed</span><span class="sxs-lookup"><span data-stu-id="1156f-106">When-Changed attribute</span></span>

<span data-ttu-id="1156f-107">Date à laquelle cet objet a été modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="1156f-107">The date when this object was last changed.</span></span> <span data-ttu-id="1156f-108">Cette valeur n’est pas répliquée et existe dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="1156f-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="1156f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-109">Entry</span></span> | <span data-ttu-id="1156f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="1156f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1156f-111">CN</span></span>                | <span data-ttu-id="1156f-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="1156f-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="1156f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1156f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1156f-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="1156f-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="1156f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="1156f-115">Size</span></span>              | <span data-ttu-id="1156f-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="1156f-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="1156f-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="1156f-117">Update Privilege</span></span>  | <span data-ttu-id="1156f-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="1156f-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="1156f-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="1156f-119">Update Frequency</span></span>  | <span data-ttu-id="1156f-120">Chaque fois que l’objet est modifié.</span><span class="sxs-lookup"><span data-stu-id="1156f-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="1156f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-121">Attribute-Id</span></span>      | <span data-ttu-id="1156f-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="1156f-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="1156f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1156f-123">System-Id-Guid</span></span>    | <span data-ttu-id="1156f-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1156f-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="1156f-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1156f-125">Syntax</span></span>            | [<span data-ttu-id="1156f-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="1156f-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="1156f-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="1156f-127">Implementations</span></span>

-   [<span data-ttu-id="1156f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1156f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1156f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1156f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1156f-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1156f-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1156f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1156f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1156f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1156f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1156f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1156f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1156f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1156f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1156f-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1156f-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1156f-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-136">Entry</span></span> | <span data-ttu-id="1156f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-139">MAPI-Id</span></span>                | <span data-ttu-id="1156f-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-140">0x3008</span></span>                          |
| <span data-ttu-id="1156f-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-141">System-Only</span></span>            | <span data-ttu-id="1156f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-142">True</span></span>                            |
| <span data-ttu-id="1156f-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-144">True</span></span>                            |
| <span data-ttu-id="1156f-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-145">Is Indexed</span></span>             | <span data-ttu-id="1156f-146">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-146">False</span></span>                           |
| <span data-ttu-id="1156f-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-147">In Global Catalog</span></span>      | <span data-ttu-id="1156f-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-148">True</span></span>                            |
| <span data-ttu-id="1156f-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-153">Search-Flags</span></span>           | <span data-ttu-id="1156f-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-154">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-155">System-Flags</span></span>           | <span data-ttu-id="1156f-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-156">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-157">Classes used in</span></span>        | [<span data-ttu-id="1156f-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1156f-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1156f-159">Windows Server 2003</span></span>



| <span data-ttu-id="1156f-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-160">Entry</span></span> | <span data-ttu-id="1156f-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-163">MAPI-Id</span></span>                | <span data-ttu-id="1156f-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-164">0x3008</span></span>                          |
| <span data-ttu-id="1156f-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-165">System-Only</span></span>            | <span data-ttu-id="1156f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-166">True</span></span>                            |
| <span data-ttu-id="1156f-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-168">True</span></span>                            |
| <span data-ttu-id="1156f-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-169">Is Indexed</span></span>             | <span data-ttu-id="1156f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-170">False</span></span>                           |
| <span data-ttu-id="1156f-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-171">In Global Catalog</span></span>      | <span data-ttu-id="1156f-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-172">True</span></span>                            |
| <span data-ttu-id="1156f-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-177">Search-Flags</span></span>           | <span data-ttu-id="1156f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-178">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-179">System-Flags</span></span>           | <span data-ttu-id="1156f-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-180">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-181">Classes used in</span></span>        | [<span data-ttu-id="1156f-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1156f-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="1156f-183">ADAM</span></span>



| <span data-ttu-id="1156f-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-184">Entry</span></span> | <span data-ttu-id="1156f-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-187">MAPI-Id</span></span>                | <span data-ttu-id="1156f-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-188">0x3008</span></span>                          |
| <span data-ttu-id="1156f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-189">System-Only</span></span>            | <span data-ttu-id="1156f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-190">True</span></span>                            |
| <span data-ttu-id="1156f-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-192">True</span></span>                            |
| <span data-ttu-id="1156f-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-193">Is Indexed</span></span>             | <span data-ttu-id="1156f-194">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-194">False</span></span>                           |
| <span data-ttu-id="1156f-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-195">In Global Catalog</span></span>      | <span data-ttu-id="1156f-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-196">True</span></span>                            |
| <span data-ttu-id="1156f-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-201">Search-Flags</span></span>           | <span data-ttu-id="1156f-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-202">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-203">System-Flags</span></span>           | <span data-ttu-id="1156f-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-204">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-205">Classes used in</span></span>        | [<span data-ttu-id="1156f-206">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1156f-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1156f-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1156f-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-208">Entry</span></span> | <span data-ttu-id="1156f-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-211">MAPI-Id</span></span>                | <span data-ttu-id="1156f-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-212">0x3008</span></span>                          |
| <span data-ttu-id="1156f-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-213">System-Only</span></span>            | <span data-ttu-id="1156f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-214">True</span></span>                            |
| <span data-ttu-id="1156f-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-215">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-216">True</span></span>                            |
| <span data-ttu-id="1156f-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-217">Is Indexed</span></span>             | <span data-ttu-id="1156f-218">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-218">False</span></span>                           |
| <span data-ttu-id="1156f-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-219">In Global Catalog</span></span>      | <span data-ttu-id="1156f-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-220">True</span></span>                            |
| <span data-ttu-id="1156f-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-225">Search-Flags</span></span>           | <span data-ttu-id="1156f-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-226">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-227">System-Flags</span></span>           | <span data-ttu-id="1156f-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-228">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-229">Classes used in</span></span>        | [<span data-ttu-id="1156f-230">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1156f-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1156f-231">Windows Server 2008</span></span>



| <span data-ttu-id="1156f-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-232">Entry</span></span> | <span data-ttu-id="1156f-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-235">MAPI-Id</span></span>                | <span data-ttu-id="1156f-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-236">0x3008</span></span>                          |
| <span data-ttu-id="1156f-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-237">System-Only</span></span>            | <span data-ttu-id="1156f-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-238">True</span></span>                            |
| <span data-ttu-id="1156f-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-239">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-240">True</span></span>                            |
| <span data-ttu-id="1156f-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-241">Is Indexed</span></span>             | <span data-ttu-id="1156f-242">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-242">False</span></span>                           |
| <span data-ttu-id="1156f-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-243">In Global Catalog</span></span>      | <span data-ttu-id="1156f-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-244">True</span></span>                            |
| <span data-ttu-id="1156f-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-249">Search-Flags</span></span>           | <span data-ttu-id="1156f-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-250">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-251">System-Flags</span></span>           | <span data-ttu-id="1156f-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-252">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-253">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-253">Classes used in</span></span>        | [<span data-ttu-id="1156f-254">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1156f-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1156f-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1156f-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-256">Entry</span></span> | <span data-ttu-id="1156f-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-258">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-259">MAPI-Id</span></span>                | <span data-ttu-id="1156f-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-260">0x3008</span></span>                          |
| <span data-ttu-id="1156f-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-261">System-Only</span></span>            | <span data-ttu-id="1156f-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-262">True</span></span>                            |
| <span data-ttu-id="1156f-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-263">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-264">True</span></span>                            |
| <span data-ttu-id="1156f-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-265">Is Indexed</span></span>             | <span data-ttu-id="1156f-266">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-266">False</span></span>                           |
| <span data-ttu-id="1156f-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-267">In Global Catalog</span></span>      | <span data-ttu-id="1156f-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-268">True</span></span>                            |
| <span data-ttu-id="1156f-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-273">Search-Flags</span></span>           | <span data-ttu-id="1156f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-274">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-275">System-Flags</span></span>           | <span data-ttu-id="1156f-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-276">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-277">Classes used in</span></span>        | [<span data-ttu-id="1156f-278">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1156f-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1156f-279">Windows Server 2012</span></span>



| <span data-ttu-id="1156f-280">Entrée</span><span class="sxs-lookup"><span data-stu-id="1156f-280">Entry</span></span> | <span data-ttu-id="1156f-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="1156f-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1156f-282">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1156f-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1156f-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1156f-283">MAPI-Id</span></span>                | <span data-ttu-id="1156f-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="1156f-284">0x3008</span></span>                          |
| <span data-ttu-id="1156f-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="1156f-285">System-Only</span></span>            | <span data-ttu-id="1156f-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-286">True</span></span>                            |
| <span data-ttu-id="1156f-287">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1156f-287">Is-Single-Valued</span></span>       | <span data-ttu-id="1156f-288">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-288">True</span></span>                            |
| <span data-ttu-id="1156f-289">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1156f-289">Is Indexed</span></span>             | <span data-ttu-id="1156f-290">Faux</span><span class="sxs-lookup"><span data-stu-id="1156f-290">False</span></span>                           |
| <span data-ttu-id="1156f-291">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1156f-291">In Global Catalog</span></span>      | <span data-ttu-id="1156f-292">Vrai</span><span class="sxs-lookup"><span data-stu-id="1156f-292">True</span></span>                            |
| <span data-ttu-id="1156f-293">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1156f-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="1156f-294">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1156f-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1156f-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1156f-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1156f-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1156f-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1156f-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-297">Search-Flags</span></span>           | <span data-ttu-id="1156f-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1156f-298">0x00000000</span></span>                      |
| <span data-ttu-id="1156f-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1156f-299">System-Flags</span></span>           | <span data-ttu-id="1156f-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1156f-300">0x00000013</span></span>                      |
| <span data-ttu-id="1156f-301">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1156f-301">Classes used in</span></span>        | [<span data-ttu-id="1156f-302">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="1156f-302">**Top**</span></span>](c-top.md)<br/> |



 

 





