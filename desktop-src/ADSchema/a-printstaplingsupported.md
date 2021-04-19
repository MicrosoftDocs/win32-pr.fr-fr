---
title: Print-agrafeuse-attribut pris en charge
description: TRUE si l’imprimante prend en charge l’agrafage. Fourni par le pilote.
ms.assetid: c0d1cbc5-7657-45a8-b154-a67f57386f52
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour l’Association d’impression-attribut pris en charge
- Schéma AD de l’attribut printStaplingSupported
topic_type:
- apiref
api_name:
- Print-Stapling-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12303d9a18f267ec4eaef3a33dc8ec7350967aa6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516302"
---
# <a name="print-stapling-supported-attribute"></a><span data-ttu-id="31caa-106">Print-agrafeuse-attribut pris en charge</span><span class="sxs-lookup"><span data-stu-id="31caa-106">Print-Stapling-Supported attribute</span></span>

<span data-ttu-id="31caa-107">**True** si l’imprimante prend en charge l’agrafage.</span><span class="sxs-lookup"><span data-stu-id="31caa-107">**TRUE** if the printer supports stapling.</span></span> <span data-ttu-id="31caa-108">Fourni par le pilote.</span><span class="sxs-lookup"><span data-stu-id="31caa-108">Supplied by the driver.</span></span>



| <span data-ttu-id="31caa-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-109">Entry</span></span> | <span data-ttu-id="31caa-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="31caa-111">CN</span><span class="sxs-lookup"><span data-stu-id="31caa-111">CN</span></span>                | <span data-ttu-id="31caa-112">Impression-agrafage-pris en charge</span><span class="sxs-lookup"><span data-stu-id="31caa-112">Print-Stapling-Supported</span></span>             |
| <span data-ttu-id="31caa-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="31caa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="31caa-114">printStaplingSupported</span><span class="sxs-lookup"><span data-stu-id="31caa-114">printStaplingSupported</span></span>               |
| <span data-ttu-id="31caa-115">Taille</span><span class="sxs-lookup"><span data-stu-id="31caa-115">Size</span></span>              | <span data-ttu-id="31caa-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="31caa-116">4 bytes</span></span>                              |
| <span data-ttu-id="31caa-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="31caa-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="31caa-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="31caa-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="31caa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-119">Attribute-Id</span></span>      | <span data-ttu-id="31caa-120">1.2.840.113556.1.4.281</span><span class="sxs-lookup"><span data-stu-id="31caa-120">1.2.840.113556.1.4.281</span></span>               |
| <span data-ttu-id="31caa-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="31caa-121">System-Id-Guid</span></span>    | <span data-ttu-id="31caa-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="31caa-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="31caa-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31caa-123">Syntax</span></span>            | [<span data-ttu-id="31caa-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="31caa-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="31caa-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="31caa-125">Implementations</span></span>

-   [<span data-ttu-id="31caa-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="31caa-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="31caa-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="31caa-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="31caa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="31caa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="31caa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="31caa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="31caa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="31caa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="31caa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="31caa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="31caa-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31caa-132">Windows 2000 Server</span></span>



| <span data-ttu-id="31caa-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-133">Entry</span></span> | <span data-ttu-id="31caa-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-137">System-Only</span></span>            | <span data-ttu-id="31caa-138">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-138">False</span></span>                                          |
| <span data-ttu-id="31caa-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-140">True</span></span>                                           |
| <span data-ttu-id="31caa-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-141">Is Indexed</span></span>             | <span data-ttu-id="31caa-142">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-142">False</span></span>                                          |
| <span data-ttu-id="31caa-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-143">In Global Catalog</span></span>      | <span data-ttu-id="31caa-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-144">True</span></span>                                           |
| <span data-ttu-id="31caa-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-149">Search-Flags</span></span>           | <span data-ttu-id="31caa-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-150">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-151">System-Flags</span></span>           | <span data-ttu-id="31caa-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-152">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-153">Classes used in</span></span>        | [<span data-ttu-id="31caa-154">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="31caa-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31caa-155">Windows Server 2003</span></span>



| <span data-ttu-id="31caa-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-156">Entry</span></span> | <span data-ttu-id="31caa-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-160">System-Only</span></span>            | <span data-ttu-id="31caa-161">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-161">False</span></span>                                          |
| <span data-ttu-id="31caa-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-163">True</span></span>                                           |
| <span data-ttu-id="31caa-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-164">Is Indexed</span></span>             | <span data-ttu-id="31caa-165">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-165">False</span></span>                                          |
| <span data-ttu-id="31caa-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-166">In Global Catalog</span></span>      | <span data-ttu-id="31caa-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-167">True</span></span>                                           |
| <span data-ttu-id="31caa-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-172">Search-Flags</span></span>           | <span data-ttu-id="31caa-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-173">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-174">System-Flags</span></span>           | <span data-ttu-id="31caa-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-175">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-176">Classes used in</span></span>        | [<span data-ttu-id="31caa-177">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="31caa-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="31caa-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="31caa-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-179">Entry</span></span> | <span data-ttu-id="31caa-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-183">System-Only</span></span>            | <span data-ttu-id="31caa-184">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-184">False</span></span>                                          |
| <span data-ttu-id="31caa-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-185">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-186">True</span></span>                                           |
| <span data-ttu-id="31caa-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-187">Is Indexed</span></span>             | <span data-ttu-id="31caa-188">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-188">False</span></span>                                          |
| <span data-ttu-id="31caa-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-189">In Global Catalog</span></span>      | <span data-ttu-id="31caa-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-190">True</span></span>                                           |
| <span data-ttu-id="31caa-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-195">Search-Flags</span></span>           | <span data-ttu-id="31caa-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-196">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-197">System-Flags</span></span>           | <span data-ttu-id="31caa-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-198">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-199">Classes used in</span></span>        | [<span data-ttu-id="31caa-200">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="31caa-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31caa-201">Windows Server 2008</span></span>



| <span data-ttu-id="31caa-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-202">Entry</span></span> | <span data-ttu-id="31caa-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-206">System-Only</span></span>            | <span data-ttu-id="31caa-207">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-207">False</span></span>                                          |
| <span data-ttu-id="31caa-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-208">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-209">True</span></span>                                           |
| <span data-ttu-id="31caa-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-210">Is Indexed</span></span>             | <span data-ttu-id="31caa-211">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-211">False</span></span>                                          |
| <span data-ttu-id="31caa-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-212">In Global Catalog</span></span>      | <span data-ttu-id="31caa-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-213">True</span></span>                                           |
| <span data-ttu-id="31caa-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-218">Search-Flags</span></span>           | <span data-ttu-id="31caa-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-219">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-220">System-Flags</span></span>           | <span data-ttu-id="31caa-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-221">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-222">Classes used in</span></span>        | [<span data-ttu-id="31caa-223">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="31caa-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31caa-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="31caa-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-225">Entry</span></span> | <span data-ttu-id="31caa-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-229">System-Only</span></span>            | <span data-ttu-id="31caa-230">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-230">False</span></span>                                          |
| <span data-ttu-id="31caa-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-231">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-232">True</span></span>                                           |
| <span data-ttu-id="31caa-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-233">Is Indexed</span></span>             | <span data-ttu-id="31caa-234">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-234">False</span></span>                                          |
| <span data-ttu-id="31caa-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-235">In Global Catalog</span></span>      | <span data-ttu-id="31caa-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-236">True</span></span>                                           |
| <span data-ttu-id="31caa-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-241">Search-Flags</span></span>           | <span data-ttu-id="31caa-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-242">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-243">System-Flags</span></span>           | <span data-ttu-id="31caa-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-244">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-245">Classes used in</span></span>        | [<span data-ttu-id="31caa-246">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="31caa-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31caa-247">Windows Server 2012</span></span>



| <span data-ttu-id="31caa-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="31caa-248">Entry</span></span> | <span data-ttu-id="31caa-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="31caa-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="31caa-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="31caa-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31caa-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="31caa-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="31caa-252">System-Only</span></span>            | <span data-ttu-id="31caa-253">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-253">False</span></span>                                          |
| <span data-ttu-id="31caa-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="31caa-254">Is-Single-Valued</span></span>       | <span data-ttu-id="31caa-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-255">True</span></span>                                           |
| <span data-ttu-id="31caa-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="31caa-256">Is Indexed</span></span>             | <span data-ttu-id="31caa-257">Faux</span><span class="sxs-lookup"><span data-stu-id="31caa-257">False</span></span>                                          |
| <span data-ttu-id="31caa-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="31caa-258">In Global Catalog</span></span>      | <span data-ttu-id="31caa-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="31caa-259">True</span></span>                                           |
| <span data-ttu-id="31caa-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="31caa-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="31caa-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="31caa-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="31caa-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31caa-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="31caa-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31caa-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="31caa-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-264">Search-Flags</span></span>           | <span data-ttu-id="31caa-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31caa-265">0x00000000</span></span>                                     |
| <span data-ttu-id="31caa-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31caa-266">System-Flags</span></span>           | <span data-ttu-id="31caa-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31caa-267">0x00000010</span></span>                                     |
| <span data-ttu-id="31caa-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="31caa-268">Classes used in</span></span>        | [<span data-ttu-id="31caa-269">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="31caa-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





