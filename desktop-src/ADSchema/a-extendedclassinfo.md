---
title: Attribut Extended-Class-info
description: Propriété à valeurs multiples qui contient des chaînes qui représentent des informations supplémentaires pour chaque classe. Chaque valeur contient les valeurs governsID, lDAPDisplayName et schemaIDGUID de la classe.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Extended-Class-info
- Schéma AD de l’attribut extendedClassInfo
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385351"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="bbbb5-106">Attribut Extended-Class-info</span><span class="sxs-lookup"><span data-stu-id="bbbb5-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="bbbb5-107">Propriété à valeurs multiples qui contient des chaînes qui représentent des informations supplémentaires pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="bbbb5-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="bbbb5-108">Chaque valeur contient les valeurs governsID, lDAPDisplayName et schemaIDGUID de la classe.</span><span class="sxs-lookup"><span data-stu-id="bbbb5-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="bbbb5-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-109">Entry</span></span> | <span data-ttu-id="bbbb5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-111">CN</span><span class="sxs-lookup"><span data-stu-id="bbbb5-111">CN</span></span>                | <span data-ttu-id="bbbb5-112">Extended-Class-info</span><span class="sxs-lookup"><span data-stu-id="bbbb5-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="bbbb5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bbbb5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bbbb5-114">extendedClassInfo</span><span class="sxs-lookup"><span data-stu-id="bbbb5-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="bbbb5-115">Taille</span><span class="sxs-lookup"><span data-stu-id="bbbb5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="bbbb5-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bbbb5-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="bbbb5-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bbbb5-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bbbb5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-118">Attribute-Id</span></span>      | <span data-ttu-id="bbbb5-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="bbbb5-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="bbbb5-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bbbb5-120">System-Id-Guid</span></span>    | <span data-ttu-id="bbbb5-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="bbbb5-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="bbbb5-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbbb5-122">Syntax</span></span>            | [<span data-ttu-id="bbbb5-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bbbb5-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bbbb5-124">Implementations</span></span>

-   [<span data-ttu-id="bbbb5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bbbb5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bbbb5-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bbbb5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bbbb5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bbbb5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bbbb5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bbbb5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bbbb5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="bbbb5-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-133">Entry</span></span> | <span data-ttu-id="bbbb5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-137">System-Only</span></span>            | <span data-ttu-id="bbbb5-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-138">True</span></span>                                        |
| <span data-ttu-id="bbbb5-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-140">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-140">False</span></span>                                       |
| <span data-ttu-id="bbbb5-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-141">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-142">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-142">False</span></span>                                       |
| <span data-ttu-id="bbbb5-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-143">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-144">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-144">False</span></span>                                       |
| <span data-ttu-id="bbbb5-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-149">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-150">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-151">System-Flags</span></span>           | <span data-ttu-id="bbbb5-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-152">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-153">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-154">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bbbb5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbbb5-155">Windows Server 2003</span></span>



| <span data-ttu-id="bbbb5-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-156">Entry</span></span> | <span data-ttu-id="bbbb5-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-160">System-Only</span></span>            | <span data-ttu-id="bbbb5-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-161">True</span></span>                                        |
| <span data-ttu-id="bbbb5-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-163">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-163">False</span></span>                                       |
| <span data-ttu-id="bbbb5-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-164">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-165">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-165">False</span></span>                                       |
| <span data-ttu-id="bbbb5-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-166">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-167">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-167">False</span></span>                                       |
| <span data-ttu-id="bbbb5-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-172">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-173">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-174">System-Flags</span></span>           | <span data-ttu-id="bbbb5-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-175">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-176">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-177">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bbbb5-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="bbbb5-178">ADAM</span></span>



| <span data-ttu-id="bbbb5-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-179">Entry</span></span> | <span data-ttu-id="bbbb5-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-183">System-Only</span></span>            | <span data-ttu-id="bbbb5-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-184">True</span></span>                                        |
| <span data-ttu-id="bbbb5-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-186">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-186">False</span></span>                                       |
| <span data-ttu-id="bbbb5-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-187">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-188">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-188">False</span></span>                                       |
| <span data-ttu-id="bbbb5-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-189">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-190">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-190">False</span></span>                                       |
| <span data-ttu-id="bbbb5-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-195">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-196">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-197">System-Flags</span></span>           | <span data-ttu-id="bbbb5-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-198">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-199">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-200">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bbbb5-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bbbb5-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bbbb5-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-202">Entry</span></span> | <span data-ttu-id="bbbb5-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-206">System-Only</span></span>            | <span data-ttu-id="bbbb5-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-207">True</span></span>                                        |
| <span data-ttu-id="bbbb5-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-209">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-209">False</span></span>                                       |
| <span data-ttu-id="bbbb5-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-210">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-211">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-211">False</span></span>                                       |
| <span data-ttu-id="bbbb5-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-212">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-213">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-213">False</span></span>                                       |
| <span data-ttu-id="bbbb5-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-218">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-219">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-220">System-Flags</span></span>           | <span data-ttu-id="bbbb5-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-221">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-222">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-223">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bbbb5-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbbb5-224">Windows Server 2008</span></span>



| <span data-ttu-id="bbbb5-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-225">Entry</span></span> | <span data-ttu-id="bbbb5-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-229">System-Only</span></span>            | <span data-ttu-id="bbbb5-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-230">True</span></span>                                        |
| <span data-ttu-id="bbbb5-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-232">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-232">False</span></span>                                       |
| <span data-ttu-id="bbbb5-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-233">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-234">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-234">False</span></span>                                       |
| <span data-ttu-id="bbbb5-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-235">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-236">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-236">False</span></span>                                       |
| <span data-ttu-id="bbbb5-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-241">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-242">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-243">System-Flags</span></span>           | <span data-ttu-id="bbbb5-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-244">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-245">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-246">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bbbb5-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bbbb5-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bbbb5-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-248">Entry</span></span> | <span data-ttu-id="bbbb5-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-252">System-Only</span></span>            | <span data-ttu-id="bbbb5-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-253">True</span></span>                                        |
| <span data-ttu-id="bbbb5-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-255">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-255">False</span></span>                                       |
| <span data-ttu-id="bbbb5-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-256">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-257">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-257">False</span></span>                                       |
| <span data-ttu-id="bbbb5-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-258">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-259">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-259">False</span></span>                                       |
| <span data-ttu-id="bbbb5-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-264">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-265">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-266">System-Flags</span></span>           | <span data-ttu-id="bbbb5-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-267">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-268">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-269">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bbbb5-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbbb5-270">Windows Server 2012</span></span>



| <span data-ttu-id="bbbb5-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbbb5-271">Entry</span></span> | <span data-ttu-id="bbbb5-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbb5-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="bbbb5-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbbb5-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbbb5-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="bbbb5-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbbb5-275">System-Only</span></span>            | <span data-ttu-id="bbbb5-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="bbbb5-276">True</span></span>                                        |
| <span data-ttu-id="bbbb5-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbbb5-277">Is-Single-Valued</span></span>       | <span data-ttu-id="bbbb5-278">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-278">False</span></span>                                       |
| <span data-ttu-id="bbbb5-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbbb5-279">Is Indexed</span></span>             | <span data-ttu-id="bbbb5-280">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-280">False</span></span>                                       |
| <span data-ttu-id="bbbb5-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbbb5-281">In Global Catalog</span></span>      | <span data-ttu-id="bbbb5-282">Faux</span><span class="sxs-lookup"><span data-stu-id="bbbb5-282">False</span></span>                                       |
| <span data-ttu-id="bbbb5-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbbb5-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbbb5-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbbb5-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="bbbb5-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbbb5-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbbb5-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="bbbb5-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-287">Search-Flags</span></span>           | <span data-ttu-id="bbbb5-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbbb5-288">0x00000000</span></span>                                  |
| <span data-ttu-id="bbbb5-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbbb5-289">System-Flags</span></span>           | <span data-ttu-id="bbbb5-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bbbb5-290">0x08000014</span></span>                                  |
| <span data-ttu-id="bbbb5-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbbb5-291">Classes used in</span></span>        | [<span data-ttu-id="bbbb5-292">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="bbbb5-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





