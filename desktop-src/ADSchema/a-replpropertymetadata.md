---
title: Attribut REPL-Property-Meta-Data
description: Effectue le suivi des informations d’état de réplication interne pour les objets DS. Les informations fournies ici peuvent être extraites sous forme publique via l’API publique DsReplicaGetInfo (). Présent sur tous les objets DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut REPL-Property-Meta-Data
- Schéma AD de l’attribut replPropertyMetaData
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744908"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="cb5ba-107">Attribut REPL-Property-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="cb5ba-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="cb5ba-108">Effectue le suivi des informations d’état de réplication interne pour les objets DS.</span><span class="sxs-lookup"><span data-stu-id="cb5ba-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="cb5ba-109">Les informations fournies ici peuvent être extraites sous forme publique via l’API publique DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="cb5ba-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="cb5ba-110">Présent sur tous les objets DS.</span><span class="sxs-lookup"><span data-stu-id="cb5ba-110">Present on all DS objects.</span></span>



| <span data-ttu-id="cb5ba-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-111">Entry</span></span> | <span data-ttu-id="cb5ba-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cb5ba-113">CN</span><span class="sxs-lookup"><span data-stu-id="cb5ba-113">CN</span></span>                | <span data-ttu-id="cb5ba-114">REPL-Property-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="cb5ba-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="cb5ba-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cb5ba-115">Ldap-Display-Name</span></span> | <span data-ttu-id="cb5ba-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="cb5ba-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="cb5ba-117">Taille</span><span class="sxs-lookup"><span data-stu-id="cb5ba-117">Size</span></span>              | <span data-ttu-id="cb5ba-118">La longueur est proportionnelle au nombre d’attributs réplicables sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb5ba-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="cb5ba-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cb5ba-119">Update Privilege</span></span>  | <span data-ttu-id="cb5ba-120">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="cb5ba-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="cb5ba-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cb5ba-121">Update Frequency</span></span>  | <span data-ttu-id="cb5ba-122">Modifications en réponse à des modifications de réplication dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb5ba-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="cb5ba-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-123">Attribute-Id</span></span>      | <span data-ttu-id="cb5ba-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="cb5ba-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="cb5ba-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cb5ba-125">System-Id-Guid</span></span>    | <span data-ttu-id="cb5ba-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cb5ba-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="cb5ba-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb5ba-127">Syntax</span></span>            | [<span data-ttu-id="cb5ba-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="cb5ba-129">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cb5ba-129">Implementations</span></span>

-   [<span data-ttu-id="cb5ba-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cb5ba-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb5ba-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cb5ba-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb5ba-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb5ba-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb5ba-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cb5ba-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb5ba-137">Windows 2000 Server</span></span>



| <span data-ttu-id="cb5ba-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-138">Entry</span></span> | <span data-ttu-id="cb5ba-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-140">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-142">System-Only</span></span>            | <span data-ttu-id="cb5ba-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-143">True</span></span>                            |
| <span data-ttu-id="cb5ba-144">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-144">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-145">True</span></span>                            |
| <span data-ttu-id="cb5ba-146">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-146">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-147">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-147">False</span></span>                           |
| <span data-ttu-id="cb5ba-148">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-148">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-149">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-149">True</span></span>                            |
| <span data-ttu-id="cb5ba-150">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-151">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-154">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-155">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-156">System-Flags</span></span>           | <span data-ttu-id="cb5ba-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cb5ba-157">0x00000013</span></span>                      |
| <span data-ttu-id="cb5ba-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-158">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-159">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cb5ba-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb5ba-160">Windows Server 2003</span></span>



| <span data-ttu-id="cb5ba-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-161">Entry</span></span> | <span data-ttu-id="cb5ba-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-165">System-Only</span></span>            | <span data-ttu-id="cb5ba-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-166">True</span></span>                            |
| <span data-ttu-id="cb5ba-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-167">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-168">True</span></span>                            |
| <span data-ttu-id="cb5ba-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-169">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-170">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-170">False</span></span>                           |
| <span data-ttu-id="cb5ba-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-171">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-172">True</span></span>                            |
| <span data-ttu-id="cb5ba-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-177">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-178">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-179">System-Flags</span></span>           | <span data-ttu-id="cb5ba-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-180">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-181">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cb5ba-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="cb5ba-183">ADAM</span></span>



| <span data-ttu-id="cb5ba-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-184">Entry</span></span> | <span data-ttu-id="cb5ba-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-188">System-Only</span></span>            | <span data-ttu-id="cb5ba-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-189">True</span></span>                            |
| <span data-ttu-id="cb5ba-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-190">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-191">True</span></span>                            |
| <span data-ttu-id="cb5ba-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-192">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-193">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-193">False</span></span>                           |
| <span data-ttu-id="cb5ba-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-194">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-195">True</span></span>                            |
| <span data-ttu-id="cb5ba-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-200">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-201">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-202">System-Flags</span></span>           | <span data-ttu-id="cb5ba-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-203">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-204">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-205">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb5ba-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb5ba-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb5ba-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-207">Entry</span></span> | <span data-ttu-id="cb5ba-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-211">System-Only</span></span>            | <span data-ttu-id="cb5ba-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-212">True</span></span>                            |
| <span data-ttu-id="cb5ba-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-213">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-214">True</span></span>                            |
| <span data-ttu-id="cb5ba-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-215">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-216">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-216">False</span></span>                           |
| <span data-ttu-id="cb5ba-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-217">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-218">True</span></span>                            |
| <span data-ttu-id="cb5ba-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-223">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-224">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-225">System-Flags</span></span>           | <span data-ttu-id="cb5ba-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-226">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-227">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb5ba-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-229">Windows Server 2008</span></span>



| <span data-ttu-id="cb5ba-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-230">Entry</span></span> | <span data-ttu-id="cb5ba-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-234">System-Only</span></span>            | <span data-ttu-id="cb5ba-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-235">True</span></span>                            |
| <span data-ttu-id="cb5ba-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-236">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-237">True</span></span>                            |
| <span data-ttu-id="cb5ba-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-238">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-239">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-239">False</span></span>                           |
| <span data-ttu-id="cb5ba-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-240">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-241">True</span></span>                            |
| <span data-ttu-id="cb5ba-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-246">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-247">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-248">System-Flags</span></span>           | <span data-ttu-id="cb5ba-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-249">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-250">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-251">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb5ba-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb5ba-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb5ba-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-253">Entry</span></span> | <span data-ttu-id="cb5ba-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-257">System-Only</span></span>            | <span data-ttu-id="cb5ba-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-258">True</span></span>                            |
| <span data-ttu-id="cb5ba-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-259">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-260">True</span></span>                            |
| <span data-ttu-id="cb5ba-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-261">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-262">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-262">False</span></span>                           |
| <span data-ttu-id="cb5ba-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-263">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-264">True</span></span>                            |
| <span data-ttu-id="cb5ba-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-269">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-270">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-271">System-Flags</span></span>           | <span data-ttu-id="cb5ba-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-272">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-273">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-274">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb5ba-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb5ba-275">Windows Server 2012</span></span>



| <span data-ttu-id="cb5ba-276">Entrée</span><span class="sxs-lookup"><span data-stu-id="cb5ba-276">Entry</span></span> | <span data-ttu-id="cb5ba-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5ba-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cb5ba-278">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cb5ba-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb5ba-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cb5ba-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb5ba-280">System-Only</span></span>            | <span data-ttu-id="cb5ba-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-281">True</span></span>                            |
| <span data-ttu-id="cb5ba-282">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cb5ba-282">Is-Single-Valued</span></span>       | <span data-ttu-id="cb5ba-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-283">True</span></span>                            |
| <span data-ttu-id="cb5ba-284">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cb5ba-284">Is Indexed</span></span>             | <span data-ttu-id="cb5ba-285">Faux</span><span class="sxs-lookup"><span data-stu-id="cb5ba-285">False</span></span>                           |
| <span data-ttu-id="cb5ba-286">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cb5ba-286">In Global Catalog</span></span>      | <span data-ttu-id="cb5ba-287">Vrai</span><span class="sxs-lookup"><span data-stu-id="cb5ba-287">True</span></span>                            |
| <span data-ttu-id="cb5ba-288">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cb5ba-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb5ba-289">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cb5ba-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cb5ba-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb5ba-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb5ba-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cb5ba-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-292">Search-Flags</span></span>           | <span data-ttu-id="cb5ba-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb5ba-293">0x00000008</span></span>                      |
| <span data-ttu-id="cb5ba-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb5ba-294">System-Flags</span></span>           | <span data-ttu-id="cb5ba-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="cb5ba-295">0x0000001B</span></span>                      |
| <span data-ttu-id="cb5ba-296">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cb5ba-296">Classes used in</span></span>        | [<span data-ttu-id="cb5ba-297">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cb5ba-297">**Top**</span></span>](c-top.md)<br/> |



 

 





