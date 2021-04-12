---
title: Attribut is-Critical-System-Object
description: Si la valeur est TRUE, l’objet qui héberge cet attribut doit être répliqué lors de l’installation d’un nouveau réplica.
ms.assetid: 736c8b25-0f82-4b3c-a4fc-4643cd71474e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut is-Critical-System-Object
- Schéma AD de l’attribut isCriticalSystemObject
topic_type:
- apiref
api_name:
- Is-Critical-System-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6030da908fe96a4bea5267872e8bae928a6555e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479677"
---
# <a name="is-critical-system-object-attribute"></a><span data-ttu-id="fda79-105">Attribut is-Critical-System-Object</span><span class="sxs-lookup"><span data-stu-id="fda79-105">Is-Critical-System-Object attribute</span></span>

<span data-ttu-id="fda79-106">Si la **valeur est true**, l’objet qui héberge cet attribut doit être répliqué lors de l’installation d’un nouveau réplica.</span><span class="sxs-lookup"><span data-stu-id="fda79-106">If **TRUE**, the object hosting this attribute must be replicated during installation of a new replica.</span></span>



| <span data-ttu-id="fda79-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-107">Entry</span></span> | <span data-ttu-id="fda79-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fda79-109">CN</span><span class="sxs-lookup"><span data-stu-id="fda79-109">CN</span></span>                | <span data-ttu-id="fda79-110">Is-Critical-System-Object</span><span class="sxs-lookup"><span data-stu-id="fda79-110">Is-Critical-System-Object</span></span>            |
| <span data-ttu-id="fda79-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fda79-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fda79-112">isCriticalSystemObject</span><span class="sxs-lookup"><span data-stu-id="fda79-112">isCriticalSystemObject</span></span>               |
| <span data-ttu-id="fda79-113">Taille</span><span class="sxs-lookup"><span data-stu-id="fda79-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="fda79-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="fda79-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fda79-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="fda79-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fda79-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-116">Attribute-Id</span></span>      | <span data-ttu-id="fda79-117">1.2.840.113556.1.4.868</span><span class="sxs-lookup"><span data-stu-id="fda79-117">1.2.840.113556.1.4.868</span></span>               |
| <span data-ttu-id="fda79-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fda79-118">System-Id-Guid</span></span>    | <span data-ttu-id="fda79-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fda79-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="fda79-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fda79-120">Syntax</span></span>            | [<span data-ttu-id="fda79-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fda79-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fda79-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="fda79-122">Implementations</span></span>

-   [<span data-ttu-id="fda79-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fda79-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fda79-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fda79-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fda79-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fda79-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fda79-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fda79-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fda79-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fda79-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fda79-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fda79-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fda79-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fda79-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fda79-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fda79-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fda79-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-131">Entry</span></span> | <span data-ttu-id="fda79-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-135">System-Only</span></span>            | <span data-ttu-id="fda79-136">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-136">False</span></span>                           |
| <span data-ttu-id="fda79-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-138">True</span></span>                            |
| <span data-ttu-id="fda79-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-139">Is Indexed</span></span>             | <span data-ttu-id="fda79-140">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-140">False</span></span>                           |
| <span data-ttu-id="fda79-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-141">In Global Catalog</span></span>      | <span data-ttu-id="fda79-142">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-142">False</span></span>                           |
| <span data-ttu-id="fda79-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-147">Search-Flags</span></span>           | <span data-ttu-id="fda79-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-148">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-149">System-Flags</span></span>           | <span data-ttu-id="fda79-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-150">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-151">Classes used in</span></span>        | [<span data-ttu-id="fda79-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fda79-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fda79-153">Windows Server 2003</span></span>



| <span data-ttu-id="fda79-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-154">Entry</span></span> | <span data-ttu-id="fda79-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-158">System-Only</span></span>            | <span data-ttu-id="fda79-159">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-159">False</span></span>                           |
| <span data-ttu-id="fda79-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-161">True</span></span>                            |
| <span data-ttu-id="fda79-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-162">Is Indexed</span></span>             | <span data-ttu-id="fda79-163">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-163">False</span></span>                           |
| <span data-ttu-id="fda79-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-164">In Global Catalog</span></span>      | <span data-ttu-id="fda79-165">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-165">False</span></span>                           |
| <span data-ttu-id="fda79-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-170">Search-Flags</span></span>           | <span data-ttu-id="fda79-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-171">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-172">System-Flags</span></span>           | <span data-ttu-id="fda79-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-173">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-174">Classes used in</span></span>        | [<span data-ttu-id="fda79-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fda79-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="fda79-176">ADAM</span></span>



| <span data-ttu-id="fda79-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-177">Entry</span></span> | <span data-ttu-id="fda79-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-181">System-Only</span></span>            | <span data-ttu-id="fda79-182">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-182">False</span></span>                           |
| <span data-ttu-id="fda79-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-184">True</span></span>                            |
| <span data-ttu-id="fda79-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-185">Is Indexed</span></span>             | <span data-ttu-id="fda79-186">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-186">False</span></span>                           |
| <span data-ttu-id="fda79-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-187">In Global Catalog</span></span>      | <span data-ttu-id="fda79-188">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-188">False</span></span>                           |
| <span data-ttu-id="fda79-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-193">Search-Flags</span></span>           | <span data-ttu-id="fda79-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-194">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-195">System-Flags</span></span>           | <span data-ttu-id="fda79-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-196">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-197">Classes used in</span></span>        | [<span data-ttu-id="fda79-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fda79-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fda79-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fda79-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-200">Entry</span></span> | <span data-ttu-id="fda79-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-204">System-Only</span></span>            | <span data-ttu-id="fda79-205">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-205">False</span></span>                           |
| <span data-ttu-id="fda79-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-207">True</span></span>                            |
| <span data-ttu-id="fda79-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-208">Is Indexed</span></span>             | <span data-ttu-id="fda79-209">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-209">False</span></span>                           |
| <span data-ttu-id="fda79-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-210">In Global Catalog</span></span>      | <span data-ttu-id="fda79-211">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-211">False</span></span>                           |
| <span data-ttu-id="fda79-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-216">Search-Flags</span></span>           | <span data-ttu-id="fda79-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-217">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-218">System-Flags</span></span>           | <span data-ttu-id="fda79-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-219">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-220">Classes used in</span></span>        | [<span data-ttu-id="fda79-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fda79-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fda79-222">Windows Server 2008</span></span>



| <span data-ttu-id="fda79-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-223">Entry</span></span> | <span data-ttu-id="fda79-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-227">System-Only</span></span>            | <span data-ttu-id="fda79-228">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-228">False</span></span>                           |
| <span data-ttu-id="fda79-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-230">True</span></span>                            |
| <span data-ttu-id="fda79-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-231">Is Indexed</span></span>             | <span data-ttu-id="fda79-232">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-232">False</span></span>                           |
| <span data-ttu-id="fda79-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-233">In Global Catalog</span></span>      | <span data-ttu-id="fda79-234">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-234">False</span></span>                           |
| <span data-ttu-id="fda79-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-239">Search-Flags</span></span>           | <span data-ttu-id="fda79-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-240">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-241">System-Flags</span></span>           | <span data-ttu-id="fda79-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-242">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-243">Classes used in</span></span>        | [<span data-ttu-id="fda79-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fda79-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fda79-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fda79-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-246">Entry</span></span> | <span data-ttu-id="fda79-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-250">System-Only</span></span>            | <span data-ttu-id="fda79-251">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-251">False</span></span>                           |
| <span data-ttu-id="fda79-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-253">True</span></span>                            |
| <span data-ttu-id="fda79-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-254">Is Indexed</span></span>             | <span data-ttu-id="fda79-255">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-255">False</span></span>                           |
| <span data-ttu-id="fda79-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-256">In Global Catalog</span></span>      | <span data-ttu-id="fda79-257">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-257">False</span></span>                           |
| <span data-ttu-id="fda79-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-262">Search-Flags</span></span>           | <span data-ttu-id="fda79-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-263">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-264">System-Flags</span></span>           | <span data-ttu-id="fda79-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-265">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-266">Classes used in</span></span>        | [<span data-ttu-id="fda79-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fda79-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fda79-268">Windows Server 2012</span></span>



| <span data-ttu-id="fda79-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="fda79-269">Entry</span></span> | <span data-ttu-id="fda79-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda79-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fda79-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fda79-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda79-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fda79-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda79-273">System-Only</span></span>            | <span data-ttu-id="fda79-274">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-274">False</span></span>                           |
| <span data-ttu-id="fda79-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fda79-275">Is-Single-Valued</span></span>       | <span data-ttu-id="fda79-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="fda79-276">True</span></span>                            |
| <span data-ttu-id="fda79-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fda79-277">Is Indexed</span></span>             | <span data-ttu-id="fda79-278">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-278">False</span></span>                           |
| <span data-ttu-id="fda79-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fda79-279">In Global Catalog</span></span>      | <span data-ttu-id="fda79-280">Faux</span><span class="sxs-lookup"><span data-stu-id="fda79-280">False</span></span>                           |
| <span data-ttu-id="fda79-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fda79-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda79-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fda79-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fda79-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda79-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fda79-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda79-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fda79-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-285">Search-Flags</span></span>           | <span data-ttu-id="fda79-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda79-286">0x00000000</span></span>                      |
| <span data-ttu-id="fda79-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda79-287">System-Flags</span></span>           | <span data-ttu-id="fda79-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda79-288">0x00000010</span></span>                      |
| <span data-ttu-id="fda79-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fda79-289">Classes used in</span></span>        | [<span data-ttu-id="fda79-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="fda79-290">**Top**</span></span>](c-top.md)<br/> |



 

 





