---
title: Attribut système-peut contenir
description: Liste des attributs facultatifs d’une classe. La liste des attributs ne peut être modifiée que par le système.
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut système-peut-être
- Schéma AD de l’attribut systemMayContain
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03730e9904cbaa6ee5954662556fba261c51cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107503"
---
# <a name="system-may-contain-attribute"></a><span data-ttu-id="d46c1-106">Attribut système-peut contenir</span><span class="sxs-lookup"><span data-stu-id="d46c1-106">System-May-Contain attribute</span></span>

<span data-ttu-id="d46c1-107">Liste des attributs facultatifs d’une classe.</span><span class="sxs-lookup"><span data-stu-id="d46c1-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="d46c1-108">La liste des attributs ne peut être modifiée que par le système.</span><span class="sxs-lookup"><span data-stu-id="d46c1-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="d46c1-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-109">Entry</span></span> | <span data-ttu-id="d46c1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d46c1-111">CN</span><span class="sxs-lookup"><span data-stu-id="d46c1-111">CN</span></span>                | <span data-ttu-id="d46c1-112">Système-peut contenir</span><span class="sxs-lookup"><span data-stu-id="d46c1-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="d46c1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d46c1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d46c1-114">systemMayContain</span><span class="sxs-lookup"><span data-stu-id="d46c1-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="d46c1-115">Taille</span><span class="sxs-lookup"><span data-stu-id="d46c1-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="d46c1-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d46c1-116">Update Privilege</span></span>  | <span data-ttu-id="d46c1-117">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="d46c1-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="d46c1-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d46c1-118">Update Frequency</span></span>  | <span data-ttu-id="d46c1-119">Lorsque la classe est créée ou qu’un nouvel attribut facultatif est ajouté à la classe.</span><span class="sxs-lookup"><span data-stu-id="d46c1-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="d46c1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-120">Attribute-Id</span></span>      | <span data-ttu-id="d46c1-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="d46c1-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="d46c1-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d46c1-122">System-Id-Guid</span></span>    | <span data-ttu-id="d46c1-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d46c1-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="d46c1-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d46c1-124">Syntax</span></span>            | [<span data-ttu-id="d46c1-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="d46c1-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="d46c1-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d46c1-126">Implementations</span></span>

-   [<span data-ttu-id="d46c1-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d46c1-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d46c1-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d46c1-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d46c1-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d46c1-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d46c1-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d46c1-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d46c1-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d46c1-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d46c1-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d46c1-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d46c1-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d46c1-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d46c1-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d46c1-134">Windows 2000 Server</span></span>



| <span data-ttu-id="d46c1-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-135">Entry</span></span> | <span data-ttu-id="d46c1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-139">System-Only</span></span>            | <span data-ttu-id="d46c1-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-140">True</span></span>                                             |
| <span data-ttu-id="d46c1-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-142">False</span></span>                                            |
| <span data-ttu-id="d46c1-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-143">Is Indexed</span></span>             | <span data-ttu-id="d46c1-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-144">False</span></span>                                            |
| <span data-ttu-id="d46c1-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-145">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-146">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-146">False</span></span>                                            |
| <span data-ttu-id="d46c1-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-151">Search-Flags</span></span>           | <span data-ttu-id="d46c1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-152">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-153">System-Flags</span></span>           | <span data-ttu-id="d46c1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-154">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-155">Classes used in</span></span>        | [<span data-ttu-id="d46c1-156">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d46c1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d46c1-157">Windows Server 2003</span></span>



| <span data-ttu-id="d46c1-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-158">Entry</span></span> | <span data-ttu-id="d46c1-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-162">System-Only</span></span>            | <span data-ttu-id="d46c1-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-163">True</span></span>                                             |
| <span data-ttu-id="d46c1-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-165">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-165">False</span></span>                                            |
| <span data-ttu-id="d46c1-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-166">Is Indexed</span></span>             | <span data-ttu-id="d46c1-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-167">False</span></span>                                            |
| <span data-ttu-id="d46c1-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-168">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-169">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-169">False</span></span>                                            |
| <span data-ttu-id="d46c1-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-174">Search-Flags</span></span>           | <span data-ttu-id="d46c1-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-175">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-176">System-Flags</span></span>           | <span data-ttu-id="d46c1-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-177">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-178">Classes used in</span></span>        | [<span data-ttu-id="d46c1-179">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d46c1-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="d46c1-180">ADAM</span></span>



| <span data-ttu-id="d46c1-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-181">Entry</span></span> | <span data-ttu-id="d46c1-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-185">System-Only</span></span>            | <span data-ttu-id="d46c1-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-186">True</span></span>                                             |
| <span data-ttu-id="d46c1-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-187">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-188">False</span></span>                                            |
| <span data-ttu-id="d46c1-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-189">Is Indexed</span></span>             | <span data-ttu-id="d46c1-190">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-190">False</span></span>                                            |
| <span data-ttu-id="d46c1-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-191">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-192">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-192">False</span></span>                                            |
| <span data-ttu-id="d46c1-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-197">Search-Flags</span></span>           | <span data-ttu-id="d46c1-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-198">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-199">System-Flags</span></span>           | <span data-ttu-id="d46c1-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-200">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-201">Classes used in</span></span>        | [<span data-ttu-id="d46c1-202">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d46c1-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d46c1-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d46c1-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-204">Entry</span></span> | <span data-ttu-id="d46c1-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-208">System-Only</span></span>            | <span data-ttu-id="d46c1-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-209">True</span></span>                                             |
| <span data-ttu-id="d46c1-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-211">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-211">False</span></span>                                            |
| <span data-ttu-id="d46c1-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-212">Is Indexed</span></span>             | <span data-ttu-id="d46c1-213">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-213">False</span></span>                                            |
| <span data-ttu-id="d46c1-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-214">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-215">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-215">False</span></span>                                            |
| <span data-ttu-id="d46c1-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-220">Search-Flags</span></span>           | <span data-ttu-id="d46c1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-221">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-222">System-Flags</span></span>           | <span data-ttu-id="d46c1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-223">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-224">Classes used in</span></span>        | [<span data-ttu-id="d46c1-225">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d46c1-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d46c1-226">Windows Server 2008</span></span>



| <span data-ttu-id="d46c1-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-227">Entry</span></span> | <span data-ttu-id="d46c1-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-231">System-Only</span></span>            | <span data-ttu-id="d46c1-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-232">True</span></span>                                             |
| <span data-ttu-id="d46c1-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-233">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-234">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-234">False</span></span>                                            |
| <span data-ttu-id="d46c1-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-235">Is Indexed</span></span>             | <span data-ttu-id="d46c1-236">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-236">False</span></span>                                            |
| <span data-ttu-id="d46c1-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-237">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-238">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-238">False</span></span>                                            |
| <span data-ttu-id="d46c1-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-243">Search-Flags</span></span>           | <span data-ttu-id="d46c1-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-244">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-245">System-Flags</span></span>           | <span data-ttu-id="d46c1-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-246">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-247">Classes used in</span></span>        | [<span data-ttu-id="d46c1-248">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d46c1-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d46c1-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d46c1-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-250">Entry</span></span> | <span data-ttu-id="d46c1-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-254">System-Only</span></span>            | <span data-ttu-id="d46c1-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-255">True</span></span>                                             |
| <span data-ttu-id="d46c1-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-256">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-257">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-257">False</span></span>                                            |
| <span data-ttu-id="d46c1-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-258">Is Indexed</span></span>             | <span data-ttu-id="d46c1-259">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-259">False</span></span>                                            |
| <span data-ttu-id="d46c1-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-260">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-261">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-261">False</span></span>                                            |
| <span data-ttu-id="d46c1-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-266">Search-Flags</span></span>           | <span data-ttu-id="d46c1-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-267">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-268">System-Flags</span></span>           | <span data-ttu-id="d46c1-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-269">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-270">Classes used in</span></span>        | [<span data-ttu-id="d46c1-271">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d46c1-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d46c1-272">Windows Server 2012</span></span>



| <span data-ttu-id="d46c1-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="d46c1-273">Entry</span></span> | <span data-ttu-id="d46c1-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46c1-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d46c1-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d46c1-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46c1-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d46c1-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46c1-277">System-Only</span></span>            | <span data-ttu-id="d46c1-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="d46c1-278">True</span></span>                                             |
| <span data-ttu-id="d46c1-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d46c1-279">Is-Single-Valued</span></span>       | <span data-ttu-id="d46c1-280">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-280">False</span></span>                                            |
| <span data-ttu-id="d46c1-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d46c1-281">Is Indexed</span></span>             | <span data-ttu-id="d46c1-282">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-282">False</span></span>                                            |
| <span data-ttu-id="d46c1-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d46c1-283">In Global Catalog</span></span>      | <span data-ttu-id="d46c1-284">Faux</span><span class="sxs-lookup"><span data-stu-id="d46c1-284">False</span></span>                                            |
| <span data-ttu-id="d46c1-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d46c1-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46c1-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d46c1-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d46c1-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46c1-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46c1-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d46c1-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-289">Search-Flags</span></span>           | <span data-ttu-id="d46c1-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46c1-290">0x00000000</span></span>                                       |
| <span data-ttu-id="d46c1-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46c1-291">System-Flags</span></span>           | <span data-ttu-id="d46c1-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d46c1-292">0x00000010</span></span>                                       |
| <span data-ttu-id="d46c1-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d46c1-293">Classes used in</span></span>        | [<span data-ttu-id="d46c1-294">**Classe-schéma**</span><span class="sxs-lookup"><span data-stu-id="d46c1-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





