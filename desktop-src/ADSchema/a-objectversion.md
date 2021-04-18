---
title: Attribut Object-Version
description: Cela peut être utilisé pour stocker un numéro de version pour l’objet.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Version
- Schéma AD de l’attribut objectVersion
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106512006"
---
# <a name="object-version-attribute"></a><span data-ttu-id="d06b2-105">Attribut Object-Version</span><span class="sxs-lookup"><span data-stu-id="d06b2-105">Object-Version attribute</span></span>

<span data-ttu-id="d06b2-106">Cela peut être utilisé pour stocker un numéro de version pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="d06b2-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="d06b2-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-107">Entry</span></span> | <span data-ttu-id="d06b2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="d06b2-109">CN</span><span class="sxs-lookup"><span data-stu-id="d06b2-109">CN</span></span>                | <span data-ttu-id="d06b2-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="d06b2-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="d06b2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d06b2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d06b2-112">objectVersion</span><span class="sxs-lookup"><span data-stu-id="d06b2-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="d06b2-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d06b2-113">Size</span></span>              | <span data-ttu-id="d06b2-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="d06b2-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="d06b2-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d06b2-115">Update Privilege</span></span>  | <span data-ttu-id="d06b2-116">Le concepteur de l’objet définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d06b2-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="d06b2-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d06b2-117">Update Frequency</span></span>  | <span data-ttu-id="d06b2-118">Cette valeur doit être incrémentée chaque fois que l’objet change.</span><span class="sxs-lookup"><span data-stu-id="d06b2-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="d06b2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-119">Attribute-Id</span></span>      | <span data-ttu-id="d06b2-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="d06b2-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="d06b2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d06b2-121">System-Id-Guid</span></span>    | <span data-ttu-id="d06b2-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d06b2-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="d06b2-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d06b2-123">Syntax</span></span>            | [<span data-ttu-id="d06b2-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d06b2-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="d06b2-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d06b2-125">Implementations</span></span>

-   [<span data-ttu-id="d06b2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d06b2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d06b2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d06b2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d06b2-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d06b2-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d06b2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d06b2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d06b2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d06b2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d06b2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d06b2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d06b2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d06b2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d06b2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d06b2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d06b2-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-134">Entry</span></span> | <span data-ttu-id="d06b2-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-137">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-138">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-139">System-Only</span></span>            | <span data-ttu-id="d06b2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-140">False</span></span>                           |
| <span data-ttu-id="d06b2-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-142">True</span></span>                            |
| <span data-ttu-id="d06b2-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-143">Is Indexed</span></span>             | <span data-ttu-id="d06b2-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-144">False</span></span>                           |
| <span data-ttu-id="d06b2-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-145">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-146">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-146">False</span></span>                           |
| <span data-ttu-id="d06b2-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-151">Search-Flags</span></span>           | <span data-ttu-id="d06b2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-152">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-153">System-Flags</span></span>           | <span data-ttu-id="d06b2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-154">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-155">Classes used in</span></span>        | [<span data-ttu-id="d06b2-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d06b2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d06b2-157">Windows Server 2003</span></span>



| <span data-ttu-id="d06b2-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-158">Entry</span></span> | <span data-ttu-id="d06b2-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-161">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-162">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-163">System-Only</span></span>            | <span data-ttu-id="d06b2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-164">False</span></span>                           |
| <span data-ttu-id="d06b2-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-166">True</span></span>                            |
| <span data-ttu-id="d06b2-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-167">Is Indexed</span></span>             | <span data-ttu-id="d06b2-168">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-168">False</span></span>                           |
| <span data-ttu-id="d06b2-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-169">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-170">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-170">False</span></span>                           |
| <span data-ttu-id="d06b2-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-175">Search-Flags</span></span>           | <span data-ttu-id="d06b2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-176">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-177">System-Flags</span></span>           | <span data-ttu-id="d06b2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-178">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-179">Classes used in</span></span>        | [<span data-ttu-id="d06b2-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d06b2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="d06b2-181">ADAM</span></span>



| <span data-ttu-id="d06b2-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-182">Entry</span></span> | <span data-ttu-id="d06b2-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-185">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-186">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-187">System-Only</span></span>            | <span data-ttu-id="d06b2-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-188">False</span></span>                           |
| <span data-ttu-id="d06b2-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-190">True</span></span>                            |
| <span data-ttu-id="d06b2-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-191">Is Indexed</span></span>             | <span data-ttu-id="d06b2-192">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-192">False</span></span>                           |
| <span data-ttu-id="d06b2-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-193">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-194">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-194">False</span></span>                           |
| <span data-ttu-id="d06b2-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-199">Search-Flags</span></span>           | <span data-ttu-id="d06b2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-200">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-201">System-Flags</span></span>           | <span data-ttu-id="d06b2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-202">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-203">Classes used in</span></span>        | [<span data-ttu-id="d06b2-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d06b2-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d06b2-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d06b2-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-206">Entry</span></span> | <span data-ttu-id="d06b2-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-209">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-210">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-211">System-Only</span></span>            | <span data-ttu-id="d06b2-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-212">False</span></span>                           |
| <span data-ttu-id="d06b2-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-214">True</span></span>                            |
| <span data-ttu-id="d06b2-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-215">Is Indexed</span></span>             | <span data-ttu-id="d06b2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-216">False</span></span>                           |
| <span data-ttu-id="d06b2-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-217">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-218">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-218">False</span></span>                           |
| <span data-ttu-id="d06b2-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-223">Search-Flags</span></span>           | <span data-ttu-id="d06b2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-224">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-225">System-Flags</span></span>           | <span data-ttu-id="d06b2-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-226">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-227">Classes used in</span></span>        | [<span data-ttu-id="d06b2-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d06b2-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d06b2-229">Windows Server 2008</span></span>



| <span data-ttu-id="d06b2-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-230">Entry</span></span> | <span data-ttu-id="d06b2-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-233">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-234">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-235">System-Only</span></span>            | <span data-ttu-id="d06b2-236">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-236">False</span></span>                           |
| <span data-ttu-id="d06b2-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-238">True</span></span>                            |
| <span data-ttu-id="d06b2-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-239">Is Indexed</span></span>             | <span data-ttu-id="d06b2-240">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-240">False</span></span>                           |
| <span data-ttu-id="d06b2-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-241">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-242">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-242">False</span></span>                           |
| <span data-ttu-id="d06b2-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-247">Search-Flags</span></span>           | <span data-ttu-id="d06b2-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-248">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-249">System-Flags</span></span>           | <span data-ttu-id="d06b2-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-250">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-251">Classes used in</span></span>        | [<span data-ttu-id="d06b2-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d06b2-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d06b2-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d06b2-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-254">Entry</span></span> | <span data-ttu-id="d06b2-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-257">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-258">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-259">System-Only</span></span>            | <span data-ttu-id="d06b2-260">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-260">False</span></span>                           |
| <span data-ttu-id="d06b2-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-261">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-262">True</span></span>                            |
| <span data-ttu-id="d06b2-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-263">Is Indexed</span></span>             | <span data-ttu-id="d06b2-264">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-264">False</span></span>                           |
| <span data-ttu-id="d06b2-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-265">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-266">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-266">False</span></span>                           |
| <span data-ttu-id="d06b2-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-271">Search-Flags</span></span>           | <span data-ttu-id="d06b2-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-272">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-273">System-Flags</span></span>           | <span data-ttu-id="d06b2-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-274">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-275">Classes used in</span></span>        | [<span data-ttu-id="d06b2-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d06b2-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d06b2-277">Windows Server 2012</span></span>



| <span data-ttu-id="d06b2-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="d06b2-278">Entry</span></span> | <span data-ttu-id="d06b2-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06b2-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d06b2-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d06b2-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d06b2-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d06b2-281">MAPI-Id</span></span>                | <span data-ttu-id="d06b2-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="d06b2-282">0x80F7</span></span>                          |
| <span data-ttu-id="d06b2-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="d06b2-283">System-Only</span></span>            | <span data-ttu-id="d06b2-284">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-284">False</span></span>                           |
| <span data-ttu-id="d06b2-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d06b2-285">Is-Single-Valued</span></span>       | <span data-ttu-id="d06b2-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="d06b2-286">True</span></span>                            |
| <span data-ttu-id="d06b2-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d06b2-287">Is Indexed</span></span>             | <span data-ttu-id="d06b2-288">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-288">False</span></span>                           |
| <span data-ttu-id="d06b2-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d06b2-289">In Global Catalog</span></span>      | <span data-ttu-id="d06b2-290">Faux</span><span class="sxs-lookup"><span data-stu-id="d06b2-290">False</span></span>                           |
| <span data-ttu-id="d06b2-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d06b2-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="d06b2-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d06b2-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d06b2-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d06b2-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d06b2-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d06b2-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d06b2-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-295">Search-Flags</span></span>           | <span data-ttu-id="d06b2-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d06b2-296">0x00000000</span></span>                      |
| <span data-ttu-id="d06b2-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d06b2-297">System-Flags</span></span>           | <span data-ttu-id="d06b2-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d06b2-298">0x00000010</span></span>                      |
| <span data-ttu-id="d06b2-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d06b2-299">Classes used in</span></span>        | [<span data-ttu-id="d06b2-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="d06b2-300">**Top**</span></span>](c-top.md)<br/> |



 

 





