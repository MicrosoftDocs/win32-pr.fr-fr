---
title: Attribut Dns-Record
description: Utilisé pour stocker des enregistrements de ressources DNS binaires sur des objets DNS.
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Dns-Record
- Schéma AD de l’attribut dnsRecord
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108214"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="e4fa3-105">Attribut Dns-Record</span><span class="sxs-lookup"><span data-stu-id="e4fa3-105">Dns-Record attribute</span></span>

<span data-ttu-id="e4fa3-106">Utilisé pour stocker des enregistrements de ressources DNS binaires sur des objets DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fa3-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="e4fa3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-107">Entry</span></span> | <span data-ttu-id="e4fa3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e4fa3-109">CN</span><span class="sxs-lookup"><span data-stu-id="e4fa3-109">CN</span></span>                | <span data-ttu-id="e4fa3-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="e4fa3-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="e4fa3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e4fa3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e4fa3-112">dnsRecord</span><span class="sxs-lookup"><span data-stu-id="e4fa3-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="e4fa3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e4fa3-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e4fa3-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e4fa3-114">Update Privilege</span></span>  | <span data-ttu-id="e4fa3-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e4fa3-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e4fa3-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e4fa3-116">Update Frequency</span></span>  | <span data-ttu-id="e4fa3-117">Chaque fois que les enregistrements de ressources DNS changent.</span><span class="sxs-lookup"><span data-stu-id="e4fa3-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="e4fa3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-118">Attribute-Id</span></span>      | <span data-ttu-id="e4fa3-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="e4fa3-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="e4fa3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e4fa3-120">System-Id-Guid</span></span>    | <span data-ttu-id="e4fa3-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e4fa3-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="e4fa3-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4fa3-122">Syntax</span></span>            | [<span data-ttu-id="e4fa3-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e4fa3-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e4fa3-124">Implementations</span></span>

-   [<span data-ttu-id="e4fa3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e4fa3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e4fa3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e4fa3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4fa3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4fa3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e4fa3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4fa3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e4fa3-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-132">Entry</span></span> | <span data-ttu-id="e4fa3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-136">System-Only</span></span>            | <span data-ttu-id="e4fa3-137">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-137">False</span></span>                                    |
| <span data-ttu-id="e4fa3-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-139">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-139">False</span></span>                                    |
| <span data-ttu-id="e4fa3-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-140">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-141">False</span></span>                                    |
| <span data-ttu-id="e4fa3-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-142">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-143">False</span></span>                                    |
| <span data-ttu-id="e4fa3-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-148">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-149">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-150">System-Flags</span></span>           | <span data-ttu-id="e4fa3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-151">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-152">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-153">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e4fa3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4fa3-154">Windows Server 2003</span></span>



| <span data-ttu-id="e4fa3-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-155">Entry</span></span> | <span data-ttu-id="e4fa3-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-159">System-Only</span></span>            | <span data-ttu-id="e4fa3-160">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-160">False</span></span>                                    |
| <span data-ttu-id="e4fa3-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-162">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-162">False</span></span>                                    |
| <span data-ttu-id="e4fa3-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-163">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-164">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-164">False</span></span>                                    |
| <span data-ttu-id="e4fa3-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-165">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-166">False</span></span>                                    |
| <span data-ttu-id="e4fa3-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-171">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-172">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-173">System-Flags</span></span>           | <span data-ttu-id="e4fa3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-174">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-175">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-176">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e4fa3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e4fa3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e4fa3-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-178">Entry</span></span> | <span data-ttu-id="e4fa3-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-182">System-Only</span></span>            | <span data-ttu-id="e4fa3-183">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-183">False</span></span>                                    |
| <span data-ttu-id="e4fa3-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-185">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-185">False</span></span>                                    |
| <span data-ttu-id="e4fa3-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-186">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-187">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-187">False</span></span>                                    |
| <span data-ttu-id="e4fa3-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-188">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-189">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-189">False</span></span>                                    |
| <span data-ttu-id="e4fa3-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-194">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-195">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-196">System-Flags</span></span>           | <span data-ttu-id="e4fa3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-197">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-198">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-199">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e4fa3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4fa3-200">Windows Server 2008</span></span>



| <span data-ttu-id="e4fa3-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-201">Entry</span></span> | <span data-ttu-id="e4fa3-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-205">System-Only</span></span>            | <span data-ttu-id="e4fa3-206">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-206">False</span></span>                                    |
| <span data-ttu-id="e4fa3-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-208">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-208">False</span></span>                                    |
| <span data-ttu-id="e4fa3-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-209">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-210">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-210">False</span></span>                                    |
| <span data-ttu-id="e4fa3-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-211">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-212">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-212">False</span></span>                                    |
| <span data-ttu-id="e4fa3-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-217">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-218">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-219">System-Flags</span></span>           | <span data-ttu-id="e4fa3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-220">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-221">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-222">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4fa3-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4fa3-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4fa3-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-224">Entry</span></span> | <span data-ttu-id="e4fa3-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-228">System-Only</span></span>            | <span data-ttu-id="e4fa3-229">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-229">False</span></span>                                    |
| <span data-ttu-id="e4fa3-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-231">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-231">False</span></span>                                    |
| <span data-ttu-id="e4fa3-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-232">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-233">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-233">False</span></span>                                    |
| <span data-ttu-id="e4fa3-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-234">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-235">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-235">False</span></span>                                    |
| <span data-ttu-id="e4fa3-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-240">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-241">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-242">System-Flags</span></span>           | <span data-ttu-id="e4fa3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-243">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-244">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-245">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4fa3-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4fa3-246">Windows Server 2012</span></span>



| <span data-ttu-id="e4fa3-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="e4fa3-247">Entry</span></span> | <span data-ttu-id="e4fa3-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fa3-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e4fa3-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e4fa3-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4fa3-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e4fa3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4fa3-251">System-Only</span></span>            | <span data-ttu-id="e4fa3-252">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-252">False</span></span>                                    |
| <span data-ttu-id="e4fa3-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e4fa3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e4fa3-254">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-254">False</span></span>                                    |
| <span data-ttu-id="e4fa3-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e4fa3-255">Is Indexed</span></span>             | <span data-ttu-id="e4fa3-256">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-256">False</span></span>                                    |
| <span data-ttu-id="e4fa3-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e4fa3-257">In Global Catalog</span></span>      | <span data-ttu-id="e4fa3-258">Faux</span><span class="sxs-lookup"><span data-stu-id="e4fa3-258">False</span></span>                                    |
| <span data-ttu-id="e4fa3-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e4fa3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4fa3-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e4fa3-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e4fa3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4fa3-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4fa3-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e4fa3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-263">Search-Flags</span></span>           | <span data-ttu-id="e4fa3-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4fa3-264">0x00000000</span></span>                               |
| <span data-ttu-id="e4fa3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4fa3-265">System-Flags</span></span>           | <span data-ttu-id="e4fa3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4fa3-266">0x00000010</span></span>                               |
| <span data-ttu-id="e4fa3-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e4fa3-267">Classes used in</span></span>        | [<span data-ttu-id="e4fa3-268">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="e4fa3-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





