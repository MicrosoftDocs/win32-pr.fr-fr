---
title: ms-DS-attribut quota-effectif
description: Quota effectif pour un principal de sécurité calculé à partir des quotas attribués pour une partition d’annuaire.
ms.assetid: 22422499-9b56-4d74-a30e-63917abacdd1
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de quota effectif de ms-DS
- Schéma Active Directory de l’attribut msDS-QuotaEffective
topic_type:
- apiref
api_name:
- ms-DS-Quota-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe610c87c356431883cecded5eda3e0a9c42297
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480364"
---
# <a name="ms-ds-quota-effective-attribute"></a><span data-ttu-id="941ac-105">ms-DS-attribut quota-effectif</span><span class="sxs-lookup"><span data-stu-id="941ac-105">ms-DS-Quota-Effective attribute</span></span>

<span data-ttu-id="941ac-106">Quota effectif pour un principal de sécurité calculé à partir des quotas attribués pour une partition d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="941ac-106">The effective quota for a security principal computed from the assigned quotas for a directory partition.</span></span>



| <span data-ttu-id="941ac-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-107">Entry</span></span> | <span data-ttu-id="941ac-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="941ac-109">CN</span><span class="sxs-lookup"><span data-stu-id="941ac-109">CN</span></span>                | <span data-ttu-id="941ac-110">ms-DS-quota-effectif</span><span class="sxs-lookup"><span data-stu-id="941ac-110">ms-DS-Quota-Effective</span></span>                |
| <span data-ttu-id="941ac-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="941ac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="941ac-112">msDS-QuotaEffective</span><span class="sxs-lookup"><span data-stu-id="941ac-112">msDS-QuotaEffective</span></span>                  |
| <span data-ttu-id="941ac-113">Taille</span><span class="sxs-lookup"><span data-stu-id="941ac-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="941ac-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="941ac-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="941ac-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="941ac-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="941ac-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-116">Attribute-Id</span></span>      | <span data-ttu-id="941ac-117">1.2.840.113556.1.4.1848</span><span class="sxs-lookup"><span data-stu-id="941ac-117">1.2.840.113556.1.4.1848</span></span>              |
| <span data-ttu-id="941ac-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="941ac-118">System-Id-Guid</span></span>    | <span data-ttu-id="941ac-119">6655b152-101c-48b4-b347-e1fcebc60157</span><span class="sxs-lookup"><span data-stu-id="941ac-119">6655b152-101c-48b4-b347-e1fcebc60157</span></span> |
| <span data-ttu-id="941ac-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="941ac-120">Syntax</span></span>            | [<span data-ttu-id="941ac-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="941ac-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="941ac-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="941ac-122">Implementations</span></span>

-   [<span data-ttu-id="941ac-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="941ac-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="941ac-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="941ac-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="941ac-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="941ac-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="941ac-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="941ac-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="941ac-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="941ac-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="941ac-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="941ac-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="941ac-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="941ac-129">Windows Server 2003</span></span>



| <span data-ttu-id="941ac-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-130">Entry</span></span> | <span data-ttu-id="941ac-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-134">System-Only</span></span>            | <span data-ttu-id="941ac-135">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-135">False</span></span>                                                             |
| <span data-ttu-id="941ac-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-136">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-137">True</span></span>                                                              |
| <span data-ttu-id="941ac-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-138">Is Indexed</span></span>             | <span data-ttu-id="941ac-139">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-139">False</span></span>                                                             |
| <span data-ttu-id="941ac-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-140">In Global Catalog</span></span>      | <span data-ttu-id="941ac-141">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-141">False</span></span>                                                             |
| <span data-ttu-id="941ac-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-146">Search-Flags</span></span>           | <span data-ttu-id="941ac-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-148">System-Flags</span></span>           | <span data-ttu-id="941ac-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-150">Classes used in</span></span>        | [<span data-ttu-id="941ac-151">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="941ac-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="941ac-152">ADAM</span></span>



| <span data-ttu-id="941ac-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-153">Entry</span></span> | <span data-ttu-id="941ac-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-157">System-Only</span></span>            | <span data-ttu-id="941ac-158">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-158">False</span></span>                                                             |
| <span data-ttu-id="941ac-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-159">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-160">True</span></span>                                                              |
| <span data-ttu-id="941ac-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-161">Is Indexed</span></span>             | <span data-ttu-id="941ac-162">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-162">False</span></span>                                                             |
| <span data-ttu-id="941ac-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-163">In Global Catalog</span></span>      | <span data-ttu-id="941ac-164">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-164">False</span></span>                                                             |
| <span data-ttu-id="941ac-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-169">Search-Flags</span></span>           | <span data-ttu-id="941ac-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-171">System-Flags</span></span>           | <span data-ttu-id="941ac-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-173">Classes used in</span></span>        | [<span data-ttu-id="941ac-174">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="941ac-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="941ac-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="941ac-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-176">Entry</span></span> | <span data-ttu-id="941ac-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-180">System-Only</span></span>            | <span data-ttu-id="941ac-181">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-181">False</span></span>                                                             |
| <span data-ttu-id="941ac-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-182">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-183">True</span></span>                                                              |
| <span data-ttu-id="941ac-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-184">Is Indexed</span></span>             | <span data-ttu-id="941ac-185">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-185">False</span></span>                                                             |
| <span data-ttu-id="941ac-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-186">In Global Catalog</span></span>      | <span data-ttu-id="941ac-187">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-187">False</span></span>                                                             |
| <span data-ttu-id="941ac-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-192">Search-Flags</span></span>           | <span data-ttu-id="941ac-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-194">System-Flags</span></span>           | <span data-ttu-id="941ac-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-196">Classes used in</span></span>        | [<span data-ttu-id="941ac-197">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="941ac-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="941ac-198">Windows Server 2008</span></span>



| <span data-ttu-id="941ac-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-199">Entry</span></span> | <span data-ttu-id="941ac-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-203">System-Only</span></span>            | <span data-ttu-id="941ac-204">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-204">False</span></span>                                                             |
| <span data-ttu-id="941ac-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-205">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-206">True</span></span>                                                              |
| <span data-ttu-id="941ac-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-207">Is Indexed</span></span>             | <span data-ttu-id="941ac-208">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-208">False</span></span>                                                             |
| <span data-ttu-id="941ac-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-209">In Global Catalog</span></span>      | <span data-ttu-id="941ac-210">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-210">False</span></span>                                                             |
| <span data-ttu-id="941ac-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-215">Search-Flags</span></span>           | <span data-ttu-id="941ac-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-217">System-Flags</span></span>           | <span data-ttu-id="941ac-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-219">Classes used in</span></span>        | [<span data-ttu-id="941ac-220">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="941ac-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="941ac-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="941ac-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-222">Entry</span></span> | <span data-ttu-id="941ac-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-226">System-Only</span></span>            | <span data-ttu-id="941ac-227">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-227">False</span></span>                                                             |
| <span data-ttu-id="941ac-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-228">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-229">True</span></span>                                                              |
| <span data-ttu-id="941ac-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-230">Is Indexed</span></span>             | <span data-ttu-id="941ac-231">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-231">False</span></span>                                                             |
| <span data-ttu-id="941ac-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-232">In Global Catalog</span></span>      | <span data-ttu-id="941ac-233">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-233">False</span></span>                                                             |
| <span data-ttu-id="941ac-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-238">Search-Flags</span></span>           | <span data-ttu-id="941ac-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-240">System-Flags</span></span>           | <span data-ttu-id="941ac-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-242">Classes used in</span></span>        | [<span data-ttu-id="941ac-243">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="941ac-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="941ac-244">Windows Server 2012</span></span>



| <span data-ttu-id="941ac-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="941ac-245">Entry</span></span> | <span data-ttu-id="941ac-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="941ac-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="941ac-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="941ac-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="941ac-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="941ac-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="941ac-249">System-Only</span></span>            | <span data-ttu-id="941ac-250">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-250">False</span></span>                                                             |
| <span data-ttu-id="941ac-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="941ac-251">Is-Single-Valued</span></span>       | <span data-ttu-id="941ac-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="941ac-252">True</span></span>                                                              |
| <span data-ttu-id="941ac-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="941ac-253">Is Indexed</span></span>             | <span data-ttu-id="941ac-254">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-254">False</span></span>                                                             |
| <span data-ttu-id="941ac-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="941ac-255">In Global Catalog</span></span>      | <span data-ttu-id="941ac-256">Faux</span><span class="sxs-lookup"><span data-stu-id="941ac-256">False</span></span>                                                             |
| <span data-ttu-id="941ac-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="941ac-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="941ac-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="941ac-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="941ac-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="941ac-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="941ac-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="941ac-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-261">Search-Flags</span></span>           | <span data-ttu-id="941ac-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="941ac-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="941ac-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="941ac-263">System-Flags</span></span>           | <span data-ttu-id="941ac-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="941ac-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="941ac-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="941ac-265">Classes used in</span></span>        | [<span data-ttu-id="941ac-266">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="941ac-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





