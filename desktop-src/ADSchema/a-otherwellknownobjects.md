---
title: Autre attribut-bien connu-Objects
description: Contient une liste de conteneurs par GUID et nom unique. Cela permet de récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine. Chaque fois que l’objet est déplacé, le système met automatiquement à jour le nom unique.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory d’un autre attribut des objets bien connus
- Schéma AD de l’attribut otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480269"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="d1134-107">Autre attribut-bien connu-Objects</span><span class="sxs-lookup"><span data-stu-id="d1134-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="d1134-108">Contient une liste de conteneurs par GUID et nom unique.</span><span class="sxs-lookup"><span data-stu-id="d1134-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="d1134-109">Cela permet de récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="d1134-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="d1134-110">Chaque fois que l’objet est déplacé, le système met automatiquement à jour le nom unique.</span><span class="sxs-lookup"><span data-stu-id="d1134-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="d1134-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-111">Entry</span></span> | <span data-ttu-id="d1134-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1134-113">CN</span><span class="sxs-lookup"><span data-stu-id="d1134-113">CN</span></span>                | <span data-ttu-id="d1134-114">Autres objets bien connus</span><span class="sxs-lookup"><span data-stu-id="d1134-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="d1134-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d1134-115">Ldap-Display-Name</span></span> | <span data-ttu-id="d1134-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="d1134-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="d1134-117">Taille</span><span class="sxs-lookup"><span data-stu-id="d1134-117">Size</span></span>              | <span data-ttu-id="d1134-118">Exemple de récupération du conteneur utilisateurs dans le domaine Microsoft : LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="d1134-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="d1134-119">Remarque : les chevrons sont remplacés par des parenthèses pour éviter les conflits XML.</span><span class="sxs-lookup"><span data-stu-id="d1134-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="d1134-120">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d1134-120">Update Privilege</span></span>  | <span data-ttu-id="d1134-121">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="d1134-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="d1134-122">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d1134-122">Update Frequency</span></span>  | <span data-ttu-id="d1134-123">Chaque fois que l’objet est déplacé.</span><span class="sxs-lookup"><span data-stu-id="d1134-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d1134-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-124">Attribute-Id</span></span>      | <span data-ttu-id="d1134-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="d1134-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d1134-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1134-126">System-Id-Guid</span></span>    | <span data-ttu-id="d1134-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="d1134-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="d1134-128">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1134-128">Syntax</span></span>            | [<span data-ttu-id="d1134-129">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="d1134-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="d1134-130">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d1134-130">Implementations</span></span>

-   [<span data-ttu-id="d1134-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d1134-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d1134-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1134-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1134-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d1134-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d1134-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1134-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1134-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1134-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1134-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1134-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1134-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1134-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d1134-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1134-138">Windows 2000 Server</span></span>



| <span data-ttu-id="d1134-139">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-139">Entry</span></span> | <span data-ttu-id="d1134-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-141">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-143">System-Only</span></span>            | <span data-ttu-id="d1134-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-144">False</span></span>                           |
| <span data-ttu-id="d1134-145">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-145">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-146">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-146">False</span></span>                           |
| <span data-ttu-id="d1134-147">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-147">Is Indexed</span></span>             | <span data-ttu-id="d1134-148">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-148">False</span></span>                           |
| <span data-ttu-id="d1134-149">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-149">In Global Catalog</span></span>      | <span data-ttu-id="d1134-150">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-150">False</span></span>                           |
| <span data-ttu-id="d1134-151">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-152">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d1134-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d1134-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-155">Search-Flags</span></span>           | <span data-ttu-id="d1134-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-156">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-157">System-Flags</span></span>           | <span data-ttu-id="d1134-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-158">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-159">Classes used in</span></span>        | [<span data-ttu-id="d1134-160">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d1134-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1134-161">Windows Server 2003</span></span>



| <span data-ttu-id="d1134-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-162">Entry</span></span> | <span data-ttu-id="d1134-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-166">System-Only</span></span>            | <span data-ttu-id="d1134-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-167">False</span></span>                           |
| <span data-ttu-id="d1134-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-168">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-169">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-169">False</span></span>                           |
| <span data-ttu-id="d1134-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-170">Is Indexed</span></span>             | <span data-ttu-id="d1134-171">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-171">False</span></span>                           |
| <span data-ttu-id="d1134-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-172">In Global Catalog</span></span>      | <span data-ttu-id="d1134-173">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-173">False</span></span>                           |
| <span data-ttu-id="d1134-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-176">Range-Lower</span></span>            | <span data-ttu-id="d1134-177">16</span><span class="sxs-lookup"><span data-stu-id="d1134-177">16</span></span>                              |
| <span data-ttu-id="d1134-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-178">Range-Upper</span></span>            | <span data-ttu-id="d1134-179">16</span><span class="sxs-lookup"><span data-stu-id="d1134-179">16</span></span>                              |
| <span data-ttu-id="d1134-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-180">Search-Flags</span></span>           | <span data-ttu-id="d1134-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-181">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-182">System-Flags</span></span>           | <span data-ttu-id="d1134-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-183">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-184">Classes used in</span></span>        | [<span data-ttu-id="d1134-185">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d1134-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="d1134-186">ADAM</span></span>



| <span data-ttu-id="d1134-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-187">Entry</span></span> | <span data-ttu-id="d1134-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-191">System-Only</span></span>            | <span data-ttu-id="d1134-192">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-192">False</span></span>                           |
| <span data-ttu-id="d1134-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-193">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-194">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-194">False</span></span>                           |
| <span data-ttu-id="d1134-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-195">Is Indexed</span></span>             | <span data-ttu-id="d1134-196">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-196">False</span></span>                           |
| <span data-ttu-id="d1134-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-197">In Global Catalog</span></span>      | <span data-ttu-id="d1134-198">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-198">False</span></span>                           |
| <span data-ttu-id="d1134-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-201">Range-Lower</span></span>            | <span data-ttu-id="d1134-202">16</span><span class="sxs-lookup"><span data-stu-id="d1134-202">16</span></span>                              |
| <span data-ttu-id="d1134-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-203">Range-Upper</span></span>            | <span data-ttu-id="d1134-204">16</span><span class="sxs-lookup"><span data-stu-id="d1134-204">16</span></span>                              |
| <span data-ttu-id="d1134-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-205">Search-Flags</span></span>           | <span data-ttu-id="d1134-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-206">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-207">System-Flags</span></span>           | <span data-ttu-id="d1134-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-208">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-209">Classes used in</span></span>        | [<span data-ttu-id="d1134-210">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1134-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1134-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1134-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-212">Entry</span></span> | <span data-ttu-id="d1134-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-216">System-Only</span></span>            | <span data-ttu-id="d1134-217">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-217">False</span></span>                           |
| <span data-ttu-id="d1134-218">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-218">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-219">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-219">False</span></span>                           |
| <span data-ttu-id="d1134-220">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-220">Is Indexed</span></span>             | <span data-ttu-id="d1134-221">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-221">False</span></span>                           |
| <span data-ttu-id="d1134-222">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-222">In Global Catalog</span></span>      | <span data-ttu-id="d1134-223">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-223">False</span></span>                           |
| <span data-ttu-id="d1134-224">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-225">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-226">Range-Lower</span></span>            | <span data-ttu-id="d1134-227">16</span><span class="sxs-lookup"><span data-stu-id="d1134-227">16</span></span>                              |
| <span data-ttu-id="d1134-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-228">Range-Upper</span></span>            | <span data-ttu-id="d1134-229">16</span><span class="sxs-lookup"><span data-stu-id="d1134-229">16</span></span>                              |
| <span data-ttu-id="d1134-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-230">Search-Flags</span></span>           | <span data-ttu-id="d1134-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-231">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-232">System-Flags</span></span>           | <span data-ttu-id="d1134-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-233">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-234">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-234">Classes used in</span></span>        | [<span data-ttu-id="d1134-235">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1134-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1134-236">Windows Server 2008</span></span>



| <span data-ttu-id="d1134-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-237">Entry</span></span> | <span data-ttu-id="d1134-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-241">System-Only</span></span>            | <span data-ttu-id="d1134-242">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-242">False</span></span>                           |
| <span data-ttu-id="d1134-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-243">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-244">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-244">False</span></span>                           |
| <span data-ttu-id="d1134-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-245">Is Indexed</span></span>             | <span data-ttu-id="d1134-246">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-246">False</span></span>                           |
| <span data-ttu-id="d1134-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-247">In Global Catalog</span></span>      | <span data-ttu-id="d1134-248">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-248">False</span></span>                           |
| <span data-ttu-id="d1134-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-251">Range-Lower</span></span>            | <span data-ttu-id="d1134-252">16</span><span class="sxs-lookup"><span data-stu-id="d1134-252">16</span></span>                              |
| <span data-ttu-id="d1134-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-253">Range-Upper</span></span>            | <span data-ttu-id="d1134-254">16</span><span class="sxs-lookup"><span data-stu-id="d1134-254">16</span></span>                              |
| <span data-ttu-id="d1134-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-255">Search-Flags</span></span>           | <span data-ttu-id="d1134-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-256">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-257">System-Flags</span></span>           | <span data-ttu-id="d1134-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-258">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-259">Classes used in</span></span>        | [<span data-ttu-id="d1134-260">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1134-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1134-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1134-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-262">Entry</span></span> | <span data-ttu-id="d1134-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-266">System-Only</span></span>            | <span data-ttu-id="d1134-267">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-267">False</span></span>                           |
| <span data-ttu-id="d1134-268">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-268">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-269">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-269">False</span></span>                           |
| <span data-ttu-id="d1134-270">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-270">Is Indexed</span></span>             | <span data-ttu-id="d1134-271">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-271">False</span></span>                           |
| <span data-ttu-id="d1134-272">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-272">In Global Catalog</span></span>      | <span data-ttu-id="d1134-273">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-273">False</span></span>                           |
| <span data-ttu-id="d1134-274">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-275">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-276">Range-Lower</span></span>            | <span data-ttu-id="d1134-277">16</span><span class="sxs-lookup"><span data-stu-id="d1134-277">16</span></span>                              |
| <span data-ttu-id="d1134-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-278">Range-Upper</span></span>            | <span data-ttu-id="d1134-279">16</span><span class="sxs-lookup"><span data-stu-id="d1134-279">16</span></span>                              |
| <span data-ttu-id="d1134-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-280">Search-Flags</span></span>           | <span data-ttu-id="d1134-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-281">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-282">System-Flags</span></span>           | <span data-ttu-id="d1134-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-283">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-284">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-284">Classes used in</span></span>        | [<span data-ttu-id="d1134-285">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1134-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1134-286">Windows Server 2012</span></span>



| <span data-ttu-id="d1134-287">Entrée</span><span class="sxs-lookup"><span data-stu-id="d1134-287">Entry</span></span> | <span data-ttu-id="d1134-288">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1134-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d1134-289">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d1134-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1134-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d1134-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1134-291">System-Only</span></span>            | <span data-ttu-id="d1134-292">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-292">False</span></span>                           |
| <span data-ttu-id="d1134-293">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d1134-293">Is-Single-Valued</span></span>       | <span data-ttu-id="d1134-294">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-294">False</span></span>                           |
| <span data-ttu-id="d1134-295">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d1134-295">Is Indexed</span></span>             | <span data-ttu-id="d1134-296">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-296">False</span></span>                           |
| <span data-ttu-id="d1134-297">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d1134-297">In Global Catalog</span></span>      | <span data-ttu-id="d1134-298">Faux</span><span class="sxs-lookup"><span data-stu-id="d1134-298">False</span></span>                           |
| <span data-ttu-id="d1134-299">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d1134-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1134-300">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d1134-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d1134-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1134-301">Range-Lower</span></span>            | <span data-ttu-id="d1134-302">16</span><span class="sxs-lookup"><span data-stu-id="d1134-302">16</span></span>                              |
| <span data-ttu-id="d1134-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1134-303">Range-Upper</span></span>            | <span data-ttu-id="d1134-304">16</span><span class="sxs-lookup"><span data-stu-id="d1134-304">16</span></span>                              |
| <span data-ttu-id="d1134-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-305">Search-Flags</span></span>           | <span data-ttu-id="d1134-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1134-306">0x00000000</span></span>                      |
| <span data-ttu-id="d1134-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1134-307">System-Flags</span></span>           | <span data-ttu-id="d1134-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1134-308">0x00000010</span></span>                      |
| <span data-ttu-id="d1134-309">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d1134-309">Classes used in</span></span>        | [<span data-ttu-id="d1134-310">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d1134-310">**Top**</span></span>](c-top.md)<br/> |



 

 





