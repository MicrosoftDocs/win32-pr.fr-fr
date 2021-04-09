---
title: Attribut Object-Class
description: Liste des classes à partir desquelles cette classe est dérivée.
ms.assetid: def98723-2d8a-49ea-84f8-afe6ff9cdfd9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Class
- Schéma AD de l’attribut objectClass
topic_type:
- apiref
api_name:
- Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851d48bcbcc40640af3ee555c343feaab05edf6b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107999"
---
# <a name="object-class-attribute"></a><span data-ttu-id="47413-105">Attribut Object-Class</span><span class="sxs-lookup"><span data-stu-id="47413-105">Object-Class attribute</span></span>

<span data-ttu-id="47413-106">Liste des classes à partir desquelles cette classe est dérivée.</span><span class="sxs-lookup"><span data-stu-id="47413-106">The list of classes from which this class is derived.</span></span>



| <span data-ttu-id="47413-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-107">Entry</span></span> | <span data-ttu-id="47413-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="47413-109">CN</span><span class="sxs-lookup"><span data-stu-id="47413-109">CN</span></span>                | <span data-ttu-id="47413-110">Object-Class</span><span class="sxs-lookup"><span data-stu-id="47413-110">Object-Class</span></span>                                                    |
| <span data-ttu-id="47413-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="47413-111">Ldap-Display-Name</span></span> | <span data-ttu-id="47413-112">objectClass</span><span class="sxs-lookup"><span data-stu-id="47413-112">objectClass</span></span>                                                     |
| <span data-ttu-id="47413-113">Taille</span><span class="sxs-lookup"><span data-stu-id="47413-113">Size</span></span>              | <span data-ttu-id="47413-114">Environ 20 octets en moyenne.</span><span class="sxs-lookup"><span data-stu-id="47413-114">About 20 bytes on average.</span></span>                                      |
| <span data-ttu-id="47413-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="47413-115">Update Privilege</span></span>  | <span data-ttu-id="47413-116">Le concepteur de l’objet définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="47413-116">The designer of the object would set this value.</span></span>                |
| <span data-ttu-id="47413-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="47413-117">Update Frequency</span></span>  | <span data-ttu-id="47413-118">Cette valeur ne doit jamais changer.</span><span class="sxs-lookup"><span data-stu-id="47413-118">This value should never change.</span></span>                                 |
| <span data-ttu-id="47413-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47413-119">Attribute-Id</span></span>      | <span data-ttu-id="47413-120">2.5.4.0</span><span class="sxs-lookup"><span data-stu-id="47413-120">2.5.4.0</span></span>                                                         |
| <span data-ttu-id="47413-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="47413-121">System-Id-Guid</span></span>    | <span data-ttu-id="47413-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="47413-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="47413-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47413-123">Syntax</span></span>            | [<span data-ttu-id="47413-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="47413-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="47413-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="47413-125">Implementations</span></span>

-   [<span data-ttu-id="47413-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="47413-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="47413-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47413-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47413-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="47413-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="47413-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47413-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47413-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47413-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47413-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47413-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47413-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47413-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="47413-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47413-133">Windows 2000 Server</span></span>



| <span data-ttu-id="47413-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-134">Entry</span></span> | <span data-ttu-id="47413-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-138">System-Only</span></span>            | <span data-ttu-id="47413-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-139">True</span></span>                            |
| <span data-ttu-id="47413-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-140">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-141">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-141">False</span></span>                           |
| <span data-ttu-id="47413-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-142">Is Indexed</span></span>             | <span data-ttu-id="47413-143">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-143">False</span></span>                           |
| <span data-ttu-id="47413-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-144">In Global Catalog</span></span>      | <span data-ttu-id="47413-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-145">True</span></span>                            |
| <span data-ttu-id="47413-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-150">Search-Flags</span></span>           | <span data-ttu-id="47413-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47413-151">0x00000008</span></span>                      |
| <span data-ttu-id="47413-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-152">System-Flags</span></span>           | <span data-ttu-id="47413-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-153">0x00000012</span></span>                      |
| <span data-ttu-id="47413-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-154">Classes used in</span></span>        | [<span data-ttu-id="47413-155">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="47413-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47413-156">Windows Server 2003</span></span>



| <span data-ttu-id="47413-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-157">Entry</span></span> | <span data-ttu-id="47413-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-161">System-Only</span></span>            | <span data-ttu-id="47413-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-162">True</span></span>                            |
| <span data-ttu-id="47413-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-163">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-164">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-164">False</span></span>                           |
| <span data-ttu-id="47413-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-165">Is Indexed</span></span>             | <span data-ttu-id="47413-166">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-166">False</span></span>                           |
| <span data-ttu-id="47413-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-167">In Global Catalog</span></span>      | <span data-ttu-id="47413-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-168">True</span></span>                            |
| <span data-ttu-id="47413-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-173">Search-Flags</span></span>           | <span data-ttu-id="47413-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47413-174">0x00000008</span></span>                      |
| <span data-ttu-id="47413-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-175">System-Flags</span></span>           | <span data-ttu-id="47413-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-176">0x00000012</span></span>                      |
| <span data-ttu-id="47413-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-177">Classes used in</span></span>        | [<span data-ttu-id="47413-178">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="47413-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="47413-179">ADAM</span></span>



| <span data-ttu-id="47413-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-180">Entry</span></span> | <span data-ttu-id="47413-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-184">System-Only</span></span>            | <span data-ttu-id="47413-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-185">True</span></span>                            |
| <span data-ttu-id="47413-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-186">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-187">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-187">False</span></span>                           |
| <span data-ttu-id="47413-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-188">Is Indexed</span></span>             | <span data-ttu-id="47413-189">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-189">False</span></span>                           |
| <span data-ttu-id="47413-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-190">In Global Catalog</span></span>      | <span data-ttu-id="47413-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-191">True</span></span>                            |
| <span data-ttu-id="47413-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-196">Search-Flags</span></span>           | <span data-ttu-id="47413-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47413-197">0x00000008</span></span>                      |
| <span data-ttu-id="47413-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-198">System-Flags</span></span>           | <span data-ttu-id="47413-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-199">0x00000012</span></span>                      |
| <span data-ttu-id="47413-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-200">Classes used in</span></span>        | [<span data-ttu-id="47413-201">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47413-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47413-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47413-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-203">Entry</span></span> | <span data-ttu-id="47413-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-207">System-Only</span></span>            | <span data-ttu-id="47413-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-208">True</span></span>                            |
| <span data-ttu-id="47413-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-209">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-210">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-210">False</span></span>                           |
| <span data-ttu-id="47413-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-211">Is Indexed</span></span>             | <span data-ttu-id="47413-212">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-212">False</span></span>                           |
| <span data-ttu-id="47413-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-213">In Global Catalog</span></span>      | <span data-ttu-id="47413-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-214">True</span></span>                            |
| <span data-ttu-id="47413-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-219">Search-Flags</span></span>           | <span data-ttu-id="47413-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47413-220">0x00000008</span></span>                      |
| <span data-ttu-id="47413-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-221">System-Flags</span></span>           | <span data-ttu-id="47413-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-222">0x00000012</span></span>                      |
| <span data-ttu-id="47413-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-223">Classes used in</span></span>        | [<span data-ttu-id="47413-224">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47413-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47413-225">Windows Server 2008</span></span>



| <span data-ttu-id="47413-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-226">Entry</span></span> | <span data-ttu-id="47413-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-230">System-Only</span></span>            | <span data-ttu-id="47413-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-231">True</span></span>                            |
| <span data-ttu-id="47413-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-232">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-233">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-233">False</span></span>                           |
| <span data-ttu-id="47413-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-234">Is Indexed</span></span>             | <span data-ttu-id="47413-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-235">True</span></span>                            |
| <span data-ttu-id="47413-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-236">In Global Catalog</span></span>      | <span data-ttu-id="47413-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-237">True</span></span>                            |
| <span data-ttu-id="47413-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-242">Search-Flags</span></span>           | <span data-ttu-id="47413-243">0x00000009</span><span class="sxs-lookup"><span data-stu-id="47413-243">0x00000009</span></span>                      |
| <span data-ttu-id="47413-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-244">System-Flags</span></span>           | <span data-ttu-id="47413-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-245">0x00000012</span></span>                      |
| <span data-ttu-id="47413-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-246">Classes used in</span></span>        | [<span data-ttu-id="47413-247">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47413-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47413-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47413-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-249">Entry</span></span> | <span data-ttu-id="47413-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-253">System-Only</span></span>            | <span data-ttu-id="47413-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-254">True</span></span>                            |
| <span data-ttu-id="47413-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-255">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-256">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-256">False</span></span>                           |
| <span data-ttu-id="47413-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-257">Is Indexed</span></span>             | <span data-ttu-id="47413-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-258">True</span></span>                            |
| <span data-ttu-id="47413-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-259">In Global Catalog</span></span>      | <span data-ttu-id="47413-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-260">True</span></span>                            |
| <span data-ttu-id="47413-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-265">Search-Flags</span></span>           | <span data-ttu-id="47413-266">0x00000009</span><span class="sxs-lookup"><span data-stu-id="47413-266">0x00000009</span></span>                      |
| <span data-ttu-id="47413-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-267">System-Flags</span></span>           | <span data-ttu-id="47413-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-268">0x00000012</span></span>                      |
| <span data-ttu-id="47413-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-269">Classes used in</span></span>        | [<span data-ttu-id="47413-270">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47413-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47413-271">Windows Server 2012</span></span>



| <span data-ttu-id="47413-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="47413-272">Entry</span></span> | <span data-ttu-id="47413-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="47413-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47413-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47413-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47413-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47413-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="47413-276">System-Only</span></span>            | <span data-ttu-id="47413-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-277">True</span></span>                            |
| <span data-ttu-id="47413-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47413-278">Is-Single-Valued</span></span>       | <span data-ttu-id="47413-279">Faux</span><span class="sxs-lookup"><span data-stu-id="47413-279">False</span></span>                           |
| <span data-ttu-id="47413-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47413-280">Is Indexed</span></span>             | <span data-ttu-id="47413-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-281">True</span></span>                            |
| <span data-ttu-id="47413-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47413-282">In Global Catalog</span></span>      | <span data-ttu-id="47413-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="47413-283">True</span></span>                            |
| <span data-ttu-id="47413-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47413-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="47413-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47413-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47413-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47413-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47413-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47413-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47413-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-288">Search-Flags</span></span>           | <span data-ttu-id="47413-289">0x00000009</span><span class="sxs-lookup"><span data-stu-id="47413-289">0x00000009</span></span>                      |
| <span data-ttu-id="47413-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47413-290">System-Flags</span></span>           | <span data-ttu-id="47413-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47413-291">0x00000012</span></span>                      |
| <span data-ttu-id="47413-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47413-292">Classes used in</span></span>        | [<span data-ttu-id="47413-293">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="47413-293">**Top**</span></span>](c-top.md)<br/> |



 

 





