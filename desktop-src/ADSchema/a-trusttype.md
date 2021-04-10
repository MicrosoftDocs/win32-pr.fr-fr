---
title: Attribut Trust-Type
description: Type d’approbation, par exemple, Windows NT ou MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Trust-Type
- Schéma AD de l’attribut trustType
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943097"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="0c89d-105">Attribut Trust-Type</span><span class="sxs-lookup"><span data-stu-id="0c89d-105">Trust-Type attribute</span></span>

<span data-ttu-id="0c89d-106">Type d’approbation, par exemple, Windows NT ou MIT.</span><span class="sxs-lookup"><span data-stu-id="0c89d-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="0c89d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-107">Entry</span></span> | <span data-ttu-id="0c89d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0c89d-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c89d-109">CN</span></span>                | <span data-ttu-id="0c89d-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="0c89d-110">Trust-Type</span></span>                           |
| <span data-ttu-id="0c89d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c89d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c89d-112">trustType</span><span class="sxs-lookup"><span data-stu-id="0c89d-112">trustType</span></span>                            |
| <span data-ttu-id="0c89d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="0c89d-113">Size</span></span>              | <span data-ttu-id="0c89d-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="0c89d-114">4 bytes</span></span>                              |
| <span data-ttu-id="0c89d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="0c89d-115">Update Privilege</span></span>  | <span data-ttu-id="0c89d-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="0c89d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="0c89d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="0c89d-117">Update Frequency</span></span>  | <span data-ttu-id="0c89d-118">Lors de la création d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="0c89d-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="0c89d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-119">Attribute-Id</span></span>      | <span data-ttu-id="0c89d-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="0c89d-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="0c89d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c89d-121">System-Id-Guid</span></span>    | <span data-ttu-id="0c89d-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0c89d-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0c89d-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c89d-123">Syntax</span></span>            | [<span data-ttu-id="0c89d-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="0c89d-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0c89d-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="0c89d-125">Implementations</span></span>

-   [<span data-ttu-id="0c89d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c89d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c89d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c89d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c89d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c89d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c89d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c89d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c89d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c89d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c89d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c89d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c89d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c89d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0c89d-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-133">Entry</span></span> | <span data-ttu-id="0c89d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-137">System-Only</span></span>            | <span data-ttu-id="0c89d-138">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-138">False</span></span>                                                |
| <span data-ttu-id="0c89d-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-140">True</span></span>                                                 |
| <span data-ttu-id="0c89d-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-141">Is Indexed</span></span>             | <span data-ttu-id="0c89d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-142">False</span></span>                                                |
| <span data-ttu-id="0c89d-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-143">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-144">False</span></span>                                                |
| <span data-ttu-id="0c89d-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-149">Search-Flags</span></span>           | <span data-ttu-id="0c89d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-150">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-151">System-Flags</span></span>           | <span data-ttu-id="0c89d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-152">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-153">Classes used in</span></span>        | [<span data-ttu-id="0c89d-154">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c89d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c89d-155">Windows Server 2003</span></span>



| <span data-ttu-id="0c89d-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-156">Entry</span></span> | <span data-ttu-id="0c89d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-160">System-Only</span></span>            | <span data-ttu-id="0c89d-161">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-161">False</span></span>                                                |
| <span data-ttu-id="0c89d-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-163">True</span></span>                                                 |
| <span data-ttu-id="0c89d-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-164">Is Indexed</span></span>             | <span data-ttu-id="0c89d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-165">False</span></span>                                                |
| <span data-ttu-id="0c89d-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-166">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-167">True</span></span>                                                 |
| <span data-ttu-id="0c89d-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-172">Search-Flags</span></span>           | <span data-ttu-id="0c89d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-173">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-174">System-Flags</span></span>           | <span data-ttu-id="0c89d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-175">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-176">Classes used in</span></span>        | [<span data-ttu-id="0c89d-177">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c89d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c89d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c89d-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-179">Entry</span></span> | <span data-ttu-id="0c89d-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-183">System-Only</span></span>            | <span data-ttu-id="0c89d-184">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-184">False</span></span>                                                |
| <span data-ttu-id="0c89d-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-186">True</span></span>                                                 |
| <span data-ttu-id="0c89d-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-187">Is Indexed</span></span>             | <span data-ttu-id="0c89d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-188">False</span></span>                                                |
| <span data-ttu-id="0c89d-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-189">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-190">True</span></span>                                                 |
| <span data-ttu-id="0c89d-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-195">Search-Flags</span></span>           | <span data-ttu-id="0c89d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-196">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-197">System-Flags</span></span>           | <span data-ttu-id="0c89d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-198">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-199">Classes used in</span></span>        | [<span data-ttu-id="0c89d-200">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c89d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c89d-201">Windows Server 2008</span></span>



| <span data-ttu-id="0c89d-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-202">Entry</span></span> | <span data-ttu-id="0c89d-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-206">System-Only</span></span>            | <span data-ttu-id="0c89d-207">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-207">False</span></span>                                                |
| <span data-ttu-id="0c89d-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-209">True</span></span>                                                 |
| <span data-ttu-id="0c89d-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-210">Is Indexed</span></span>             | <span data-ttu-id="0c89d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-211">False</span></span>                                                |
| <span data-ttu-id="0c89d-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-212">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-213">True</span></span>                                                 |
| <span data-ttu-id="0c89d-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-218">Search-Flags</span></span>           | <span data-ttu-id="0c89d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-219">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-220">System-Flags</span></span>           | <span data-ttu-id="0c89d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-221">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-222">Classes used in</span></span>        | [<span data-ttu-id="0c89d-223">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c89d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c89d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c89d-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-225">Entry</span></span> | <span data-ttu-id="0c89d-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-229">System-Only</span></span>            | <span data-ttu-id="0c89d-230">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-230">False</span></span>                                                |
| <span data-ttu-id="0c89d-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-232">True</span></span>                                                 |
| <span data-ttu-id="0c89d-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-233">Is Indexed</span></span>             | <span data-ttu-id="0c89d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-234">False</span></span>                                                |
| <span data-ttu-id="0c89d-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-235">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-236">True</span></span>                                                 |
| <span data-ttu-id="0c89d-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-241">Search-Flags</span></span>           | <span data-ttu-id="0c89d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-242">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-243">System-Flags</span></span>           | <span data-ttu-id="0c89d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-244">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-245">Classes used in</span></span>        | [<span data-ttu-id="0c89d-246">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c89d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c89d-247">Windows Server 2012</span></span>



| <span data-ttu-id="0c89d-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="0c89d-248">Entry</span></span> | <span data-ttu-id="0c89d-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c89d-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0c89d-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0c89d-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c89d-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0c89d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c89d-252">System-Only</span></span>            | <span data-ttu-id="0c89d-253">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-253">False</span></span>                                                |
| <span data-ttu-id="0c89d-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0c89d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="0c89d-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-255">True</span></span>                                                 |
| <span data-ttu-id="0c89d-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0c89d-256">Is Indexed</span></span>             | <span data-ttu-id="0c89d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="0c89d-257">False</span></span>                                                |
| <span data-ttu-id="0c89d-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0c89d-258">In Global Catalog</span></span>      | <span data-ttu-id="0c89d-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="0c89d-259">True</span></span>                                                 |
| <span data-ttu-id="0c89d-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0c89d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c89d-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0c89d-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0c89d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c89d-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c89d-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0c89d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-264">Search-Flags</span></span>           | <span data-ttu-id="0c89d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c89d-265">0x00000000</span></span>                                           |
| <span data-ttu-id="0c89d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c89d-266">System-Flags</span></span>           | <span data-ttu-id="0c89d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c89d-267">0x00000010</span></span>                                           |
| <span data-ttu-id="0c89d-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0c89d-268">Classes used in</span></span>        | [<span data-ttu-id="0c89d-269">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0c89d-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





