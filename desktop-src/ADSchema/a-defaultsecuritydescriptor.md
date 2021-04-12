---
title: Attribut de descripteur de sécurité par défaut
description: Descripteur de sécurité à assigner à l’objet lors de sa création.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut default-Security-Descriptor
- Schéma AD de l’attribut defaultSecurityDescriptor
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479733"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="92ea1-105">Attribut de descripteur de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="92ea1-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="92ea1-106">Descripteur de sécurité à assigner à l’objet lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="92ea1-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="92ea1-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-107">Entry</span></span> | <span data-ttu-id="92ea1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="92ea1-109">CN</span><span class="sxs-lookup"><span data-stu-id="92ea1-109">CN</span></span>                | <span data-ttu-id="92ea1-110">Descripteur de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="92ea1-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="92ea1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="92ea1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92ea1-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="92ea1-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="92ea1-113">Taille</span><span class="sxs-lookup"><span data-stu-id="92ea1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="92ea1-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="92ea1-114">Update Privilege</span></span>  | <span data-ttu-id="92ea1-115">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="92ea1-115">Schema administrator</span></span>                        |
| <span data-ttu-id="92ea1-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="92ea1-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="92ea1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-117">Attribute-Id</span></span>      | <span data-ttu-id="92ea1-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="92ea1-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="92ea1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92ea1-119">System-Id-Guid</span></span>    | <span data-ttu-id="92ea1-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="92ea1-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="92ea1-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92ea1-121">Syntax</span></span>            | [<span data-ttu-id="92ea1-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="92ea1-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="92ea1-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="92ea1-123">Implementations</span></span>

-   [<span data-ttu-id="92ea1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92ea1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92ea1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92ea1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92ea1-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="92ea1-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="92ea1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92ea1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92ea1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92ea1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92ea1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92ea1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92ea1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92ea1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92ea1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92ea1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="92ea1-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-132">Entry</span></span> | <span data-ttu-id="92ea1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-136">System-Only</span></span>            | <span data-ttu-id="92ea1-137">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-137">False</span></span>                                            |
| <span data-ttu-id="92ea1-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-139">True</span></span>                                             |
| <span data-ttu-id="92ea1-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-140">Is Indexed</span></span>             | <span data-ttu-id="92ea1-141">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-141">False</span></span>                                            |
| <span data-ttu-id="92ea1-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-142">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-143">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-143">False</span></span>                                            |
| <span data-ttu-id="92ea1-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-146">Range-Lower</span></span>            | <span data-ttu-id="92ea1-147">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-147">0</span></span>                                                |
| <span data-ttu-id="92ea1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-148">Range-Upper</span></span>            | <span data-ttu-id="92ea1-149">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-149">32767</span></span>                                            |
| <span data-ttu-id="92ea1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-150">Search-Flags</span></span>           | <span data-ttu-id="92ea1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-151">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-152">System-Flags</span></span>           | <span data-ttu-id="92ea1-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-153">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-154">Classes used in</span></span>        | [<span data-ttu-id="92ea1-155">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92ea1-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92ea1-156">Windows Server 2003</span></span>



| <span data-ttu-id="92ea1-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-157">Entry</span></span> | <span data-ttu-id="92ea1-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-161">System-Only</span></span>            | <span data-ttu-id="92ea1-162">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-162">False</span></span>                                            |
| <span data-ttu-id="92ea1-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-164">True</span></span>                                             |
| <span data-ttu-id="92ea1-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-165">Is Indexed</span></span>             | <span data-ttu-id="92ea1-166">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-166">False</span></span>                                            |
| <span data-ttu-id="92ea1-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-167">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-168">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-168">False</span></span>                                            |
| <span data-ttu-id="92ea1-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-171">Range-Lower</span></span>            | <span data-ttu-id="92ea1-172">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-172">0</span></span>                                                |
| <span data-ttu-id="92ea1-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-173">Range-Upper</span></span>            | <span data-ttu-id="92ea1-174">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-174">32767</span></span>                                            |
| <span data-ttu-id="92ea1-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-175">Search-Flags</span></span>           | <span data-ttu-id="92ea1-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-176">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-177">System-Flags</span></span>           | <span data-ttu-id="92ea1-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-178">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-179">Classes used in</span></span>        | [<span data-ttu-id="92ea1-180">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="92ea1-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="92ea1-181">ADAM</span></span>



| <span data-ttu-id="92ea1-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-182">Entry</span></span> | <span data-ttu-id="92ea1-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-186">System-Only</span></span>            | <span data-ttu-id="92ea1-187">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-187">False</span></span>                                            |
| <span data-ttu-id="92ea1-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-188">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-189">True</span></span>                                             |
| <span data-ttu-id="92ea1-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-190">Is Indexed</span></span>             | <span data-ttu-id="92ea1-191">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-191">False</span></span>                                            |
| <span data-ttu-id="92ea1-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-192">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-193">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-193">False</span></span>                                            |
| <span data-ttu-id="92ea1-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-196">Range-Lower</span></span>            | <span data-ttu-id="92ea1-197">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-197">0</span></span>                                                |
| <span data-ttu-id="92ea1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-198">Range-Upper</span></span>            | <span data-ttu-id="92ea1-199">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-199">32767</span></span>                                            |
| <span data-ttu-id="92ea1-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-200">Search-Flags</span></span>           | <span data-ttu-id="92ea1-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-201">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-202">System-Flags</span></span>           | <span data-ttu-id="92ea1-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-203">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-204">Classes used in</span></span>        | [<span data-ttu-id="92ea1-205">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92ea1-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92ea1-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92ea1-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-207">Entry</span></span> | <span data-ttu-id="92ea1-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-211">System-Only</span></span>            | <span data-ttu-id="92ea1-212">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-212">False</span></span>                                            |
| <span data-ttu-id="92ea1-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-213">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-214">True</span></span>                                             |
| <span data-ttu-id="92ea1-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-215">Is Indexed</span></span>             | <span data-ttu-id="92ea1-216">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-216">False</span></span>                                            |
| <span data-ttu-id="92ea1-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-217">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-218">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-218">False</span></span>                                            |
| <span data-ttu-id="92ea1-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-221">Range-Lower</span></span>            | <span data-ttu-id="92ea1-222">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-222">0</span></span>                                                |
| <span data-ttu-id="92ea1-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-223">Range-Upper</span></span>            | <span data-ttu-id="92ea1-224">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-224">32767</span></span>                                            |
| <span data-ttu-id="92ea1-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-225">Search-Flags</span></span>           | <span data-ttu-id="92ea1-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-226">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-227">System-Flags</span></span>           | <span data-ttu-id="92ea1-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-228">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-229">Classes used in</span></span>        | [<span data-ttu-id="92ea1-230">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92ea1-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92ea1-231">Windows Server 2008</span></span>



| <span data-ttu-id="92ea1-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-232">Entry</span></span> | <span data-ttu-id="92ea1-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-236">System-Only</span></span>            | <span data-ttu-id="92ea1-237">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-237">False</span></span>                                            |
| <span data-ttu-id="92ea1-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-238">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-239">True</span></span>                                             |
| <span data-ttu-id="92ea1-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-240">Is Indexed</span></span>             | <span data-ttu-id="92ea1-241">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-241">False</span></span>                                            |
| <span data-ttu-id="92ea1-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-242">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-243">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-243">False</span></span>                                            |
| <span data-ttu-id="92ea1-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-246">Range-Lower</span></span>            | <span data-ttu-id="92ea1-247">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-247">0</span></span>                                                |
| <span data-ttu-id="92ea1-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-248">Range-Upper</span></span>            | <span data-ttu-id="92ea1-249">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-249">32767</span></span>                                            |
| <span data-ttu-id="92ea1-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-250">Search-Flags</span></span>           | <span data-ttu-id="92ea1-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-251">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-252">System-Flags</span></span>           | <span data-ttu-id="92ea1-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-253">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-254">Classes used in</span></span>        | [<span data-ttu-id="92ea1-255">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92ea1-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92ea1-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92ea1-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-257">Entry</span></span> | <span data-ttu-id="92ea1-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-261">System-Only</span></span>            | <span data-ttu-id="92ea1-262">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-262">False</span></span>                                            |
| <span data-ttu-id="92ea1-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-263">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-264">True</span></span>                                             |
| <span data-ttu-id="92ea1-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-265">Is Indexed</span></span>             | <span data-ttu-id="92ea1-266">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-266">False</span></span>                                            |
| <span data-ttu-id="92ea1-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-267">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-268">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-268">False</span></span>                                            |
| <span data-ttu-id="92ea1-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-271">Range-Lower</span></span>            | <span data-ttu-id="92ea1-272">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-272">0</span></span>                                                |
| <span data-ttu-id="92ea1-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-273">Range-Upper</span></span>            | <span data-ttu-id="92ea1-274">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-274">32767</span></span>                                            |
| <span data-ttu-id="92ea1-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-275">Search-Flags</span></span>           | <span data-ttu-id="92ea1-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-276">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-277">System-Flags</span></span>           | <span data-ttu-id="92ea1-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-278">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-279">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-279">Classes used in</span></span>        | [<span data-ttu-id="92ea1-280">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92ea1-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92ea1-281">Windows Server 2012</span></span>



| <span data-ttu-id="92ea1-282">Entrée</span><span class="sxs-lookup"><span data-stu-id="92ea1-282">Entry</span></span> | <span data-ttu-id="92ea1-283">Valeur</span><span class="sxs-lookup"><span data-stu-id="92ea1-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="92ea1-284">ID de lien</span><span class="sxs-lookup"><span data-stu-id="92ea1-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ea1-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="92ea1-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ea1-286">System-Only</span></span>            | <span data-ttu-id="92ea1-287">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-287">False</span></span>                                            |
| <span data-ttu-id="92ea1-288">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="92ea1-288">Is-Single-Valued</span></span>       | <span data-ttu-id="92ea1-289">Vrai</span><span class="sxs-lookup"><span data-stu-id="92ea1-289">True</span></span>                                             |
| <span data-ttu-id="92ea1-290">Est indexé</span><span class="sxs-lookup"><span data-stu-id="92ea1-290">Is Indexed</span></span>             | <span data-ttu-id="92ea1-291">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-291">False</span></span>                                            |
| <span data-ttu-id="92ea1-292">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="92ea1-292">In Global Catalog</span></span>      | <span data-ttu-id="92ea1-293">Faux</span><span class="sxs-lookup"><span data-stu-id="92ea1-293">False</span></span>                                            |
| <span data-ttu-id="92ea1-294">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="92ea1-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ea1-295">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="92ea1-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="92ea1-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ea1-296">Range-Lower</span></span>            | <span data-ttu-id="92ea1-297">0</span><span class="sxs-lookup"><span data-stu-id="92ea1-297">0</span></span>                                                |
| <span data-ttu-id="92ea1-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ea1-298">Range-Upper</span></span>            | <span data-ttu-id="92ea1-299">32767</span><span class="sxs-lookup"><span data-stu-id="92ea1-299">32767</span></span>                                            |
| <span data-ttu-id="92ea1-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-300">Search-Flags</span></span>           | <span data-ttu-id="92ea1-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92ea1-301">0x00000000</span></span>                                       |
| <span data-ttu-id="92ea1-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ea1-302">System-Flags</span></span>           | <span data-ttu-id="92ea1-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92ea1-303">0x00000010</span></span>                                       |
| <span data-ttu-id="92ea1-304">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="92ea1-304">Classes used in</span></span>        | [<span data-ttu-id="92ea1-305">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="92ea1-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





