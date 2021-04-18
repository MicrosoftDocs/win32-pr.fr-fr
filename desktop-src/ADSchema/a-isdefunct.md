---
title: Attribut Is-Defunct
description: Si la valeur est TRUE, la classe ou l’attribut n’est plus utilisable. Les anciennes versions de cet objet peuvent exister, mais de nouvelles ne peuvent pas être créées.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Is-Defunct
- Schéma AD de l’attribut isDefunct
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106512001"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="304ae-106">Attribut Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="304ae-106">Is-Defunct attribute</span></span>

<span data-ttu-id="304ae-107">Si la **valeur est true**, la classe ou l’attribut n’est plus utilisable.</span><span class="sxs-lookup"><span data-stu-id="304ae-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="304ae-108">Les anciennes versions de cet objet peuvent exister, mais de nouvelles ne peuvent pas être créées.</span><span class="sxs-lookup"><span data-stu-id="304ae-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="304ae-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-109">Entry</span></span> | <span data-ttu-id="304ae-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="304ae-111">CN</span><span class="sxs-lookup"><span data-stu-id="304ae-111">CN</span></span>                | <span data-ttu-id="304ae-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="304ae-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="304ae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="304ae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="304ae-114">Définie</span><span class="sxs-lookup"><span data-stu-id="304ae-114">isDefunct</span></span>                            |
| <span data-ttu-id="304ae-115">Taille</span><span class="sxs-lookup"><span data-stu-id="304ae-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="304ae-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="304ae-116">Update Privilege</span></span>  | <span data-ttu-id="304ae-117">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="304ae-117">Schema administrator</span></span>                 |
| <span data-ttu-id="304ae-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="304ae-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="304ae-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-119">Attribute-Id</span></span>      | <span data-ttu-id="304ae-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="304ae-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="304ae-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="304ae-121">System-Id-Guid</span></span>    | <span data-ttu-id="304ae-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="304ae-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="304ae-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="304ae-123">Syntax</span></span>            | [<span data-ttu-id="304ae-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="304ae-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="304ae-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="304ae-125">Implementations</span></span>

-   [<span data-ttu-id="304ae-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="304ae-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="304ae-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="304ae-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="304ae-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="304ae-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="304ae-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="304ae-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="304ae-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="304ae-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="304ae-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="304ae-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="304ae-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="304ae-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="304ae-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="304ae-133">Windows 2000 Server</span></span>



| <span data-ttu-id="304ae-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-134">Entry</span></span> | <span data-ttu-id="304ae-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-138">System-Only</span></span>            | <span data-ttu-id="304ae-139">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-139">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-140">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-141">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-142">Is Indexed</span></span>             | <span data-ttu-id="304ae-143">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-143">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-144">In Global Catalog</span></span>      | <span data-ttu-id="304ae-145">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-145">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-150">Search-Flags</span></span>           | <span data-ttu-id="304ae-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-152">System-Flags</span></span>           | <span data-ttu-id="304ae-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-154">Classes used in</span></span>        | [<span data-ttu-id="304ae-155">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-156">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="304ae-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="304ae-157">Windows Server 2003</span></span>



| <span data-ttu-id="304ae-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-158">Entry</span></span> | <span data-ttu-id="304ae-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-162">System-Only</span></span>            | <span data-ttu-id="304ae-163">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-163">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-164">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-165">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-166">Is Indexed</span></span>             | <span data-ttu-id="304ae-167">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-167">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-168">In Global Catalog</span></span>      | <span data-ttu-id="304ae-169">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-169">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-174">Search-Flags</span></span>           | <span data-ttu-id="304ae-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-176">System-Flags</span></span>           | <span data-ttu-id="304ae-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-178">Classes used in</span></span>        | [<span data-ttu-id="304ae-179">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-180">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="304ae-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="304ae-181">ADAM</span></span>



| <span data-ttu-id="304ae-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-182">Entry</span></span> | <span data-ttu-id="304ae-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-186">System-Only</span></span>            | <span data-ttu-id="304ae-187">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-187">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-188">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-189">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-190">Is Indexed</span></span>             | <span data-ttu-id="304ae-191">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-191">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-192">In Global Catalog</span></span>      | <span data-ttu-id="304ae-193">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-193">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-198">Search-Flags</span></span>           | <span data-ttu-id="304ae-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-200">System-Flags</span></span>           | <span data-ttu-id="304ae-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-202">Classes used in</span></span>        | [<span data-ttu-id="304ae-203">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-204">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="304ae-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="304ae-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="304ae-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-206">Entry</span></span> | <span data-ttu-id="304ae-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-210">System-Only</span></span>            | <span data-ttu-id="304ae-211">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-211">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-212">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-213">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-214">Is Indexed</span></span>             | <span data-ttu-id="304ae-215">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-215">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-216">In Global Catalog</span></span>      | <span data-ttu-id="304ae-217">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-217">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-222">Search-Flags</span></span>           | <span data-ttu-id="304ae-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-224">System-Flags</span></span>           | <span data-ttu-id="304ae-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-226">Classes used in</span></span>        | [<span data-ttu-id="304ae-227">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-228">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="304ae-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="304ae-229">Windows Server 2008</span></span>



| <span data-ttu-id="304ae-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-230">Entry</span></span> | <span data-ttu-id="304ae-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-234">System-Only</span></span>            | <span data-ttu-id="304ae-235">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-235">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-236">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-237">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-238">Is Indexed</span></span>             | <span data-ttu-id="304ae-239">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-239">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-240">In Global Catalog</span></span>      | <span data-ttu-id="304ae-241">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-241">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-246">Search-Flags</span></span>           | <span data-ttu-id="304ae-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-248">System-Flags</span></span>           | <span data-ttu-id="304ae-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-250">Classes used in</span></span>        | [<span data-ttu-id="304ae-251">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-252">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="304ae-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="304ae-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="304ae-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-254">Entry</span></span> | <span data-ttu-id="304ae-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-258">System-Only</span></span>            | <span data-ttu-id="304ae-259">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-259">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-260">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-261">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-262">Is Indexed</span></span>             | <span data-ttu-id="304ae-263">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-263">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-264">In Global Catalog</span></span>      | <span data-ttu-id="304ae-265">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-265">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-270">Search-Flags</span></span>           | <span data-ttu-id="304ae-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-272">System-Flags</span></span>           | <span data-ttu-id="304ae-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-274">Classes used in</span></span>        | [<span data-ttu-id="304ae-275">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-276">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="304ae-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="304ae-277">Windows Server 2012</span></span>



| <span data-ttu-id="304ae-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="304ae-278">Entry</span></span> | <span data-ttu-id="304ae-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ae-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ae-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="304ae-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="304ae-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="304ae-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="304ae-282">System-Only</span></span>            | <span data-ttu-id="304ae-283">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-283">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="304ae-284">Is-Single-Valued</span></span>       | <span data-ttu-id="304ae-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="304ae-285">True</span></span>                                                                                                      |
| <span data-ttu-id="304ae-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="304ae-286">Is Indexed</span></span>             | <span data-ttu-id="304ae-287">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-287">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="304ae-288">In Global Catalog</span></span>      | <span data-ttu-id="304ae-289">Faux</span><span class="sxs-lookup"><span data-stu-id="304ae-289">False</span></span>                                                                                                     |
| <span data-ttu-id="304ae-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="304ae-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="304ae-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="304ae-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="304ae-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="304ae-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="304ae-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="304ae-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-294">Search-Flags</span></span>           | <span data-ttu-id="304ae-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="304ae-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="304ae-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="304ae-296">System-Flags</span></span>           | <span data-ttu-id="304ae-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="304ae-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="304ae-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="304ae-298">Classes used in</span></span>        | [<span data-ttu-id="304ae-299">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="304ae-300">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="304ae-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





