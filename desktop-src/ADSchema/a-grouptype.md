---
title: Attribut Group-Type
description: Contient un jeu d’indicateurs qui définissent le type et la portée d’un objet de groupe.
ms.assetid: cd37ed2f-8503-4227-b0d2-c8135605cb84
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Group-Type
- Schéma AD de l’attribut groupType
topic_type:
- apiref
api_name:
- Group-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e1db8f102e7e56b38d15d74fedb7c5a5366ee47
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515690"
---
# <a name="group-type-attribute"></a><span data-ttu-id="cf86f-105">Attribut Group-Type</span><span class="sxs-lookup"><span data-stu-id="cf86f-105">Group-Type attribute</span></span>

<span data-ttu-id="cf86f-106">Contient un jeu d’indicateurs qui définissent le type et la portée d’un objet de groupe.</span><span class="sxs-lookup"><span data-stu-id="cf86f-106">Contains a set of flags that define the type and scope of a group object.</span></span> <span data-ttu-id="cf86f-107">Pour connaître les valeurs possibles pour cet attribut, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cf86f-107">For the possible values for this attribute, see Remarks.</span></span>



| <span data-ttu-id="cf86f-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-108">Entry</span></span> | <span data-ttu-id="cf86f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cf86f-110">CN</span><span class="sxs-lookup"><span data-stu-id="cf86f-110">CN</span></span>                | <span data-ttu-id="cf86f-111">Group-Type</span><span class="sxs-lookup"><span data-stu-id="cf86f-111">Group-Type</span></span>                           |
| <span data-ttu-id="cf86f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cf86f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="cf86f-113">groupType</span><span class="sxs-lookup"><span data-stu-id="cf86f-113">groupType</span></span>                            |
| <span data-ttu-id="cf86f-114">Taille</span><span class="sxs-lookup"><span data-stu-id="cf86f-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="cf86f-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cf86f-115">Update Privilege</span></span>  | <span data-ttu-id="cf86f-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="cf86f-116">Domain administrator</span></span>                 |
| <span data-ttu-id="cf86f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cf86f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cf86f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-118">Attribute-Id</span></span>      | <span data-ttu-id="cf86f-119">1.2.840.113556.1.4.750</span><span class="sxs-lookup"><span data-stu-id="cf86f-119">1.2.840.113556.1.4.750</span></span>               |
| <span data-ttu-id="cf86f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cf86f-120">System-Id-Guid</span></span>    | <span data-ttu-id="cf86f-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="cf86f-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="cf86f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf86f-122">Syntax</span></span>            | [<span data-ttu-id="cf86f-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="cf86f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cf86f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cf86f-124">Implementations</span></span>

-   [<span data-ttu-id="cf86f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf86f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf86f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf86f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf86f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cf86f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cf86f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf86f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf86f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf86f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf86f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf86f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf86f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf86f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf86f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf86f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="cf86f-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-133">Entry</span></span> | <span data-ttu-id="cf86f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-134">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-135">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-136">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-137">System-Only</span></span>            | <span data-ttu-id="cf86f-138">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-138">False</span></span>                               |
| <span data-ttu-id="cf86f-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-140">True</span></span>                                |
| <span data-ttu-id="cf86f-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-141">Is Indexed</span></span>             | <span data-ttu-id="cf86f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-142">True</span></span>                                |
| <span data-ttu-id="cf86f-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-143">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-144">True</span></span>                                |
| <span data-ttu-id="cf86f-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-146">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-147">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-148">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-149">Search-Flags</span></span>           | <span data-ttu-id="cf86f-150">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-150">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-151">System-Flags</span></span>           | <span data-ttu-id="cf86f-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-152">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-153">Classes used in</span></span>        | [<span data-ttu-id="cf86f-154">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-154">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf86f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf86f-155">Windows Server 2003</span></span>



| <span data-ttu-id="cf86f-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-156">Entry</span></span> | <span data-ttu-id="cf86f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-157">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-158">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-160">System-Only</span></span>            | <span data-ttu-id="cf86f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-161">False</span></span>                               |
| <span data-ttu-id="cf86f-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-163">True</span></span>                                |
| <span data-ttu-id="cf86f-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-164">Is Indexed</span></span>             | <span data-ttu-id="cf86f-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-165">True</span></span>                                |
| <span data-ttu-id="cf86f-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-166">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-167">True</span></span>                                |
| <span data-ttu-id="cf86f-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-172">Search-Flags</span></span>           | <span data-ttu-id="cf86f-173">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-173">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-174">System-Flags</span></span>           | <span data-ttu-id="cf86f-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-175">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-176">Classes used in</span></span>        | [<span data-ttu-id="cf86f-177">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cf86f-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="cf86f-178">ADAM</span></span>



| <span data-ttu-id="cf86f-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-179">Entry</span></span> | <span data-ttu-id="cf86f-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-181">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-182">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-183">System-Only</span></span>            | <span data-ttu-id="cf86f-184">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-184">False</span></span>                               |
| <span data-ttu-id="cf86f-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-186">True</span></span>                                |
| <span data-ttu-id="cf86f-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-187">Is Indexed</span></span>             | <span data-ttu-id="cf86f-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-188">True</span></span>                                |
| <span data-ttu-id="cf86f-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-189">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-190">True</span></span>                                |
| <span data-ttu-id="cf86f-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-192">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-193">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-194">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-195">Search-Flags</span></span>           | <span data-ttu-id="cf86f-196">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-196">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-197">System-Flags</span></span>           | <span data-ttu-id="cf86f-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-198">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-199">Classes used in</span></span>        | [<span data-ttu-id="cf86f-200">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-200">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf86f-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf86f-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf86f-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-202">Entry</span></span> | <span data-ttu-id="cf86f-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-203">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-204">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-205">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-206">System-Only</span></span>            | <span data-ttu-id="cf86f-207">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-207">False</span></span>                               |
| <span data-ttu-id="cf86f-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-209">True</span></span>                                |
| <span data-ttu-id="cf86f-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-210">Is Indexed</span></span>             | <span data-ttu-id="cf86f-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-211">True</span></span>                                |
| <span data-ttu-id="cf86f-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-212">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-213">True</span></span>                                |
| <span data-ttu-id="cf86f-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-215">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-216">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-217">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-218">Search-Flags</span></span>           | <span data-ttu-id="cf86f-219">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-219">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-220">System-Flags</span></span>           | <span data-ttu-id="cf86f-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-221">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-222">Classes used in</span></span>        | [<span data-ttu-id="cf86f-223">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-223">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf86f-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf86f-224">Windows Server 2008</span></span>



| <span data-ttu-id="cf86f-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-225">Entry</span></span> | <span data-ttu-id="cf86f-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-226">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-227">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-228">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-229">System-Only</span></span>            | <span data-ttu-id="cf86f-230">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-230">False</span></span>                               |
| <span data-ttu-id="cf86f-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-232">True</span></span>                                |
| <span data-ttu-id="cf86f-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-233">Is Indexed</span></span>             | <span data-ttu-id="cf86f-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-234">True</span></span>                                |
| <span data-ttu-id="cf86f-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-235">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-236">True</span></span>                                |
| <span data-ttu-id="cf86f-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-238">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-239">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-240">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-241">Search-Flags</span></span>           | <span data-ttu-id="cf86f-242">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-242">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-243">System-Flags</span></span>           | <span data-ttu-id="cf86f-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-244">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-245">Classes used in</span></span>        | [<span data-ttu-id="cf86f-246">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-246">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf86f-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf86f-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf86f-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-248">Entry</span></span> | <span data-ttu-id="cf86f-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-249">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-250">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-251">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-252">System-Only</span></span>            | <span data-ttu-id="cf86f-253">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-253">False</span></span>                               |
| <span data-ttu-id="cf86f-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-255">True</span></span>                                |
| <span data-ttu-id="cf86f-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-256">Is Indexed</span></span>             | <span data-ttu-id="cf86f-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-257">True</span></span>                                |
| <span data-ttu-id="cf86f-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-258">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-259">True</span></span>                                |
| <span data-ttu-id="cf86f-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-261">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-262">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-263">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-264">Search-Flags</span></span>           | <span data-ttu-id="cf86f-265">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-265">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-266">System-Flags</span></span>           | <span data-ttu-id="cf86f-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-267">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-268">Classes used in</span></span>        | [<span data-ttu-id="cf86f-269">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-269">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf86f-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf86f-270">Windows Server 2012</span></span>



| <span data-ttu-id="cf86f-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf86f-271">Entry</span></span> | <span data-ttu-id="cf86f-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-272">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="cf86f-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf86f-273">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf86f-274">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="cf86f-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf86f-275">System-Only</span></span>            | <span data-ttu-id="cf86f-276">Faux</span><span class="sxs-lookup"><span data-stu-id="cf86f-276">False</span></span>                               |
| <span data-ttu-id="cf86f-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf86f-277">Is-Single-Valued</span></span>       | <span data-ttu-id="cf86f-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-278">True</span></span>                                |
| <span data-ttu-id="cf86f-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf86f-279">Is Indexed</span></span>             | <span data-ttu-id="cf86f-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-280">True</span></span>                                |
| <span data-ttu-id="cf86f-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf86f-281">In Global Catalog</span></span>      | <span data-ttu-id="cf86f-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf86f-282">True</span></span>                                |
| <span data-ttu-id="cf86f-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf86f-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf86f-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf86f-284">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="cf86f-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf86f-285">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf86f-286">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="cf86f-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-287">Search-Flags</span></span>           | <span data-ttu-id="cf86f-288">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cf86f-288">0x00000009</span></span>                          |
| <span data-ttu-id="cf86f-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf86f-289">System-Flags</span></span>           | <span data-ttu-id="cf86f-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="cf86f-290">0x00000012</span></span>                          |
| <span data-ttu-id="cf86f-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf86f-291">Classes used in</span></span>        | [<span data-ttu-id="cf86f-292">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="cf86f-292">**Group**</span></span>](c-group.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cf86f-293">Notes</span><span class="sxs-lookup"><span data-stu-id="cf86f-293">Remarks</span></span>

<span data-ttu-id="cf86f-294">Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf86f-294">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="cf86f-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf86f-295">Value</span></span>                   | <span data-ttu-id="cf86f-296">Description</span><span class="sxs-lookup"><span data-stu-id="cf86f-296">Description</span></span>                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf86f-297">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="cf86f-297">1 (0x00000001)</span></span>          | <span data-ttu-id="cf86f-298">Spécifie un groupe créé par le système.</span><span class="sxs-lookup"><span data-stu-id="cf86f-298">Specifies a group that is created by the system.</span></span>                                             |
| <span data-ttu-id="cf86f-299">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="cf86f-299">2 (0x00000002)</span></span>          | <span data-ttu-id="cf86f-300">Spécifie un groupe avec une étendue globale.</span><span class="sxs-lookup"><span data-stu-id="cf86f-300">Specifies a group with global scope.</span></span>                                                         |
| <span data-ttu-id="cf86f-301">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="cf86f-301">4 (0x00000004)</span></span>          | <span data-ttu-id="cf86f-302">Spécifie un groupe avec une étendue de domaine local.</span><span class="sxs-lookup"><span data-stu-id="cf86f-302">Specifies a group with domain local scope.</span></span>                                                   |
| <span data-ttu-id="cf86f-303">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="cf86f-303">8 (0x00000008)</span></span>          | <span data-ttu-id="cf86f-304">Spécifie un groupe avec une étendue universelle.</span><span class="sxs-lookup"><span data-stu-id="cf86f-304">Specifies a group with universal scope.</span></span>                                                      |
| <span data-ttu-id="cf86f-305">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="cf86f-305">16 (0x00000010)</span></span>         | <span data-ttu-id="cf86f-306">Spécifie un \_ groupe d’applications de base pour le gestionnaire d’autorisations Windows Server.</span><span class="sxs-lookup"><span data-stu-id="cf86f-306">Specifies an APP\_BASIC group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="cf86f-307">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="cf86f-307">32 (0x00000020)</span></span>         | <span data-ttu-id="cf86f-308">Spécifie un \_ groupe de requêtes d’application pour le gestionnaire d’autorisations Windows Server.</span><span class="sxs-lookup"><span data-stu-id="cf86f-308">Specifies an APP\_QUERY group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="cf86f-309">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="cf86f-309">2147483648 (0x80000000)</span></span> | <span data-ttu-id="cf86f-310">Spécifie un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cf86f-310">Specifies a security group.</span></span> <span data-ttu-id="cf86f-311">Si cet indicateur n’est pas défini, le groupe est un groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="cf86f-311">If this flag is not set, then the group is a distribution group.</span></span> |



 

<span data-ttu-id="cf86f-312">Pour plus d’informations sur le type de groupe et l’étendue, consultez les rubriques [types](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) de groupes et [étendues de groupes](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="cf86f-312">For more information about group type and scope, see the [Group types](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) and [Group scope](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) topics on Microsoft TechNet.</span></span>

 

