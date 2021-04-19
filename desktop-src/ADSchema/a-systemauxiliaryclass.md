---
title: Attribut de classe système-auxiliaire
description: Liste des classes auxiliaires qui ne peuvent pas être modifiées par l’utilisateur.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de classe auxiliaire système
- Schéma AD de l’attribut systemAuxiliaryClass
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106513061"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="3a169-105">Attribut de classe système-auxiliaire</span><span class="sxs-lookup"><span data-stu-id="3a169-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="3a169-106">Liste des classes auxiliaires qui ne peuvent pas être modifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a169-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="3a169-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-107">Entry</span></span> | <span data-ttu-id="3a169-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3a169-109">CN</span><span class="sxs-lookup"><span data-stu-id="3a169-109">CN</span></span>                | <span data-ttu-id="3a169-110">System-auxiliaire-Class</span><span class="sxs-lookup"><span data-stu-id="3a169-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="3a169-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3a169-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3a169-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="3a169-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="3a169-113">Taille</span><span class="sxs-lookup"><span data-stu-id="3a169-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="3a169-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3a169-114">Update Privilege</span></span>  | <span data-ttu-id="3a169-115">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="3a169-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="3a169-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3a169-116">Update Frequency</span></span>  | <span data-ttu-id="3a169-117">Lorsque la classe est créée ou qu’une nouvelle classe auxiliaire y est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3a169-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="3a169-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-118">Attribute-Id</span></span>      | <span data-ttu-id="3a169-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="3a169-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="3a169-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3a169-120">System-Id-Guid</span></span>    | <span data-ttu-id="3a169-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3a169-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="3a169-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a169-122">Syntax</span></span>            | [<span data-ttu-id="3a169-123">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="3a169-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="3a169-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3a169-124">Implementations</span></span>

-   [<span data-ttu-id="3a169-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3a169-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3a169-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3a169-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3a169-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3a169-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3a169-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3a169-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3a169-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3a169-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3a169-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3a169-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3a169-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3a169-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3a169-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3a169-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3a169-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-133">Entry</span></span> | <span data-ttu-id="3a169-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-137">System-Only</span></span>            | <span data-ttu-id="3a169-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-138">True</span></span>                                             |
| <span data-ttu-id="3a169-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-140">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-140">False</span></span>                                            |
| <span data-ttu-id="3a169-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-141">Is Indexed</span></span>             | <span data-ttu-id="3a169-142">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-142">False</span></span>                                            |
| <span data-ttu-id="3a169-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-143">In Global Catalog</span></span>      | <span data-ttu-id="3a169-144">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-144">False</span></span>                                            |
| <span data-ttu-id="3a169-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-149">Search-Flags</span></span>           | <span data-ttu-id="3a169-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-150">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-151">System-Flags</span></span>           | <span data-ttu-id="3a169-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-152">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-153">Classes used in</span></span>        | [<span data-ttu-id="3a169-154">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3a169-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a169-155">Windows Server 2003</span></span>



| <span data-ttu-id="3a169-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-156">Entry</span></span> | <span data-ttu-id="3a169-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-160">System-Only</span></span>            | <span data-ttu-id="3a169-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-161">True</span></span>                                             |
| <span data-ttu-id="3a169-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-163">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-163">False</span></span>                                            |
| <span data-ttu-id="3a169-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-164">Is Indexed</span></span>             | <span data-ttu-id="3a169-165">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-165">False</span></span>                                            |
| <span data-ttu-id="3a169-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-166">In Global Catalog</span></span>      | <span data-ttu-id="3a169-167">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-167">False</span></span>                                            |
| <span data-ttu-id="3a169-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-172">Search-Flags</span></span>           | <span data-ttu-id="3a169-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-173">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-174">System-Flags</span></span>           | <span data-ttu-id="3a169-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-175">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-176">Classes used in</span></span>        | [<span data-ttu-id="3a169-177">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3a169-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="3a169-178">ADAM</span></span>



| <span data-ttu-id="3a169-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-179">Entry</span></span> | <span data-ttu-id="3a169-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-183">System-Only</span></span>            | <span data-ttu-id="3a169-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-184">True</span></span>                                             |
| <span data-ttu-id="3a169-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-186">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-186">False</span></span>                                            |
| <span data-ttu-id="3a169-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-187">Is Indexed</span></span>             | <span data-ttu-id="3a169-188">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-188">False</span></span>                                            |
| <span data-ttu-id="3a169-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-189">In Global Catalog</span></span>      | <span data-ttu-id="3a169-190">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-190">False</span></span>                                            |
| <span data-ttu-id="3a169-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-195">Search-Flags</span></span>           | <span data-ttu-id="3a169-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-196">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-197">System-Flags</span></span>           | <span data-ttu-id="3a169-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-198">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-199">Classes used in</span></span>        | [<span data-ttu-id="3a169-200">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3a169-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3a169-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3a169-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-202">Entry</span></span> | <span data-ttu-id="3a169-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-206">System-Only</span></span>            | <span data-ttu-id="3a169-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-207">True</span></span>                                             |
| <span data-ttu-id="3a169-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-208">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-209">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-209">False</span></span>                                            |
| <span data-ttu-id="3a169-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-210">Is Indexed</span></span>             | <span data-ttu-id="3a169-211">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-211">False</span></span>                                            |
| <span data-ttu-id="3a169-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-212">In Global Catalog</span></span>      | <span data-ttu-id="3a169-213">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-213">False</span></span>                                            |
| <span data-ttu-id="3a169-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-218">Search-Flags</span></span>           | <span data-ttu-id="3a169-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-219">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-220">System-Flags</span></span>           | <span data-ttu-id="3a169-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-221">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-222">Classes used in</span></span>        | [<span data-ttu-id="3a169-223">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3a169-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a169-224">Windows Server 2008</span></span>



| <span data-ttu-id="3a169-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-225">Entry</span></span> | <span data-ttu-id="3a169-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-229">System-Only</span></span>            | <span data-ttu-id="3a169-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-230">True</span></span>                                             |
| <span data-ttu-id="3a169-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-231">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-232">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-232">False</span></span>                                            |
| <span data-ttu-id="3a169-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-233">Is Indexed</span></span>             | <span data-ttu-id="3a169-234">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-234">False</span></span>                                            |
| <span data-ttu-id="3a169-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-235">In Global Catalog</span></span>      | <span data-ttu-id="3a169-236">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-236">False</span></span>                                            |
| <span data-ttu-id="3a169-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-241">Search-Flags</span></span>           | <span data-ttu-id="3a169-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-242">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-243">System-Flags</span></span>           | <span data-ttu-id="3a169-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-244">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-245">Classes used in</span></span>        | [<span data-ttu-id="3a169-246">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3a169-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a169-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3a169-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-248">Entry</span></span> | <span data-ttu-id="3a169-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-252">System-Only</span></span>            | <span data-ttu-id="3a169-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-253">True</span></span>                                             |
| <span data-ttu-id="3a169-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-254">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-255">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-255">False</span></span>                                            |
| <span data-ttu-id="3a169-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-256">Is Indexed</span></span>             | <span data-ttu-id="3a169-257">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-257">False</span></span>                                            |
| <span data-ttu-id="3a169-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-258">In Global Catalog</span></span>      | <span data-ttu-id="3a169-259">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-259">False</span></span>                                            |
| <span data-ttu-id="3a169-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-264">Search-Flags</span></span>           | <span data-ttu-id="3a169-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-265">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-266">System-Flags</span></span>           | <span data-ttu-id="3a169-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-267">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-268">Classes used in</span></span>        | [<span data-ttu-id="3a169-269">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3a169-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a169-270">Windows Server 2012</span></span>



| <span data-ttu-id="3a169-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="3a169-271">Entry</span></span> | <span data-ttu-id="3a169-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a169-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3a169-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3a169-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a169-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3a169-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a169-275">System-Only</span></span>            | <span data-ttu-id="3a169-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="3a169-276">True</span></span>                                             |
| <span data-ttu-id="3a169-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3a169-277">Is-Single-Valued</span></span>       | <span data-ttu-id="3a169-278">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-278">False</span></span>                                            |
| <span data-ttu-id="3a169-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3a169-279">Is Indexed</span></span>             | <span data-ttu-id="3a169-280">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-280">False</span></span>                                            |
| <span data-ttu-id="3a169-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3a169-281">In Global Catalog</span></span>      | <span data-ttu-id="3a169-282">Faux</span><span class="sxs-lookup"><span data-stu-id="3a169-282">False</span></span>                                            |
| <span data-ttu-id="3a169-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3a169-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a169-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3a169-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3a169-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a169-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3a169-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a169-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3a169-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-287">Search-Flags</span></span>           | <span data-ttu-id="3a169-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a169-288">0x00000000</span></span>                                       |
| <span data-ttu-id="3a169-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a169-289">System-Flags</span></span>           | <span data-ttu-id="3a169-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a169-290">0x00000010</span></span>                                       |
| <span data-ttu-id="3a169-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3a169-291">Classes used in</span></span>        | [<span data-ttu-id="3a169-292">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="3a169-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





