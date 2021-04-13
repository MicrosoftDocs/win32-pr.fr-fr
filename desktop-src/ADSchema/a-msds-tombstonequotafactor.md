---
title: attribut de facteur de quota ms-DS-Tombstone
description: Facteur de pourcentage par lequel le nombre d’objets tombstone doit être réduit dans le cadre de la gestion des quotas.
ms.assetid: 602c2fe0-d3b7-45e8-8ce8-35a7163f7b25
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-Tombstone-quota-Factor Attribute
- Schéma Active Directory de l’attribut msDS-TombstoneQuotaFactor
topic_type:
- apiref
api_name:
- ms-DS-Tombstone-Quota-Factor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a44dd7f648754c2ded7334c9b221022d936ebfb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519801"
---
# <a name="ms-ds-tombstone-quota-factor-attribute"></a><span data-ttu-id="be481-105">attribut de facteur de quota ms-DS-Tombstone</span><span class="sxs-lookup"><span data-stu-id="be481-105">ms-DS-Tombstone-Quota-Factor attribute</span></span>

<span data-ttu-id="be481-106">Facteur de pourcentage par lequel le nombre d’objets tombstone doit être réduit dans le cadre de la gestion des quotas.</span><span class="sxs-lookup"><span data-stu-id="be481-106">The percentage factor by which the tombstone object count should be reduced for the purpose of quota accounting.</span></span>



| <span data-ttu-id="be481-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-107">Entry</span></span> | <span data-ttu-id="be481-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="be481-109">CN</span><span class="sxs-lookup"><span data-stu-id="be481-109">CN</span></span>                | <span data-ttu-id="be481-110">ms-DS-Tombstone-quota-Factor</span><span class="sxs-lookup"><span data-stu-id="be481-110">ms-DS-Tombstone-Quota-Factor</span></span>         |
| <span data-ttu-id="be481-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="be481-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be481-112">msDS-TombstoneQuotaFactor</span><span class="sxs-lookup"><span data-stu-id="be481-112">msDS-TombstoneQuotaFactor</span></span>            |
| <span data-ttu-id="be481-113">Taille</span><span class="sxs-lookup"><span data-stu-id="be481-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="be481-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="be481-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="be481-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="be481-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="be481-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be481-116">Attribute-Id</span></span>      | <span data-ttu-id="be481-117">1.2.840.113556.1.4.1847</span><span class="sxs-lookup"><span data-stu-id="be481-117">1.2.840.113556.1.4.1847</span></span>              |
| <span data-ttu-id="be481-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="be481-118">System-Id-Guid</span></span>    | <span data-ttu-id="be481-119">461744d7-F3B6-45ba-8753-fb9552a5df32</span><span class="sxs-lookup"><span data-stu-id="be481-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span></span> |
| <span data-ttu-id="be481-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be481-120">Syntax</span></span>            | [<span data-ttu-id="be481-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="be481-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="be481-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="be481-122">Implementations</span></span>

-   [<span data-ttu-id="be481-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be481-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be481-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="be481-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="be481-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be481-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be481-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be481-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be481-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be481-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be481-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be481-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="be481-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be481-129">Windows Server 2003</span></span>



| <span data-ttu-id="be481-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-130">Entry</span></span> | <span data-ttu-id="be481-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-134">System-Only</span></span>            | <span data-ttu-id="be481-135">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-135">False</span></span>                                                             |
| <span data-ttu-id="be481-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-136">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-137">True</span></span>                                                              |
| <span data-ttu-id="be481-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-138">Is Indexed</span></span>             | <span data-ttu-id="be481-139">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-139">False</span></span>                                                             |
| <span data-ttu-id="be481-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-140">In Global Catalog</span></span>      | <span data-ttu-id="be481-141">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-141">False</span></span>                                                             |
| <span data-ttu-id="be481-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-144">Range-Lower</span></span>            | <span data-ttu-id="be481-145">0</span><span class="sxs-lookup"><span data-stu-id="be481-145">0</span></span>                                                                 |
| <span data-ttu-id="be481-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-146">Range-Upper</span></span>            | <span data-ttu-id="be481-147">100</span><span class="sxs-lookup"><span data-stu-id="be481-147">100</span></span>                                                               |
| <span data-ttu-id="be481-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-148">Search-Flags</span></span>           | <span data-ttu-id="be481-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-150">System-Flags</span></span>           | <span data-ttu-id="be481-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-152">Classes used in</span></span>        | [<span data-ttu-id="be481-153">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="be481-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="be481-154">ADAM</span></span>



| <span data-ttu-id="be481-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-155">Entry</span></span> | <span data-ttu-id="be481-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-159">System-Only</span></span>            | <span data-ttu-id="be481-160">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-160">False</span></span>                                                             |
| <span data-ttu-id="be481-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-161">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-162">True</span></span>                                                              |
| <span data-ttu-id="be481-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-163">Is Indexed</span></span>             | <span data-ttu-id="be481-164">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-164">False</span></span>                                                             |
| <span data-ttu-id="be481-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-165">In Global Catalog</span></span>      | <span data-ttu-id="be481-166">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-166">False</span></span>                                                             |
| <span data-ttu-id="be481-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-169">Range-Lower</span></span>            | <span data-ttu-id="be481-170">0</span><span class="sxs-lookup"><span data-stu-id="be481-170">0</span></span>                                                                 |
| <span data-ttu-id="be481-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-171">Range-Upper</span></span>            | <span data-ttu-id="be481-172">100</span><span class="sxs-lookup"><span data-stu-id="be481-172">100</span></span>                                                               |
| <span data-ttu-id="be481-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-173">Search-Flags</span></span>           | <span data-ttu-id="be481-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-175">System-Flags</span></span>           | <span data-ttu-id="be481-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-177">Classes used in</span></span>        | [<span data-ttu-id="be481-178">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-178">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be481-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be481-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be481-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-180">Entry</span></span> | <span data-ttu-id="be481-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-184">System-Only</span></span>            | <span data-ttu-id="be481-185">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-185">False</span></span>                                                             |
| <span data-ttu-id="be481-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-186">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-187">True</span></span>                                                              |
| <span data-ttu-id="be481-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-188">Is Indexed</span></span>             | <span data-ttu-id="be481-189">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-189">False</span></span>                                                             |
| <span data-ttu-id="be481-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-190">In Global Catalog</span></span>      | <span data-ttu-id="be481-191">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-191">False</span></span>                                                             |
| <span data-ttu-id="be481-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-194">Range-Lower</span></span>            | <span data-ttu-id="be481-195">0</span><span class="sxs-lookup"><span data-stu-id="be481-195">0</span></span>                                                                 |
| <span data-ttu-id="be481-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-196">Range-Upper</span></span>            | <span data-ttu-id="be481-197">100</span><span class="sxs-lookup"><span data-stu-id="be481-197">100</span></span>                                                               |
| <span data-ttu-id="be481-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-198">Search-Flags</span></span>           | <span data-ttu-id="be481-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-200">System-Flags</span></span>           | <span data-ttu-id="be481-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-202">Classes used in</span></span>        | [<span data-ttu-id="be481-203">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-203">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be481-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be481-204">Windows Server 2008</span></span>



| <span data-ttu-id="be481-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-205">Entry</span></span> | <span data-ttu-id="be481-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-209">System-Only</span></span>            | <span data-ttu-id="be481-210">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-210">False</span></span>                                                             |
| <span data-ttu-id="be481-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-211">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-212">True</span></span>                                                              |
| <span data-ttu-id="be481-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-213">Is Indexed</span></span>             | <span data-ttu-id="be481-214">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-214">False</span></span>                                                             |
| <span data-ttu-id="be481-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-215">In Global Catalog</span></span>      | <span data-ttu-id="be481-216">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-216">False</span></span>                                                             |
| <span data-ttu-id="be481-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-219">Range-Lower</span></span>            | <span data-ttu-id="be481-220">0</span><span class="sxs-lookup"><span data-stu-id="be481-220">0</span></span>                                                                 |
| <span data-ttu-id="be481-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-221">Range-Upper</span></span>            | <span data-ttu-id="be481-222">100</span><span class="sxs-lookup"><span data-stu-id="be481-222">100</span></span>                                                               |
| <span data-ttu-id="be481-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-223">Search-Flags</span></span>           | <span data-ttu-id="be481-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-225">System-Flags</span></span>           | <span data-ttu-id="be481-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-227">Classes used in</span></span>        | [<span data-ttu-id="be481-228">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-228">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be481-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be481-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be481-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-230">Entry</span></span> | <span data-ttu-id="be481-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-234">System-Only</span></span>            | <span data-ttu-id="be481-235">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-235">False</span></span>                                                             |
| <span data-ttu-id="be481-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-236">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-237">True</span></span>                                                              |
| <span data-ttu-id="be481-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-238">Is Indexed</span></span>             | <span data-ttu-id="be481-239">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-239">False</span></span>                                                             |
| <span data-ttu-id="be481-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-240">In Global Catalog</span></span>      | <span data-ttu-id="be481-241">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-241">False</span></span>                                                             |
| <span data-ttu-id="be481-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-244">Range-Lower</span></span>            | <span data-ttu-id="be481-245">0</span><span class="sxs-lookup"><span data-stu-id="be481-245">0</span></span>                                                                 |
| <span data-ttu-id="be481-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-246">Range-Upper</span></span>            | <span data-ttu-id="be481-247">100</span><span class="sxs-lookup"><span data-stu-id="be481-247">100</span></span>                                                               |
| <span data-ttu-id="be481-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-248">Search-Flags</span></span>           | <span data-ttu-id="be481-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-250">System-Flags</span></span>           | <span data-ttu-id="be481-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-252">Classes used in</span></span>        | [<span data-ttu-id="be481-253">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-253">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be481-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be481-254">Windows Server 2012</span></span>



| <span data-ttu-id="be481-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="be481-255">Entry</span></span> | <span data-ttu-id="be481-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="be481-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="be481-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="be481-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be481-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="be481-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="be481-259">System-Only</span></span>            | <span data-ttu-id="be481-260">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-260">False</span></span>                                                             |
| <span data-ttu-id="be481-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="be481-261">Is-Single-Valued</span></span>       | <span data-ttu-id="be481-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="be481-262">True</span></span>                                                              |
| <span data-ttu-id="be481-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="be481-263">Is Indexed</span></span>             | <span data-ttu-id="be481-264">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-264">False</span></span>                                                             |
| <span data-ttu-id="be481-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="be481-265">In Global Catalog</span></span>      | <span data-ttu-id="be481-266">Faux</span><span class="sxs-lookup"><span data-stu-id="be481-266">False</span></span>                                                             |
| <span data-ttu-id="be481-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="be481-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="be481-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="be481-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="be481-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be481-269">Range-Lower</span></span>            | <span data-ttu-id="be481-270">0</span><span class="sxs-lookup"><span data-stu-id="be481-270">0</span></span>                                                                 |
| <span data-ttu-id="be481-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be481-271">Range-Upper</span></span>            | <span data-ttu-id="be481-272">100</span><span class="sxs-lookup"><span data-stu-id="be481-272">100</span></span>                                                               |
| <span data-ttu-id="be481-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-273">Search-Flags</span></span>           | <span data-ttu-id="be481-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be481-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="be481-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be481-275">System-Flags</span></span>           | <span data-ttu-id="be481-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be481-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="be481-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="be481-277">Classes used in</span></span>        | [<span data-ttu-id="be481-278">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="be481-278">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





