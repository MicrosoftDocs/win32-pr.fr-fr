---
title: Attribut System-Only
description: Valeur booléenne qui spécifie si seul Active Directory peut modifier la classe. Les classes uniquement du système peuvent être créées ou supprimées par l’agent de système d’annuaire.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut System-Only
- Schéma AD de l’attribut systemOnly
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844914"
---
# <a name="system-only-attribute"></a><span data-ttu-id="9ad21-106">Attribut System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-106">System-Only attribute</span></span>

<span data-ttu-id="9ad21-107">Valeur booléenne qui spécifie si seul Active Directory peut modifier la classe.</span><span class="sxs-lookup"><span data-stu-id="9ad21-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="9ad21-108">Les classes uniquement du système peuvent être créées ou supprimées par l’agent de système d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="9ad21-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="9ad21-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-109">Entry</span></span> | <span data-ttu-id="9ad21-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9ad21-111">CN</span><span class="sxs-lookup"><span data-stu-id="9ad21-111">CN</span></span>                | <span data-ttu-id="9ad21-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-112">System-Only</span></span>                          |
| <span data-ttu-id="9ad21-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9ad21-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9ad21-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="9ad21-114">systemOnly</span></span>                           |
| <span data-ttu-id="9ad21-115">Taille</span><span class="sxs-lookup"><span data-stu-id="9ad21-115">Size</span></span>              | <span data-ttu-id="9ad21-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="9ad21-116">4 bytes</span></span>                              |
| <span data-ttu-id="9ad21-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9ad21-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9ad21-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9ad21-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9ad21-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-119">Attribute-Id</span></span>      | <span data-ttu-id="9ad21-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="9ad21-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="9ad21-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9ad21-121">System-Id-Guid</span></span>    | <span data-ttu-id="9ad21-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9ad21-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="9ad21-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ad21-123">Syntax</span></span>            | [<span data-ttu-id="9ad21-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ad21-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="9ad21-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9ad21-125">Implementations</span></span>

-   [<span data-ttu-id="9ad21-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9ad21-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9ad21-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ad21-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ad21-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9ad21-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9ad21-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ad21-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ad21-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ad21-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ad21-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ad21-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ad21-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ad21-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9ad21-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ad21-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9ad21-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-134">Entry</span></span> | <span data-ttu-id="9ad21-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-138">System-Only</span></span>            | <span data-ttu-id="9ad21-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-139">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-141">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-142">Is Indexed</span></span>             | <span data-ttu-id="9ad21-143">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-143">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-144">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-145">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-145">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-150">Search-Flags</span></span>           | <span data-ttu-id="9ad21-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-152">System-Flags</span></span>           | <span data-ttu-id="9ad21-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-154">Classes used in</span></span>        | [<span data-ttu-id="9ad21-155">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-156">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9ad21-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ad21-157">Windows Server 2003</span></span>



| <span data-ttu-id="9ad21-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-158">Entry</span></span> | <span data-ttu-id="9ad21-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-162">System-Only</span></span>            | <span data-ttu-id="9ad21-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-163">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-165">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-166">Is Indexed</span></span>             | <span data-ttu-id="9ad21-167">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-167">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-168">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-169">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-169">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-174">Search-Flags</span></span>           | <span data-ttu-id="9ad21-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-176">System-Flags</span></span>           | <span data-ttu-id="9ad21-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-178">Classes used in</span></span>        | [<span data-ttu-id="9ad21-179">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-180">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9ad21-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="9ad21-181">ADAM</span></span>



| <span data-ttu-id="9ad21-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-182">Entry</span></span> | <span data-ttu-id="9ad21-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-186">System-Only</span></span>            | <span data-ttu-id="9ad21-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-187">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-188">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-189">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-190">Is Indexed</span></span>             | <span data-ttu-id="9ad21-191">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-191">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-192">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-193">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-193">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-198">Search-Flags</span></span>           | <span data-ttu-id="9ad21-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-200">System-Flags</span></span>           | <span data-ttu-id="9ad21-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-202">Classes used in</span></span>        | [<span data-ttu-id="9ad21-203">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-204">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ad21-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ad21-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ad21-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-206">Entry</span></span> | <span data-ttu-id="9ad21-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-210">System-Only</span></span>            | <span data-ttu-id="9ad21-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-211">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-212">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-213">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-214">Is Indexed</span></span>             | <span data-ttu-id="9ad21-215">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-215">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-216">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-217">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-217">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-222">Search-Flags</span></span>           | <span data-ttu-id="9ad21-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-224">System-Flags</span></span>           | <span data-ttu-id="9ad21-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-226">Classes used in</span></span>        | [<span data-ttu-id="9ad21-227">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-228">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ad21-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ad21-229">Windows Server 2008</span></span>



| <span data-ttu-id="9ad21-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-230">Entry</span></span> | <span data-ttu-id="9ad21-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-234">System-Only</span></span>            | <span data-ttu-id="9ad21-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-235">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-237">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-238">Is Indexed</span></span>             | <span data-ttu-id="9ad21-239">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-239">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-240">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-241">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-241">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-246">Search-Flags</span></span>           | <span data-ttu-id="9ad21-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-248">System-Flags</span></span>           | <span data-ttu-id="9ad21-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-250">Classes used in</span></span>        | [<span data-ttu-id="9ad21-251">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-252">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ad21-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ad21-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ad21-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-254">Entry</span></span> | <span data-ttu-id="9ad21-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-258">System-Only</span></span>            | <span data-ttu-id="9ad21-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-259">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-260">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-261">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-262">Is Indexed</span></span>             | <span data-ttu-id="9ad21-263">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-263">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-264">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-265">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-265">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-270">Search-Flags</span></span>           | <span data-ttu-id="9ad21-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-272">System-Flags</span></span>           | <span data-ttu-id="9ad21-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-274">Classes used in</span></span>        | [<span data-ttu-id="9ad21-275">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-276">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ad21-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ad21-277">Windows Server 2012</span></span>



| <span data-ttu-id="9ad21-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ad21-278">Entry</span></span> | <span data-ttu-id="9ad21-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad21-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad21-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ad21-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ad21-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9ad21-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ad21-282">System-Only</span></span>            | <span data-ttu-id="9ad21-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-283">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ad21-284">Is-Single-Valued</span></span>       | <span data-ttu-id="9ad21-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ad21-285">True</span></span>                                                                                                      |
| <span data-ttu-id="9ad21-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ad21-286">Is Indexed</span></span>             | <span data-ttu-id="9ad21-287">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-287">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ad21-288">In Global Catalog</span></span>      | <span data-ttu-id="9ad21-289">Faux</span><span class="sxs-lookup"><span data-stu-id="9ad21-289">False</span></span>                                                                                                     |
| <span data-ttu-id="9ad21-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ad21-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ad21-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ad21-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9ad21-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ad21-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ad21-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="9ad21-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-294">Search-Flags</span></span>           | <span data-ttu-id="9ad21-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ad21-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9ad21-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ad21-296">System-Flags</span></span>           | <span data-ttu-id="9ad21-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ad21-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9ad21-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ad21-298">Classes used in</span></span>        | [<span data-ttu-id="9ad21-299">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9ad21-300">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="9ad21-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





