---
title: Attribut DNS-Property
description: Utilisé pour stocker les paramètres binaires (propriétés) sur les objets de zone DNS.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut DNS-Property
- Schéma AD de l’attribut dNSProperty
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106541170"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="5262f-105">Attribut DNS-Property</span><span class="sxs-lookup"><span data-stu-id="5262f-105">DNS-Property attribute</span></span>

<span data-ttu-id="5262f-106">Utilisé pour stocker les paramètres binaires (propriétés) sur les objets de zone DNS.</span><span class="sxs-lookup"><span data-stu-id="5262f-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="5262f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-107">Entry</span></span> | <span data-ttu-id="5262f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5262f-109">CN</span><span class="sxs-lookup"><span data-stu-id="5262f-109">CN</span></span>                | <span data-ttu-id="5262f-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="5262f-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="5262f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5262f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5262f-112">dNSProperty</span><span class="sxs-lookup"><span data-stu-id="5262f-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="5262f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="5262f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="5262f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="5262f-114">Update Privilege</span></span>  | <span data-ttu-id="5262f-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="5262f-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5262f-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="5262f-116">Update Frequency</span></span>  | <span data-ttu-id="5262f-117">Chaque fois que les enregistrements de zone DNS changent.</span><span class="sxs-lookup"><span data-stu-id="5262f-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="5262f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-118">Attribute-Id</span></span>      | <span data-ttu-id="5262f-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="5262f-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="5262f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5262f-120">System-Id-Guid</span></span>    | <span data-ttu-id="5262f-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="5262f-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="5262f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5262f-122">Syntax</span></span>            | [<span data-ttu-id="5262f-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="5262f-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5262f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="5262f-124">Implementations</span></span>

-   [<span data-ttu-id="5262f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5262f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5262f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5262f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5262f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5262f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5262f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5262f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5262f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5262f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5262f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5262f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5262f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5262f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5262f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-132">Entry</span></span> | <span data-ttu-id="5262f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-136">System-Only</span></span>            | <span data-ttu-id="5262f-137">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-137">False</span></span>                                                                             |
| <span data-ttu-id="5262f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-139">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-139">False</span></span>                                                                             |
| <span data-ttu-id="5262f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-140">Is Indexed</span></span>             | <span data-ttu-id="5262f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-141">False</span></span>                                                                             |
| <span data-ttu-id="5262f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-142">In Global Catalog</span></span>      | <span data-ttu-id="5262f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-143">False</span></span>                                                                             |
| <span data-ttu-id="5262f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-148">Search-Flags</span></span>           | <span data-ttu-id="5262f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-150">System-Flags</span></span>           | <span data-ttu-id="5262f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-152">Classes used in</span></span>        | [<span data-ttu-id="5262f-153">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-154">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5262f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5262f-155">Windows Server 2003</span></span>



| <span data-ttu-id="5262f-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-156">Entry</span></span> | <span data-ttu-id="5262f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-160">System-Only</span></span>            | <span data-ttu-id="5262f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-161">False</span></span>                                                                             |
| <span data-ttu-id="5262f-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-163">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-163">False</span></span>                                                                             |
| <span data-ttu-id="5262f-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-164">Is Indexed</span></span>             | <span data-ttu-id="5262f-165">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-165">False</span></span>                                                                             |
| <span data-ttu-id="5262f-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-166">In Global Catalog</span></span>      | <span data-ttu-id="5262f-167">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-167">False</span></span>                                                                             |
| <span data-ttu-id="5262f-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-172">Search-Flags</span></span>           | <span data-ttu-id="5262f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-174">System-Flags</span></span>           | <span data-ttu-id="5262f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-176">Classes used in</span></span>        | [<span data-ttu-id="5262f-177">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-178">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5262f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5262f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5262f-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-180">Entry</span></span> | <span data-ttu-id="5262f-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-184">System-Only</span></span>            | <span data-ttu-id="5262f-185">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-185">False</span></span>                                                                             |
| <span data-ttu-id="5262f-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-187">False</span></span>                                                                             |
| <span data-ttu-id="5262f-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-188">Is Indexed</span></span>             | <span data-ttu-id="5262f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-189">False</span></span>                                                                             |
| <span data-ttu-id="5262f-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-190">In Global Catalog</span></span>      | <span data-ttu-id="5262f-191">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-191">False</span></span>                                                                             |
| <span data-ttu-id="5262f-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-196">Search-Flags</span></span>           | <span data-ttu-id="5262f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-198">System-Flags</span></span>           | <span data-ttu-id="5262f-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-200">Classes used in</span></span>        | [<span data-ttu-id="5262f-201">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-202">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5262f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5262f-203">Windows Server 2008</span></span>



| <span data-ttu-id="5262f-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-204">Entry</span></span> | <span data-ttu-id="5262f-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-208">System-Only</span></span>            | <span data-ttu-id="5262f-209">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-209">False</span></span>                                                                             |
| <span data-ttu-id="5262f-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-211">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-211">False</span></span>                                                                             |
| <span data-ttu-id="5262f-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-212">Is Indexed</span></span>             | <span data-ttu-id="5262f-213">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-213">False</span></span>                                                                             |
| <span data-ttu-id="5262f-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-214">In Global Catalog</span></span>      | <span data-ttu-id="5262f-215">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-215">False</span></span>                                                                             |
| <span data-ttu-id="5262f-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-220">Search-Flags</span></span>           | <span data-ttu-id="5262f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-222">System-Flags</span></span>           | <span data-ttu-id="5262f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-224">Classes used in</span></span>        | [<span data-ttu-id="5262f-225">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-226">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5262f-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5262f-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5262f-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-228">Entry</span></span> | <span data-ttu-id="5262f-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-232">System-Only</span></span>            | <span data-ttu-id="5262f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-233">False</span></span>                                                                             |
| <span data-ttu-id="5262f-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-235">False</span></span>                                                                             |
| <span data-ttu-id="5262f-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-236">Is Indexed</span></span>             | <span data-ttu-id="5262f-237">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-237">False</span></span>                                                                             |
| <span data-ttu-id="5262f-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-238">In Global Catalog</span></span>      | <span data-ttu-id="5262f-239">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-239">False</span></span>                                                                             |
| <span data-ttu-id="5262f-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-244">Search-Flags</span></span>           | <span data-ttu-id="5262f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-246">System-Flags</span></span>           | <span data-ttu-id="5262f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-248">Classes used in</span></span>        | [<span data-ttu-id="5262f-249">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-250">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5262f-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5262f-251">Windows Server 2012</span></span>



| <span data-ttu-id="5262f-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="5262f-252">Entry</span></span> | <span data-ttu-id="5262f-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="5262f-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5262f-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5262f-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5262f-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="5262f-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="5262f-256">System-Only</span></span>            | <span data-ttu-id="5262f-257">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-257">False</span></span>                                                                             |
| <span data-ttu-id="5262f-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5262f-258">Is-Single-Valued</span></span>       | <span data-ttu-id="5262f-259">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-259">False</span></span>                                                                             |
| <span data-ttu-id="5262f-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5262f-260">Is Indexed</span></span>             | <span data-ttu-id="5262f-261">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-261">False</span></span>                                                                             |
| <span data-ttu-id="5262f-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5262f-262">In Global Catalog</span></span>      | <span data-ttu-id="5262f-263">Faux</span><span class="sxs-lookup"><span data-stu-id="5262f-263">False</span></span>                                                                             |
| <span data-ttu-id="5262f-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5262f-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="5262f-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5262f-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="5262f-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5262f-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5262f-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="5262f-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-268">Search-Flags</span></span>           | <span data-ttu-id="5262f-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5262f-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="5262f-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5262f-270">System-Flags</span></span>           | <span data-ttu-id="5262f-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5262f-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="5262f-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5262f-272">Classes used in</span></span>        | [<span data-ttu-id="5262f-273">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="5262f-274">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="5262f-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





