---
title: Attribut DNS-Tombstoned
description: True si cet objet a été désactivé. Cet attribut permet de faciliter et d’accélérer la recherche d’enregistrements désactivés. Les objets désactivés sont des objets qui ont été supprimés mais qui n’ont pas encore été supprimés de l’annuaire.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut DNS-Tombstoned
- Schéma AD de l’attribut dNSTombstoned
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844765"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="8081a-107">Attribut DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="8081a-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="8081a-108">True si cet objet a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="8081a-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="8081a-109">Cet attribut permet de faciliter et d’accélérer la recherche d’enregistrements désactivés.</span><span class="sxs-lookup"><span data-stu-id="8081a-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="8081a-110">Les objets désactivés sont des objets qui ont été supprimés mais qui n’ont pas encore été supprimés de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8081a-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="8081a-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-111">Entry</span></span> | <span data-ttu-id="8081a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8081a-113">CN</span><span class="sxs-lookup"><span data-stu-id="8081a-113">CN</span></span>                | <span data-ttu-id="8081a-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="8081a-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="8081a-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8081a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="8081a-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="8081a-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="8081a-117">Taille</span><span class="sxs-lookup"><span data-stu-id="8081a-117">Size</span></span>              | <span data-ttu-id="8081a-118">4 octets</span><span class="sxs-lookup"><span data-stu-id="8081a-118">4 bytes</span></span>                              |
| <span data-ttu-id="8081a-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8081a-119">Update Privilege</span></span>  | <span data-ttu-id="8081a-120">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="8081a-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="8081a-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8081a-121">Update Frequency</span></span>  | <span data-ttu-id="8081a-122">Chaque fois qu’un objet est supprimé.</span><span class="sxs-lookup"><span data-stu-id="8081a-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="8081a-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-123">Attribute-Id</span></span>      | <span data-ttu-id="8081a-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="8081a-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="8081a-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8081a-125">System-Id-Guid</span></span>    | <span data-ttu-id="8081a-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="8081a-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="8081a-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8081a-127">Syntax</span></span>            | [<span data-ttu-id="8081a-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8081a-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="8081a-129">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8081a-129">Implementations</span></span>

-   [<span data-ttu-id="8081a-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8081a-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8081a-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8081a-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8081a-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8081a-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8081a-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8081a-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8081a-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8081a-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8081a-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8081a-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8081a-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8081a-136">Windows 2000 Server</span></span>



| <span data-ttu-id="8081a-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-137">Entry</span></span> | <span data-ttu-id="8081a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-141">System-Only</span></span>            | <span data-ttu-id="8081a-142">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-142">False</span></span>                                    |
| <span data-ttu-id="8081a-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-144">True</span></span>                                     |
| <span data-ttu-id="8081a-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-145">Is Indexed</span></span>             | <span data-ttu-id="8081a-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-146">True</span></span>                                     |
| <span data-ttu-id="8081a-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-147">In Global Catalog</span></span>      | <span data-ttu-id="8081a-148">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-148">False</span></span>                                    |
| <span data-ttu-id="8081a-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-153">Search-Flags</span></span>           | <span data-ttu-id="8081a-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-154">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-155">System-Flags</span></span>           | <span data-ttu-id="8081a-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-156">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-157">Classes used in</span></span>        | [<span data-ttu-id="8081a-158">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8081a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8081a-159">Windows Server 2003</span></span>



| <span data-ttu-id="8081a-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-160">Entry</span></span> | <span data-ttu-id="8081a-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-164">System-Only</span></span>            | <span data-ttu-id="8081a-165">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-165">False</span></span>                                    |
| <span data-ttu-id="8081a-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-167">True</span></span>                                     |
| <span data-ttu-id="8081a-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-168">Is Indexed</span></span>             | <span data-ttu-id="8081a-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-169">True</span></span>                                     |
| <span data-ttu-id="8081a-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-170">In Global Catalog</span></span>      | <span data-ttu-id="8081a-171">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-171">False</span></span>                                    |
| <span data-ttu-id="8081a-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-176">Search-Flags</span></span>           | <span data-ttu-id="8081a-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-177">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-178">System-Flags</span></span>           | <span data-ttu-id="8081a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-179">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-180">Classes used in</span></span>        | [<span data-ttu-id="8081a-181">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8081a-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8081a-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8081a-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-183">Entry</span></span> | <span data-ttu-id="8081a-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-187">System-Only</span></span>            | <span data-ttu-id="8081a-188">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-188">False</span></span>                                    |
| <span data-ttu-id="8081a-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-190">True</span></span>                                     |
| <span data-ttu-id="8081a-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-191">Is Indexed</span></span>             | <span data-ttu-id="8081a-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-192">True</span></span>                                     |
| <span data-ttu-id="8081a-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-193">In Global Catalog</span></span>      | <span data-ttu-id="8081a-194">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-194">False</span></span>                                    |
| <span data-ttu-id="8081a-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-199">Search-Flags</span></span>           | <span data-ttu-id="8081a-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-200">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-201">System-Flags</span></span>           | <span data-ttu-id="8081a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-202">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-203">Classes used in</span></span>        | [<span data-ttu-id="8081a-204">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8081a-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8081a-205">Windows Server 2008</span></span>



| <span data-ttu-id="8081a-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-206">Entry</span></span> | <span data-ttu-id="8081a-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-210">System-Only</span></span>            | <span data-ttu-id="8081a-211">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-211">False</span></span>                                    |
| <span data-ttu-id="8081a-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-213">True</span></span>                                     |
| <span data-ttu-id="8081a-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-214">Is Indexed</span></span>             | <span data-ttu-id="8081a-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-215">True</span></span>                                     |
| <span data-ttu-id="8081a-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-216">In Global Catalog</span></span>      | <span data-ttu-id="8081a-217">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-217">False</span></span>                                    |
| <span data-ttu-id="8081a-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-222">Search-Flags</span></span>           | <span data-ttu-id="8081a-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-223">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-224">System-Flags</span></span>           | <span data-ttu-id="8081a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-225">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-226">Classes used in</span></span>        | [<span data-ttu-id="8081a-227">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8081a-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8081a-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8081a-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-229">Entry</span></span> | <span data-ttu-id="8081a-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-233">System-Only</span></span>            | <span data-ttu-id="8081a-234">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-234">False</span></span>                                    |
| <span data-ttu-id="8081a-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-236">True</span></span>                                     |
| <span data-ttu-id="8081a-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-237">Is Indexed</span></span>             | <span data-ttu-id="8081a-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-238">True</span></span>                                     |
| <span data-ttu-id="8081a-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-239">In Global Catalog</span></span>      | <span data-ttu-id="8081a-240">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-240">False</span></span>                                    |
| <span data-ttu-id="8081a-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-245">Search-Flags</span></span>           | <span data-ttu-id="8081a-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-246">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-247">System-Flags</span></span>           | <span data-ttu-id="8081a-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-248">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-249">Classes used in</span></span>        | [<span data-ttu-id="8081a-250">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8081a-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8081a-251">Windows Server 2012</span></span>



| <span data-ttu-id="8081a-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="8081a-252">Entry</span></span> | <span data-ttu-id="8081a-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="8081a-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8081a-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8081a-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8081a-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8081a-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="8081a-256">System-Only</span></span>            | <span data-ttu-id="8081a-257">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-257">False</span></span>                                    |
| <span data-ttu-id="8081a-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8081a-258">Is-Single-Valued</span></span>       | <span data-ttu-id="8081a-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-259">True</span></span>                                     |
| <span data-ttu-id="8081a-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8081a-260">Is Indexed</span></span>             | <span data-ttu-id="8081a-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="8081a-261">True</span></span>                                     |
| <span data-ttu-id="8081a-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8081a-262">In Global Catalog</span></span>      | <span data-ttu-id="8081a-263">Faux</span><span class="sxs-lookup"><span data-stu-id="8081a-263">False</span></span>                                    |
| <span data-ttu-id="8081a-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8081a-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="8081a-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8081a-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8081a-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8081a-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8081a-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8081a-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8081a-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-268">Search-Flags</span></span>           | <span data-ttu-id="8081a-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8081a-269">0x00000001</span></span>                               |
| <span data-ttu-id="8081a-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8081a-270">System-Flags</span></span>           | <span data-ttu-id="8081a-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8081a-271">0x00000010</span></span>                               |
| <span data-ttu-id="8081a-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8081a-272">Classes used in</span></span>        | [<span data-ttu-id="8081a-273">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="8081a-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





