---
title: Attribut système-doit contenir
description: Liste des attributs obligatoires pour une classe. Ces attributs doivent être spécifiés lors de la création d’une instance de la classe. La liste des attributs ne peut être modifiée que par le système.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut système-doit contenir
- Schéma AD de l’attribut systemMustContain
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8d36419ca7e6cd24422645579fb7f9ecc69457
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519969"
---
# <a name="system-must-contain-attribute"></a><span data-ttu-id="7c94a-107">Attribut système-doit contenir</span><span class="sxs-lookup"><span data-stu-id="7c94a-107">System-Must-Contain attribute</span></span>

<span data-ttu-id="7c94a-108">Liste des attributs obligatoires pour une classe.</span><span class="sxs-lookup"><span data-stu-id="7c94a-108">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="7c94a-109">Ces attributs doivent être spécifiés lors de la création d’une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="7c94a-109">These attributes must be specified when an instance of the class is created.</span></span> <span data-ttu-id="7c94a-110">La liste des attributs ne peut être modifiée que par le système.</span><span class="sxs-lookup"><span data-stu-id="7c94a-110">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="7c94a-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-111">Entry</span></span> | <span data-ttu-id="7c94a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-112">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="7c94a-113">CN</span><span class="sxs-lookup"><span data-stu-id="7c94a-113">CN</span></span>                | <span data-ttu-id="7c94a-114">Système-doit contenir</span><span class="sxs-lookup"><span data-stu-id="7c94a-114">System-Must-Contain</span></span>                                                           |
| <span data-ttu-id="7c94a-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c94a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7c94a-116">systemMustContain</span><span class="sxs-lookup"><span data-stu-id="7c94a-116">systemMustContain</span></span>                                                             |
| <span data-ttu-id="7c94a-117">Taille</span><span class="sxs-lookup"><span data-stu-id="7c94a-117">Size</span></span>              | \-                                                                            |
| <span data-ttu-id="7c94a-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7c94a-118">Update Privilege</span></span>  | <span data-ttu-id="7c94a-119">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="7c94a-119">Schema administrator</span></span>                                                          |
| <span data-ttu-id="7c94a-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7c94a-120">Update Frequency</span></span>  | <span data-ttu-id="7c94a-121">Lorsque la classe est créée ou qu’un nouvel attribut obligatoire est ajouté à la classe.</span><span class="sxs-lookup"><span data-stu-id="7c94a-121">When the class is created or a new mandatory attribute is added to the class.</span></span> |
| <span data-ttu-id="7c94a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-122">Attribute-Id</span></span>      | <span data-ttu-id="7c94a-123">1.2.840.113556.1.4.197</span><span class="sxs-lookup"><span data-stu-id="7c94a-123">1.2.840.113556.1.4.197</span></span>                                                        |
| <span data-ttu-id="7c94a-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7c94a-124">System-Id-Guid</span></span>    | <span data-ttu-id="7c94a-125">bf967a45-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7c94a-125">bf967a45-0de6-11d0-a285-00aa003049e2</span></span>                                          |
| <span data-ttu-id="7c94a-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c94a-126">Syntax</span></span>            | [<span data-ttu-id="7c94a-127">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="7c94a-127">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)               |



## <a name="implementations"></a><span data-ttu-id="7c94a-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7c94a-128">Implementations</span></span>

-   [<span data-ttu-id="7c94a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c94a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c94a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c94a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c94a-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7c94a-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7c94a-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c94a-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c94a-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c94a-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c94a-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c94a-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c94a-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c94a-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c94a-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c94a-136">Windows 2000 Server</span></span>



| <span data-ttu-id="7c94a-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-137">Entry</span></span> | <span data-ttu-id="7c94a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-138">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-139">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-140">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-141">System-Only</span></span>            | <span data-ttu-id="7c94a-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-142">True</span></span>                                             |
| <span data-ttu-id="7c94a-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-144">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-144">False</span></span>                                            |
| <span data-ttu-id="7c94a-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-145">Is Indexed</span></span>             | <span data-ttu-id="7c94a-146">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-146">False</span></span>                                            |
| <span data-ttu-id="7c94a-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-147">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-148">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-148">False</span></span>                                            |
| <span data-ttu-id="7c94a-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-151">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-152">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-153">Search-Flags</span></span>           | <span data-ttu-id="7c94a-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-154">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-155">System-Flags</span></span>           | <span data-ttu-id="7c94a-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-156">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-157">Classes used in</span></span>        | [<span data-ttu-id="7c94a-158">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c94a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c94a-159">Windows Server 2003</span></span>



| <span data-ttu-id="7c94a-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-160">Entry</span></span> | <span data-ttu-id="7c94a-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-161">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-162">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-163">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-164">System-Only</span></span>            | <span data-ttu-id="7c94a-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-165">True</span></span>                                             |
| <span data-ttu-id="7c94a-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-167">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-167">False</span></span>                                            |
| <span data-ttu-id="7c94a-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-168">Is Indexed</span></span>             | <span data-ttu-id="7c94a-169">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-169">False</span></span>                                            |
| <span data-ttu-id="7c94a-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-170">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-171">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-171">False</span></span>                                            |
| <span data-ttu-id="7c94a-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-176">Search-Flags</span></span>           | <span data-ttu-id="7c94a-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-177">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-178">System-Flags</span></span>           | <span data-ttu-id="7c94a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-179">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-180">Classes used in</span></span>        | [<span data-ttu-id="7c94a-181">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-181">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7c94a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="7c94a-182">ADAM</span></span>



| <span data-ttu-id="7c94a-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-183">Entry</span></span> | <span data-ttu-id="7c94a-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-186">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-187">System-Only</span></span>            | <span data-ttu-id="7c94a-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-188">True</span></span>                                             |
| <span data-ttu-id="7c94a-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-190">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-190">False</span></span>                                            |
| <span data-ttu-id="7c94a-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-191">Is Indexed</span></span>             | <span data-ttu-id="7c94a-192">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-192">False</span></span>                                            |
| <span data-ttu-id="7c94a-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-193">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-194">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-194">False</span></span>                                            |
| <span data-ttu-id="7c94a-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-196">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-197">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-198">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-199">Search-Flags</span></span>           | <span data-ttu-id="7c94a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-200">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-201">System-Flags</span></span>           | <span data-ttu-id="7c94a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-202">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-203">Classes used in</span></span>        | [<span data-ttu-id="7c94a-204">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c94a-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c94a-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c94a-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-206">Entry</span></span> | <span data-ttu-id="7c94a-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-207">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-208">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-209">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-210">System-Only</span></span>            | <span data-ttu-id="7c94a-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-211">True</span></span>                                             |
| <span data-ttu-id="7c94a-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-213">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-213">False</span></span>                                            |
| <span data-ttu-id="7c94a-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-214">Is Indexed</span></span>             | <span data-ttu-id="7c94a-215">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-215">False</span></span>                                            |
| <span data-ttu-id="7c94a-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-216">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-217">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-217">False</span></span>                                            |
| <span data-ttu-id="7c94a-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-219">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-220">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-221">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-222">Search-Flags</span></span>           | <span data-ttu-id="7c94a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-223">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-224">System-Flags</span></span>           | <span data-ttu-id="7c94a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-225">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-226">Classes used in</span></span>        | [<span data-ttu-id="7c94a-227">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-227">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c94a-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c94a-228">Windows Server 2008</span></span>



| <span data-ttu-id="7c94a-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-229">Entry</span></span> | <span data-ttu-id="7c94a-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-230">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-231">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-232">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-233">System-Only</span></span>            | <span data-ttu-id="7c94a-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-234">True</span></span>                                             |
| <span data-ttu-id="7c94a-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-236">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-236">False</span></span>                                            |
| <span data-ttu-id="7c94a-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-237">Is Indexed</span></span>             | <span data-ttu-id="7c94a-238">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-238">False</span></span>                                            |
| <span data-ttu-id="7c94a-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-239">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-240">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-240">False</span></span>                                            |
| <span data-ttu-id="7c94a-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-242">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-243">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-244">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-245">Search-Flags</span></span>           | <span data-ttu-id="7c94a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-246">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-247">System-Flags</span></span>           | <span data-ttu-id="7c94a-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-248">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-249">Classes used in</span></span>        | [<span data-ttu-id="7c94a-250">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-250">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c94a-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c94a-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c94a-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-252">Entry</span></span> | <span data-ttu-id="7c94a-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-253">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-254">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-255">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-256">System-Only</span></span>            | <span data-ttu-id="7c94a-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-257">True</span></span>                                             |
| <span data-ttu-id="7c94a-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-258">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-259">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-259">False</span></span>                                            |
| <span data-ttu-id="7c94a-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-260">Is Indexed</span></span>             | <span data-ttu-id="7c94a-261">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-261">False</span></span>                                            |
| <span data-ttu-id="7c94a-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-262">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-263">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-263">False</span></span>                                            |
| <span data-ttu-id="7c94a-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-265">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-266">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-267">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-268">Search-Flags</span></span>           | <span data-ttu-id="7c94a-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-269">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-270">System-Flags</span></span>           | <span data-ttu-id="7c94a-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-271">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-272">Classes used in</span></span>        | [<span data-ttu-id="7c94a-273">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-273">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c94a-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c94a-274">Windows Server 2012</span></span>



| <span data-ttu-id="7c94a-275">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c94a-275">Entry</span></span> | <span data-ttu-id="7c94a-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c94a-276">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c94a-277">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c94a-277">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c94a-278">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c94a-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c94a-279">System-Only</span></span>            | <span data-ttu-id="7c94a-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c94a-280">True</span></span>                                             |
| <span data-ttu-id="7c94a-281">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c94a-281">Is-Single-Valued</span></span>       | <span data-ttu-id="7c94a-282">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-282">False</span></span>                                            |
| <span data-ttu-id="7c94a-283">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c94a-283">Is Indexed</span></span>             | <span data-ttu-id="7c94a-284">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-284">False</span></span>                                            |
| <span data-ttu-id="7c94a-285">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c94a-285">In Global Catalog</span></span>      | <span data-ttu-id="7c94a-286">Faux</span><span class="sxs-lookup"><span data-stu-id="7c94a-286">False</span></span>                                            |
| <span data-ttu-id="7c94a-287">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c94a-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c94a-288">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c94a-288">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c94a-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c94a-289">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c94a-290">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c94a-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-291">Search-Flags</span></span>           | <span data-ttu-id="7c94a-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c94a-292">0x00000000</span></span>                                       |
| <span data-ttu-id="7c94a-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c94a-293">System-Flags</span></span>           | <span data-ttu-id="7c94a-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c94a-294">0x00000010</span></span>                                       |
| <span data-ttu-id="7c94a-295">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c94a-295">Classes used in</span></span>        | [<span data-ttu-id="7c94a-296">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="7c94a-296">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





