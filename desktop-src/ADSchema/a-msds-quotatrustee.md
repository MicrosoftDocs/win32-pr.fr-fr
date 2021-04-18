---
title: attribut ms-DS-quota-tiers de confiance
description: SID du principal de sécurité pour lequel le quota est affecté.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-quota-tiers de confiance
- Schéma Active Directory de l’attribut msDS-QuotaTrustee
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106519156"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="9c690-105">attribut ms-DS-quota-tiers de confiance</span><span class="sxs-lookup"><span data-stu-id="9c690-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="9c690-106">SID du principal de sécurité pour lequel le quota est affecté.</span><span class="sxs-lookup"><span data-stu-id="9c690-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="9c690-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-107">Entry</span></span> | <span data-ttu-id="9c690-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9c690-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c690-109">CN</span></span>                | <span data-ttu-id="9c690-110">ms-DS-quota-tiers de confiance</span><span class="sxs-lookup"><span data-stu-id="9c690-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="9c690-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c690-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9c690-112">msDS-QuotaTrustee</span><span class="sxs-lookup"><span data-stu-id="9c690-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="9c690-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9c690-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9c690-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9c690-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9c690-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9c690-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9c690-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-116">Attribute-Id</span></span>      | <span data-ttu-id="9c690-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="9c690-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="9c690-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9c690-118">System-Id-Guid</span></span>    | <span data-ttu-id="9c690-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="9c690-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="9c690-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c690-120">Syntax</span></span>            | [<span data-ttu-id="9c690-121">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="9c690-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="9c690-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9c690-122">Implementations</span></span>

-   [<span data-ttu-id="9c690-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c690-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c690-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9c690-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9c690-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c690-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c690-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c690-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c690-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c690-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c690-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c690-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9c690-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c690-129">Windows Server 2003</span></span>



| <span data-ttu-id="9c690-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-130">Entry</span></span> | <span data-ttu-id="9c690-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-134">System-Only</span></span>            | <span data-ttu-id="9c690-135">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-135">False</span></span>                                                         |
| <span data-ttu-id="9c690-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-137">True</span></span>                                                          |
| <span data-ttu-id="9c690-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-138">Is Indexed</span></span>             | <span data-ttu-id="9c690-139">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-139">False</span></span>                                                         |
| <span data-ttu-id="9c690-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-140">In Global Catalog</span></span>      | <span data-ttu-id="9c690-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-141">False</span></span>                                                         |
| <span data-ttu-id="9c690-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-144">Range-Lower</span></span>            | <span data-ttu-id="9c690-145">0</span><span class="sxs-lookup"><span data-stu-id="9c690-145">0</span></span>                                                             |
| <span data-ttu-id="9c690-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-146">Range-Upper</span></span>            | <span data-ttu-id="9c690-147">28</span><span class="sxs-lookup"><span data-stu-id="9c690-147">28</span></span>                                                            |
| <span data-ttu-id="9c690-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-148">Search-Flags</span></span>           | <span data-ttu-id="9c690-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-150">System-Flags</span></span>           | <span data-ttu-id="9c690-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-152">Classes used in</span></span>        | [<span data-ttu-id="9c690-153">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9c690-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="9c690-154">ADAM</span></span>



| <span data-ttu-id="9c690-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-155">Entry</span></span> | <span data-ttu-id="9c690-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-159">System-Only</span></span>            | <span data-ttu-id="9c690-160">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-160">False</span></span>                                                         |
| <span data-ttu-id="9c690-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-162">True</span></span>                                                          |
| <span data-ttu-id="9c690-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-163">Is Indexed</span></span>             | <span data-ttu-id="9c690-164">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-164">False</span></span>                                                         |
| <span data-ttu-id="9c690-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-165">In Global Catalog</span></span>      | <span data-ttu-id="9c690-166">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-166">False</span></span>                                                         |
| <span data-ttu-id="9c690-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-169">Range-Lower</span></span>            | <span data-ttu-id="9c690-170">0</span><span class="sxs-lookup"><span data-stu-id="9c690-170">0</span></span>                                                             |
| <span data-ttu-id="9c690-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-171">Range-Upper</span></span>            | <span data-ttu-id="9c690-172">28</span><span class="sxs-lookup"><span data-stu-id="9c690-172">28</span></span>                                                            |
| <span data-ttu-id="9c690-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-173">Search-Flags</span></span>           | <span data-ttu-id="9c690-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-175">System-Flags</span></span>           | <span data-ttu-id="9c690-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-177">Classes used in</span></span>        | [<span data-ttu-id="9c690-178">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c690-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c690-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c690-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-180">Entry</span></span> | <span data-ttu-id="9c690-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-184">System-Only</span></span>            | <span data-ttu-id="9c690-185">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-185">False</span></span>                                                         |
| <span data-ttu-id="9c690-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-187">True</span></span>                                                          |
| <span data-ttu-id="9c690-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-188">Is Indexed</span></span>             | <span data-ttu-id="9c690-189">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-189">False</span></span>                                                         |
| <span data-ttu-id="9c690-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-190">In Global Catalog</span></span>      | <span data-ttu-id="9c690-191">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-191">False</span></span>                                                         |
| <span data-ttu-id="9c690-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-194">Range-Lower</span></span>            | <span data-ttu-id="9c690-195">0</span><span class="sxs-lookup"><span data-stu-id="9c690-195">0</span></span>                                                             |
| <span data-ttu-id="9c690-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-196">Range-Upper</span></span>            | <span data-ttu-id="9c690-197">28</span><span class="sxs-lookup"><span data-stu-id="9c690-197">28</span></span>                                                            |
| <span data-ttu-id="9c690-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-198">Search-Flags</span></span>           | <span data-ttu-id="9c690-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-200">System-Flags</span></span>           | <span data-ttu-id="9c690-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-202">Classes used in</span></span>        | [<span data-ttu-id="9c690-203">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9c690-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c690-204">Windows Server 2008</span></span>



| <span data-ttu-id="9c690-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-205">Entry</span></span> | <span data-ttu-id="9c690-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-209">System-Only</span></span>            | <span data-ttu-id="9c690-210">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-210">False</span></span>                                                         |
| <span data-ttu-id="9c690-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-212">True</span></span>                                                          |
| <span data-ttu-id="9c690-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-213">Is Indexed</span></span>             | <span data-ttu-id="9c690-214">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-214">False</span></span>                                                         |
| <span data-ttu-id="9c690-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-215">In Global Catalog</span></span>      | <span data-ttu-id="9c690-216">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-216">False</span></span>                                                         |
| <span data-ttu-id="9c690-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-219">Range-Lower</span></span>            | <span data-ttu-id="9c690-220">0</span><span class="sxs-lookup"><span data-stu-id="9c690-220">0</span></span>                                                             |
| <span data-ttu-id="9c690-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-221">Range-Upper</span></span>            | <span data-ttu-id="9c690-222">28</span><span class="sxs-lookup"><span data-stu-id="9c690-222">28</span></span>                                                            |
| <span data-ttu-id="9c690-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-223">Search-Flags</span></span>           | <span data-ttu-id="9c690-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-225">System-Flags</span></span>           | <span data-ttu-id="9c690-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-227">Classes used in</span></span>        | [<span data-ttu-id="9c690-228">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c690-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c690-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c690-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-230">Entry</span></span> | <span data-ttu-id="9c690-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-234">System-Only</span></span>            | <span data-ttu-id="9c690-235">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-235">False</span></span>                                                         |
| <span data-ttu-id="9c690-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-237">True</span></span>                                                          |
| <span data-ttu-id="9c690-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-238">Is Indexed</span></span>             | <span data-ttu-id="9c690-239">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-239">False</span></span>                                                         |
| <span data-ttu-id="9c690-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-240">In Global Catalog</span></span>      | <span data-ttu-id="9c690-241">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-241">False</span></span>                                                         |
| <span data-ttu-id="9c690-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-244">Range-Lower</span></span>            | <span data-ttu-id="9c690-245">0</span><span class="sxs-lookup"><span data-stu-id="9c690-245">0</span></span>                                                             |
| <span data-ttu-id="9c690-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-246">Range-Upper</span></span>            | <span data-ttu-id="9c690-247">28</span><span class="sxs-lookup"><span data-stu-id="9c690-247">28</span></span>                                                            |
| <span data-ttu-id="9c690-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-248">Search-Flags</span></span>           | <span data-ttu-id="9c690-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-250">System-Flags</span></span>           | <span data-ttu-id="9c690-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-252">Classes used in</span></span>        | [<span data-ttu-id="9c690-253">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9c690-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c690-254">Windows Server 2012</span></span>



| <span data-ttu-id="9c690-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="9c690-255">Entry</span></span> | <span data-ttu-id="9c690-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c690-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c690-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9c690-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c690-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9c690-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c690-259">System-Only</span></span>            | <span data-ttu-id="9c690-260">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-260">False</span></span>                                                         |
| <span data-ttu-id="9c690-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9c690-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9c690-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="9c690-262">True</span></span>                                                          |
| <span data-ttu-id="9c690-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9c690-263">Is Indexed</span></span>             | <span data-ttu-id="9c690-264">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-264">False</span></span>                                                         |
| <span data-ttu-id="9c690-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9c690-265">In Global Catalog</span></span>      | <span data-ttu-id="9c690-266">Faux</span><span class="sxs-lookup"><span data-stu-id="9c690-266">False</span></span>                                                         |
| <span data-ttu-id="9c690-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9c690-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c690-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9c690-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9c690-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c690-269">Range-Lower</span></span>            | <span data-ttu-id="9c690-270">0</span><span class="sxs-lookup"><span data-stu-id="9c690-270">0</span></span>                                                             |
| <span data-ttu-id="9c690-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c690-271">Range-Upper</span></span>            | <span data-ttu-id="9c690-272">28</span><span class="sxs-lookup"><span data-stu-id="9c690-272">28</span></span>                                                            |
| <span data-ttu-id="9c690-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-273">Search-Flags</span></span>           | <span data-ttu-id="9c690-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c690-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="9c690-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c690-275">System-Flags</span></span>           | <span data-ttu-id="9c690-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c690-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="9c690-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9c690-277">Classes used in</span></span>        | [<span data-ttu-id="9c690-278">**ms-DS-quota-Control**</span><span class="sxs-lookup"><span data-stu-id="9c690-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





