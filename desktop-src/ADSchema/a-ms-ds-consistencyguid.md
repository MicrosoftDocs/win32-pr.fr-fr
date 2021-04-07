---
title: MS-DS-Consistency-attribut Guid
description: Cet attribut est utilisé pour vérifier la cohérence entre le répertoire et un autre objet, base de données ou application, en comparant les GUID.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de cohérence MS-DS-Consistency-GUID
- Schéma AD de l’attribut mS-DS-ConsistencyGuid
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845210"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="fea12-105">MS-DS-Consistency-attribut Guid</span><span class="sxs-lookup"><span data-stu-id="fea12-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="fea12-106">Cet attribut est utilisé pour vérifier la cohérence entre le répertoire et un autre objet, base de données ou application, en comparant les GUID.</span><span class="sxs-lookup"><span data-stu-id="fea12-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="fea12-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-107">Entry</span></span> | <span data-ttu-id="fea12-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="fea12-109">CN</span><span class="sxs-lookup"><span data-stu-id="fea12-109">CN</span></span>                | <span data-ttu-id="fea12-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="fea12-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="fea12-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fea12-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fea12-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="fea12-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="fea12-113">Taille</span><span class="sxs-lookup"><span data-stu-id="fea12-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="fea12-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="fea12-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="fea12-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="fea12-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="fea12-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-116">Attribute-Id</span></span>      | <span data-ttu-id="fea12-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="fea12-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="fea12-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fea12-118">System-Id-Guid</span></span>    | <span data-ttu-id="fea12-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="fea12-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="fea12-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fea12-120">Syntax</span></span>            | [<span data-ttu-id="fea12-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="fea12-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="fea12-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="fea12-122">Implementations</span></span>

-   [<span data-ttu-id="fea12-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fea12-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fea12-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fea12-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fea12-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fea12-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fea12-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fea12-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fea12-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fea12-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fea12-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fea12-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fea12-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fea12-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fea12-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fea12-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fea12-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-131">Entry</span></span> | <span data-ttu-id="fea12-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-135">System-Only</span></span>            | <span data-ttu-id="fea12-136">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-136">False</span></span>                           |
| <span data-ttu-id="fea12-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-138">True</span></span>                            |
| <span data-ttu-id="fea12-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-139">Is Indexed</span></span>             | <span data-ttu-id="fea12-140">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-140">False</span></span>                           |
| <span data-ttu-id="fea12-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-141">In Global Catalog</span></span>      | <span data-ttu-id="fea12-142">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-142">False</span></span>                           |
| <span data-ttu-id="fea12-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-147">Search-Flags</span></span>           | <span data-ttu-id="fea12-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-148">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-149">System-Flags</span></span>           | <span data-ttu-id="fea12-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-150">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-151">Classes used in</span></span>        | [<span data-ttu-id="fea12-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fea12-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fea12-153">Windows Server 2003</span></span>



| <span data-ttu-id="fea12-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-154">Entry</span></span> | <span data-ttu-id="fea12-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-158">System-Only</span></span>            | <span data-ttu-id="fea12-159">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-159">False</span></span>                           |
| <span data-ttu-id="fea12-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-161">True</span></span>                            |
| <span data-ttu-id="fea12-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-162">Is Indexed</span></span>             | <span data-ttu-id="fea12-163">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-163">False</span></span>                           |
| <span data-ttu-id="fea12-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-164">In Global Catalog</span></span>      | <span data-ttu-id="fea12-165">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-165">False</span></span>                           |
| <span data-ttu-id="fea12-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-170">Search-Flags</span></span>           | <span data-ttu-id="fea12-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-171">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-172">System-Flags</span></span>           | <span data-ttu-id="fea12-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-173">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-174">Classes used in</span></span>        | [<span data-ttu-id="fea12-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fea12-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="fea12-176">ADAM</span></span>



| <span data-ttu-id="fea12-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-177">Entry</span></span> | <span data-ttu-id="fea12-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-181">System-Only</span></span>            | <span data-ttu-id="fea12-182">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-182">False</span></span>                           |
| <span data-ttu-id="fea12-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-184">True</span></span>                            |
| <span data-ttu-id="fea12-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-185">Is Indexed</span></span>             | <span data-ttu-id="fea12-186">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-186">False</span></span>                           |
| <span data-ttu-id="fea12-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-187">In Global Catalog</span></span>      | <span data-ttu-id="fea12-188">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-188">False</span></span>                           |
| <span data-ttu-id="fea12-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-193">Search-Flags</span></span>           | <span data-ttu-id="fea12-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-194">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-195">System-Flags</span></span>           | <span data-ttu-id="fea12-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-196">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-197">Classes used in</span></span>        | [<span data-ttu-id="fea12-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fea12-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fea12-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fea12-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-200">Entry</span></span> | <span data-ttu-id="fea12-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-204">System-Only</span></span>            | <span data-ttu-id="fea12-205">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-205">False</span></span>                           |
| <span data-ttu-id="fea12-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-207">True</span></span>                            |
| <span data-ttu-id="fea12-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-208">Is Indexed</span></span>             | <span data-ttu-id="fea12-209">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-209">False</span></span>                           |
| <span data-ttu-id="fea12-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-210">In Global Catalog</span></span>      | <span data-ttu-id="fea12-211">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-211">False</span></span>                           |
| <span data-ttu-id="fea12-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-216">Search-Flags</span></span>           | <span data-ttu-id="fea12-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-217">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-218">System-Flags</span></span>           | <span data-ttu-id="fea12-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-219">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-220">Classes used in</span></span>        | [<span data-ttu-id="fea12-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fea12-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fea12-222">Windows Server 2008</span></span>



| <span data-ttu-id="fea12-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-223">Entry</span></span> | <span data-ttu-id="fea12-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-227">System-Only</span></span>            | <span data-ttu-id="fea12-228">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-228">False</span></span>                           |
| <span data-ttu-id="fea12-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-230">True</span></span>                            |
| <span data-ttu-id="fea12-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-231">Is Indexed</span></span>             | <span data-ttu-id="fea12-232">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-232">False</span></span>                           |
| <span data-ttu-id="fea12-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-233">In Global Catalog</span></span>      | <span data-ttu-id="fea12-234">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-234">False</span></span>                           |
| <span data-ttu-id="fea12-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-239">Search-Flags</span></span>           | <span data-ttu-id="fea12-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-240">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-241">System-Flags</span></span>           | <span data-ttu-id="fea12-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-242">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-243">Classes used in</span></span>        | [<span data-ttu-id="fea12-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fea12-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fea12-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fea12-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-246">Entry</span></span> | <span data-ttu-id="fea12-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-250">System-Only</span></span>            | <span data-ttu-id="fea12-251">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-251">False</span></span>                           |
| <span data-ttu-id="fea12-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-253">True</span></span>                            |
| <span data-ttu-id="fea12-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-254">Is Indexed</span></span>             | <span data-ttu-id="fea12-255">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-255">False</span></span>                           |
| <span data-ttu-id="fea12-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-256">In Global Catalog</span></span>      | <span data-ttu-id="fea12-257">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-257">False</span></span>                           |
| <span data-ttu-id="fea12-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-262">Search-Flags</span></span>           | <span data-ttu-id="fea12-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-263">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-264">System-Flags</span></span>           | <span data-ttu-id="fea12-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-265">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-266">Classes used in</span></span>        | [<span data-ttu-id="fea12-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fea12-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fea12-268">Windows Server 2012</span></span>



| <span data-ttu-id="fea12-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="fea12-269">Entry</span></span> | <span data-ttu-id="fea12-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea12-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fea12-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fea12-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fea12-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fea12-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="fea12-273">System-Only</span></span>            | <span data-ttu-id="fea12-274">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-274">False</span></span>                           |
| <span data-ttu-id="fea12-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fea12-275">Is-Single-Valued</span></span>       | <span data-ttu-id="fea12-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="fea12-276">True</span></span>                            |
| <span data-ttu-id="fea12-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fea12-277">Is Indexed</span></span>             | <span data-ttu-id="fea12-278">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-278">False</span></span>                           |
| <span data-ttu-id="fea12-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fea12-279">In Global Catalog</span></span>      | <span data-ttu-id="fea12-280">Faux</span><span class="sxs-lookup"><span data-stu-id="fea12-280">False</span></span>                           |
| <span data-ttu-id="fea12-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fea12-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="fea12-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fea12-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fea12-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fea12-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fea12-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fea12-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fea12-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-285">Search-Flags</span></span>           | <span data-ttu-id="fea12-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fea12-286">0x00000000</span></span>                      |
| <span data-ttu-id="fea12-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fea12-287">System-Flags</span></span>           | <span data-ttu-id="fea12-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fea12-288">0x00000010</span></span>                      |
| <span data-ttu-id="fea12-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fea12-289">Classes used in</span></span>        | [<span data-ttu-id="fea12-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fea12-290">**Top**</span></span>](c-top.md)<br/> |



 

 





