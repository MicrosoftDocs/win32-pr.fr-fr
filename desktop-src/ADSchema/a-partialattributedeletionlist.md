---
title: Attribut partial-attribute-suppression-liste
description: Effectue le suivi de l’état de réplication interne des réplicas partiels (autrement dit, sur des catalogues globaux). Attribut de l’objet de contexte de nommage de réplica partiel. Utilisé lorsque le garbage collector est en train de supprimer des attributs des objets dans ses NC de réplica partiels.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut partial-attribute-suppression-List
- Schéma AD de l’attribut partialAttributeDeletionList
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509962"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="ad56f-107">Attribut partial-attribute-suppression-liste</span><span class="sxs-lookup"><span data-stu-id="ad56f-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="ad56f-108">Effectue le suivi de l’état de réplication interne des réplicas partiels (autrement dit, sur des catalogues globaux).</span><span class="sxs-lookup"><span data-stu-id="ad56f-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="ad56f-109">Attribut de l’objet de contexte de nommage de réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="ad56f-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="ad56f-110">Utilisé lorsque le garbage collector est en train de supprimer des attributs des objets dans ses NC de réplica partiels.</span><span class="sxs-lookup"><span data-stu-id="ad56f-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="ad56f-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-111">Entry</span></span> | <span data-ttu-id="ad56f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ad56f-113">CN</span><span class="sxs-lookup"><span data-stu-id="ad56f-113">CN</span></span>                | <span data-ttu-id="ad56f-114">Partial-attribute-suppression-liste</span><span class="sxs-lookup"><span data-stu-id="ad56f-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="ad56f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ad56f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ad56f-116">partialAttributeDeletionList</span><span class="sxs-lookup"><span data-stu-id="ad56f-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="ad56f-117">Taille</span><span class="sxs-lookup"><span data-stu-id="ad56f-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ad56f-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ad56f-118">Update Privilege</span></span>  | <span data-ttu-id="ad56f-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ad56f-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="ad56f-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ad56f-120">Update Frequency</span></span>  | <span data-ttu-id="ad56f-121">Pendant la réplication</span><span class="sxs-lookup"><span data-stu-id="ad56f-121">During replication</span></span>                                    |
| <span data-ttu-id="ad56f-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-122">Attribute-Id</span></span>      | <span data-ttu-id="ad56f-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="ad56f-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="ad56f-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad56f-124">System-Id-Guid</span></span>    | <span data-ttu-id="ad56f-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ad56f-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="ad56f-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad56f-126">Syntax</span></span>            | [<span data-ttu-id="ad56f-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ad56f-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ad56f-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ad56f-128">Implementations</span></span>

-   [<span data-ttu-id="ad56f-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ad56f-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ad56f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad56f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad56f-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ad56f-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ad56f-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad56f-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad56f-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad56f-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad56f-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad56f-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad56f-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad56f-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ad56f-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad56f-136">Windows 2000 Server</span></span>



| <span data-ttu-id="ad56f-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-137">Entry</span></span> | <span data-ttu-id="ad56f-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-141">System-Only</span></span>            | <span data-ttu-id="ad56f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-142">True</span></span>                            |
| <span data-ttu-id="ad56f-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-143">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-144">True</span></span>                            |
| <span data-ttu-id="ad56f-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-145">Is Indexed</span></span>             | <span data-ttu-id="ad56f-146">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-146">False</span></span>                           |
| <span data-ttu-id="ad56f-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-147">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-148">True</span></span>                            |
| <span data-ttu-id="ad56f-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-153">Search-Flags</span></span>           | <span data-ttu-id="ad56f-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-154">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-155">System-Flags</span></span>           | <span data-ttu-id="ad56f-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-156">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-157">Classes used in</span></span>        | [<span data-ttu-id="ad56f-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ad56f-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad56f-159">Windows Server 2003</span></span>



| <span data-ttu-id="ad56f-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-160">Entry</span></span> | <span data-ttu-id="ad56f-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-164">System-Only</span></span>            | <span data-ttu-id="ad56f-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-165">True</span></span>                            |
| <span data-ttu-id="ad56f-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-167">True</span></span>                            |
| <span data-ttu-id="ad56f-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-168">Is Indexed</span></span>             | <span data-ttu-id="ad56f-169">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-169">False</span></span>                           |
| <span data-ttu-id="ad56f-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-170">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-171">True</span></span>                            |
| <span data-ttu-id="ad56f-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-176">Search-Flags</span></span>           | <span data-ttu-id="ad56f-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-177">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-178">System-Flags</span></span>           | <span data-ttu-id="ad56f-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-179">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-180">Classes used in</span></span>        | [<span data-ttu-id="ad56f-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ad56f-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="ad56f-182">ADAM</span></span>



| <span data-ttu-id="ad56f-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-183">Entry</span></span> | <span data-ttu-id="ad56f-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-187">System-Only</span></span>            | <span data-ttu-id="ad56f-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-188">True</span></span>                            |
| <span data-ttu-id="ad56f-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-190">True</span></span>                            |
| <span data-ttu-id="ad56f-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-191">Is Indexed</span></span>             | <span data-ttu-id="ad56f-192">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-192">False</span></span>                           |
| <span data-ttu-id="ad56f-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-193">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-194">True</span></span>                            |
| <span data-ttu-id="ad56f-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-199">Search-Flags</span></span>           | <span data-ttu-id="ad56f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-200">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-201">System-Flags</span></span>           | <span data-ttu-id="ad56f-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-202">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-203">Classes used in</span></span>        | [<span data-ttu-id="ad56f-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad56f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad56f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad56f-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-206">Entry</span></span> | <span data-ttu-id="ad56f-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-210">System-Only</span></span>            | <span data-ttu-id="ad56f-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-211">True</span></span>                            |
| <span data-ttu-id="ad56f-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-213">True</span></span>                            |
| <span data-ttu-id="ad56f-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-214">Is Indexed</span></span>             | <span data-ttu-id="ad56f-215">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-215">False</span></span>                           |
| <span data-ttu-id="ad56f-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-216">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-217">True</span></span>                            |
| <span data-ttu-id="ad56f-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-222">Search-Flags</span></span>           | <span data-ttu-id="ad56f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-223">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-224">System-Flags</span></span>           | <span data-ttu-id="ad56f-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-225">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-226">Classes used in</span></span>        | [<span data-ttu-id="ad56f-227">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad56f-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad56f-228">Windows Server 2008</span></span>



| <span data-ttu-id="ad56f-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-229">Entry</span></span> | <span data-ttu-id="ad56f-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-233">System-Only</span></span>            | <span data-ttu-id="ad56f-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-234">True</span></span>                            |
| <span data-ttu-id="ad56f-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-235">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-236">True</span></span>                            |
| <span data-ttu-id="ad56f-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-237">Is Indexed</span></span>             | <span data-ttu-id="ad56f-238">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-238">False</span></span>                           |
| <span data-ttu-id="ad56f-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-239">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-240">True</span></span>                            |
| <span data-ttu-id="ad56f-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-245">Search-Flags</span></span>           | <span data-ttu-id="ad56f-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-246">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-247">System-Flags</span></span>           | <span data-ttu-id="ad56f-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-248">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-249">Classes used in</span></span>        | [<span data-ttu-id="ad56f-250">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad56f-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad56f-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad56f-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-252">Entry</span></span> | <span data-ttu-id="ad56f-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-256">System-Only</span></span>            | <span data-ttu-id="ad56f-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-257">True</span></span>                            |
| <span data-ttu-id="ad56f-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-259">True</span></span>                            |
| <span data-ttu-id="ad56f-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-260">Is Indexed</span></span>             | <span data-ttu-id="ad56f-261">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-261">False</span></span>                           |
| <span data-ttu-id="ad56f-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-262">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-263">True</span></span>                            |
| <span data-ttu-id="ad56f-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-268">Search-Flags</span></span>           | <span data-ttu-id="ad56f-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-269">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-270">System-Flags</span></span>           | <span data-ttu-id="ad56f-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-271">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-272">Classes used in</span></span>        | [<span data-ttu-id="ad56f-273">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad56f-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad56f-274">Windows Server 2012</span></span>



| <span data-ttu-id="ad56f-275">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad56f-275">Entry</span></span> | <span data-ttu-id="ad56f-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad56f-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad56f-277">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad56f-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad56f-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad56f-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad56f-279">System-Only</span></span>            | <span data-ttu-id="ad56f-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-280">True</span></span>                            |
| <span data-ttu-id="ad56f-281">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad56f-281">Is-Single-Valued</span></span>       | <span data-ttu-id="ad56f-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-282">True</span></span>                            |
| <span data-ttu-id="ad56f-283">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad56f-283">Is Indexed</span></span>             | <span data-ttu-id="ad56f-284">Faux</span><span class="sxs-lookup"><span data-stu-id="ad56f-284">False</span></span>                           |
| <span data-ttu-id="ad56f-285">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad56f-285">In Global Catalog</span></span>      | <span data-ttu-id="ad56f-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad56f-286">True</span></span>                            |
| <span data-ttu-id="ad56f-287">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad56f-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad56f-288">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad56f-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad56f-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad56f-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad56f-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad56f-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad56f-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-291">Search-Flags</span></span>           | <span data-ttu-id="ad56f-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad56f-292">0x00000000</span></span>                      |
| <span data-ttu-id="ad56f-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad56f-293">System-Flags</span></span>           | <span data-ttu-id="ad56f-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ad56f-294">0x00000013</span></span>                      |
| <span data-ttu-id="ad56f-295">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad56f-295">Classes used in</span></span>        | [<span data-ttu-id="ad56f-296">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ad56f-296">**Top**</span></span>](c-top.md)<br/> |



 

 





