---
title: Attribut LSA-modified-Count
description: L’attribut LSA-modified-Count est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.
ms.assetid: 6af5931c-5d4f-4061-81a1-e8947d760abc
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs LSA-modifié-Count
- Schéma AD de l’attribut lSAModifiedCount
topic_type:
- apiref
api_name:
- LSA-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042d4d52974457eb1853a3705adb87cc24a7dc3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516129"
---
# <a name="lsa-modified-count-attribute"></a><span data-ttu-id="4a073-105">Attribut LSA-modified-Count</span><span class="sxs-lookup"><span data-stu-id="4a073-105">LSA-Modified-Count attribute</span></span>

<span data-ttu-id="4a073-106">L’attribut **LSA-modified-Count** est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="4a073-106">The **LSA-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="4a073-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-107">Entry</span></span> | <span data-ttu-id="4a073-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4a073-109">CN</span><span class="sxs-lookup"><span data-stu-id="4a073-109">CN</span></span>                | <span data-ttu-id="4a073-110">LSA-modifié-nombre</span><span class="sxs-lookup"><span data-stu-id="4a073-110">LSA-Modified-Count</span></span>                   |
| <span data-ttu-id="4a073-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a073-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4a073-112">lSAModifiedCount</span><span class="sxs-lookup"><span data-stu-id="4a073-112">lSAModifiedCount</span></span>                     |
| <span data-ttu-id="4a073-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4a073-113">Size</span></span>              | <span data-ttu-id="4a073-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="4a073-114">8 bytes</span></span>                              |
| <span data-ttu-id="4a073-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4a073-115">Update Privilege</span></span>  | <span data-ttu-id="4a073-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="4a073-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4a073-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4a073-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4a073-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-118">Attribute-Id</span></span>      | <span data-ttu-id="4a073-119">1.2.840.113556.1.4.67</span><span class="sxs-lookup"><span data-stu-id="4a073-119">1.2.840.113556.1.4.67</span></span>                |
| <span data-ttu-id="4a073-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a073-120">System-Id-Guid</span></span>    | <span data-ttu-id="4a073-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4a073-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="4a073-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a073-122">Syntax</span></span>            | [<span data-ttu-id="4a073-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="4a073-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4a073-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4a073-124">Implementations</span></span>

-   [<span data-ttu-id="4a073-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a073-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a073-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a073-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a073-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a073-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a073-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a073-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a073-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a073-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a073-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a073-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a073-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a073-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4a073-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-132">Entry</span></span> | <span data-ttu-id="4a073-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-136">System-Only</span></span>            | <span data-ttu-id="4a073-137">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-137">False</span></span>                                        |
| <span data-ttu-id="4a073-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-139">True</span></span>                                         |
| <span data-ttu-id="4a073-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-140">Is Indexed</span></span>             | <span data-ttu-id="4a073-141">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-141">False</span></span>                                        |
| <span data-ttu-id="4a073-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-142">In Global Catalog</span></span>      | <span data-ttu-id="4a073-143">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-143">False</span></span>                                        |
| <span data-ttu-id="4a073-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-148">Search-Flags</span></span>           | <span data-ttu-id="4a073-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-150">System-Flags</span></span>           | <span data-ttu-id="4a073-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-152">Classes used in</span></span>        | [<span data-ttu-id="4a073-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a073-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a073-154">Windows Server 2003</span></span>



| <span data-ttu-id="4a073-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-155">Entry</span></span> | <span data-ttu-id="4a073-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-159">System-Only</span></span>            | <span data-ttu-id="4a073-160">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-160">False</span></span>                                        |
| <span data-ttu-id="4a073-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-162">True</span></span>                                         |
| <span data-ttu-id="4a073-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-163">Is Indexed</span></span>             | <span data-ttu-id="4a073-164">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-164">False</span></span>                                        |
| <span data-ttu-id="4a073-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-165">In Global Catalog</span></span>      | <span data-ttu-id="4a073-166">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-166">False</span></span>                                        |
| <span data-ttu-id="4a073-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-171">Search-Flags</span></span>           | <span data-ttu-id="4a073-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-173">System-Flags</span></span>           | <span data-ttu-id="4a073-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-175">Classes used in</span></span>        | [<span data-ttu-id="4a073-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a073-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a073-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a073-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-178">Entry</span></span> | <span data-ttu-id="4a073-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-182">System-Only</span></span>            | <span data-ttu-id="4a073-183">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-183">False</span></span>                                        |
| <span data-ttu-id="4a073-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-185">True</span></span>                                         |
| <span data-ttu-id="4a073-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-186">Is Indexed</span></span>             | <span data-ttu-id="4a073-187">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-187">False</span></span>                                        |
| <span data-ttu-id="4a073-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-188">In Global Catalog</span></span>      | <span data-ttu-id="4a073-189">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-189">False</span></span>                                        |
| <span data-ttu-id="4a073-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-194">Search-Flags</span></span>           | <span data-ttu-id="4a073-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-196">System-Flags</span></span>           | <span data-ttu-id="4a073-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-198">Classes used in</span></span>        | [<span data-ttu-id="4a073-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a073-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a073-200">Windows Server 2008</span></span>



| <span data-ttu-id="4a073-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-201">Entry</span></span> | <span data-ttu-id="4a073-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-205">System-Only</span></span>            | <span data-ttu-id="4a073-206">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-206">False</span></span>                                        |
| <span data-ttu-id="4a073-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-208">True</span></span>                                         |
| <span data-ttu-id="4a073-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-209">Is Indexed</span></span>             | <span data-ttu-id="4a073-210">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-210">False</span></span>                                        |
| <span data-ttu-id="4a073-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-211">In Global Catalog</span></span>      | <span data-ttu-id="4a073-212">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-212">False</span></span>                                        |
| <span data-ttu-id="4a073-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-217">Search-Flags</span></span>           | <span data-ttu-id="4a073-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-219">System-Flags</span></span>           | <span data-ttu-id="4a073-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-221">Classes used in</span></span>        | [<span data-ttu-id="4a073-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a073-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a073-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a073-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-224">Entry</span></span> | <span data-ttu-id="4a073-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-228">System-Only</span></span>            | <span data-ttu-id="4a073-229">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-229">False</span></span>                                        |
| <span data-ttu-id="4a073-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-231">True</span></span>                                         |
| <span data-ttu-id="4a073-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-232">Is Indexed</span></span>             | <span data-ttu-id="4a073-233">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-233">False</span></span>                                        |
| <span data-ttu-id="4a073-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-234">In Global Catalog</span></span>      | <span data-ttu-id="4a073-235">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-235">False</span></span>                                        |
| <span data-ttu-id="4a073-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-240">Search-Flags</span></span>           | <span data-ttu-id="4a073-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-242">System-Flags</span></span>           | <span data-ttu-id="4a073-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-244">Classes used in</span></span>        | [<span data-ttu-id="4a073-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a073-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a073-246">Windows Server 2012</span></span>



| <span data-ttu-id="4a073-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a073-247">Entry</span></span> | <span data-ttu-id="4a073-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a073-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a073-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4a073-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a073-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a073-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a073-251">System-Only</span></span>            | <span data-ttu-id="4a073-252">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-252">False</span></span>                                        |
| <span data-ttu-id="4a073-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4a073-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4a073-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="4a073-254">True</span></span>                                         |
| <span data-ttu-id="4a073-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4a073-255">Is Indexed</span></span>             | <span data-ttu-id="4a073-256">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-256">False</span></span>                                        |
| <span data-ttu-id="4a073-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4a073-257">In Global Catalog</span></span>      | <span data-ttu-id="4a073-258">Faux</span><span class="sxs-lookup"><span data-stu-id="4a073-258">False</span></span>                                        |
| <span data-ttu-id="4a073-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4a073-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a073-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4a073-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a073-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a073-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a073-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a073-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a073-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-263">Search-Flags</span></span>           | <span data-ttu-id="4a073-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a073-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4a073-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a073-265">System-Flags</span></span>           | <span data-ttu-id="4a073-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a073-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4a073-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4a073-267">Classes used in</span></span>        | [<span data-ttu-id="4a073-268">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="4a073-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





