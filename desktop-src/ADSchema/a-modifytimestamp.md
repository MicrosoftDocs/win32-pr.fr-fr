---
title: Attribut de date et d’heure de modification
description: Attribut calculé qui représente la date de la dernière modification de cet objet. Cette valeur n’est pas répliquée.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de modification d’horodatage
- Schéma AD de l’attribut modifyTimeStamp
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744340"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="def18-106">Attribut de date et d’heure de modification</span><span class="sxs-lookup"><span data-stu-id="def18-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="def18-107">Attribut calculé qui représente la date de la dernière modification de cet objet.</span><span class="sxs-lookup"><span data-stu-id="def18-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="def18-108">Cette valeur n’est pas répliquée.</span><span class="sxs-lookup"><span data-stu-id="def18-108">This value is not replicated.</span></span>



| <span data-ttu-id="def18-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-109">Entry</span></span> | <span data-ttu-id="def18-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="def18-111">CN</span><span class="sxs-lookup"><span data-stu-id="def18-111">CN</span></span>                | <span data-ttu-id="def18-112">Date et heure de modification</span><span class="sxs-lookup"><span data-stu-id="def18-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="def18-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="def18-113">Ldap-Display-Name</span></span> | <span data-ttu-id="def18-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="def18-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="def18-115">Taille</span><span class="sxs-lookup"><span data-stu-id="def18-115">Size</span></span>              | <span data-ttu-id="def18-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="def18-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="def18-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="def18-117">Update Privilege</span></span>  | <span data-ttu-id="def18-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="def18-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="def18-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="def18-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="def18-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="def18-120">Attribute-Id</span></span>      | <span data-ttu-id="def18-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="def18-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="def18-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="def18-122">System-Id-Guid</span></span>    | <span data-ttu-id="def18-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="def18-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="def18-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="def18-124">Syntax</span></span>            | [<span data-ttu-id="def18-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="def18-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="def18-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="def18-126">Implementations</span></span>

-   [<span data-ttu-id="def18-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="def18-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="def18-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="def18-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="def18-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="def18-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="def18-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="def18-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="def18-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="def18-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="def18-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="def18-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="def18-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="def18-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="def18-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="def18-134">Windows 2000 Server</span></span>



| <span data-ttu-id="def18-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-135">Entry</span></span> | <span data-ttu-id="def18-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-139">System-Only</span></span>            | <span data-ttu-id="def18-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-140">True</span></span>                                                                        |
| <span data-ttu-id="def18-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-141">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-142">True</span></span>                                                                        |
| <span data-ttu-id="def18-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-143">Is Indexed</span></span>             | <span data-ttu-id="def18-144">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-144">False</span></span>                                                                       |
| <span data-ttu-id="def18-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-145">In Global Catalog</span></span>      | <span data-ttu-id="def18-146">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-146">False</span></span>                                                                       |
| <span data-ttu-id="def18-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-151">Search-Flags</span></span>           | <span data-ttu-id="def18-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-153">System-Flags</span></span>           | <span data-ttu-id="def18-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-155">Classes used in</span></span>        | [<span data-ttu-id="def18-156">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-157">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="def18-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="def18-158">Windows Server 2003</span></span>



| <span data-ttu-id="def18-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-159">Entry</span></span> | <span data-ttu-id="def18-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-163">System-Only</span></span>            | <span data-ttu-id="def18-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-164">True</span></span>                                                                        |
| <span data-ttu-id="def18-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-165">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-166">True</span></span>                                                                        |
| <span data-ttu-id="def18-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-167">Is Indexed</span></span>             | <span data-ttu-id="def18-168">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-168">False</span></span>                                                                       |
| <span data-ttu-id="def18-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-169">In Global Catalog</span></span>      | <span data-ttu-id="def18-170">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-170">False</span></span>                                                                       |
| <span data-ttu-id="def18-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-175">Search-Flags</span></span>           | <span data-ttu-id="def18-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-177">System-Flags</span></span>           | <span data-ttu-id="def18-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-179">Classes used in</span></span>        | [<span data-ttu-id="def18-180">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="def18-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="def18-182">ADAM</span></span>



| <span data-ttu-id="def18-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-183">Entry</span></span> | <span data-ttu-id="def18-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-187">System-Only</span></span>            | <span data-ttu-id="def18-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-188">True</span></span>                                                                        |
| <span data-ttu-id="def18-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-189">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-190">True</span></span>                                                                        |
| <span data-ttu-id="def18-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-191">Is Indexed</span></span>             | <span data-ttu-id="def18-192">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-192">False</span></span>                                                                       |
| <span data-ttu-id="def18-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-193">In Global Catalog</span></span>      | <span data-ttu-id="def18-194">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-194">False</span></span>                                                                       |
| <span data-ttu-id="def18-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-199">Search-Flags</span></span>           | <span data-ttu-id="def18-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-201">System-Flags</span></span>           | <span data-ttu-id="def18-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-203">Classes used in</span></span>        | [<span data-ttu-id="def18-204">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-205">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="def18-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="def18-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="def18-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-207">Entry</span></span> | <span data-ttu-id="def18-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-211">System-Only</span></span>            | <span data-ttu-id="def18-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-212">True</span></span>                                                                        |
| <span data-ttu-id="def18-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-213">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-214">True</span></span>                                                                        |
| <span data-ttu-id="def18-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-215">Is Indexed</span></span>             | <span data-ttu-id="def18-216">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-216">False</span></span>                                                                       |
| <span data-ttu-id="def18-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-217">In Global Catalog</span></span>      | <span data-ttu-id="def18-218">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-218">False</span></span>                                                                       |
| <span data-ttu-id="def18-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-223">Search-Flags</span></span>           | <span data-ttu-id="def18-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-225">System-Flags</span></span>           | <span data-ttu-id="def18-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-227">Classes used in</span></span>        | [<span data-ttu-id="def18-228">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-229">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="def18-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="def18-230">Windows Server 2008</span></span>



| <span data-ttu-id="def18-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-231">Entry</span></span> | <span data-ttu-id="def18-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-235">System-Only</span></span>            | <span data-ttu-id="def18-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-236">True</span></span>                                                                        |
| <span data-ttu-id="def18-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-237">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-238">True</span></span>                                                                        |
| <span data-ttu-id="def18-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-239">Is Indexed</span></span>             | <span data-ttu-id="def18-240">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-240">False</span></span>                                                                       |
| <span data-ttu-id="def18-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-241">In Global Catalog</span></span>      | <span data-ttu-id="def18-242">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-242">False</span></span>                                                                       |
| <span data-ttu-id="def18-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-247">Search-Flags</span></span>           | <span data-ttu-id="def18-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-249">System-Flags</span></span>           | <span data-ttu-id="def18-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-251">Classes used in</span></span>        | [<span data-ttu-id="def18-252">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-253">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="def18-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="def18-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="def18-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-255">Entry</span></span> | <span data-ttu-id="def18-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-259">System-Only</span></span>            | <span data-ttu-id="def18-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-260">True</span></span>                                                                        |
| <span data-ttu-id="def18-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-261">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-262">True</span></span>                                                                        |
| <span data-ttu-id="def18-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-263">Is Indexed</span></span>             | <span data-ttu-id="def18-264">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-264">False</span></span>                                                                       |
| <span data-ttu-id="def18-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-265">In Global Catalog</span></span>      | <span data-ttu-id="def18-266">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-266">False</span></span>                                                                       |
| <span data-ttu-id="def18-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-271">Search-Flags</span></span>           | <span data-ttu-id="def18-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-273">System-Flags</span></span>           | <span data-ttu-id="def18-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-275">Classes used in</span></span>        | [<span data-ttu-id="def18-276">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-277">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="def18-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="def18-278">Windows Server 2012</span></span>



| <span data-ttu-id="def18-279">Entrée</span><span class="sxs-lookup"><span data-stu-id="def18-279">Entry</span></span> | <span data-ttu-id="def18-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="def18-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="def18-281">ID de lien</span><span class="sxs-lookup"><span data-stu-id="def18-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def18-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="def18-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="def18-283">System-Only</span></span>            | <span data-ttu-id="def18-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-284">True</span></span>                                                                        |
| <span data-ttu-id="def18-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="def18-285">Is-Single-Valued</span></span>       | <span data-ttu-id="def18-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="def18-286">True</span></span>                                                                        |
| <span data-ttu-id="def18-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="def18-287">Is Indexed</span></span>             | <span data-ttu-id="def18-288">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-288">False</span></span>                                                                       |
| <span data-ttu-id="def18-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="def18-289">In Global Catalog</span></span>      | <span data-ttu-id="def18-290">Faux</span><span class="sxs-lookup"><span data-stu-id="def18-290">False</span></span>                                                                       |
| <span data-ttu-id="def18-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="def18-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="def18-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="def18-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="def18-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def18-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def18-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="def18-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-295">Search-Flags</span></span>           | <span data-ttu-id="def18-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def18-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="def18-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def18-297">System-Flags</span></span>           | <span data-ttu-id="def18-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="def18-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="def18-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="def18-299">Classes used in</span></span>        | [<span data-ttu-id="def18-300">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="def18-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="def18-301">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="def18-301">**Top**</span></span>](c-top.md)<br/> |



 

 





