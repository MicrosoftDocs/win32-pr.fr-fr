---
title: Attribut Object-Classes
description: Propriété à valeurs multiples qui contient des chaînes représentant chaque classe dans le schéma. Chaque valeur contient les valeurs governsID, lDAPDisplayName, mustContain, mayContain, etc.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Classes
- Schéma AD de l’attribut objectClasses
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845378"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="2d6d9-106">Attribut Object-Classes</span><span class="sxs-lookup"><span data-stu-id="2d6d9-106">Object-Classes attribute</span></span>

<span data-ttu-id="2d6d9-107">Propriété à valeurs multiples qui contient des chaînes représentant chaque classe dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="2d6d9-108">Chaque valeur contient les valeurs governsID, lDAPDisplayName, mustContain, mayContain, etc.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="2d6d9-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-109">Entry</span></span> | <span data-ttu-id="2d6d9-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="2d6d9-111">CN</span><span class="sxs-lookup"><span data-stu-id="2d6d9-111">CN</span></span>                | <span data-ttu-id="2d6d9-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="2d6d9-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="2d6d9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2d6d9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2d6d9-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="2d6d9-114">objectClasses</span></span>                                    |
| <span data-ttu-id="2d6d9-115">Taille</span><span class="sxs-lookup"><span data-stu-id="2d6d9-115">Size</span></span>              | <span data-ttu-id="2d6d9-116">Environ 20 octets en moyenne par nom de classe.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="2d6d9-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2d6d9-117">Update Privilege</span></span>  | <span data-ttu-id="2d6d9-118">Le concepteur de l’objet définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="2d6d9-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2d6d9-119">Update Frequency</span></span>  | <span data-ttu-id="2d6d9-120">Chaque fois que la conception de la classe change.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="2d6d9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-121">Attribute-Id</span></span>      | <span data-ttu-id="2d6d9-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="2d6d9-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="2d6d9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2d6d9-123">System-Id-Guid</span></span>    | <span data-ttu-id="2d6d9-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2d6d9-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="2d6d9-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d6d9-125">Syntax</span></span>            | [<span data-ttu-id="2d6d9-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="2d6d9-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2d6d9-127">Implementations</span></span>

-   [<span data-ttu-id="2d6d9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d6d9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d6d9-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2d6d9-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d6d9-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d6d9-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d6d9-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d6d9-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d6d9-135">Windows 2000 Server</span></span>



| <span data-ttu-id="2d6d9-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-136">Entry</span></span> | <span data-ttu-id="2d6d9-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-140">System-Only</span></span>            | <span data-ttu-id="2d6d9-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-141">True</span></span>                                        |
| <span data-ttu-id="2d6d9-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-143">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-143">False</span></span>                                       |
| <span data-ttu-id="2d6d9-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-144">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-145">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-145">False</span></span>                                       |
| <span data-ttu-id="2d6d9-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-146">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-147">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-147">False</span></span>                                       |
| <span data-ttu-id="2d6d9-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-152">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-153">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-154">System-Flags</span></span>           | <span data-ttu-id="2d6d9-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-155">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-156">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-157">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d6d9-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d6d9-158">Windows Server 2003</span></span>



| <span data-ttu-id="2d6d9-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-159">Entry</span></span> | <span data-ttu-id="2d6d9-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-163">System-Only</span></span>            | <span data-ttu-id="2d6d9-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-164">True</span></span>                                        |
| <span data-ttu-id="2d6d9-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-166">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-166">False</span></span>                                       |
| <span data-ttu-id="2d6d9-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-167">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-168">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-168">False</span></span>                                       |
| <span data-ttu-id="2d6d9-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-169">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-170">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-170">False</span></span>                                       |
| <span data-ttu-id="2d6d9-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-175">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-176">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-177">System-Flags</span></span>           | <span data-ttu-id="2d6d9-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-178">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-179">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-180">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2d6d9-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="2d6d9-181">ADAM</span></span>



| <span data-ttu-id="2d6d9-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-182">Entry</span></span> | <span data-ttu-id="2d6d9-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-186">System-Only</span></span>            | <span data-ttu-id="2d6d9-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-187">True</span></span>                                        |
| <span data-ttu-id="2d6d9-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-189">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-189">False</span></span>                                       |
| <span data-ttu-id="2d6d9-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-190">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-191">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-191">False</span></span>                                       |
| <span data-ttu-id="2d6d9-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-192">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-193">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-193">False</span></span>                                       |
| <span data-ttu-id="2d6d9-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-198">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-199">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-200">System-Flags</span></span>           | <span data-ttu-id="2d6d9-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-201">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-202">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-203">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d6d9-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d6d9-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d6d9-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-205">Entry</span></span> | <span data-ttu-id="2d6d9-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-209">System-Only</span></span>            | <span data-ttu-id="2d6d9-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-210">True</span></span>                                        |
| <span data-ttu-id="2d6d9-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-212">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-212">False</span></span>                                       |
| <span data-ttu-id="2d6d9-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-213">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-214">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-214">False</span></span>                                       |
| <span data-ttu-id="2d6d9-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-215">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-216">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-216">False</span></span>                                       |
| <span data-ttu-id="2d6d9-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-221">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-222">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-223">System-Flags</span></span>           | <span data-ttu-id="2d6d9-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-224">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-225">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-226">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d6d9-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d6d9-227">Windows Server 2008</span></span>



| <span data-ttu-id="2d6d9-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-228">Entry</span></span> | <span data-ttu-id="2d6d9-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-232">System-Only</span></span>            | <span data-ttu-id="2d6d9-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-233">True</span></span>                                        |
| <span data-ttu-id="2d6d9-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-235">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-235">False</span></span>                                       |
| <span data-ttu-id="2d6d9-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-236">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-237">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-237">False</span></span>                                       |
| <span data-ttu-id="2d6d9-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-238">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-239">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-239">False</span></span>                                       |
| <span data-ttu-id="2d6d9-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-244">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-245">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-246">System-Flags</span></span>           | <span data-ttu-id="2d6d9-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-247">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-248">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-249">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d6d9-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d6d9-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d6d9-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-251">Entry</span></span> | <span data-ttu-id="2d6d9-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-255">System-Only</span></span>            | <span data-ttu-id="2d6d9-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-256">True</span></span>                                        |
| <span data-ttu-id="2d6d9-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-257">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-258">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-258">False</span></span>                                       |
| <span data-ttu-id="2d6d9-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-259">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-260">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-260">False</span></span>                                       |
| <span data-ttu-id="2d6d9-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-261">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-262">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-262">False</span></span>                                       |
| <span data-ttu-id="2d6d9-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-267">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-268">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-269">System-Flags</span></span>           | <span data-ttu-id="2d6d9-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-270">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-271">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-272">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d6d9-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d6d9-273">Windows Server 2012</span></span>



| <span data-ttu-id="2d6d9-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d6d9-274">Entry</span></span> | <span data-ttu-id="2d6d9-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6d9-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d6d9-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d6d9-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d6d9-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d6d9-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d6d9-278">System-Only</span></span>            | <span data-ttu-id="2d6d9-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d6d9-279">True</span></span>                                        |
| <span data-ttu-id="2d6d9-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d6d9-280">Is-Single-Valued</span></span>       | <span data-ttu-id="2d6d9-281">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-281">False</span></span>                                       |
| <span data-ttu-id="2d6d9-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d6d9-282">Is Indexed</span></span>             | <span data-ttu-id="2d6d9-283">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-283">False</span></span>                                       |
| <span data-ttu-id="2d6d9-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d6d9-284">In Global Catalog</span></span>      | <span data-ttu-id="2d6d9-285">Faux</span><span class="sxs-lookup"><span data-stu-id="2d6d9-285">False</span></span>                                       |
| <span data-ttu-id="2d6d9-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d6d9-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d6d9-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d6d9-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d6d9-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d6d9-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d6d9-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d6d9-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-290">Search-Flags</span></span>           | <span data-ttu-id="2d6d9-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d6d9-291">0x00000000</span></span>                                  |
| <span data-ttu-id="2d6d9-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d6d9-292">System-Flags</span></span>           | <span data-ttu-id="2d6d9-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d6d9-293">0x08000014</span></span>                                  |
| <span data-ttu-id="2d6d9-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d6d9-294">Classes used in</span></span>        | [<span data-ttu-id="2d6d9-295">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





