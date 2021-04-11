---
title: ACS-attribut de taille de jeton non réservé
description: L’attribut ACS-non-reserved-Token-Size est destiné à un usage interne uniquement.
ms.assetid: 50c11f5f-2188-43ab-9d40-094ca8a3d526
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ACS-non-reserved-Token-Size
- Schéma AD de l’attribut aCSNonReservedTokenSize
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Token-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90351a660cfbeafbcd468edb1e6eca8c589b5d72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108307"
---
# <a name="acs-non-reserved-token-size-attribute"></a><span data-ttu-id="76885-105">ACS-attribut de taille de jeton non réservé</span><span class="sxs-lookup"><span data-stu-id="76885-105">ACS-Non-Reserved-Token-Size attribute</span></span>

<span data-ttu-id="76885-106">L’attribut **ACS-non-reserved-Token-Size** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="76885-106">The **ACS-Non-Reserved-Token-Size** attribute is for internal use only.</span></span> <span data-ttu-id="76885-107">Basé sur RFC2814.</span><span class="sxs-lookup"><span data-stu-id="76885-107">Based on RFC2814.</span></span>



| <span data-ttu-id="76885-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-108">Entry</span></span> | <span data-ttu-id="76885-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="76885-110">CN</span><span class="sxs-lookup"><span data-stu-id="76885-110">CN</span></span>                | <span data-ttu-id="76885-111">ACS-non-réservé-Token-Size</span><span class="sxs-lookup"><span data-stu-id="76885-111">ACS-Non-Reserved-Token-Size</span></span>          |
| <span data-ttu-id="76885-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="76885-112">Ldap-Display-Name</span></span> | <span data-ttu-id="76885-113">aCSNonReservedTokenSize</span><span class="sxs-lookup"><span data-stu-id="76885-113">aCSNonReservedTokenSize</span></span>              |
| <span data-ttu-id="76885-114">Taille</span><span class="sxs-lookup"><span data-stu-id="76885-114">Size</span></span>              | <span data-ttu-id="76885-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="76885-115">8 bytes</span></span>                              |
| <span data-ttu-id="76885-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="76885-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="76885-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="76885-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="76885-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76885-118">Attribute-Id</span></span>      | <span data-ttu-id="76885-119">1.2.840.113556.1.4.1319</span><span class="sxs-lookup"><span data-stu-id="76885-119">1.2.840.113556.1.4.1319</span></span>              |
| <span data-ttu-id="76885-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="76885-120">System-Id-Guid</span></span>    | <span data-ttu-id="76885-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="76885-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="76885-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76885-122">Syntax</span></span>            | [<span data-ttu-id="76885-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="76885-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="76885-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="76885-124">Implementations</span></span>

-   [<span data-ttu-id="76885-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="76885-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="76885-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76885-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76885-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76885-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76885-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76885-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76885-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76885-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76885-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76885-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="76885-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76885-131">Windows 2000 Server</span></span>



| <span data-ttu-id="76885-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-132">Entry</span></span> | <span data-ttu-id="76885-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-136">System-Only</span></span>            | <span data-ttu-id="76885-137">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-137">False</span></span>                                        |
| <span data-ttu-id="76885-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-138">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-139">True</span></span>                                         |
| <span data-ttu-id="76885-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-140">Is Indexed</span></span>             | <span data-ttu-id="76885-141">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-141">False</span></span>                                        |
| <span data-ttu-id="76885-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-142">In Global Catalog</span></span>      | <span data-ttu-id="76885-143">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-143">False</span></span>                                        |
| <span data-ttu-id="76885-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-148">Search-Flags</span></span>           | <span data-ttu-id="76885-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-149">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-150">System-Flags</span></span>           | <span data-ttu-id="76885-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-151">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-152">Classes used in</span></span>        | [<span data-ttu-id="76885-153">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="76885-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76885-154">Windows Server 2003</span></span>



| <span data-ttu-id="76885-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-155">Entry</span></span> | <span data-ttu-id="76885-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-159">System-Only</span></span>            | <span data-ttu-id="76885-160">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-160">False</span></span>                                        |
| <span data-ttu-id="76885-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-161">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-162">True</span></span>                                         |
| <span data-ttu-id="76885-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-163">Is Indexed</span></span>             | <span data-ttu-id="76885-164">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-164">False</span></span>                                        |
| <span data-ttu-id="76885-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-165">In Global Catalog</span></span>      | <span data-ttu-id="76885-166">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-166">False</span></span>                                        |
| <span data-ttu-id="76885-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-171">Search-Flags</span></span>           | <span data-ttu-id="76885-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-172">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-173">System-Flags</span></span>           | <span data-ttu-id="76885-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-174">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-175">Classes used in</span></span>        | [<span data-ttu-id="76885-176">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76885-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76885-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76885-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-178">Entry</span></span> | <span data-ttu-id="76885-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-182">System-Only</span></span>            | <span data-ttu-id="76885-183">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-183">False</span></span>                                        |
| <span data-ttu-id="76885-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-184">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-185">True</span></span>                                         |
| <span data-ttu-id="76885-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-186">Is Indexed</span></span>             | <span data-ttu-id="76885-187">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-187">False</span></span>                                        |
| <span data-ttu-id="76885-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-188">In Global Catalog</span></span>      | <span data-ttu-id="76885-189">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-189">False</span></span>                                        |
| <span data-ttu-id="76885-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-194">Search-Flags</span></span>           | <span data-ttu-id="76885-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-195">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-196">System-Flags</span></span>           | <span data-ttu-id="76885-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-197">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-198">Classes used in</span></span>        | [<span data-ttu-id="76885-199">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76885-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76885-200">Windows Server 2008</span></span>



| <span data-ttu-id="76885-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-201">Entry</span></span> | <span data-ttu-id="76885-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-205">System-Only</span></span>            | <span data-ttu-id="76885-206">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-206">False</span></span>                                        |
| <span data-ttu-id="76885-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-207">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-208">True</span></span>                                         |
| <span data-ttu-id="76885-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-209">Is Indexed</span></span>             | <span data-ttu-id="76885-210">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-210">False</span></span>                                        |
| <span data-ttu-id="76885-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-211">In Global Catalog</span></span>      | <span data-ttu-id="76885-212">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-212">False</span></span>                                        |
| <span data-ttu-id="76885-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-217">Search-Flags</span></span>           | <span data-ttu-id="76885-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-218">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-219">System-Flags</span></span>           | <span data-ttu-id="76885-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-220">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-221">Classes used in</span></span>        | [<span data-ttu-id="76885-222">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76885-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76885-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76885-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-224">Entry</span></span> | <span data-ttu-id="76885-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-228">System-Only</span></span>            | <span data-ttu-id="76885-229">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-229">False</span></span>                                        |
| <span data-ttu-id="76885-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-230">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-231">True</span></span>                                         |
| <span data-ttu-id="76885-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-232">Is Indexed</span></span>             | <span data-ttu-id="76885-233">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-233">False</span></span>                                        |
| <span data-ttu-id="76885-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-234">In Global Catalog</span></span>      | <span data-ttu-id="76885-235">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-235">False</span></span>                                        |
| <span data-ttu-id="76885-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-240">Search-Flags</span></span>           | <span data-ttu-id="76885-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-241">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-242">System-Flags</span></span>           | <span data-ttu-id="76885-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-243">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-244">Classes used in</span></span>        | [<span data-ttu-id="76885-245">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76885-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76885-246">Windows Server 2012</span></span>



| <span data-ttu-id="76885-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="76885-247">Entry</span></span> | <span data-ttu-id="76885-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="76885-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="76885-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76885-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76885-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="76885-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="76885-251">System-Only</span></span>            | <span data-ttu-id="76885-252">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-252">False</span></span>                                        |
| <span data-ttu-id="76885-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76885-253">Is-Single-Valued</span></span>       | <span data-ttu-id="76885-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="76885-254">True</span></span>                                         |
| <span data-ttu-id="76885-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76885-255">Is Indexed</span></span>             | <span data-ttu-id="76885-256">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-256">False</span></span>                                        |
| <span data-ttu-id="76885-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76885-257">In Global Catalog</span></span>      | <span data-ttu-id="76885-258">Faux</span><span class="sxs-lookup"><span data-stu-id="76885-258">False</span></span>                                        |
| <span data-ttu-id="76885-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76885-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="76885-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76885-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="76885-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76885-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="76885-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76885-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="76885-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-263">Search-Flags</span></span>           | <span data-ttu-id="76885-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76885-264">0x00000000</span></span>                                   |
| <span data-ttu-id="76885-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76885-265">System-Flags</span></span>           | <span data-ttu-id="76885-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76885-266">0x00000010</span></span>                                   |
| <span data-ttu-id="76885-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76885-267">Classes used in</span></span>        | [<span data-ttu-id="76885-268">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="76885-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





