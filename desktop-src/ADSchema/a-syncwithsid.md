---
title: Attribut sync-with-SID
description: Pour la synchronisation de la stratégie locale/objet du groupe builtin SAM, il s’agit du groupe local auquel correspond un objet.
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut sync-with-SID
- Schéma AD de l’attribut syncWithSID
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107938"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="9c94f-105">Attribut sync-with-SID</span><span class="sxs-lookup"><span data-stu-id="9c94f-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="9c94f-106">Pour la synchronisation de la stratégie locale/objet du groupe builtin SAM, il s’agit du groupe local auquel correspond un objet.</span><span class="sxs-lookup"><span data-stu-id="9c94f-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="9c94f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-107">Entry</span></span> | <span data-ttu-id="9c94f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9c94f-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c94f-109">CN</span></span>                | <span data-ttu-id="9c94f-110">Synchronisation avec SID</span><span class="sxs-lookup"><span data-stu-id="9c94f-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="9c94f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c94f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9c94f-112">syncWithSID</span><span class="sxs-lookup"><span data-stu-id="9c94f-112">syncWithSID</span></span>                          |
| <span data-ttu-id="9c94f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9c94f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9c94f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9c94f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9c94f-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9c94f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9c94f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-116">Attribute-Id</span></span>      | <span data-ttu-id="9c94f-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="9c94f-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="9c94f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9c94f-118">System-Id-Guid</span></span>    | <span data-ttu-id="9c94f-119">037651e5-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9c94f-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="9c94f-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c94f-120">Syntax</span></span>            | [<span data-ttu-id="9c94f-121">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="9c94f-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="9c94f-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9c94f-122">Implementations</span></span>

-   [<span data-ttu-id="9c94f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9c94f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9c94f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c94f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c94f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c94f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c94f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c94f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c94f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c94f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c94f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c94f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9c94f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c94f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9c94f-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-130">Entry</span></span> | <span data-ttu-id="9c94f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-134">System-Only</span></span>            | <span data-ttu-id="9c94f-135">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-135">False</span></span>        |
| <span data-ttu-id="9c94f-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-137">True</span></span>         |
| <span data-ttu-id="9c94f-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-138">Is Indexed</span></span>             | <span data-ttu-id="9c94f-139">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-139">False</span></span>        |
| <span data-ttu-id="9c94f-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-140">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-141">False</span></span>        |
| <span data-ttu-id="9c94f-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-146">Search-Flags</span></span>           | <span data-ttu-id="9c94f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-147">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-148">System-Flags</span></span>           | <span data-ttu-id="9c94f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-149">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="9c94f-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c94f-151">Windows Server 2003</span></span>



| <span data-ttu-id="9c94f-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-152">Entry</span></span> | <span data-ttu-id="9c94f-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-154">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-156">System-Only</span></span>            | <span data-ttu-id="9c94f-157">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-157">False</span></span>        |
| <span data-ttu-id="9c94f-158">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-158">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-159">True</span></span>         |
| <span data-ttu-id="9c94f-160">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-160">Is Indexed</span></span>             | <span data-ttu-id="9c94f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-161">False</span></span>        |
| <span data-ttu-id="9c94f-162">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-162">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-163">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-163">False</span></span>        |
| <span data-ttu-id="9c94f-164">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-165">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-168">Search-Flags</span></span>           | <span data-ttu-id="9c94f-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-169">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-170">System-Flags</span></span>           | <span data-ttu-id="9c94f-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-171">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-172">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c94f-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c94f-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c94f-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-174">Entry</span></span> | <span data-ttu-id="9c94f-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-176">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-178">System-Only</span></span>            | <span data-ttu-id="9c94f-179">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-179">False</span></span>        |
| <span data-ttu-id="9c94f-180">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-180">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-181">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-181">True</span></span>         |
| <span data-ttu-id="9c94f-182">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-182">Is Indexed</span></span>             | <span data-ttu-id="9c94f-183">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-183">False</span></span>        |
| <span data-ttu-id="9c94f-184">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-184">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-185">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-185">False</span></span>        |
| <span data-ttu-id="9c94f-186">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-187">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-190">Search-Flags</span></span>           | <span data-ttu-id="9c94f-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-191">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-192">System-Flags</span></span>           | <span data-ttu-id="9c94f-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-193">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-194">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="9c94f-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c94f-195">Windows Server 2008</span></span>



| <span data-ttu-id="9c94f-196">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-196">Entry</span></span> | <span data-ttu-id="9c94f-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-198">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-200">System-Only</span></span>            | <span data-ttu-id="9c94f-201">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-201">False</span></span>        |
| <span data-ttu-id="9c94f-202">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-202">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-203">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-203">True</span></span>         |
| <span data-ttu-id="9c94f-204">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-204">Is Indexed</span></span>             | <span data-ttu-id="9c94f-205">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-205">False</span></span>        |
| <span data-ttu-id="9c94f-206">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-206">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-207">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-207">False</span></span>        |
| <span data-ttu-id="9c94f-208">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-209">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-212">Search-Flags</span></span>           | <span data-ttu-id="9c94f-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-213">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-214">System-Flags</span></span>           | <span data-ttu-id="9c94f-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-215">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-216">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c94f-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c94f-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c94f-218">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-218">Entry</span></span> | <span data-ttu-id="9c94f-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-220">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-222">System-Only</span></span>            | <span data-ttu-id="9c94f-223">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-223">False</span></span>        |
| <span data-ttu-id="9c94f-224">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-224">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-225">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-225">True</span></span>         |
| <span data-ttu-id="9c94f-226">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-226">Is Indexed</span></span>             | <span data-ttu-id="9c94f-227">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-227">False</span></span>        |
| <span data-ttu-id="9c94f-228">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-228">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-229">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-229">False</span></span>        |
| <span data-ttu-id="9c94f-230">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-231">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-234">Search-Flags</span></span>           | <span data-ttu-id="9c94f-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-235">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-236">System-Flags</span></span>           | <span data-ttu-id="9c94f-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-237">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-238">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="9c94f-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c94f-239">Windows Server 2012</span></span>



| <span data-ttu-id="9c94f-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c94f-240">Entry</span></span> | <span data-ttu-id="9c94f-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c94f-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9c94f-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c94f-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c94f-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9c94f-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c94f-244">System-Only</span></span>            | <span data-ttu-id="9c94f-245">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-245">False</span></span>        |
| <span data-ttu-id="9c94f-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c94f-246">Is-Single-Valued</span></span>       | <span data-ttu-id="9c94f-247">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c94f-247">True</span></span>         |
| <span data-ttu-id="9c94f-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c94f-248">Is Indexed</span></span>             | <span data-ttu-id="9c94f-249">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-249">False</span></span>        |
| <span data-ttu-id="9c94f-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c94f-250">In Global Catalog</span></span>      | <span data-ttu-id="9c94f-251">Faux</span><span class="sxs-lookup"><span data-stu-id="9c94f-251">False</span></span>        |
| <span data-ttu-id="9c94f-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c94f-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c94f-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c94f-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9c94f-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c94f-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9c94f-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c94f-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9c94f-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-256">Search-Flags</span></span>           | <span data-ttu-id="9c94f-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c94f-257">0x00000000</span></span>   |
| <span data-ttu-id="9c94f-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c94f-258">System-Flags</span></span>           | <span data-ttu-id="9c94f-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c94f-259">0x00000010</span></span>   |
| <span data-ttu-id="9c94f-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c94f-260">Classes used in</span></span>        | \-           |



 

 




