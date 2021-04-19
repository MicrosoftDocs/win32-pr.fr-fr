---
title: Extended-chars-attribute allowed
description: Indique si les caractères étendus sont autorisés dans la valeur de cet attribut. S’applique uniquement aux attributs de chaîne IA5, numérique, imprimable et TELETEX.
ms.assetid: aeacb5ef-9af2-498b-ae53-b3095de0d0c6
ms.tgt_platform: multiple
keywords:
- 'Extended-chars : schéma AD de l’attribut allowed'
- Schéma AD de l’attribut extendedCharsAllowed
topic_type:
- apiref
api_name:
- Extended-Chars-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e26194232387f27f3177f13edeab90efc97a4bb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516510"
---
# <a name="extended-chars-allowed-attribute"></a><span data-ttu-id="168fe-106">Extended-chars-attribute allowed</span><span class="sxs-lookup"><span data-stu-id="168fe-106">Extended-Chars-Allowed attribute</span></span>

<span data-ttu-id="168fe-107">Indique si les caractères étendus sont autorisés dans la valeur de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="168fe-107">Indicates whether extended characters are allowed in the value of this attribute.</span></span> <span data-ttu-id="168fe-108">S’applique uniquement aux attributs de chaîne IA5, numérique, imprimable et TELETEX.</span><span class="sxs-lookup"><span data-stu-id="168fe-108">Only applies to IA5, Numeric, Printable, and Teletex string attributes.</span></span>



| <span data-ttu-id="168fe-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-109">Entry</span></span> | <span data-ttu-id="168fe-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="168fe-111">CN</span><span class="sxs-lookup"><span data-stu-id="168fe-111">CN</span></span>                | <span data-ttu-id="168fe-112">Caractères étendus-autorisés</span><span class="sxs-lookup"><span data-stu-id="168fe-112">Extended-Chars-Allowed</span></span>               |
| <span data-ttu-id="168fe-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="168fe-113">Ldap-Display-Name</span></span> | <span data-ttu-id="168fe-114">extendedCharsAllowed</span><span class="sxs-lookup"><span data-stu-id="168fe-114">extendedCharsAllowed</span></span>                 |
| <span data-ttu-id="168fe-115">Taille</span><span class="sxs-lookup"><span data-stu-id="168fe-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="168fe-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="168fe-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="168fe-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="168fe-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="168fe-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-118">Attribute-Id</span></span>      | <span data-ttu-id="168fe-119">1.2.840.113556.1.2.380</span><span class="sxs-lookup"><span data-stu-id="168fe-119">1.2.840.113556.1.2.380</span></span>               |
| <span data-ttu-id="168fe-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="168fe-120">System-Id-Guid</span></span>    | <span data-ttu-id="168fe-121">bf967966-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="168fe-121">bf967966-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="168fe-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="168fe-122">Syntax</span></span>            | [<span data-ttu-id="168fe-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="168fe-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="168fe-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="168fe-124">Implementations</span></span>

-   [<span data-ttu-id="168fe-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="168fe-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="168fe-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="168fe-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="168fe-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="168fe-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="168fe-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="168fe-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="168fe-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="168fe-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="168fe-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="168fe-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="168fe-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="168fe-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="168fe-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="168fe-132">Windows 2000 Server</span></span>



| <span data-ttu-id="168fe-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-133">Entry</span></span> | <span data-ttu-id="168fe-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-136">MAPI-Id</span></span>                | <span data-ttu-id="168fe-137">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-137">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-138">System-Only</span></span>            | <span data-ttu-id="168fe-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-139">True</span></span>                                                     |
| <span data-ttu-id="168fe-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-140">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-141">True</span></span>                                                     |
| <span data-ttu-id="168fe-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-142">Is Indexed</span></span>             | <span data-ttu-id="168fe-143">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-143">False</span></span>                                                    |
| <span data-ttu-id="168fe-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-144">In Global Catalog</span></span>      | <span data-ttu-id="168fe-145">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-145">False</span></span>                                                    |
| <span data-ttu-id="168fe-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-150">Search-Flags</span></span>           | <span data-ttu-id="168fe-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-151">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-152">System-Flags</span></span>           | <span data-ttu-id="168fe-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-153">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-154">Classes used in</span></span>        | [<span data-ttu-id="168fe-155">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="168fe-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="168fe-156">Windows Server 2003</span></span>



| <span data-ttu-id="168fe-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-157">Entry</span></span> | <span data-ttu-id="168fe-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-160">MAPI-Id</span></span>                | <span data-ttu-id="168fe-161">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-161">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-162">System-Only</span></span>            | <span data-ttu-id="168fe-163">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-163">False</span></span>                                                    |
| <span data-ttu-id="168fe-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-164">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-165">True</span></span>                                                     |
| <span data-ttu-id="168fe-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-166">Is Indexed</span></span>             | <span data-ttu-id="168fe-167">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-167">False</span></span>                                                    |
| <span data-ttu-id="168fe-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-168">In Global Catalog</span></span>      | <span data-ttu-id="168fe-169">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-169">False</span></span>                                                    |
| <span data-ttu-id="168fe-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-174">Search-Flags</span></span>           | <span data-ttu-id="168fe-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-175">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-176">System-Flags</span></span>           | <span data-ttu-id="168fe-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-177">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-178">Classes used in</span></span>        | [<span data-ttu-id="168fe-179">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="168fe-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="168fe-180">ADAM</span></span>



| <span data-ttu-id="168fe-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-181">Entry</span></span> | <span data-ttu-id="168fe-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-184">MAPI-Id</span></span>                | <span data-ttu-id="168fe-185">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-185">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-186">System-Only</span></span>            | <span data-ttu-id="168fe-187">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-187">False</span></span>                                                    |
| <span data-ttu-id="168fe-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-188">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-189">True</span></span>                                                     |
| <span data-ttu-id="168fe-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-190">Is Indexed</span></span>             | <span data-ttu-id="168fe-191">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-191">False</span></span>                                                    |
| <span data-ttu-id="168fe-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-192">In Global Catalog</span></span>      | <span data-ttu-id="168fe-193">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-193">False</span></span>                                                    |
| <span data-ttu-id="168fe-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-198">Search-Flags</span></span>           | <span data-ttu-id="168fe-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-199">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-200">System-Flags</span></span>           | <span data-ttu-id="168fe-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-201">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-202">Classes used in</span></span>        | [<span data-ttu-id="168fe-203">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="168fe-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="168fe-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="168fe-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-205">Entry</span></span> | <span data-ttu-id="168fe-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-208">MAPI-Id</span></span>                | <span data-ttu-id="168fe-209">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-209">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-210">System-Only</span></span>            | <span data-ttu-id="168fe-211">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-211">False</span></span>                                                    |
| <span data-ttu-id="168fe-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-212">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-213">True</span></span>                                                     |
| <span data-ttu-id="168fe-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-214">Is Indexed</span></span>             | <span data-ttu-id="168fe-215">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-215">False</span></span>                                                    |
| <span data-ttu-id="168fe-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-216">In Global Catalog</span></span>      | <span data-ttu-id="168fe-217">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-217">False</span></span>                                                    |
| <span data-ttu-id="168fe-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-222">Search-Flags</span></span>           | <span data-ttu-id="168fe-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-223">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-224">System-Flags</span></span>           | <span data-ttu-id="168fe-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-225">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-226">Classes used in</span></span>        | [<span data-ttu-id="168fe-227">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="168fe-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="168fe-228">Windows Server 2008</span></span>



| <span data-ttu-id="168fe-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-229">Entry</span></span> | <span data-ttu-id="168fe-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-232">MAPI-Id</span></span>                | <span data-ttu-id="168fe-233">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-233">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-234">System-Only</span></span>            | <span data-ttu-id="168fe-235">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-235">False</span></span>                                                    |
| <span data-ttu-id="168fe-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-236">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-237">True</span></span>                                                     |
| <span data-ttu-id="168fe-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-238">Is Indexed</span></span>             | <span data-ttu-id="168fe-239">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-239">False</span></span>                                                    |
| <span data-ttu-id="168fe-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-240">In Global Catalog</span></span>      | <span data-ttu-id="168fe-241">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-241">False</span></span>                                                    |
| <span data-ttu-id="168fe-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-246">Search-Flags</span></span>           | <span data-ttu-id="168fe-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-247">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-248">System-Flags</span></span>           | <span data-ttu-id="168fe-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-249">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-250">Classes used in</span></span>        | [<span data-ttu-id="168fe-251">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="168fe-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="168fe-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="168fe-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-253">Entry</span></span> | <span data-ttu-id="168fe-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-256">MAPI-Id</span></span>                | <span data-ttu-id="168fe-257">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-257">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-258">System-Only</span></span>            | <span data-ttu-id="168fe-259">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-259">False</span></span>                                                    |
| <span data-ttu-id="168fe-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-260">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-261">True</span></span>                                                     |
| <span data-ttu-id="168fe-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-262">Is Indexed</span></span>             | <span data-ttu-id="168fe-263">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-263">False</span></span>                                                    |
| <span data-ttu-id="168fe-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-264">In Global Catalog</span></span>      | <span data-ttu-id="168fe-265">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-265">False</span></span>                                                    |
| <span data-ttu-id="168fe-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-270">Search-Flags</span></span>           | <span data-ttu-id="168fe-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-271">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-272">System-Flags</span></span>           | <span data-ttu-id="168fe-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-273">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-274">Classes used in</span></span>        | [<span data-ttu-id="168fe-275">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="168fe-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="168fe-276">Windows Server 2012</span></span>



| <span data-ttu-id="168fe-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="168fe-277">Entry</span></span> | <span data-ttu-id="168fe-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="168fe-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="168fe-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="168fe-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="168fe-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="168fe-280">MAPI-Id</span></span>                | <span data-ttu-id="168fe-281">0x80A7</span><span class="sxs-lookup"><span data-stu-id="168fe-281">0x80A7</span></span>                                                   |
| <span data-ttu-id="168fe-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="168fe-282">System-Only</span></span>            | <span data-ttu-id="168fe-283">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-283">False</span></span>                                                    |
| <span data-ttu-id="168fe-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="168fe-284">Is-Single-Valued</span></span>       | <span data-ttu-id="168fe-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="168fe-285">True</span></span>                                                     |
| <span data-ttu-id="168fe-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="168fe-286">Is Indexed</span></span>             | <span data-ttu-id="168fe-287">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-287">False</span></span>                                                    |
| <span data-ttu-id="168fe-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="168fe-288">In Global Catalog</span></span>      | <span data-ttu-id="168fe-289">Faux</span><span class="sxs-lookup"><span data-stu-id="168fe-289">False</span></span>                                                    |
| <span data-ttu-id="168fe-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="168fe-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="168fe-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="168fe-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="168fe-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="168fe-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="168fe-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="168fe-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-294">Search-Flags</span></span>           | <span data-ttu-id="168fe-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="168fe-295">0x00000000</span></span>                                               |
| <span data-ttu-id="168fe-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="168fe-296">System-Flags</span></span>           | <span data-ttu-id="168fe-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="168fe-297">0x00000010</span></span>                                               |
| <span data-ttu-id="168fe-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="168fe-298">Classes used in</span></span>        | [<span data-ttu-id="168fe-299">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="168fe-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





