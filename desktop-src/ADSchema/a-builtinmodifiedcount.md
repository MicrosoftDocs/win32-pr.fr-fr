---
title: Attribut builtin-modified-Count
description: L’attribut builtin-modified-Count est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut builtin-modified-Count
- Schéma AD de l’attribut builtinModifiedCount
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108231"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="6ce45-105">Attribut builtin-modified-Count</span><span class="sxs-lookup"><span data-stu-id="6ce45-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="6ce45-106">L’attribut **BuiltIn-modified-Count** est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="6ce45-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="6ce45-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-107">Entry</span></span> | <span data-ttu-id="6ce45-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6ce45-109">CN</span><span class="sxs-lookup"><span data-stu-id="6ce45-109">CN</span></span>                | <span data-ttu-id="6ce45-110">Builtin-modifié-nombre</span><span class="sxs-lookup"><span data-stu-id="6ce45-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="6ce45-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6ce45-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6ce45-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="6ce45-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="6ce45-113">Taille</span><span class="sxs-lookup"><span data-stu-id="6ce45-113">Size</span></span>              | <span data-ttu-id="6ce45-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="6ce45-114">8 bytes</span></span>                              |
| <span data-ttu-id="6ce45-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6ce45-115">Update Privilege</span></span>  | <span data-ttu-id="6ce45-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="6ce45-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="6ce45-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6ce45-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6ce45-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-118">Attribute-Id</span></span>      | <span data-ttu-id="6ce45-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="6ce45-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="6ce45-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6ce45-120">System-Id-Guid</span></span>    | <span data-ttu-id="6ce45-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6ce45-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6ce45-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ce45-122">Syntax</span></span>            | [<span data-ttu-id="6ce45-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="6ce45-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6ce45-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6ce45-124">Implementations</span></span>

-   [<span data-ttu-id="6ce45-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6ce45-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6ce45-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ce45-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ce45-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ce45-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ce45-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ce45-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ce45-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ce45-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ce45-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ce45-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6ce45-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ce45-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6ce45-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-132">Entry</span></span> | <span data-ttu-id="6ce45-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-136">System-Only</span></span>            | <span data-ttu-id="6ce45-137">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-137">False</span></span>                                        |
| <span data-ttu-id="6ce45-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-139">True</span></span>                                         |
| <span data-ttu-id="6ce45-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-140">Is Indexed</span></span>             | <span data-ttu-id="6ce45-141">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-141">False</span></span>                                        |
| <span data-ttu-id="6ce45-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-142">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-143">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-143">False</span></span>                                        |
| <span data-ttu-id="6ce45-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-148">Search-Flags</span></span>           | <span data-ttu-id="6ce45-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-149">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-150">System-Flags</span></span>           | <span data-ttu-id="6ce45-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-151">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-152">Classes used in</span></span>        | [<span data-ttu-id="6ce45-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6ce45-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ce45-154">Windows Server 2003</span></span>



| <span data-ttu-id="6ce45-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-155">Entry</span></span> | <span data-ttu-id="6ce45-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-159">System-Only</span></span>            | <span data-ttu-id="6ce45-160">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-160">False</span></span>                                        |
| <span data-ttu-id="6ce45-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-162">True</span></span>                                         |
| <span data-ttu-id="6ce45-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-163">Is Indexed</span></span>             | <span data-ttu-id="6ce45-164">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-164">False</span></span>                                        |
| <span data-ttu-id="6ce45-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-165">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-166">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-166">False</span></span>                                        |
| <span data-ttu-id="6ce45-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-171">Search-Flags</span></span>           | <span data-ttu-id="6ce45-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-172">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-173">System-Flags</span></span>           | <span data-ttu-id="6ce45-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-174">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-175">Classes used in</span></span>        | [<span data-ttu-id="6ce45-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ce45-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ce45-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ce45-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-178">Entry</span></span> | <span data-ttu-id="6ce45-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-182">System-Only</span></span>            | <span data-ttu-id="6ce45-183">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-183">False</span></span>                                        |
| <span data-ttu-id="6ce45-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-185">True</span></span>                                         |
| <span data-ttu-id="6ce45-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-186">Is Indexed</span></span>             | <span data-ttu-id="6ce45-187">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-187">False</span></span>                                        |
| <span data-ttu-id="6ce45-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-188">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-189">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-189">False</span></span>                                        |
| <span data-ttu-id="6ce45-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-194">Search-Flags</span></span>           | <span data-ttu-id="6ce45-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-195">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-196">System-Flags</span></span>           | <span data-ttu-id="6ce45-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-197">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-198">Classes used in</span></span>        | [<span data-ttu-id="6ce45-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ce45-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ce45-200">Windows Server 2008</span></span>



| <span data-ttu-id="6ce45-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-201">Entry</span></span> | <span data-ttu-id="6ce45-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-205">System-Only</span></span>            | <span data-ttu-id="6ce45-206">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-206">False</span></span>                                        |
| <span data-ttu-id="6ce45-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-208">True</span></span>                                         |
| <span data-ttu-id="6ce45-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-209">Is Indexed</span></span>             | <span data-ttu-id="6ce45-210">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-210">False</span></span>                                        |
| <span data-ttu-id="6ce45-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-211">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-212">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-212">False</span></span>                                        |
| <span data-ttu-id="6ce45-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-217">Search-Flags</span></span>           | <span data-ttu-id="6ce45-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-218">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-219">System-Flags</span></span>           | <span data-ttu-id="6ce45-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-220">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-221">Classes used in</span></span>        | [<span data-ttu-id="6ce45-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ce45-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ce45-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ce45-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-224">Entry</span></span> | <span data-ttu-id="6ce45-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-228">System-Only</span></span>            | <span data-ttu-id="6ce45-229">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-229">False</span></span>                                        |
| <span data-ttu-id="6ce45-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-231">True</span></span>                                         |
| <span data-ttu-id="6ce45-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-232">Is Indexed</span></span>             | <span data-ttu-id="6ce45-233">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-233">False</span></span>                                        |
| <span data-ttu-id="6ce45-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-234">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-235">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-235">False</span></span>                                        |
| <span data-ttu-id="6ce45-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-240">Search-Flags</span></span>           | <span data-ttu-id="6ce45-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-241">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-242">System-Flags</span></span>           | <span data-ttu-id="6ce45-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-243">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-244">Classes used in</span></span>        | [<span data-ttu-id="6ce45-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ce45-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ce45-246">Windows Server 2012</span></span>



| <span data-ttu-id="6ce45-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ce45-247">Entry</span></span> | <span data-ttu-id="6ce45-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ce45-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ce45-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ce45-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ce45-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ce45-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ce45-251">System-Only</span></span>            | <span data-ttu-id="6ce45-252">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-252">False</span></span>                                        |
| <span data-ttu-id="6ce45-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ce45-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6ce45-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ce45-254">True</span></span>                                         |
| <span data-ttu-id="6ce45-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ce45-255">Is Indexed</span></span>             | <span data-ttu-id="6ce45-256">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-256">False</span></span>                                        |
| <span data-ttu-id="6ce45-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ce45-257">In Global Catalog</span></span>      | <span data-ttu-id="6ce45-258">Faux</span><span class="sxs-lookup"><span data-stu-id="6ce45-258">False</span></span>                                        |
| <span data-ttu-id="6ce45-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ce45-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ce45-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ce45-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ce45-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ce45-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ce45-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ce45-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-263">Search-Flags</span></span>           | <span data-ttu-id="6ce45-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ce45-264">0x00000000</span></span>                                   |
| <span data-ttu-id="6ce45-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ce45-265">System-Flags</span></span>           | <span data-ttu-id="6ce45-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ce45-266">0x00000010</span></span>                                   |
| <span data-ttu-id="6ce45-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ce45-267">Classes used in</span></span>        | [<span data-ttu-id="6ce45-268">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="6ce45-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





