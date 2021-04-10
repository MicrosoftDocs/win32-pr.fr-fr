---
title: MS-DS-Consistency-attribut de nombre d’enfants
description: Cet attribut est utilisé pour vérifier la cohérence entre le répertoire et un autre objet, base de données ou application, en comparant le nombre d’objets enfants.
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de nombre d’enfants-cohérence MS-DS-Consistency
- Schéma AD de l’attribut mS-DS-ConsistencyChildCount
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107191"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="cf58f-105">MS-DS-Consistency-attribut de nombre d’enfants</span><span class="sxs-lookup"><span data-stu-id="cf58f-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="cf58f-106">Cet attribut est utilisé pour vérifier la cohérence entre le répertoire et un autre objet, base de données ou application, en comparant le nombre d’objets enfants.</span><span class="sxs-lookup"><span data-stu-id="cf58f-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="cf58f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-107">Entry</span></span> | <span data-ttu-id="cf58f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cf58f-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf58f-109">CN</span></span>                | <span data-ttu-id="cf58f-110">MS-DS-Consistency-enfant-nombre</span><span class="sxs-lookup"><span data-stu-id="cf58f-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="cf58f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cf58f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf58f-112">mS-DS-ConsistencyChildCount</span><span class="sxs-lookup"><span data-stu-id="cf58f-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="cf58f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="cf58f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="cf58f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cf58f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cf58f-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cf58f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cf58f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-116">Attribute-Id</span></span>      | <span data-ttu-id="cf58f-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="cf58f-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="cf58f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cf58f-118">System-Id-Guid</span></span>    | <span data-ttu-id="cf58f-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="cf58f-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="cf58f-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf58f-120">Syntax</span></span>            | [<span data-ttu-id="cf58f-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="cf58f-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cf58f-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cf58f-122">Implementations</span></span>

-   [<span data-ttu-id="cf58f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf58f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf58f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf58f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf58f-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cf58f-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cf58f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf58f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf58f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf58f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf58f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf58f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf58f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf58f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf58f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf58f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cf58f-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-131">Entry</span></span> | <span data-ttu-id="cf58f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-135">System-Only</span></span>            | <span data-ttu-id="cf58f-136">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-136">False</span></span>                           |
| <span data-ttu-id="cf58f-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-138">True</span></span>                            |
| <span data-ttu-id="cf58f-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-139">Is Indexed</span></span>             | <span data-ttu-id="cf58f-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-140">False</span></span>                           |
| <span data-ttu-id="cf58f-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-141">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-142">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-142">False</span></span>                           |
| <span data-ttu-id="cf58f-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-147">Search-Flags</span></span>           | <span data-ttu-id="cf58f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-148">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-149">System-Flags</span></span>           | <span data-ttu-id="cf58f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-150">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-151">Classes used in</span></span>        | [<span data-ttu-id="cf58f-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf58f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf58f-153">Windows Server 2003</span></span>



| <span data-ttu-id="cf58f-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-154">Entry</span></span> | <span data-ttu-id="cf58f-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-158">System-Only</span></span>            | <span data-ttu-id="cf58f-159">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-159">False</span></span>                           |
| <span data-ttu-id="cf58f-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-161">True</span></span>                            |
| <span data-ttu-id="cf58f-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-162">Is Indexed</span></span>             | <span data-ttu-id="cf58f-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-163">False</span></span>                           |
| <span data-ttu-id="cf58f-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-164">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-165">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-165">False</span></span>                           |
| <span data-ttu-id="cf58f-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-170">Search-Flags</span></span>           | <span data-ttu-id="cf58f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-171">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-172">System-Flags</span></span>           | <span data-ttu-id="cf58f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-173">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-174">Classes used in</span></span>        | [<span data-ttu-id="cf58f-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cf58f-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="cf58f-176">ADAM</span></span>



| <span data-ttu-id="cf58f-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-177">Entry</span></span> | <span data-ttu-id="cf58f-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-181">System-Only</span></span>            | <span data-ttu-id="cf58f-182">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-182">False</span></span>                           |
| <span data-ttu-id="cf58f-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-184">True</span></span>                            |
| <span data-ttu-id="cf58f-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-185">Is Indexed</span></span>             | <span data-ttu-id="cf58f-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-186">False</span></span>                           |
| <span data-ttu-id="cf58f-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-187">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-188">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-188">False</span></span>                           |
| <span data-ttu-id="cf58f-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-193">Search-Flags</span></span>           | <span data-ttu-id="cf58f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-194">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-195">System-Flags</span></span>           | <span data-ttu-id="cf58f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-196">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-197">Classes used in</span></span>        | [<span data-ttu-id="cf58f-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf58f-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf58f-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf58f-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-200">Entry</span></span> | <span data-ttu-id="cf58f-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-204">System-Only</span></span>            | <span data-ttu-id="cf58f-205">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-205">False</span></span>                           |
| <span data-ttu-id="cf58f-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-207">True</span></span>                            |
| <span data-ttu-id="cf58f-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-208">Is Indexed</span></span>             | <span data-ttu-id="cf58f-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-209">False</span></span>                           |
| <span data-ttu-id="cf58f-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-210">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-211">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-211">False</span></span>                           |
| <span data-ttu-id="cf58f-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-216">Search-Flags</span></span>           | <span data-ttu-id="cf58f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-217">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-218">System-Flags</span></span>           | <span data-ttu-id="cf58f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-219">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-220">Classes used in</span></span>        | [<span data-ttu-id="cf58f-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf58f-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf58f-222">Windows Server 2008</span></span>



| <span data-ttu-id="cf58f-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-223">Entry</span></span> | <span data-ttu-id="cf58f-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-227">System-Only</span></span>            | <span data-ttu-id="cf58f-228">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-228">False</span></span>                           |
| <span data-ttu-id="cf58f-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-230">True</span></span>                            |
| <span data-ttu-id="cf58f-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-231">Is Indexed</span></span>             | <span data-ttu-id="cf58f-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-232">False</span></span>                           |
| <span data-ttu-id="cf58f-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-233">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-234">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-234">False</span></span>                           |
| <span data-ttu-id="cf58f-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-239">Search-Flags</span></span>           | <span data-ttu-id="cf58f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-240">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-241">System-Flags</span></span>           | <span data-ttu-id="cf58f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-242">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-243">Classes used in</span></span>        | [<span data-ttu-id="cf58f-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf58f-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf58f-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf58f-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-246">Entry</span></span> | <span data-ttu-id="cf58f-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-250">System-Only</span></span>            | <span data-ttu-id="cf58f-251">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-251">False</span></span>                           |
| <span data-ttu-id="cf58f-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-253">True</span></span>                            |
| <span data-ttu-id="cf58f-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-254">Is Indexed</span></span>             | <span data-ttu-id="cf58f-255">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-255">False</span></span>                           |
| <span data-ttu-id="cf58f-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-256">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-257">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-257">False</span></span>                           |
| <span data-ttu-id="cf58f-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-262">Search-Flags</span></span>           | <span data-ttu-id="cf58f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-263">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-264">System-Flags</span></span>           | <span data-ttu-id="cf58f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-265">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-266">Classes used in</span></span>        | [<span data-ttu-id="cf58f-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf58f-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf58f-268">Windows Server 2012</span></span>



| <span data-ttu-id="cf58f-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="cf58f-269">Entry</span></span> | <span data-ttu-id="cf58f-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf58f-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf58f-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cf58f-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf58f-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf58f-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf58f-273">System-Only</span></span>            | <span data-ttu-id="cf58f-274">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-274">False</span></span>                           |
| <span data-ttu-id="cf58f-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cf58f-275">Is-Single-Valued</span></span>       | <span data-ttu-id="cf58f-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf58f-276">True</span></span>                            |
| <span data-ttu-id="cf58f-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cf58f-277">Is Indexed</span></span>             | <span data-ttu-id="cf58f-278">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-278">False</span></span>                           |
| <span data-ttu-id="cf58f-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cf58f-279">In Global Catalog</span></span>      | <span data-ttu-id="cf58f-280">Faux</span><span class="sxs-lookup"><span data-stu-id="cf58f-280">False</span></span>                           |
| <span data-ttu-id="cf58f-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cf58f-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf58f-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cf58f-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf58f-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf58f-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf58f-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf58f-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf58f-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-285">Search-Flags</span></span>           | <span data-ttu-id="cf58f-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf58f-286">0x00000000</span></span>                      |
| <span data-ttu-id="cf58f-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf58f-287">System-Flags</span></span>           | <span data-ttu-id="cf58f-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf58f-288">0x00000010</span></span>                      |
| <span data-ttu-id="cf58f-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cf58f-289">Classes used in</span></span>        | [<span data-ttu-id="cf58f-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cf58f-290">**Top**</span></span>](c-top.md)<br/> |



 

 





