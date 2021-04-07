---
title: Attribut de temps de création builtin
description: L’attribut builtin-Creation-Time est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut builtin-Creation-Time
- Schéma AD de l’attribut builtinCreationTime
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845621"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="2766d-105">Attribut de temps de création builtin</span><span class="sxs-lookup"><span data-stu-id="2766d-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="2766d-106">L’attribut **BuiltIn-Creation-Time** est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="2766d-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="2766d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-107">Entry</span></span> | <span data-ttu-id="2766d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2766d-109">CN</span><span class="sxs-lookup"><span data-stu-id="2766d-109">CN</span></span>                | <span data-ttu-id="2766d-110">Au moment de la création builtin</span><span class="sxs-lookup"><span data-stu-id="2766d-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="2766d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2766d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2766d-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="2766d-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="2766d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="2766d-113">Size</span></span>              | <span data-ttu-id="2766d-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="2766d-114">8 bytes</span></span>                              |
| <span data-ttu-id="2766d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2766d-115">Update Privilege</span></span>  | <span data-ttu-id="2766d-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="2766d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2766d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2766d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2766d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-118">Attribute-Id</span></span>      | <span data-ttu-id="2766d-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="2766d-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="2766d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2766d-120">System-Id-Guid</span></span>    | <span data-ttu-id="2766d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2766d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2766d-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2766d-122">Syntax</span></span>            | [<span data-ttu-id="2766d-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="2766d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2766d-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2766d-124">Implementations</span></span>

-   [<span data-ttu-id="2766d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2766d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2766d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2766d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2766d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2766d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2766d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2766d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2766d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2766d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2766d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2766d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2766d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2766d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2766d-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-132">Entry</span></span> | <span data-ttu-id="2766d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-136">System-Only</span></span>            | <span data-ttu-id="2766d-137">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-137">False</span></span>                                        |
| <span data-ttu-id="2766d-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-139">True</span></span>                                         |
| <span data-ttu-id="2766d-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-140">Is Indexed</span></span>             | <span data-ttu-id="2766d-141">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-141">False</span></span>                                        |
| <span data-ttu-id="2766d-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-142">In Global Catalog</span></span>      | <span data-ttu-id="2766d-143">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-143">False</span></span>                                        |
| <span data-ttu-id="2766d-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-148">Search-Flags</span></span>           | <span data-ttu-id="2766d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-150">System-Flags</span></span>           | <span data-ttu-id="2766d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-151">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-152">Classes used in</span></span>        | [<span data-ttu-id="2766d-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2766d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2766d-154">Windows Server 2003</span></span>



| <span data-ttu-id="2766d-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-155">Entry</span></span> | <span data-ttu-id="2766d-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-159">System-Only</span></span>            | <span data-ttu-id="2766d-160">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-160">False</span></span>                                        |
| <span data-ttu-id="2766d-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-162">True</span></span>                                         |
| <span data-ttu-id="2766d-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-163">Is Indexed</span></span>             | <span data-ttu-id="2766d-164">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-164">False</span></span>                                        |
| <span data-ttu-id="2766d-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-165">In Global Catalog</span></span>      | <span data-ttu-id="2766d-166">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-166">False</span></span>                                        |
| <span data-ttu-id="2766d-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-171">Search-Flags</span></span>           | <span data-ttu-id="2766d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-173">System-Flags</span></span>           | <span data-ttu-id="2766d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-174">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-175">Classes used in</span></span>        | [<span data-ttu-id="2766d-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2766d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2766d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2766d-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-178">Entry</span></span> | <span data-ttu-id="2766d-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-182">System-Only</span></span>            | <span data-ttu-id="2766d-183">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-183">False</span></span>                                        |
| <span data-ttu-id="2766d-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-185">True</span></span>                                         |
| <span data-ttu-id="2766d-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-186">Is Indexed</span></span>             | <span data-ttu-id="2766d-187">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-187">False</span></span>                                        |
| <span data-ttu-id="2766d-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-188">In Global Catalog</span></span>      | <span data-ttu-id="2766d-189">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-189">False</span></span>                                        |
| <span data-ttu-id="2766d-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-194">Search-Flags</span></span>           | <span data-ttu-id="2766d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-195">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-196">System-Flags</span></span>           | <span data-ttu-id="2766d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-197">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-198">Classes used in</span></span>        | [<span data-ttu-id="2766d-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2766d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2766d-200">Windows Server 2008</span></span>



| <span data-ttu-id="2766d-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-201">Entry</span></span> | <span data-ttu-id="2766d-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-205">System-Only</span></span>            | <span data-ttu-id="2766d-206">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-206">False</span></span>                                        |
| <span data-ttu-id="2766d-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-208">True</span></span>                                         |
| <span data-ttu-id="2766d-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-209">Is Indexed</span></span>             | <span data-ttu-id="2766d-210">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-210">False</span></span>                                        |
| <span data-ttu-id="2766d-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-211">In Global Catalog</span></span>      | <span data-ttu-id="2766d-212">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-212">False</span></span>                                        |
| <span data-ttu-id="2766d-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-217">Search-Flags</span></span>           | <span data-ttu-id="2766d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-218">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-219">System-Flags</span></span>           | <span data-ttu-id="2766d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-220">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-221">Classes used in</span></span>        | [<span data-ttu-id="2766d-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2766d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2766d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2766d-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-224">Entry</span></span> | <span data-ttu-id="2766d-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-228">System-Only</span></span>            | <span data-ttu-id="2766d-229">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-229">False</span></span>                                        |
| <span data-ttu-id="2766d-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-231">True</span></span>                                         |
| <span data-ttu-id="2766d-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-232">Is Indexed</span></span>             | <span data-ttu-id="2766d-233">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-233">False</span></span>                                        |
| <span data-ttu-id="2766d-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-234">In Global Catalog</span></span>      | <span data-ttu-id="2766d-235">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-235">False</span></span>                                        |
| <span data-ttu-id="2766d-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-240">Search-Flags</span></span>           | <span data-ttu-id="2766d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-241">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-242">System-Flags</span></span>           | <span data-ttu-id="2766d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-243">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-244">Classes used in</span></span>        | [<span data-ttu-id="2766d-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2766d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2766d-246">Windows Server 2012</span></span>



| <span data-ttu-id="2766d-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="2766d-247">Entry</span></span> | <span data-ttu-id="2766d-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="2766d-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2766d-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2766d-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2766d-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2766d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2766d-251">System-Only</span></span>            | <span data-ttu-id="2766d-252">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-252">False</span></span>                                        |
| <span data-ttu-id="2766d-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2766d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2766d-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="2766d-254">True</span></span>                                         |
| <span data-ttu-id="2766d-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2766d-255">Is Indexed</span></span>             | <span data-ttu-id="2766d-256">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-256">False</span></span>                                        |
| <span data-ttu-id="2766d-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2766d-257">In Global Catalog</span></span>      | <span data-ttu-id="2766d-258">Faux</span><span class="sxs-lookup"><span data-stu-id="2766d-258">False</span></span>                                        |
| <span data-ttu-id="2766d-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2766d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2766d-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2766d-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2766d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2766d-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2766d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2766d-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2766d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-263">Search-Flags</span></span>           | <span data-ttu-id="2766d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2766d-264">0x00000000</span></span>                                   |
| <span data-ttu-id="2766d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2766d-265">System-Flags</span></span>           | <span data-ttu-id="2766d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2766d-266">0x00000010</span></span>                                   |
| <span data-ttu-id="2766d-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2766d-267">Classes used in</span></span>        | [<span data-ttu-id="2766d-268">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="2766d-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





