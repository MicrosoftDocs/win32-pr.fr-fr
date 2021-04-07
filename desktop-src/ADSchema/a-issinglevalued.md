---
title: Is-attribut à valeur unique
description: Si la valeur est TRUE, cet attribut ne peut stocker qu’une seule valeur.
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- Schéma AD-attribut is-value simple
- Schéma AD de l’attribut isSingleValued
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a1fafd047afa47b874fb0385a690e2c0d13161
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844741"
---
# <a name="is-single-valued-attribute"></a><span data-ttu-id="866d0-105">Is-attribut à valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="866d0-106">Si la **valeur est true**, cet attribut ne peut stocker qu’une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="866d0-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="866d0-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-107">Entry</span></span> | <span data-ttu-id="866d0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="866d0-109">CN</span><span class="sxs-lookup"><span data-stu-id="866d0-109">CN</span></span>                | <span data-ttu-id="866d0-110">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="866d0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="866d0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="866d0-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="866d0-112">isSingleValued</span></span>                       |
| <span data-ttu-id="866d0-113">Taille</span><span class="sxs-lookup"><span data-stu-id="866d0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="866d0-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="866d0-114">Update Privilege</span></span>  | <span data-ttu-id="866d0-115">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="866d0-115">Schema administrator</span></span>                 |
| <span data-ttu-id="866d0-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="866d0-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="866d0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-117">Attribute-Id</span></span>      | <span data-ttu-id="866d0-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="866d0-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="866d0-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="866d0-119">System-Id-Guid</span></span>    | <span data-ttu-id="866d0-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="866d0-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="866d0-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="866d0-121">Syntax</span></span>            | [<span data-ttu-id="866d0-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="866d0-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="866d0-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="866d0-123">Implementations</span></span>

-   [<span data-ttu-id="866d0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="866d0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="866d0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="866d0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="866d0-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="866d0-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="866d0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="866d0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="866d0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="866d0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="866d0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="866d0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="866d0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="866d0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="866d0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="866d0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="866d0-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-132">Entry</span></span> | <span data-ttu-id="866d0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-135">MAPI-Id</span></span>                | <span data-ttu-id="866d0-136">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-137">System-Only</span></span>            | <span data-ttu-id="866d0-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-138">True</span></span>                                                     |
| <span data-ttu-id="866d0-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-139">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-140">True</span></span>                                                     |
| <span data-ttu-id="866d0-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-141">Is Indexed</span></span>             | <span data-ttu-id="866d0-142">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-142">False</span></span>                                                    |
| <span data-ttu-id="866d0-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-143">In Global Catalog</span></span>      | <span data-ttu-id="866d0-144">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-144">False</span></span>                                                    |
| <span data-ttu-id="866d0-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-149">Search-Flags</span></span>           | <span data-ttu-id="866d0-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-150">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-151">System-Flags</span></span>           | <span data-ttu-id="866d0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-152">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-153">Classes used in</span></span>        | [<span data-ttu-id="866d0-154">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="866d0-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="866d0-155">Windows Server 2003</span></span>



| <span data-ttu-id="866d0-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-156">Entry</span></span> | <span data-ttu-id="866d0-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-159">MAPI-Id</span></span>                | <span data-ttu-id="866d0-160">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-161">System-Only</span></span>            | <span data-ttu-id="866d0-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-162">True</span></span>                                                     |
| <span data-ttu-id="866d0-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-164">True</span></span>                                                     |
| <span data-ttu-id="866d0-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-165">Is Indexed</span></span>             | <span data-ttu-id="866d0-166">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-166">False</span></span>                                                    |
| <span data-ttu-id="866d0-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-167">In Global Catalog</span></span>      | <span data-ttu-id="866d0-168">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-168">False</span></span>                                                    |
| <span data-ttu-id="866d0-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-173">Search-Flags</span></span>           | <span data-ttu-id="866d0-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-174">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-175">System-Flags</span></span>           | <span data-ttu-id="866d0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-176">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-177">Classes used in</span></span>        | [<span data-ttu-id="866d0-178">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="866d0-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="866d0-179">ADAM</span></span>



| <span data-ttu-id="866d0-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-180">Entry</span></span> | <span data-ttu-id="866d0-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-183">MAPI-Id</span></span>                | <span data-ttu-id="866d0-184">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-185">System-Only</span></span>            | <span data-ttu-id="866d0-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-186">True</span></span>                                                     |
| <span data-ttu-id="866d0-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-188">True</span></span>                                                     |
| <span data-ttu-id="866d0-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-189">Is Indexed</span></span>             | <span data-ttu-id="866d0-190">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-190">False</span></span>                                                    |
| <span data-ttu-id="866d0-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-191">In Global Catalog</span></span>      | <span data-ttu-id="866d0-192">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-192">False</span></span>                                                    |
| <span data-ttu-id="866d0-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-197">Search-Flags</span></span>           | <span data-ttu-id="866d0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-198">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-199">System-Flags</span></span>           | <span data-ttu-id="866d0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-200">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-201">Classes used in</span></span>        | [<span data-ttu-id="866d0-202">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="866d0-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="866d0-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="866d0-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-204">Entry</span></span> | <span data-ttu-id="866d0-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-207">MAPI-Id</span></span>                | <span data-ttu-id="866d0-208">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-209">System-Only</span></span>            | <span data-ttu-id="866d0-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-210">True</span></span>                                                     |
| <span data-ttu-id="866d0-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-212">True</span></span>                                                     |
| <span data-ttu-id="866d0-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-213">Is Indexed</span></span>             | <span data-ttu-id="866d0-214">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-214">False</span></span>                                                    |
| <span data-ttu-id="866d0-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-215">In Global Catalog</span></span>      | <span data-ttu-id="866d0-216">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-216">False</span></span>                                                    |
| <span data-ttu-id="866d0-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-221">Search-Flags</span></span>           | <span data-ttu-id="866d0-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-222">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-223">System-Flags</span></span>           | <span data-ttu-id="866d0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-224">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-225">Classes used in</span></span>        | [<span data-ttu-id="866d0-226">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="866d0-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="866d0-227">Windows Server 2008</span></span>



| <span data-ttu-id="866d0-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-228">Entry</span></span> | <span data-ttu-id="866d0-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-231">MAPI-Id</span></span>                | <span data-ttu-id="866d0-232">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-233">System-Only</span></span>            | <span data-ttu-id="866d0-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-234">True</span></span>                                                     |
| <span data-ttu-id="866d0-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-236">True</span></span>                                                     |
| <span data-ttu-id="866d0-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-237">Is Indexed</span></span>             | <span data-ttu-id="866d0-238">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-238">False</span></span>                                                    |
| <span data-ttu-id="866d0-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-239">In Global Catalog</span></span>      | <span data-ttu-id="866d0-240">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-240">False</span></span>                                                    |
| <span data-ttu-id="866d0-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-245">Search-Flags</span></span>           | <span data-ttu-id="866d0-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-246">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-247">System-Flags</span></span>           | <span data-ttu-id="866d0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-248">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-249">Classes used in</span></span>        | [<span data-ttu-id="866d0-250">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="866d0-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="866d0-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="866d0-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-252">Entry</span></span> | <span data-ttu-id="866d0-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-255">MAPI-Id</span></span>                | <span data-ttu-id="866d0-256">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-257">System-Only</span></span>            | <span data-ttu-id="866d0-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-258">True</span></span>                                                     |
| <span data-ttu-id="866d0-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-259">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-260">True</span></span>                                                     |
| <span data-ttu-id="866d0-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-261">Is Indexed</span></span>             | <span data-ttu-id="866d0-262">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-262">False</span></span>                                                    |
| <span data-ttu-id="866d0-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-263">In Global Catalog</span></span>      | <span data-ttu-id="866d0-264">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-264">False</span></span>                                                    |
| <span data-ttu-id="866d0-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-269">Search-Flags</span></span>           | <span data-ttu-id="866d0-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-270">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-271">System-Flags</span></span>           | <span data-ttu-id="866d0-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-272">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-273">Classes used in</span></span>        | [<span data-ttu-id="866d0-274">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="866d0-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="866d0-275">Windows Server 2012</span></span>



| <span data-ttu-id="866d0-276">Entrée</span><span class="sxs-lookup"><span data-stu-id="866d0-276">Entry</span></span> | <span data-ttu-id="866d0-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="866d0-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="866d0-278">ID de lien</span><span class="sxs-lookup"><span data-stu-id="866d0-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="866d0-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="866d0-279">MAPI-Id</span></span>                | <span data-ttu-id="866d0-280">0x80C1</span><span class="sxs-lookup"><span data-stu-id="866d0-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="866d0-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="866d0-281">System-Only</span></span>            | <span data-ttu-id="866d0-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-282">True</span></span>                                                     |
| <span data-ttu-id="866d0-283">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="866d0-283">Is-Single-Valued</span></span>       | <span data-ttu-id="866d0-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="866d0-284">True</span></span>                                                     |
| <span data-ttu-id="866d0-285">Est indexé</span><span class="sxs-lookup"><span data-stu-id="866d0-285">Is Indexed</span></span>             | <span data-ttu-id="866d0-286">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-286">False</span></span>                                                    |
| <span data-ttu-id="866d0-287">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="866d0-287">In Global Catalog</span></span>      | <span data-ttu-id="866d0-288">Faux</span><span class="sxs-lookup"><span data-stu-id="866d0-288">False</span></span>                                                    |
| <span data-ttu-id="866d0-289">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="866d0-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="866d0-290">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="866d0-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="866d0-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="866d0-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="866d0-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="866d0-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-293">Search-Flags</span></span>           | <span data-ttu-id="866d0-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="866d0-294">0x00000000</span></span>                                               |
| <span data-ttu-id="866d0-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="866d0-295">System-Flags</span></span>           | <span data-ttu-id="866d0-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="866d0-296">0x00000010</span></span>                                               |
| <span data-ttu-id="866d0-297">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="866d0-297">Classes used in</span></span>        | [<span data-ttu-id="866d0-298">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="866d0-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





