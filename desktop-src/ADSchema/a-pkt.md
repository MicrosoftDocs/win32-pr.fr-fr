---
title: Attribut PKT
description: Table de connaissance de la partition DFS. Décrit la structure d’une hiérarchie de système de fichiers DFS.
ms.assetid: a7b2e9ee-04c0-40e8-8670-8261575a45ab
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut PKT
- Schéma AD de l’attribut pKT
topic_type:
- apiref
api_name:
- PKT
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647e2730b254121763b6598a8ec365b376dd52d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107008"
---
# <a name="pkt-attribute"></a><span data-ttu-id="d2a3b-106">Attribut PKT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-106">PKT attribute</span></span>

<span data-ttu-id="d2a3b-107">Table de connaissance de la partition DFS.</span><span class="sxs-lookup"><span data-stu-id="d2a3b-107">DFS Partition Knowledge Table.</span></span> <span data-ttu-id="d2a3b-108">Décrit la structure d’une hiérarchie de système de fichiers DFS.</span><span class="sxs-lookup"><span data-stu-id="d2a3b-108">Describes the structure of a Distributed File System hierarchy.</span></span>



| <span data-ttu-id="d2a3b-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-109">Entry</span></span> | <span data-ttu-id="d2a3b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d2a3b-111">CN</span><span class="sxs-lookup"><span data-stu-id="d2a3b-111">CN</span></span>                | <span data-ttu-id="d2a3b-112">PKT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-112">PKT</span></span>                                                   |
| <span data-ttu-id="d2a3b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2a3b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d2a3b-114">pKT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-114">pKT</span></span>                                                   |
| <span data-ttu-id="d2a3b-115">Taille</span><span class="sxs-lookup"><span data-stu-id="d2a3b-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="d2a3b-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d2a3b-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="d2a3b-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d2a3b-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="d2a3b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-118">Attribute-Id</span></span>      | <span data-ttu-id="d2a3b-119">1.2.840.113556.1.4.206</span><span class="sxs-lookup"><span data-stu-id="d2a3b-119">1.2.840.113556.1.4.206</span></span>                                |
| <span data-ttu-id="d2a3b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2a3b-120">System-Id-Guid</span></span>    | <span data-ttu-id="d2a3b-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="d2a3b-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span></span>                  |
| <span data-ttu-id="d2a3b-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2a3b-122">Syntax</span></span>            | [<span data-ttu-id="d2a3b-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d2a3b-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d2a3b-124">Implementations</span></span>

-   [<span data-ttu-id="d2a3b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2a3b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2a3b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2a3b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2a3b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2a3b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2a3b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2a3b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d2a3b-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-132">Entry</span></span> | <span data-ttu-id="d2a3b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-133">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-134">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-135">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-136">System-Only</span></span>            | <span data-ttu-id="d2a3b-137">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-137">False</span></span>                                |
| <span data-ttu-id="d2a3b-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-139">True</span></span>                                 |
| <span data-ttu-id="d2a3b-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-140">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-141">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-141">False</span></span>                                |
| <span data-ttu-id="d2a3b-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-142">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-143">False</span></span>                                |
| <span data-ttu-id="d2a3b-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-145">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-146">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-147">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-148">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-149">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-150">System-Flags</span></span>           | <span data-ttu-id="d2a3b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-151">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-152">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-153">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-153">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2a3b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2a3b-154">Windows Server 2003</span></span>



| <span data-ttu-id="d2a3b-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-155">Entry</span></span> | <span data-ttu-id="d2a3b-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-156">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-157">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-158">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-159">System-Only</span></span>            | <span data-ttu-id="d2a3b-160">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-160">False</span></span>                                |
| <span data-ttu-id="d2a3b-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-162">True</span></span>                                 |
| <span data-ttu-id="d2a3b-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-163">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-164">False</span></span>                                |
| <span data-ttu-id="d2a3b-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-165">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-166">False</span></span>                                |
| <span data-ttu-id="d2a3b-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-168">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-169">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-170">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-171">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-172">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-173">System-Flags</span></span>           | <span data-ttu-id="d2a3b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-174">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-175">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-176">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-176">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2a3b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2a3b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2a3b-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-178">Entry</span></span> | <span data-ttu-id="d2a3b-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-179">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-180">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-181">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-182">System-Only</span></span>            | <span data-ttu-id="d2a3b-183">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-183">False</span></span>                                |
| <span data-ttu-id="d2a3b-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-185">True</span></span>                                 |
| <span data-ttu-id="d2a3b-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-186">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-187">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-187">False</span></span>                                |
| <span data-ttu-id="d2a3b-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-188">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-189">False</span></span>                                |
| <span data-ttu-id="d2a3b-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-191">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-192">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-193">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-194">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-195">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-196">System-Flags</span></span>           | <span data-ttu-id="d2a3b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-197">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-198">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-199">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-199">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2a3b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a3b-200">Windows Server 2008</span></span>



| <span data-ttu-id="d2a3b-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-201">Entry</span></span> | <span data-ttu-id="d2a3b-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-202">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-203">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-204">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-205">System-Only</span></span>            | <span data-ttu-id="d2a3b-206">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-206">False</span></span>                                |
| <span data-ttu-id="d2a3b-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-208">True</span></span>                                 |
| <span data-ttu-id="d2a3b-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-209">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-210">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-210">False</span></span>                                |
| <span data-ttu-id="d2a3b-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-211">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-212">False</span></span>                                |
| <span data-ttu-id="d2a3b-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-214">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-215">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-216">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-217">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-218">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-219">System-Flags</span></span>           | <span data-ttu-id="d2a3b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-220">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-221">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-222">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-222">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2a3b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2a3b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2a3b-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-224">Entry</span></span> | <span data-ttu-id="d2a3b-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-225">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-226">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-227">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-228">System-Only</span></span>            | <span data-ttu-id="d2a3b-229">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-229">False</span></span>                                |
| <span data-ttu-id="d2a3b-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-231">True</span></span>                                 |
| <span data-ttu-id="d2a3b-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-232">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-233">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-233">False</span></span>                                |
| <span data-ttu-id="d2a3b-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-234">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-235">False</span></span>                                |
| <span data-ttu-id="d2a3b-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-237">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-238">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-239">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-240">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-241">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-242">System-Flags</span></span>           | <span data-ttu-id="d2a3b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-243">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-244">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-245">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-245">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2a3b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2a3b-246">Windows Server 2012</span></span>



| <span data-ttu-id="d2a3b-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2a3b-247">Entry</span></span> | <span data-ttu-id="d2a3b-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a3b-248">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="d2a3b-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2a3b-249">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2a3b-250">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="d2a3b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2a3b-251">System-Only</span></span>            | <span data-ttu-id="d2a3b-252">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-252">False</span></span>                                |
| <span data-ttu-id="d2a3b-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2a3b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d2a3b-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2a3b-254">True</span></span>                                 |
| <span data-ttu-id="d2a3b-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2a3b-255">Is Indexed</span></span>             | <span data-ttu-id="d2a3b-256">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-256">False</span></span>                                |
| <span data-ttu-id="d2a3b-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2a3b-257">In Global Catalog</span></span>      | <span data-ttu-id="d2a3b-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d2a3b-258">False</span></span>                                |
| <span data-ttu-id="d2a3b-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2a3b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2a3b-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2a3b-260">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="d2a3b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2a3b-261">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2a3b-262">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="d2a3b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-263">Search-Flags</span></span>           | <span data-ttu-id="d2a3b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2a3b-264">0x00000000</span></span>                           |
| <span data-ttu-id="d2a3b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2a3b-265">System-Flags</span></span>           | <span data-ttu-id="d2a3b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2a3b-266">0x00000010</span></span>                           |
| <span data-ttu-id="d2a3b-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2a3b-267">Classes used in</span></span>        | [<span data-ttu-id="d2a3b-268">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="d2a3b-268">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





