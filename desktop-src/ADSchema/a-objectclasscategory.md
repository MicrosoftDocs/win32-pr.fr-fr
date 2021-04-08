---
title: Attribut de catégorie objet-classe
description: Cet attribut contient le type de classe, tel que abstract, auxiliaire ou Structured.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de catégorie objet-classe
- Schéma AD de l’attribut objectClassCategory
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943116"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="9a423-105">Attribut de catégorie objet-classe</span><span class="sxs-lookup"><span data-stu-id="9a423-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="9a423-106">Cet attribut contient le type de classe, tel que abstract, auxiliaire ou Structured.</span><span class="sxs-lookup"><span data-stu-id="9a423-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="9a423-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-107">Entry</span></span> | <span data-ttu-id="9a423-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="9a423-109">CN</span><span class="sxs-lookup"><span data-stu-id="9a423-109">CN</span></span>                | <span data-ttu-id="9a423-110">Catégorie objet-classe</span><span class="sxs-lookup"><span data-stu-id="9a423-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="9a423-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a423-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9a423-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="9a423-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="9a423-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9a423-113">Size</span></span>              | <span data-ttu-id="9a423-114">4 octets.</span><span class="sxs-lookup"><span data-stu-id="9a423-114">4 bytes.</span></span> <span data-ttu-id="9a423-115">Structural 1, abstract 2, auxiliaire 3.</span><span class="sxs-lookup"><span data-stu-id="9a423-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="9a423-116">La classe 88, 0 ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9a423-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="9a423-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9a423-117">Update Privilege</span></span>  | <span data-ttu-id="9a423-118">Le concepteur de l’objet définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9a423-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="9a423-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9a423-119">Update Frequency</span></span>  | <span data-ttu-id="9a423-120">Cette valeur ne doit jamais changer.</span><span class="sxs-lookup"><span data-stu-id="9a423-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="9a423-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-121">Attribute-Id</span></span>      | <span data-ttu-id="9a423-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="9a423-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="9a423-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a423-123">System-Id-Guid</span></span>    | <span data-ttu-id="9a423-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9a423-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="9a423-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a423-125">Syntax</span></span>            | [<span data-ttu-id="9a423-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="9a423-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="9a423-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9a423-127">Implementations</span></span>

-   [<span data-ttu-id="9a423-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9a423-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9a423-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a423-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a423-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9a423-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a423-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a423-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a423-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a423-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a423-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a423-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a423-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a423-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9a423-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a423-135">Windows 2000 Server</span></span>



| <span data-ttu-id="9a423-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-136">Entry</span></span> | <span data-ttu-id="9a423-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-139">MAPI-Id</span></span>                | <span data-ttu-id="9a423-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-140">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-141">System-Only</span></span>            | <span data-ttu-id="9a423-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-142">True</span></span>                                             |
| <span data-ttu-id="9a423-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-143">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-144">True</span></span>                                             |
| <span data-ttu-id="9a423-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-145">Is Indexed</span></span>             | <span data-ttu-id="9a423-146">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-146">False</span></span>                                            |
| <span data-ttu-id="9a423-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-147">In Global Catalog</span></span>      | <span data-ttu-id="9a423-148">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-148">False</span></span>                                            |
| <span data-ttu-id="9a423-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-151">Range-Lower</span></span>            | <span data-ttu-id="9a423-152">0</span><span class="sxs-lookup"><span data-stu-id="9a423-152">0</span></span>                                                |
| <span data-ttu-id="9a423-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-153">Range-Upper</span></span>            | <span data-ttu-id="9a423-154">3</span><span class="sxs-lookup"><span data-stu-id="9a423-154">3</span></span>                                                |
| <span data-ttu-id="9a423-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-155">Search-Flags</span></span>           | <span data-ttu-id="9a423-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-156">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-157">System-Flags</span></span>           | <span data-ttu-id="9a423-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-158">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-159">Classes used in</span></span>        | [<span data-ttu-id="9a423-160">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9a423-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a423-161">Windows Server 2003</span></span>



| <span data-ttu-id="9a423-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-162">Entry</span></span> | <span data-ttu-id="9a423-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-165">MAPI-Id</span></span>                | <span data-ttu-id="9a423-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-166">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-167">System-Only</span></span>            | <span data-ttu-id="9a423-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-168">True</span></span>                                             |
| <span data-ttu-id="9a423-169">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-169">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-170">True</span></span>                                             |
| <span data-ttu-id="9a423-171">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-171">Is Indexed</span></span>             | <span data-ttu-id="9a423-172">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-172">False</span></span>                                            |
| <span data-ttu-id="9a423-173">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-173">In Global Catalog</span></span>      | <span data-ttu-id="9a423-174">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-174">False</span></span>                                            |
| <span data-ttu-id="9a423-175">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-176">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-177">Range-Lower</span></span>            | <span data-ttu-id="9a423-178">0</span><span class="sxs-lookup"><span data-stu-id="9a423-178">0</span></span>                                                |
| <span data-ttu-id="9a423-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-179">Range-Upper</span></span>            | <span data-ttu-id="9a423-180">3</span><span class="sxs-lookup"><span data-stu-id="9a423-180">3</span></span>                                                |
| <span data-ttu-id="9a423-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-181">Search-Flags</span></span>           | <span data-ttu-id="9a423-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-182">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-183">System-Flags</span></span>           | <span data-ttu-id="9a423-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-184">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-185">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-185">Classes used in</span></span>        | [<span data-ttu-id="9a423-186">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a423-187">ADAM</span><span class="sxs-lookup"><span data-stu-id="9a423-187">ADAM</span></span>



| <span data-ttu-id="9a423-188">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-188">Entry</span></span> | <span data-ttu-id="9a423-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-190">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-191">MAPI-Id</span></span>                | <span data-ttu-id="9a423-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-192">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-193">System-Only</span></span>            | <span data-ttu-id="9a423-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-194">True</span></span>                                             |
| <span data-ttu-id="9a423-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-195">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-196">True</span></span>                                             |
| <span data-ttu-id="9a423-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-197">Is Indexed</span></span>             | <span data-ttu-id="9a423-198">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-198">False</span></span>                                            |
| <span data-ttu-id="9a423-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-199">In Global Catalog</span></span>      | <span data-ttu-id="9a423-200">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-200">False</span></span>                                            |
| <span data-ttu-id="9a423-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-203">Range-Lower</span></span>            | <span data-ttu-id="9a423-204">0</span><span class="sxs-lookup"><span data-stu-id="9a423-204">0</span></span>                                                |
| <span data-ttu-id="9a423-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-205">Range-Upper</span></span>            | <span data-ttu-id="9a423-206">3</span><span class="sxs-lookup"><span data-stu-id="9a423-206">3</span></span>                                                |
| <span data-ttu-id="9a423-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-207">Search-Flags</span></span>           | <span data-ttu-id="9a423-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-208">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-209">System-Flags</span></span>           | <span data-ttu-id="9a423-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-210">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-211">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-211">Classes used in</span></span>        | [<span data-ttu-id="9a423-212">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a423-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a423-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a423-214">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-214">Entry</span></span> | <span data-ttu-id="9a423-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-216">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-217">MAPI-Id</span></span>                | <span data-ttu-id="9a423-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-218">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-219">System-Only</span></span>            | <span data-ttu-id="9a423-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-220">True</span></span>                                             |
| <span data-ttu-id="9a423-221">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-221">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-222">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-222">True</span></span>                                             |
| <span data-ttu-id="9a423-223">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-223">Is Indexed</span></span>             | <span data-ttu-id="9a423-224">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-224">False</span></span>                                            |
| <span data-ttu-id="9a423-225">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-225">In Global Catalog</span></span>      | <span data-ttu-id="9a423-226">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-226">False</span></span>                                            |
| <span data-ttu-id="9a423-227">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-228">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-229">Range-Lower</span></span>            | <span data-ttu-id="9a423-230">0</span><span class="sxs-lookup"><span data-stu-id="9a423-230">0</span></span>                                                |
| <span data-ttu-id="9a423-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-231">Range-Upper</span></span>            | <span data-ttu-id="9a423-232">3</span><span class="sxs-lookup"><span data-stu-id="9a423-232">3</span></span>                                                |
| <span data-ttu-id="9a423-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-233">Search-Flags</span></span>           | <span data-ttu-id="9a423-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-234">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-235">System-Flags</span></span>           | <span data-ttu-id="9a423-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-236">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-237">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-237">Classes used in</span></span>        | [<span data-ttu-id="9a423-238">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a423-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a423-239">Windows Server 2008</span></span>



| <span data-ttu-id="9a423-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-240">Entry</span></span> | <span data-ttu-id="9a423-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-243">MAPI-Id</span></span>                | <span data-ttu-id="9a423-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-244">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-245">System-Only</span></span>            | <span data-ttu-id="9a423-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-246">True</span></span>                                             |
| <span data-ttu-id="9a423-247">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-247">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-248">True</span></span>                                             |
| <span data-ttu-id="9a423-249">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-249">Is Indexed</span></span>             | <span data-ttu-id="9a423-250">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-250">False</span></span>                                            |
| <span data-ttu-id="9a423-251">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-251">In Global Catalog</span></span>      | <span data-ttu-id="9a423-252">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-252">False</span></span>                                            |
| <span data-ttu-id="9a423-253">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-254">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-255">Range-Lower</span></span>            | <span data-ttu-id="9a423-256">0</span><span class="sxs-lookup"><span data-stu-id="9a423-256">0</span></span>                                                |
| <span data-ttu-id="9a423-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-257">Range-Upper</span></span>            | <span data-ttu-id="9a423-258">3</span><span class="sxs-lookup"><span data-stu-id="9a423-258">3</span></span>                                                |
| <span data-ttu-id="9a423-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-259">Search-Flags</span></span>           | <span data-ttu-id="9a423-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-260">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-261">System-Flags</span></span>           | <span data-ttu-id="9a423-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-262">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-263">Classes used in</span></span>        | [<span data-ttu-id="9a423-264">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a423-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a423-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a423-266">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-266">Entry</span></span> | <span data-ttu-id="9a423-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-268">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-269">MAPI-Id</span></span>                | <span data-ttu-id="9a423-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-270">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-271">System-Only</span></span>            | <span data-ttu-id="9a423-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-272">True</span></span>                                             |
| <span data-ttu-id="9a423-273">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-273">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-274">True</span></span>                                             |
| <span data-ttu-id="9a423-275">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-275">Is Indexed</span></span>             | <span data-ttu-id="9a423-276">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-276">False</span></span>                                            |
| <span data-ttu-id="9a423-277">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-277">In Global Catalog</span></span>      | <span data-ttu-id="9a423-278">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-278">False</span></span>                                            |
| <span data-ttu-id="9a423-279">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-280">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-281">Range-Lower</span></span>            | <span data-ttu-id="9a423-282">0</span><span class="sxs-lookup"><span data-stu-id="9a423-282">0</span></span>                                                |
| <span data-ttu-id="9a423-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-283">Range-Upper</span></span>            | <span data-ttu-id="9a423-284">3</span><span class="sxs-lookup"><span data-stu-id="9a423-284">3</span></span>                                                |
| <span data-ttu-id="9a423-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-285">Search-Flags</span></span>           | <span data-ttu-id="9a423-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-286">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-287">System-Flags</span></span>           | <span data-ttu-id="9a423-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-288">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-289">Classes used in</span></span>        | [<span data-ttu-id="9a423-290">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a423-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a423-291">Windows Server 2012</span></span>



| <span data-ttu-id="9a423-292">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a423-292">Entry</span></span> | <span data-ttu-id="9a423-293">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a423-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a423-294">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a423-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a423-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a423-295">MAPI-Id</span></span>                | <span data-ttu-id="9a423-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="9a423-296">0x80F6</span></span>                                           |
| <span data-ttu-id="9a423-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a423-297">System-Only</span></span>            | <span data-ttu-id="9a423-298">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-298">True</span></span>                                             |
| <span data-ttu-id="9a423-299">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a423-299">Is-Single-Valued</span></span>       | <span data-ttu-id="9a423-300">Vrai</span><span class="sxs-lookup"><span data-stu-id="9a423-300">True</span></span>                                             |
| <span data-ttu-id="9a423-301">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a423-301">Is Indexed</span></span>             | <span data-ttu-id="9a423-302">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-302">False</span></span>                                            |
| <span data-ttu-id="9a423-303">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a423-303">In Global Catalog</span></span>      | <span data-ttu-id="9a423-304">Faux</span><span class="sxs-lookup"><span data-stu-id="9a423-304">False</span></span>                                            |
| <span data-ttu-id="9a423-305">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a423-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a423-306">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a423-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a423-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a423-307">Range-Lower</span></span>            | <span data-ttu-id="9a423-308">0</span><span class="sxs-lookup"><span data-stu-id="9a423-308">0</span></span>                                                |
| <span data-ttu-id="9a423-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a423-309">Range-Upper</span></span>            | <span data-ttu-id="9a423-310">3</span><span class="sxs-lookup"><span data-stu-id="9a423-310">3</span></span>                                                |
| <span data-ttu-id="9a423-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-311">Search-Flags</span></span>           | <span data-ttu-id="9a423-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a423-312">0x00000000</span></span>                                       |
| <span data-ttu-id="9a423-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a423-313">System-Flags</span></span>           | <span data-ttu-id="9a423-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a423-314">0x00000010</span></span>                                       |
| <span data-ttu-id="9a423-315">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a423-315">Classes used in</span></span>        | [<span data-ttu-id="9a423-316">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9a423-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





