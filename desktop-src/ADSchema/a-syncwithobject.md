---
title: Sync-with-Object (attribut)
description: Nom unique de l’objet en cours de synchronisation pour la synchronisation de stratégie locale/de groupe builtin SAM.
ms.assetid: d7f4c855-7f53-4e6b-b39b-cb6ce76c6561
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de synchronisation avec attribut d’objet
- Schéma AD de l’attribut syncWithObject
topic_type:
- apiref
api_name:
- Sync-With-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901f5b87b5bfca6118213c6ba6f535aada4a4b3d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744524"
---
# <a name="sync-with-object-attribute"></a><span data-ttu-id="a4f4a-105">Sync-with-Object (attribut)</span><span class="sxs-lookup"><span data-stu-id="a4f4a-105">Sync-With-Object attribute</span></span>

<span data-ttu-id="a4f4a-106">Nom unique de l’objet en cours de synchronisation pour la synchronisation de stratégie locale/de groupe builtin SAM.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-106">Distinguished name of the object being synchronized for the SAM builtin group/local policy synchronization.</span></span>



| <span data-ttu-id="a4f4a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-107">Entry</span></span> | <span data-ttu-id="a4f4a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a4f4a-109">CN</span><span class="sxs-lookup"><span data-stu-id="a4f4a-109">CN</span></span>                | <span data-ttu-id="a4f4a-110">Synchronisation avec objet</span><span class="sxs-lookup"><span data-stu-id="a4f4a-110">Sync-With-Object</span></span>                        |
| <span data-ttu-id="a4f4a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4f4a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a4f4a-112">syncWithObject</span><span class="sxs-lookup"><span data-stu-id="a4f4a-112">syncWithObject</span></span>                          |
| <span data-ttu-id="a4f4a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="a4f4a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a4f4a-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a4f4a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="a4f4a-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a4f4a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a4f4a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-116">Attribute-Id</span></span>      | <span data-ttu-id="a4f4a-117">1.2.840.113556.1.4.664</span><span class="sxs-lookup"><span data-stu-id="a4f4a-117">1.2.840.113556.1.4.664</span></span>                  |
| <span data-ttu-id="a4f4a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4f4a-118">System-Id-Guid</span></span>    | <span data-ttu-id="a4f4a-119">037651e2-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a4f4a-119">037651e2-441d-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="a4f4a-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f4a-120">Syntax</span></span>            | [<span data-ttu-id="a4f4a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a4f4a-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a4f4a-122">Implementations</span></span>

-   [<span data-ttu-id="a4f4a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a4f4a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4f4a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4f4a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4f4a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4f4a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4f4a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a4f4a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4f4a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a4f4a-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-130">Entry</span></span> | <span data-ttu-id="a4f4a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-134">System-Only</span></span>            | <span data-ttu-id="a4f4a-135">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-135">False</span></span>        |
| <span data-ttu-id="a4f4a-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-137">True</span></span>         |
| <span data-ttu-id="a4f4a-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-138">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-139">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-139">False</span></span>        |
| <span data-ttu-id="a4f4a-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-140">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-141">False</span></span>        |
| <span data-ttu-id="a4f4a-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-146">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-147">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-148">System-Flags</span></span>           | <span data-ttu-id="a4f4a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-149">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="a4f4a-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4f4a-151">Windows Server 2003</span></span>



| <span data-ttu-id="a4f4a-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-152">Entry</span></span> | <span data-ttu-id="a4f4a-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-154">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-156">System-Only</span></span>            | <span data-ttu-id="a4f4a-157">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-157">False</span></span>        |
| <span data-ttu-id="a4f4a-158">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-158">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-159">True</span></span>         |
| <span data-ttu-id="a4f4a-160">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-160">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-161">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-161">False</span></span>        |
| <span data-ttu-id="a4f4a-162">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-162">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-163">False</span></span>        |
| <span data-ttu-id="a4f4a-164">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-165">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-168">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-169">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-170">System-Flags</span></span>           | <span data-ttu-id="a4f4a-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-171">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-172">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4f4a-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4f4a-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4f4a-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-174">Entry</span></span> | <span data-ttu-id="a4f4a-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-176">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-178">System-Only</span></span>            | <span data-ttu-id="a4f4a-179">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-179">False</span></span>        |
| <span data-ttu-id="a4f4a-180">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-180">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-181">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-181">True</span></span>         |
| <span data-ttu-id="a4f4a-182">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-182">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-183">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-183">False</span></span>        |
| <span data-ttu-id="a4f4a-184">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-184">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-185">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-185">False</span></span>        |
| <span data-ttu-id="a4f4a-186">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-187">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-190">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-191">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-192">System-Flags</span></span>           | <span data-ttu-id="a4f4a-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-193">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-194">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="a4f4a-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4f4a-195">Windows Server 2008</span></span>



| <span data-ttu-id="a4f4a-196">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-196">Entry</span></span> | <span data-ttu-id="a4f4a-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-198">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-200">System-Only</span></span>            | <span data-ttu-id="a4f4a-201">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-201">False</span></span>        |
| <span data-ttu-id="a4f4a-202">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-202">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-203">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-203">True</span></span>         |
| <span data-ttu-id="a4f4a-204">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-204">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-205">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-205">False</span></span>        |
| <span data-ttu-id="a4f4a-206">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-206">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-207">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-207">False</span></span>        |
| <span data-ttu-id="a4f4a-208">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-209">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-212">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-213">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-214">System-Flags</span></span>           | <span data-ttu-id="a4f4a-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-215">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-216">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4f4a-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4f4a-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4f4a-218">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-218">Entry</span></span> | <span data-ttu-id="a4f4a-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-220">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-222">System-Only</span></span>            | <span data-ttu-id="a4f4a-223">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-223">False</span></span>        |
| <span data-ttu-id="a4f4a-224">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-224">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-225">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-225">True</span></span>         |
| <span data-ttu-id="a4f4a-226">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-226">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-227">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-227">False</span></span>        |
| <span data-ttu-id="a4f4a-228">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-228">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-229">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-229">False</span></span>        |
| <span data-ttu-id="a4f4a-230">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-231">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-234">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-235">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-236">System-Flags</span></span>           | <span data-ttu-id="a4f4a-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-237">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-238">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="a4f4a-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4f4a-239">Windows Server 2012</span></span>



| <span data-ttu-id="a4f4a-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="a4f4a-240">Entry</span></span> | <span data-ttu-id="a4f4a-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4a-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a4f4a-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a4f4a-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4f4a-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a4f4a-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4f4a-244">System-Only</span></span>            | <span data-ttu-id="a4f4a-245">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-245">False</span></span>        |
| <span data-ttu-id="a4f4a-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a4f4a-246">Is-Single-Valued</span></span>       | <span data-ttu-id="a4f4a-247">Vrai</span><span class="sxs-lookup"><span data-stu-id="a4f4a-247">True</span></span>         |
| <span data-ttu-id="a4f4a-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a4f4a-248">Is Indexed</span></span>             | <span data-ttu-id="a4f4a-249">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-249">False</span></span>        |
| <span data-ttu-id="a4f4a-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a4f4a-250">In Global Catalog</span></span>      | <span data-ttu-id="a4f4a-251">Faux</span><span class="sxs-lookup"><span data-stu-id="a4f4a-251">False</span></span>        |
| <span data-ttu-id="a4f4a-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a4f4a-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4f4a-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a4f4a-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a4f4a-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4f4a-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a4f4a-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4f4a-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a4f4a-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-256">Search-Flags</span></span>           | <span data-ttu-id="a4f4a-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4f4a-257">0x00000000</span></span>   |
| <span data-ttu-id="a4f4a-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4f4a-258">System-Flags</span></span>           | <span data-ttu-id="a4f4a-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4f4a-259">0x00000010</span></span>   |
| <span data-ttu-id="a4f4a-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a4f4a-260">Classes used in</span></span>        | \-           |



 

 




