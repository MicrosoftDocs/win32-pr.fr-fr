---
title: Attribut Trust-Direction
description: Direction d’une approbation.
ms.assetid: 29ee19c6-a6c5-40e6-ad70-bfa0a16e3a84
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Trust-Direction
- Schéma AD de l’attribut trustDirection
topic_type:
- apiref
api_name:
- Trust-Direction
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54feb80079ea4ac8f1b68fee7d223275313b64b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479901"
---
# <a name="trust-direction-attribute"></a><span data-ttu-id="0ad6f-105">Attribut Trust-Direction</span><span class="sxs-lookup"><span data-stu-id="0ad6f-105">Trust-Direction attribute</span></span>

<span data-ttu-id="0ad6f-106">Direction d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="0ad6f-106">The direction of a trust.</span></span>



| <span data-ttu-id="0ad6f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-107">Entry</span></span> | <span data-ttu-id="0ad6f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0ad6f-109">CN</span><span class="sxs-lookup"><span data-stu-id="0ad6f-109">CN</span></span>                | <span data-ttu-id="0ad6f-110">Trust-Direction</span><span class="sxs-lookup"><span data-stu-id="0ad6f-110">Trust-Direction</span></span>                      |
| <span data-ttu-id="0ad6f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0ad6f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0ad6f-112">trustDirection</span><span class="sxs-lookup"><span data-stu-id="0ad6f-112">trustDirection</span></span>                       |
| <span data-ttu-id="0ad6f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="0ad6f-113">Size</span></span>              | <span data-ttu-id="0ad6f-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="0ad6f-114">4 bytes</span></span>                              |
| <span data-ttu-id="0ad6f-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="0ad6f-115">Update Privilege</span></span>  | <span data-ttu-id="0ad6f-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="0ad6f-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="0ad6f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="0ad6f-117">Update Frequency</span></span>  | <span data-ttu-id="0ad6f-118">Lors de la création d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="0ad6f-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="0ad6f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-119">Attribute-Id</span></span>      | <span data-ttu-id="0ad6f-120">1.2.840.113556.1.4.132</span><span class="sxs-lookup"><span data-stu-id="0ad6f-120">1.2.840.113556.1.4.132</span></span>               |
| <span data-ttu-id="0ad6f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0ad6f-121">System-Id-Guid</span></span>    | <span data-ttu-id="0ad6f-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0ad6f-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0ad6f-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ad6f-123">Syntax</span></span>            | [<span data-ttu-id="0ad6f-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0ad6f-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="0ad6f-125">Implementations</span></span>

-   [<span data-ttu-id="0ad6f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0ad6f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0ad6f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0ad6f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0ad6f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0ad6f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0ad6f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ad6f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0ad6f-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-133">Entry</span></span> | <span data-ttu-id="0ad6f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-137">System-Only</span></span>            | <span data-ttu-id="0ad6f-138">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-138">False</span></span>                                                |
| <span data-ttu-id="0ad6f-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-140">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-141">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-142">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-142">False</span></span>                                                |
| <span data-ttu-id="0ad6f-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-143">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-144">False</span></span>                                                |
| <span data-ttu-id="0ad6f-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-149">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-150">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-151">System-Flags</span></span>           | <span data-ttu-id="0ad6f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-152">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-153">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-154">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0ad6f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ad6f-155">Windows Server 2003</span></span>



| <span data-ttu-id="0ad6f-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-156">Entry</span></span> | <span data-ttu-id="0ad6f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-160">System-Only</span></span>            | <span data-ttu-id="0ad6f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-161">False</span></span>                                                |
| <span data-ttu-id="0ad6f-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-163">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-164">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-165">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-165">False</span></span>                                                |
| <span data-ttu-id="0ad6f-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-166">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-167">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-172">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-173">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-174">System-Flags</span></span>           | <span data-ttu-id="0ad6f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-175">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-176">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-177">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0ad6f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0ad6f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0ad6f-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-179">Entry</span></span> | <span data-ttu-id="0ad6f-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-183">System-Only</span></span>            | <span data-ttu-id="0ad6f-184">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-184">False</span></span>                                                |
| <span data-ttu-id="0ad6f-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-186">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-187">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-188">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-188">False</span></span>                                                |
| <span data-ttu-id="0ad6f-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-189">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-190">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-195">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-196">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-197">System-Flags</span></span>           | <span data-ttu-id="0ad6f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-198">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-199">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-200">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0ad6f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ad6f-201">Windows Server 2008</span></span>



| <span data-ttu-id="0ad6f-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-202">Entry</span></span> | <span data-ttu-id="0ad6f-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-206">System-Only</span></span>            | <span data-ttu-id="0ad6f-207">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-207">False</span></span>                                                |
| <span data-ttu-id="0ad6f-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-209">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-210">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-211">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-211">False</span></span>                                                |
| <span data-ttu-id="0ad6f-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-212">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-213">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-218">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-219">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-220">System-Flags</span></span>           | <span data-ttu-id="0ad6f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-221">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-222">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-223">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0ad6f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ad6f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0ad6f-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-225">Entry</span></span> | <span data-ttu-id="0ad6f-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-229">System-Only</span></span>            | <span data-ttu-id="0ad6f-230">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-230">False</span></span>                                                |
| <span data-ttu-id="0ad6f-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-232">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-233">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-234">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-234">False</span></span>                                                |
| <span data-ttu-id="0ad6f-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-235">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-236">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-241">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-242">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-243">System-Flags</span></span>           | <span data-ttu-id="0ad6f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-244">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-245">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-246">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0ad6f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ad6f-247">Windows Server 2012</span></span>



| <span data-ttu-id="0ad6f-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="0ad6f-248">Entry</span></span> | <span data-ttu-id="0ad6f-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad6f-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0ad6f-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0ad6f-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad6f-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0ad6f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad6f-252">System-Only</span></span>            | <span data-ttu-id="0ad6f-253">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-253">False</span></span>                                                |
| <span data-ttu-id="0ad6f-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0ad6f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad6f-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-255">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0ad6f-256">Is Indexed</span></span>             | <span data-ttu-id="0ad6f-257">Faux</span><span class="sxs-lookup"><span data-stu-id="0ad6f-257">False</span></span>                                                |
| <span data-ttu-id="0ad6f-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0ad6f-258">In Global Catalog</span></span>      | <span data-ttu-id="0ad6f-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="0ad6f-259">True</span></span>                                                 |
| <span data-ttu-id="0ad6f-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0ad6f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad6f-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0ad6f-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0ad6f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad6f-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad6f-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0ad6f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-264">Search-Flags</span></span>           | <span data-ttu-id="0ad6f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad6f-265">0x00000000</span></span>                                           |
| <span data-ttu-id="0ad6f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad6f-266">System-Flags</span></span>           | <span data-ttu-id="0ad6f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad6f-267">0x00000010</span></span>                                           |
| <span data-ttu-id="0ad6f-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0ad6f-268">Classes used in</span></span>        | [<span data-ttu-id="0ad6f-269">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="0ad6f-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





