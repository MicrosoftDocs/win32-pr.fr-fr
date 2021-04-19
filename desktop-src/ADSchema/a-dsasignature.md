---
title: Attribut DSA-Signature
description: La DSA-Signature d’un objet est l’ID d’appel du dernier répertoire pour modifier l’objet.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut DSA-Signature
- Schéma AD de l’attribut dSASignature
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514268"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="5cb2e-105">Attribut DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="5cb2e-105">DSA-Signature attribute</span></span>

<span data-ttu-id="5cb2e-106">La DSA-Signature d’un objet est l’ID d’appel du dernier répertoire pour modifier l’objet.</span><span class="sxs-lookup"><span data-stu-id="5cb2e-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="5cb2e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-107">Entry</span></span> | <span data-ttu-id="5cb2e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5cb2e-109">CN</span><span class="sxs-lookup"><span data-stu-id="5cb2e-109">CN</span></span>                | <span data-ttu-id="5cb2e-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="5cb2e-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="5cb2e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5cb2e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5cb2e-112">dSASignature</span><span class="sxs-lookup"><span data-stu-id="5cb2e-112">dSASignature</span></span>                                          |
| <span data-ttu-id="5cb2e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="5cb2e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="5cb2e-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="5cb2e-114">Update Privilege</span></span>  | <span data-ttu-id="5cb2e-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="5cb2e-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5cb2e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="5cb2e-116">Update Frequency</span></span>  | <span data-ttu-id="5cb2e-117">Chaque fois qu’un objet est modifié.</span><span class="sxs-lookup"><span data-stu-id="5cb2e-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="5cb2e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-118">Attribute-Id</span></span>      | <span data-ttu-id="5cb2e-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="5cb2e-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="5cb2e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5cb2e-120">System-Id-Guid</span></span>    | <span data-ttu-id="5cb2e-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5cb2e-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="5cb2e-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cb2e-122">Syntax</span></span>            | [<span data-ttu-id="5cb2e-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5cb2e-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="5cb2e-124">Implementations</span></span>

-   [<span data-ttu-id="5cb2e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5cb2e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5cb2e-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5cb2e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5cb2e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5cb2e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5cb2e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5cb2e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cb2e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5cb2e-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-133">Entry</span></span> | <span data-ttu-id="5cb2e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-136">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-137">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-138">System-Only</span></span>            | <span data-ttu-id="5cb2e-139">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-139">False</span></span>                           |
| <span data-ttu-id="5cb2e-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-141">True</span></span>                            |
| <span data-ttu-id="5cb2e-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-142">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-143">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-143">False</span></span>                           |
| <span data-ttu-id="5cb2e-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-144">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-145">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-145">False</span></span>                           |
| <span data-ttu-id="5cb2e-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-150">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-151">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-152">System-Flags</span></span>           | <span data-ttu-id="5cb2e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-153">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-154">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-155">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5cb2e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5cb2e-156">Windows Server 2003</span></span>



| <span data-ttu-id="5cb2e-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-157">Entry</span></span> | <span data-ttu-id="5cb2e-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-160">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-161">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-162">System-Only</span></span>            | <span data-ttu-id="5cb2e-163">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-163">False</span></span>                           |
| <span data-ttu-id="5cb2e-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-164">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-165">True</span></span>                            |
| <span data-ttu-id="5cb2e-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-166">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-167">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-167">False</span></span>                           |
| <span data-ttu-id="5cb2e-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-168">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-169">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-169">False</span></span>                           |
| <span data-ttu-id="5cb2e-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-174">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-175">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-176">System-Flags</span></span>           | <span data-ttu-id="5cb2e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-177">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-178">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-179">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5cb2e-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="5cb2e-180">ADAM</span></span>



| <span data-ttu-id="5cb2e-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-181">Entry</span></span> | <span data-ttu-id="5cb2e-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-184">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-185">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-186">System-Only</span></span>            | <span data-ttu-id="5cb2e-187">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-187">False</span></span>                           |
| <span data-ttu-id="5cb2e-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-189">True</span></span>                            |
| <span data-ttu-id="5cb2e-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-190">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-191">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-191">False</span></span>                           |
| <span data-ttu-id="5cb2e-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-192">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-193">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-193">False</span></span>                           |
| <span data-ttu-id="5cb2e-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-198">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-199">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-200">System-Flags</span></span>           | <span data-ttu-id="5cb2e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-201">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-202">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-203">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5cb2e-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5cb2e-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5cb2e-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-205">Entry</span></span> | <span data-ttu-id="5cb2e-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-208">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-209">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-210">System-Only</span></span>            | <span data-ttu-id="5cb2e-211">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-211">False</span></span>                           |
| <span data-ttu-id="5cb2e-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-213">True</span></span>                            |
| <span data-ttu-id="5cb2e-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-214">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-215">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-215">False</span></span>                           |
| <span data-ttu-id="5cb2e-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-216">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-217">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-217">False</span></span>                           |
| <span data-ttu-id="5cb2e-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-222">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-223">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-224">System-Flags</span></span>           | <span data-ttu-id="5cb2e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-225">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-226">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-227">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5cb2e-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cb2e-228">Windows Server 2008</span></span>



| <span data-ttu-id="5cb2e-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-229">Entry</span></span> | <span data-ttu-id="5cb2e-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-232">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-233">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-234">System-Only</span></span>            | <span data-ttu-id="5cb2e-235">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-235">False</span></span>                           |
| <span data-ttu-id="5cb2e-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-236">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-237">True</span></span>                            |
| <span data-ttu-id="5cb2e-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-238">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-239">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-239">False</span></span>                           |
| <span data-ttu-id="5cb2e-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-240">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-241">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-241">False</span></span>                           |
| <span data-ttu-id="5cb2e-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-246">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-247">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-248">System-Flags</span></span>           | <span data-ttu-id="5cb2e-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-249">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-250">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-251">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5cb2e-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5cb2e-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5cb2e-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-253">Entry</span></span> | <span data-ttu-id="5cb2e-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-256">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-257">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-258">System-Only</span></span>            | <span data-ttu-id="5cb2e-259">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-259">False</span></span>                           |
| <span data-ttu-id="5cb2e-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-261">True</span></span>                            |
| <span data-ttu-id="5cb2e-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-262">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-263">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-263">False</span></span>                           |
| <span data-ttu-id="5cb2e-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-264">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-265">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-265">False</span></span>                           |
| <span data-ttu-id="5cb2e-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-270">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-271">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-272">System-Flags</span></span>           | <span data-ttu-id="5cb2e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-273">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-274">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-275">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5cb2e-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cb2e-276">Windows Server 2012</span></span>



| <span data-ttu-id="5cb2e-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="5cb2e-277">Entry</span></span> | <span data-ttu-id="5cb2e-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cb2e-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5cb2e-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5cb2e-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5cb2e-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cb2e-280">MAPI-Id</span></span>                | <span data-ttu-id="5cb2e-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="5cb2e-281">0x8077</span></span>                          |
| <span data-ttu-id="5cb2e-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cb2e-282">System-Only</span></span>            | <span data-ttu-id="5cb2e-283">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-283">False</span></span>                           |
| <span data-ttu-id="5cb2e-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5cb2e-284">Is-Single-Valued</span></span>       | <span data-ttu-id="5cb2e-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="5cb2e-285">True</span></span>                            |
| <span data-ttu-id="5cb2e-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5cb2e-286">Is Indexed</span></span>             | <span data-ttu-id="5cb2e-287">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-287">False</span></span>                           |
| <span data-ttu-id="5cb2e-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5cb2e-288">In Global Catalog</span></span>      | <span data-ttu-id="5cb2e-289">Faux</span><span class="sxs-lookup"><span data-stu-id="5cb2e-289">False</span></span>                           |
| <span data-ttu-id="5cb2e-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5cb2e-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cb2e-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5cb2e-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5cb2e-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cb2e-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cb2e-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5cb2e-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-294">Search-Flags</span></span>           | <span data-ttu-id="5cb2e-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cb2e-295">0x00000000</span></span>                      |
| <span data-ttu-id="5cb2e-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cb2e-296">System-Flags</span></span>           | <span data-ttu-id="5cb2e-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cb2e-297">0x00000010</span></span>                      |
| <span data-ttu-id="5cb2e-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5cb2e-298">Classes used in</span></span>        | [<span data-ttu-id="5cb2e-299">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5cb2e-299">**Top**</span></span>](c-top.md)<br/> |



 

 





