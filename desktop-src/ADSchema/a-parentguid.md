---
title: Attribut parent-GUID
description: Il s’agit d’un attribut construit, inventé pour prendre en charge le contrôle DirSync. Cet attribut contient l’objectGuid du parent d’un objet lors de la réplication de la création, du changement de nom ou du déplacement d’un objet.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut parent-GUID
- Schéma AD de l’attribut parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845353"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="d4e12-106">Attribut parent-GUID</span><span class="sxs-lookup"><span data-stu-id="d4e12-106">Parent-GUID attribute</span></span>

<span data-ttu-id="d4e12-107">Il s’agit d’un attribut construit, inventé pour prendre en charge le contrôle DirSync.</span><span class="sxs-lookup"><span data-stu-id="d4e12-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="d4e12-108">Cet attribut contient l’objectGuid du parent d’un objet lors de la réplication de la création, du changement de nom ou du déplacement d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d4e12-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="d4e12-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-109">Entry</span></span> | <span data-ttu-id="d4e12-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d4e12-111">CN</span><span class="sxs-lookup"><span data-stu-id="d4e12-111">CN</span></span>                | <span data-ttu-id="d4e12-112">GUID parent</span><span class="sxs-lookup"><span data-stu-id="d4e12-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="d4e12-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d4e12-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d4e12-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="d4e12-114">parentGUID</span></span>                                            |
| <span data-ttu-id="d4e12-115">Taille</span><span class="sxs-lookup"><span data-stu-id="d4e12-115">Size</span></span>              | <span data-ttu-id="d4e12-116">16 octets</span><span class="sxs-lookup"><span data-stu-id="d4e12-116">16 bytes</span></span>                                              |
| <span data-ttu-id="d4e12-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d4e12-117">Update Privilege</span></span>  | <span data-ttu-id="d4e12-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="d4e12-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="d4e12-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d4e12-119">Update Frequency</span></span>  | <span data-ttu-id="d4e12-120">Pendant la réplication</span><span class="sxs-lookup"><span data-stu-id="d4e12-120">During replication</span></span>                                    |
| <span data-ttu-id="d4e12-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-121">Attribute-Id</span></span>      | <span data-ttu-id="d4e12-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="d4e12-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="d4e12-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d4e12-123">System-Id-Guid</span></span>    | <span data-ttu-id="d4e12-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="d4e12-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="d4e12-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4e12-125">Syntax</span></span>            | [<span data-ttu-id="d4e12-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d4e12-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d4e12-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d4e12-127">Implementations</span></span>

-   [<span data-ttu-id="d4e12-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4e12-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4e12-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4e12-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4e12-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d4e12-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d4e12-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4e12-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4e12-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4e12-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4e12-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4e12-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4e12-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4e12-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4e12-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4e12-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d4e12-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-136">Entry</span></span> | <span data-ttu-id="d4e12-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-140">System-Only</span></span>            | <span data-ttu-id="d4e12-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-141">True</span></span>         |
| <span data-ttu-id="d4e12-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-143">True</span></span>         |
| <span data-ttu-id="d4e12-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-144">Is Indexed</span></span>             | <span data-ttu-id="d4e12-145">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-145">False</span></span>        |
| <span data-ttu-id="d4e12-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-146">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-147">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-147">False</span></span>        |
| <span data-ttu-id="d4e12-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-152">Search-Flags</span></span>           | <span data-ttu-id="d4e12-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-153">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-154">System-Flags</span></span>           | <span data-ttu-id="d4e12-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-155">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="d4e12-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4e12-157">Windows Server 2003</span></span>



| <span data-ttu-id="d4e12-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-158">Entry</span></span> | <span data-ttu-id="d4e12-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-162">System-Only</span></span>            | <span data-ttu-id="d4e12-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-163">True</span></span>         |
| <span data-ttu-id="d4e12-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-165">True</span></span>         |
| <span data-ttu-id="d4e12-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-166">Is Indexed</span></span>             | <span data-ttu-id="d4e12-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-167">False</span></span>        |
| <span data-ttu-id="d4e12-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-168">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-169">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-169">False</span></span>        |
| <span data-ttu-id="d4e12-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-174">Search-Flags</span></span>           | <span data-ttu-id="d4e12-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-175">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-176">System-Flags</span></span>           | <span data-ttu-id="d4e12-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-177">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="d4e12-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="d4e12-179">ADAM</span></span>



| <span data-ttu-id="d4e12-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-180">Entry</span></span> | <span data-ttu-id="d4e12-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-184">System-Only</span></span>            | <span data-ttu-id="d4e12-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-185">True</span></span>         |
| <span data-ttu-id="d4e12-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-187">True</span></span>         |
| <span data-ttu-id="d4e12-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-188">Is Indexed</span></span>             | <span data-ttu-id="d4e12-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-189">False</span></span>        |
| <span data-ttu-id="d4e12-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-190">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-191">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-191">False</span></span>        |
| <span data-ttu-id="d4e12-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-196">Search-Flags</span></span>           | <span data-ttu-id="d4e12-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-197">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-198">System-Flags</span></span>           | <span data-ttu-id="d4e12-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-199">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4e12-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4e12-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4e12-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-202">Entry</span></span> | <span data-ttu-id="d4e12-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-206">System-Only</span></span>            | <span data-ttu-id="d4e12-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-207">True</span></span>         |
| <span data-ttu-id="d4e12-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-209">True</span></span>         |
| <span data-ttu-id="d4e12-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-210">Is Indexed</span></span>             | <span data-ttu-id="d4e12-211">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-211">False</span></span>        |
| <span data-ttu-id="d4e12-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-212">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-213">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-213">False</span></span>        |
| <span data-ttu-id="d4e12-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-218">Search-Flags</span></span>           | <span data-ttu-id="d4e12-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-219">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-220">System-Flags</span></span>           | <span data-ttu-id="d4e12-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-221">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="d4e12-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4e12-223">Windows Server 2008</span></span>



| <span data-ttu-id="d4e12-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-224">Entry</span></span> | <span data-ttu-id="d4e12-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-228">System-Only</span></span>            | <span data-ttu-id="d4e12-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-229">True</span></span>         |
| <span data-ttu-id="d4e12-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-231">True</span></span>         |
| <span data-ttu-id="d4e12-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-232">Is Indexed</span></span>             | <span data-ttu-id="d4e12-233">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-233">False</span></span>        |
| <span data-ttu-id="d4e12-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-234">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-235">False</span></span>        |
| <span data-ttu-id="d4e12-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-240">Search-Flags</span></span>           | <span data-ttu-id="d4e12-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-241">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-242">System-Flags</span></span>           | <span data-ttu-id="d4e12-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-243">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4e12-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4e12-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4e12-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-246">Entry</span></span> | <span data-ttu-id="d4e12-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-250">System-Only</span></span>            | <span data-ttu-id="d4e12-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-251">True</span></span>         |
| <span data-ttu-id="d4e12-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-253">True</span></span>         |
| <span data-ttu-id="d4e12-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-254">Is Indexed</span></span>             | <span data-ttu-id="d4e12-255">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-255">False</span></span>        |
| <span data-ttu-id="d4e12-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-256">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-257">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-257">False</span></span>        |
| <span data-ttu-id="d4e12-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-262">Search-Flags</span></span>           | <span data-ttu-id="d4e12-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-263">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-264">System-Flags</span></span>           | <span data-ttu-id="d4e12-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-265">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="d4e12-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4e12-267">Windows Server 2012</span></span>



| <span data-ttu-id="d4e12-268">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4e12-268">Entry</span></span> | <span data-ttu-id="d4e12-269">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e12-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d4e12-270">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4e12-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4e12-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d4e12-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4e12-272">System-Only</span></span>            | <span data-ttu-id="d4e12-273">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-273">True</span></span>         |
| <span data-ttu-id="d4e12-274">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4e12-274">Is-Single-Valued</span></span>       | <span data-ttu-id="d4e12-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4e12-275">True</span></span>         |
| <span data-ttu-id="d4e12-276">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4e12-276">Is Indexed</span></span>             | <span data-ttu-id="d4e12-277">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-277">False</span></span>        |
| <span data-ttu-id="d4e12-278">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4e12-278">In Global Catalog</span></span>      | <span data-ttu-id="d4e12-279">Faux</span><span class="sxs-lookup"><span data-stu-id="d4e12-279">False</span></span>        |
| <span data-ttu-id="d4e12-280">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4e12-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4e12-281">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4e12-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d4e12-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4e12-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d4e12-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4e12-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d4e12-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-284">Search-Flags</span></span>           | <span data-ttu-id="d4e12-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4e12-285">0x00000000</span></span>   |
| <span data-ttu-id="d4e12-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4e12-286">System-Flags</span></span>           | <span data-ttu-id="d4e12-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d4e12-287">0x08000014</span></span>   |
| <span data-ttu-id="d4e12-288">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4e12-288">Classes used in</span></span>        | \-           |



 

 




