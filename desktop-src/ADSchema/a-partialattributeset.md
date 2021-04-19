---
title: Partial-attribute-set (attribut)
description: Effectue le suivi de l’état de réplication interne des réplicas partiels (autrement dit, sur des catalogues globaux). Attribut de l’objet de contexte de nommage de réplica partiel. Définit l’ensemble des attributs présents sur un contexte de nommage de réplica partiel particulier.
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory d’attribut de jeu d’attributs partiels
- Schéma AD de l’attribut partialAttributeSet
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514476"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="e28a9-107">Partial-attribute-set (attribut)</span><span class="sxs-lookup"><span data-stu-id="e28a9-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="e28a9-108">Effectue le suivi de l’état de réplication interne des réplicas partiels (autrement dit, sur des catalogues globaux).</span><span class="sxs-lookup"><span data-stu-id="e28a9-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="e28a9-109">Attribut de l’objet de contexte de nommage de réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="e28a9-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="e28a9-110">Définit l’ensemble des attributs présents sur un contexte de nommage de réplica partiel particulier.</span><span class="sxs-lookup"><span data-stu-id="e28a9-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="e28a9-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-111">Entry</span></span> | <span data-ttu-id="e28a9-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e28a9-113">CN</span><span class="sxs-lookup"><span data-stu-id="e28a9-113">CN</span></span>                | <span data-ttu-id="e28a9-114">Partial-attribute-set</span><span class="sxs-lookup"><span data-stu-id="e28a9-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="e28a9-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e28a9-115">Ldap-Display-Name</span></span> | <span data-ttu-id="e28a9-116">partialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="e28a9-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="e28a9-117">Taille</span><span class="sxs-lookup"><span data-stu-id="e28a9-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e28a9-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e28a9-118">Update Privilege</span></span>  | <span data-ttu-id="e28a9-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e28a9-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e28a9-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e28a9-120">Update Frequency</span></span>  | <span data-ttu-id="e28a9-121">Pendant la réplication</span><span class="sxs-lookup"><span data-stu-id="e28a9-121">During replication</span></span>                                    |
| <span data-ttu-id="e28a9-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-122">Attribute-Id</span></span>      | <span data-ttu-id="e28a9-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="e28a9-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="e28a9-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e28a9-124">System-Id-Guid</span></span>    | <span data-ttu-id="e28a9-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e28a9-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="e28a9-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e28a9-126">Syntax</span></span>            | [<span data-ttu-id="e28a9-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e28a9-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e28a9-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e28a9-128">Implementations</span></span>

-   [<span data-ttu-id="e28a9-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e28a9-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e28a9-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e28a9-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e28a9-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e28a9-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e28a9-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e28a9-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e28a9-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e28a9-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e28a9-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e28a9-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e28a9-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e28a9-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e28a9-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e28a9-136">Windows 2000 Server</span></span>



| <span data-ttu-id="e28a9-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-137">Entry</span></span> | <span data-ttu-id="e28a9-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-141">System-Only</span></span>            | <span data-ttu-id="e28a9-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-142">True</span></span>                            |
| <span data-ttu-id="e28a9-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-143">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-144">True</span></span>                            |
| <span data-ttu-id="e28a9-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-145">Is Indexed</span></span>             | <span data-ttu-id="e28a9-146">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-146">False</span></span>                           |
| <span data-ttu-id="e28a9-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-147">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-148">True</span></span>                            |
| <span data-ttu-id="e28a9-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-153">Search-Flags</span></span>           | <span data-ttu-id="e28a9-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-154">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-155">System-Flags</span></span>           | <span data-ttu-id="e28a9-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-156">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-157">Classes used in</span></span>        | [<span data-ttu-id="e28a9-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e28a9-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e28a9-159">Windows Server 2003</span></span>



| <span data-ttu-id="e28a9-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-160">Entry</span></span> | <span data-ttu-id="e28a9-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-164">System-Only</span></span>            | <span data-ttu-id="e28a9-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-165">True</span></span>                            |
| <span data-ttu-id="e28a9-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-167">True</span></span>                            |
| <span data-ttu-id="e28a9-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-168">Is Indexed</span></span>             | <span data-ttu-id="e28a9-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-169">False</span></span>                           |
| <span data-ttu-id="e28a9-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-170">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-171">True</span></span>                            |
| <span data-ttu-id="e28a9-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-176">Search-Flags</span></span>           | <span data-ttu-id="e28a9-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-177">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-178">System-Flags</span></span>           | <span data-ttu-id="e28a9-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-179">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-180">Classes used in</span></span>        | [<span data-ttu-id="e28a9-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e28a9-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="e28a9-182">ADAM</span></span>



| <span data-ttu-id="e28a9-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-183">Entry</span></span> | <span data-ttu-id="e28a9-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-187">System-Only</span></span>            | <span data-ttu-id="e28a9-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-188">True</span></span>                            |
| <span data-ttu-id="e28a9-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-190">True</span></span>                            |
| <span data-ttu-id="e28a9-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-191">Is Indexed</span></span>             | <span data-ttu-id="e28a9-192">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-192">False</span></span>                           |
| <span data-ttu-id="e28a9-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-193">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-194">True</span></span>                            |
| <span data-ttu-id="e28a9-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-199">Search-Flags</span></span>           | <span data-ttu-id="e28a9-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-200">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-201">System-Flags</span></span>           | <span data-ttu-id="e28a9-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-202">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-203">Classes used in</span></span>        | [<span data-ttu-id="e28a9-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e28a9-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e28a9-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e28a9-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-206">Entry</span></span> | <span data-ttu-id="e28a9-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-210">System-Only</span></span>            | <span data-ttu-id="e28a9-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-211">True</span></span>                            |
| <span data-ttu-id="e28a9-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-213">True</span></span>                            |
| <span data-ttu-id="e28a9-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-214">Is Indexed</span></span>             | <span data-ttu-id="e28a9-215">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-215">False</span></span>                           |
| <span data-ttu-id="e28a9-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-216">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-217">True</span></span>                            |
| <span data-ttu-id="e28a9-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-222">Search-Flags</span></span>           | <span data-ttu-id="e28a9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-223">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-224">System-Flags</span></span>           | <span data-ttu-id="e28a9-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-225">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-226">Classes used in</span></span>        | [<span data-ttu-id="e28a9-227">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e28a9-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e28a9-228">Windows Server 2008</span></span>



| <span data-ttu-id="e28a9-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-229">Entry</span></span> | <span data-ttu-id="e28a9-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-233">System-Only</span></span>            | <span data-ttu-id="e28a9-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-234">True</span></span>                            |
| <span data-ttu-id="e28a9-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-236">True</span></span>                            |
| <span data-ttu-id="e28a9-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-237">Is Indexed</span></span>             | <span data-ttu-id="e28a9-238">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-238">False</span></span>                           |
| <span data-ttu-id="e28a9-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-239">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-240">True</span></span>                            |
| <span data-ttu-id="e28a9-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-245">Search-Flags</span></span>           | <span data-ttu-id="e28a9-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-246">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-247">System-Flags</span></span>           | <span data-ttu-id="e28a9-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-248">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-249">Classes used in</span></span>        | [<span data-ttu-id="e28a9-250">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e28a9-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e28a9-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e28a9-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-252">Entry</span></span> | <span data-ttu-id="e28a9-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-256">System-Only</span></span>            | <span data-ttu-id="e28a9-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-257">True</span></span>                            |
| <span data-ttu-id="e28a9-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-258">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-259">True</span></span>                            |
| <span data-ttu-id="e28a9-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-260">Is Indexed</span></span>             | <span data-ttu-id="e28a9-261">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-261">False</span></span>                           |
| <span data-ttu-id="e28a9-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-262">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-263">True</span></span>                            |
| <span data-ttu-id="e28a9-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-268">Search-Flags</span></span>           | <span data-ttu-id="e28a9-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-269">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-270">System-Flags</span></span>           | <span data-ttu-id="e28a9-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-271">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-272">Classes used in</span></span>        | [<span data-ttu-id="e28a9-273">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e28a9-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e28a9-274">Windows Server 2012</span></span>



| <span data-ttu-id="e28a9-275">Entrée</span><span class="sxs-lookup"><span data-stu-id="e28a9-275">Entry</span></span> | <span data-ttu-id="e28a9-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28a9-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e28a9-277">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e28a9-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e28a9-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e28a9-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="e28a9-279">System-Only</span></span>            | <span data-ttu-id="e28a9-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-280">True</span></span>                            |
| <span data-ttu-id="e28a9-281">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e28a9-281">Is-Single-Valued</span></span>       | <span data-ttu-id="e28a9-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-282">True</span></span>                            |
| <span data-ttu-id="e28a9-283">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e28a9-283">Is Indexed</span></span>             | <span data-ttu-id="e28a9-284">Faux</span><span class="sxs-lookup"><span data-stu-id="e28a9-284">False</span></span>                           |
| <span data-ttu-id="e28a9-285">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e28a9-285">In Global Catalog</span></span>      | <span data-ttu-id="e28a9-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="e28a9-286">True</span></span>                            |
| <span data-ttu-id="e28a9-287">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e28a9-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="e28a9-288">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e28a9-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e28a9-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e28a9-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e28a9-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e28a9-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e28a9-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-291">Search-Flags</span></span>           | <span data-ttu-id="e28a9-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e28a9-292">0x00000000</span></span>                      |
| <span data-ttu-id="e28a9-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e28a9-293">System-Flags</span></span>           | <span data-ttu-id="e28a9-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e28a9-294">0x00000013</span></span>                      |
| <span data-ttu-id="e28a9-295">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e28a9-295">Classes used in</span></span>        | [<span data-ttu-id="e28a9-296">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e28a9-296">**Top**</span></span>](c-top.md)<br/> |



 

 





