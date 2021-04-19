---
title: Structural-Object-Class (attribut)
description: Cet attribut construit stocke une liste de classes contenues dans une hiérarchie de classes, y compris les classes abstraites. Cette liste contient des classes auxiliaires liées de manière dynamique.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut structural-Object-Class
- Schéma AD de l’attribut structuralObjectClass
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516721"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="ebf50-106">Structural-Object-Class (attribut)</span><span class="sxs-lookup"><span data-stu-id="ebf50-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="ebf50-107">Cet attribut construit stocke une liste de classes contenues dans une hiérarchie de classes, y compris les classes abstraites.</span><span class="sxs-lookup"><span data-stu-id="ebf50-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="ebf50-108">Cette liste contient des classes auxiliaires liées de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="ebf50-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="ebf50-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-109">Entry</span></span> | <span data-ttu-id="ebf50-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ebf50-111">CN</span><span class="sxs-lookup"><span data-stu-id="ebf50-111">CN</span></span>                | <span data-ttu-id="ebf50-112">Structural-Object-Class</span><span class="sxs-lookup"><span data-stu-id="ebf50-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="ebf50-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ebf50-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ebf50-114">structuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="ebf50-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="ebf50-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ebf50-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="ebf50-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ebf50-116">Update Privilege</span></span>  | <span data-ttu-id="ebf50-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ebf50-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="ebf50-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ebf50-118">Update Frequency</span></span>  | <span data-ttu-id="ebf50-119">Lors de la création de la classe.</span><span class="sxs-lookup"><span data-stu-id="ebf50-119">At class creation.</span></span>                                              |
| <span data-ttu-id="ebf50-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-120">Attribute-Id</span></span>      | <span data-ttu-id="ebf50-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="ebf50-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="ebf50-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ebf50-122">System-Id-Guid</span></span>    | <span data-ttu-id="ebf50-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="ebf50-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="ebf50-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf50-124">Syntax</span></span>            | [<span data-ttu-id="ebf50-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="ebf50-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="ebf50-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ebf50-126">Implementations</span></span>

-   [<span data-ttu-id="ebf50-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ebf50-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ebf50-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ebf50-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ebf50-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ebf50-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ebf50-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ebf50-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ebf50-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ebf50-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ebf50-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ebf50-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ebf50-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebf50-133">Windows Server 2003</span></span>



| <span data-ttu-id="ebf50-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-134">Entry</span></span> | <span data-ttu-id="ebf50-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-138">System-Only</span></span>            | <span data-ttu-id="ebf50-139">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-139">False</span></span>                           |
| <span data-ttu-id="ebf50-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-141">False</span></span>                           |
| <span data-ttu-id="ebf50-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-142">Is Indexed</span></span>             | <span data-ttu-id="ebf50-143">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-143">False</span></span>                           |
| <span data-ttu-id="ebf50-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-144">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-145">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-145">False</span></span>                           |
| <span data-ttu-id="ebf50-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-150">Search-Flags</span></span>           | <span data-ttu-id="ebf50-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-151">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-152">System-Flags</span></span>           | <span data-ttu-id="ebf50-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-153">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-154">Classes used in</span></span>        | [<span data-ttu-id="ebf50-155">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ebf50-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="ebf50-156">ADAM</span></span>



| <span data-ttu-id="ebf50-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-157">Entry</span></span> | <span data-ttu-id="ebf50-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-161">System-Only</span></span>            | <span data-ttu-id="ebf50-162">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-162">False</span></span>                           |
| <span data-ttu-id="ebf50-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-164">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-164">False</span></span>                           |
| <span data-ttu-id="ebf50-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-165">Is Indexed</span></span>             | <span data-ttu-id="ebf50-166">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-166">False</span></span>                           |
| <span data-ttu-id="ebf50-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-167">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-168">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-168">False</span></span>                           |
| <span data-ttu-id="ebf50-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-173">Search-Flags</span></span>           | <span data-ttu-id="ebf50-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-174">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-175">System-Flags</span></span>           | <span data-ttu-id="ebf50-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-176">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-177">Classes used in</span></span>        | [<span data-ttu-id="ebf50-178">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ebf50-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ebf50-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ebf50-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-180">Entry</span></span> | <span data-ttu-id="ebf50-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-184">System-Only</span></span>            | <span data-ttu-id="ebf50-185">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-185">False</span></span>                           |
| <span data-ttu-id="ebf50-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-187">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-187">False</span></span>                           |
| <span data-ttu-id="ebf50-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-188">Is Indexed</span></span>             | <span data-ttu-id="ebf50-189">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-189">False</span></span>                           |
| <span data-ttu-id="ebf50-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-190">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-191">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-191">False</span></span>                           |
| <span data-ttu-id="ebf50-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-196">Search-Flags</span></span>           | <span data-ttu-id="ebf50-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-197">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-198">System-Flags</span></span>           | <span data-ttu-id="ebf50-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-199">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-200">Classes used in</span></span>        | [<span data-ttu-id="ebf50-201">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ebf50-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf50-202">Windows Server 2008</span></span>



| <span data-ttu-id="ebf50-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-203">Entry</span></span> | <span data-ttu-id="ebf50-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-207">System-Only</span></span>            | <span data-ttu-id="ebf50-208">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-208">False</span></span>                           |
| <span data-ttu-id="ebf50-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-210">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-210">False</span></span>                           |
| <span data-ttu-id="ebf50-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-211">Is Indexed</span></span>             | <span data-ttu-id="ebf50-212">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-212">False</span></span>                           |
| <span data-ttu-id="ebf50-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-213">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-214">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-214">False</span></span>                           |
| <span data-ttu-id="ebf50-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-219">Search-Flags</span></span>           | <span data-ttu-id="ebf50-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-220">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-221">System-Flags</span></span>           | <span data-ttu-id="ebf50-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-222">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-223">Classes used in</span></span>        | [<span data-ttu-id="ebf50-224">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ebf50-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebf50-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ebf50-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-226">Entry</span></span> | <span data-ttu-id="ebf50-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-230">System-Only</span></span>            | <span data-ttu-id="ebf50-231">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-231">False</span></span>                           |
| <span data-ttu-id="ebf50-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-233">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-233">False</span></span>                           |
| <span data-ttu-id="ebf50-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-234">Is Indexed</span></span>             | <span data-ttu-id="ebf50-235">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-235">False</span></span>                           |
| <span data-ttu-id="ebf50-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-236">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-237">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-237">False</span></span>                           |
| <span data-ttu-id="ebf50-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-242">Search-Flags</span></span>           | <span data-ttu-id="ebf50-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-243">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-244">System-Flags</span></span>           | <span data-ttu-id="ebf50-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-245">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-246">Classes used in</span></span>        | [<span data-ttu-id="ebf50-247">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ebf50-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ebf50-248">Windows Server 2012</span></span>



| <span data-ttu-id="ebf50-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="ebf50-249">Entry</span></span> | <span data-ttu-id="ebf50-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf50-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebf50-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ebf50-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf50-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebf50-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf50-253">System-Only</span></span>            | <span data-ttu-id="ebf50-254">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-254">False</span></span>                           |
| <span data-ttu-id="ebf50-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ebf50-255">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf50-256">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-256">False</span></span>                           |
| <span data-ttu-id="ebf50-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ebf50-257">Is Indexed</span></span>             | <span data-ttu-id="ebf50-258">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-258">False</span></span>                           |
| <span data-ttu-id="ebf50-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ebf50-259">In Global Catalog</span></span>      | <span data-ttu-id="ebf50-260">Faux</span><span class="sxs-lookup"><span data-stu-id="ebf50-260">False</span></span>                           |
| <span data-ttu-id="ebf50-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ebf50-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf50-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ebf50-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebf50-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf50-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebf50-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf50-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebf50-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-265">Search-Flags</span></span>           | <span data-ttu-id="ebf50-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf50-266">0x00000000</span></span>                      |
| <span data-ttu-id="ebf50-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf50-267">System-Flags</span></span>           | <span data-ttu-id="ebf50-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ebf50-268">0x00000014</span></span>                      |
| <span data-ttu-id="ebf50-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ebf50-269">Classes used in</span></span>        | [<span data-ttu-id="ebf50-270">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ebf50-270">**Top**</span></span>](c-top.md)<br/> |



 

 





