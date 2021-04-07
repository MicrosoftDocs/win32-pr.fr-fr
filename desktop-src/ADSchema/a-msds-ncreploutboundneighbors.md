---
title: attribut ms-DS-NC-REPL-sortant-voisins
description: Partenaires de réplication pour cette partition. Ce serveur envoie les données de réplication à ces autres serveurs, qui jouent le rôle de destinations. Ce serveur notifie ces autres serveurs quand de nouvelles données sont disponibles.
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-NC-REPL-Outbound-Neighbor-Neighbor
- Schéma Active Directory de l’attribut msDS-NCReplOutboundNeighbors
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845154"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="bfd69-107">attribut ms-DS-NC-REPL-sortant-voisins</span><span class="sxs-lookup"><span data-stu-id="bfd69-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="bfd69-108">Partenaires de réplication pour cette partition.</span><span class="sxs-lookup"><span data-stu-id="bfd69-108">Replication partners for this partition.</span></span> <span data-ttu-id="bfd69-109">Ce serveur envoie les données de réplication à ces autres serveurs, qui jouent le rôle de destinations.</span><span class="sxs-lookup"><span data-stu-id="bfd69-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="bfd69-110">Ce serveur notifie ces autres serveurs quand de nouvelles données sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="bfd69-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="bfd69-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-111">Entry</span></span> | <span data-ttu-id="bfd69-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bfd69-113">CN</span><span class="sxs-lookup"><span data-stu-id="bfd69-113">CN</span></span>                | <span data-ttu-id="bfd69-114">ms-DS-CN-REPL-sortant-voisins</span><span class="sxs-lookup"><span data-stu-id="bfd69-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="bfd69-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bfd69-115">Ldap-Display-Name</span></span> | <span data-ttu-id="bfd69-116">msDS-NCReplOutboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="bfd69-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="bfd69-117">Taille</span><span class="sxs-lookup"><span data-stu-id="bfd69-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="bfd69-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bfd69-118">Update Privilege</span></span>  | <span data-ttu-id="bfd69-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="bfd69-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="bfd69-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bfd69-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bfd69-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-121">Attribute-Id</span></span>      | <span data-ttu-id="bfd69-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="bfd69-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="bfd69-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bfd69-123">System-Id-Guid</span></span>    | <span data-ttu-id="bfd69-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="bfd69-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="bfd69-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd69-125">Syntax</span></span>            | [<span data-ttu-id="bfd69-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bfd69-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bfd69-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bfd69-127">Implementations</span></span>

-   [<span data-ttu-id="bfd69-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bfd69-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bfd69-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bfd69-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bfd69-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bfd69-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bfd69-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfd69-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfd69-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfd69-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfd69-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfd69-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bfd69-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfd69-134">Windows Server 2003</span></span>



| <span data-ttu-id="bfd69-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-135">Entry</span></span> | <span data-ttu-id="bfd69-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-139">System-Only</span></span>            | <span data-ttu-id="bfd69-140">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-140">False</span></span>                           |
| <span data-ttu-id="bfd69-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-142">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-142">False</span></span>                           |
| <span data-ttu-id="bfd69-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-143">Is Indexed</span></span>             | <span data-ttu-id="bfd69-144">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-144">False</span></span>                           |
| <span data-ttu-id="bfd69-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-145">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-146">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-146">False</span></span>                           |
| <span data-ttu-id="bfd69-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-151">Search-Flags</span></span>           | <span data-ttu-id="bfd69-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-152">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-153">System-Flags</span></span>           | <span data-ttu-id="bfd69-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-154">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-155">Classes used in</span></span>        | [<span data-ttu-id="bfd69-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bfd69-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="bfd69-157">ADAM</span></span>



| <span data-ttu-id="bfd69-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-158">Entry</span></span> | <span data-ttu-id="bfd69-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-162">System-Only</span></span>            | <span data-ttu-id="bfd69-163">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-163">False</span></span>                           |
| <span data-ttu-id="bfd69-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-164">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-165">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-165">False</span></span>                           |
| <span data-ttu-id="bfd69-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-166">Is Indexed</span></span>             | <span data-ttu-id="bfd69-167">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-167">False</span></span>                           |
| <span data-ttu-id="bfd69-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-168">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-169">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-169">False</span></span>                           |
| <span data-ttu-id="bfd69-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-174">Search-Flags</span></span>           | <span data-ttu-id="bfd69-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-175">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-176">System-Flags</span></span>           | <span data-ttu-id="bfd69-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-177">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-178">Classes used in</span></span>        | [<span data-ttu-id="bfd69-179">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bfd69-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bfd69-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bfd69-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-181">Entry</span></span> | <span data-ttu-id="bfd69-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-185">System-Only</span></span>            | <span data-ttu-id="bfd69-186">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-186">False</span></span>                           |
| <span data-ttu-id="bfd69-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-188">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-188">False</span></span>                           |
| <span data-ttu-id="bfd69-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-189">Is Indexed</span></span>             | <span data-ttu-id="bfd69-190">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-190">False</span></span>                           |
| <span data-ttu-id="bfd69-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-191">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-192">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-192">False</span></span>                           |
| <span data-ttu-id="bfd69-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-197">Search-Flags</span></span>           | <span data-ttu-id="bfd69-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-198">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-199">System-Flags</span></span>           | <span data-ttu-id="bfd69-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-200">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-201">Classes used in</span></span>        | [<span data-ttu-id="bfd69-202">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bfd69-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfd69-203">Windows Server 2008</span></span>



| <span data-ttu-id="bfd69-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-204">Entry</span></span> | <span data-ttu-id="bfd69-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-208">System-Only</span></span>            | <span data-ttu-id="bfd69-209">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-209">False</span></span>                           |
| <span data-ttu-id="bfd69-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-210">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-211">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-211">False</span></span>                           |
| <span data-ttu-id="bfd69-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-212">Is Indexed</span></span>             | <span data-ttu-id="bfd69-213">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-213">False</span></span>                           |
| <span data-ttu-id="bfd69-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-214">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-215">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-215">False</span></span>                           |
| <span data-ttu-id="bfd69-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-220">Search-Flags</span></span>           | <span data-ttu-id="bfd69-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-221">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-222">System-Flags</span></span>           | <span data-ttu-id="bfd69-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-223">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-224">Classes used in</span></span>        | [<span data-ttu-id="bfd69-225">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfd69-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfd69-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfd69-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-227">Entry</span></span> | <span data-ttu-id="bfd69-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-231">System-Only</span></span>            | <span data-ttu-id="bfd69-232">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-232">False</span></span>                           |
| <span data-ttu-id="bfd69-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-233">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-234">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-234">False</span></span>                           |
| <span data-ttu-id="bfd69-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-235">Is Indexed</span></span>             | <span data-ttu-id="bfd69-236">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-236">False</span></span>                           |
| <span data-ttu-id="bfd69-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-237">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-238">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-238">False</span></span>                           |
| <span data-ttu-id="bfd69-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-243">Search-Flags</span></span>           | <span data-ttu-id="bfd69-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-244">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-245">System-Flags</span></span>           | <span data-ttu-id="bfd69-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-246">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-247">Classes used in</span></span>        | [<span data-ttu-id="bfd69-248">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfd69-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfd69-249">Windows Server 2012</span></span>



| <span data-ttu-id="bfd69-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="bfd69-250">Entry</span></span> | <span data-ttu-id="bfd69-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd69-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bfd69-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bfd69-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfd69-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bfd69-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfd69-254">System-Only</span></span>            | <span data-ttu-id="bfd69-255">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-255">False</span></span>                           |
| <span data-ttu-id="bfd69-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bfd69-256">Is-Single-Valued</span></span>       | <span data-ttu-id="bfd69-257">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-257">False</span></span>                           |
| <span data-ttu-id="bfd69-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bfd69-258">Is Indexed</span></span>             | <span data-ttu-id="bfd69-259">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-259">False</span></span>                           |
| <span data-ttu-id="bfd69-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bfd69-260">In Global Catalog</span></span>      | <span data-ttu-id="bfd69-261">Faux</span><span class="sxs-lookup"><span data-stu-id="bfd69-261">False</span></span>                           |
| <span data-ttu-id="bfd69-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bfd69-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfd69-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bfd69-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bfd69-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfd69-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bfd69-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfd69-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bfd69-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-266">Search-Flags</span></span>           | <span data-ttu-id="bfd69-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfd69-267">0x00000000</span></span>                      |
| <span data-ttu-id="bfd69-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfd69-268">System-Flags</span></span>           | <span data-ttu-id="bfd69-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bfd69-269">0x00000014</span></span>                      |
| <span data-ttu-id="bfd69-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bfd69-270">Classes used in</span></span>        | [<span data-ttu-id="bfd69-271">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="bfd69-271">**Top**</span></span>](c-top.md)<br/> |



 

 





