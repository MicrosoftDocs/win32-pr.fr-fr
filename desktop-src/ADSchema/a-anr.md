---
title: Attribut ANR
description: Attribut de résolution de noms ambigu à utiliser lors du choix d’un objet à l’autre.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ANR
- Schéma AD de l’attribut aNR
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480485"
---
# <a name="anr-attribute"></a><span data-ttu-id="27b12-105">Attribut ANR</span><span class="sxs-lookup"><span data-stu-id="27b12-105">ANR attribute</span></span>

<span data-ttu-id="27b12-106">Attribut de résolution de noms ambigu à utiliser lors du choix d’un objet à l’autre.</span><span class="sxs-lookup"><span data-stu-id="27b12-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="27b12-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-107">Entry</span></span> | <span data-ttu-id="27b12-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="27b12-109">CN</span><span class="sxs-lookup"><span data-stu-id="27b12-109">CN</span></span>                | <span data-ttu-id="27b12-110">AMBIGU</span><span class="sxs-lookup"><span data-stu-id="27b12-110">ANR</span></span>                                                               |
| <span data-ttu-id="27b12-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27b12-111">Ldap-Display-Name</span></span> | <span data-ttu-id="27b12-112">Ambigu</span><span class="sxs-lookup"><span data-stu-id="27b12-112">aNR</span></span>                                                               |
| <span data-ttu-id="27b12-113">Taille</span><span class="sxs-lookup"><span data-stu-id="27b12-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="27b12-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="27b12-114">Update Privilege</span></span>  | <span data-ttu-id="27b12-115">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="27b12-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="27b12-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="27b12-116">Update Frequency</span></span>  | <span data-ttu-id="27b12-117">Lorsqu’un attribut doit être ajouté ou supprimé de la liste ANR.</span><span class="sxs-lookup"><span data-stu-id="27b12-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="27b12-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-118">Attribute-Id</span></span>      | <span data-ttu-id="27b12-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="27b12-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="27b12-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27b12-120">System-Id-Guid</span></span>    | <span data-ttu-id="27b12-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="27b12-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="27b12-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27b12-122">Syntax</span></span>            | [<span data-ttu-id="27b12-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="27b12-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="27b12-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="27b12-124">Implementations</span></span>

-   [<span data-ttu-id="27b12-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27b12-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27b12-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27b12-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27b12-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="27b12-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="27b12-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27b12-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27b12-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27b12-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27b12-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27b12-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27b12-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27b12-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27b12-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27b12-132">Windows 2000 Server</span></span>



| <span data-ttu-id="27b12-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-133">Entry</span></span> | <span data-ttu-id="27b12-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-137">System-Only</span></span>            | <span data-ttu-id="27b12-138">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-138">False</span></span>        |
| <span data-ttu-id="27b12-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-139">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-140">True</span></span>         |
| <span data-ttu-id="27b12-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-141">Is Indexed</span></span>             | <span data-ttu-id="27b12-142">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-142">False</span></span>        |
| <span data-ttu-id="27b12-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-143">In Global Catalog</span></span>      | <span data-ttu-id="27b12-144">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-144">False</span></span>        |
| <span data-ttu-id="27b12-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-149">Search-Flags</span></span>           | <span data-ttu-id="27b12-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-150">0x00000000</span></span>   |
| <span data-ttu-id="27b12-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-151">System-Flags</span></span>           | <span data-ttu-id="27b12-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-152">0x08000014</span></span>   |
| <span data-ttu-id="27b12-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="27b12-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27b12-154">Windows Server 2003</span></span>



| <span data-ttu-id="27b12-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-155">Entry</span></span> | <span data-ttu-id="27b12-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-159">System-Only</span></span>            | <span data-ttu-id="27b12-160">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-160">False</span></span>        |
| <span data-ttu-id="27b12-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-161">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-162">True</span></span>         |
| <span data-ttu-id="27b12-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-163">Is Indexed</span></span>             | <span data-ttu-id="27b12-164">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-164">False</span></span>        |
| <span data-ttu-id="27b12-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-165">In Global Catalog</span></span>      | <span data-ttu-id="27b12-166">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-166">False</span></span>        |
| <span data-ttu-id="27b12-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-171">Search-Flags</span></span>           | <span data-ttu-id="27b12-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-172">0x00000000</span></span>   |
| <span data-ttu-id="27b12-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-173">System-Flags</span></span>           | <span data-ttu-id="27b12-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-174">0x08000014</span></span>   |
| <span data-ttu-id="27b12-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="27b12-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="27b12-176">ADAM</span></span>



| <span data-ttu-id="27b12-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-177">Entry</span></span> | <span data-ttu-id="27b12-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-181">System-Only</span></span>            | <span data-ttu-id="27b12-182">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-182">False</span></span>        |
| <span data-ttu-id="27b12-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-183">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-184">True</span></span>         |
| <span data-ttu-id="27b12-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-185">Is Indexed</span></span>             | <span data-ttu-id="27b12-186">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-186">False</span></span>        |
| <span data-ttu-id="27b12-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-187">In Global Catalog</span></span>      | <span data-ttu-id="27b12-188">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-188">False</span></span>        |
| <span data-ttu-id="27b12-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-193">Search-Flags</span></span>           | <span data-ttu-id="27b12-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-194">0x00000000</span></span>   |
| <span data-ttu-id="27b12-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-195">System-Flags</span></span>           | <span data-ttu-id="27b12-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-196">0x08000014</span></span>   |
| <span data-ttu-id="27b12-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27b12-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27b12-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27b12-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-199">Entry</span></span> | <span data-ttu-id="27b12-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-203">System-Only</span></span>            | <span data-ttu-id="27b12-204">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-204">False</span></span>        |
| <span data-ttu-id="27b12-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-205">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-206">True</span></span>         |
| <span data-ttu-id="27b12-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-207">Is Indexed</span></span>             | <span data-ttu-id="27b12-208">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-208">False</span></span>        |
| <span data-ttu-id="27b12-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-209">In Global Catalog</span></span>      | <span data-ttu-id="27b12-210">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-210">False</span></span>        |
| <span data-ttu-id="27b12-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-215">Search-Flags</span></span>           | <span data-ttu-id="27b12-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-216">0x00000000</span></span>   |
| <span data-ttu-id="27b12-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-217">System-Flags</span></span>           | <span data-ttu-id="27b12-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-218">0x08000014</span></span>   |
| <span data-ttu-id="27b12-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="27b12-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27b12-220">Windows Server 2008</span></span>



| <span data-ttu-id="27b12-221">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-221">Entry</span></span> | <span data-ttu-id="27b12-222">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-223">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-225">System-Only</span></span>            | <span data-ttu-id="27b12-226">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-226">False</span></span>        |
| <span data-ttu-id="27b12-227">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-227">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-228">True</span></span>         |
| <span data-ttu-id="27b12-229">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-229">Is Indexed</span></span>             | <span data-ttu-id="27b12-230">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-230">False</span></span>        |
| <span data-ttu-id="27b12-231">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-231">In Global Catalog</span></span>      | <span data-ttu-id="27b12-232">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-232">False</span></span>        |
| <span data-ttu-id="27b12-233">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-234">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-237">Search-Flags</span></span>           | <span data-ttu-id="27b12-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-238">0x00000000</span></span>   |
| <span data-ttu-id="27b12-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-239">System-Flags</span></span>           | <span data-ttu-id="27b12-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-240">0x08000014</span></span>   |
| <span data-ttu-id="27b12-241">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27b12-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27b12-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27b12-243">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-243">Entry</span></span> | <span data-ttu-id="27b12-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-245">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-247">System-Only</span></span>            | <span data-ttu-id="27b12-248">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-248">False</span></span>        |
| <span data-ttu-id="27b12-249">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-249">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-250">True</span></span>         |
| <span data-ttu-id="27b12-251">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-251">Is Indexed</span></span>             | <span data-ttu-id="27b12-252">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-252">False</span></span>        |
| <span data-ttu-id="27b12-253">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-253">In Global Catalog</span></span>      | <span data-ttu-id="27b12-254">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-254">False</span></span>        |
| <span data-ttu-id="27b12-255">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-256">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-259">Search-Flags</span></span>           | <span data-ttu-id="27b12-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-260">0x00000000</span></span>   |
| <span data-ttu-id="27b12-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-261">System-Flags</span></span>           | <span data-ttu-id="27b12-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-262">0x08000014</span></span>   |
| <span data-ttu-id="27b12-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="27b12-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27b12-264">Windows Server 2012</span></span>



| <span data-ttu-id="27b12-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="27b12-265">Entry</span></span> | <span data-ttu-id="27b12-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b12-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="27b12-267">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27b12-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27b12-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="27b12-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="27b12-269">System-Only</span></span>            | <span data-ttu-id="27b12-270">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-270">False</span></span>        |
| <span data-ttu-id="27b12-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27b12-271">Is-Single-Valued</span></span>       | <span data-ttu-id="27b12-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="27b12-272">True</span></span>         |
| <span data-ttu-id="27b12-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27b12-273">Is Indexed</span></span>             | <span data-ttu-id="27b12-274">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-274">False</span></span>        |
| <span data-ttu-id="27b12-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27b12-275">In Global Catalog</span></span>      | <span data-ttu-id="27b12-276">Faux</span><span class="sxs-lookup"><span data-stu-id="27b12-276">False</span></span>        |
| <span data-ttu-id="27b12-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27b12-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="27b12-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27b12-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="27b12-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27b12-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="27b12-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27b12-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="27b12-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-281">Search-Flags</span></span>           | <span data-ttu-id="27b12-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27b12-282">0x00000000</span></span>   |
| <span data-ttu-id="27b12-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27b12-283">System-Flags</span></span>           | <span data-ttu-id="27b12-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27b12-284">0x08000014</span></span>   |
| <span data-ttu-id="27b12-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27b12-285">Classes used in</span></span>        | \-           |



 

 




