---
title: ms-DS-Cached-Membership-horodatage
description: L’attribut ms-DS-Cached-Membership-Time-Stamp est utilisé par le gestionnaire des comptes de sécurité pour l’extension du groupe lors de l’évaluation du jeton.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut d’horodatage en cache ms-DS-Cached-Membership
- Schéma AD de l’attribut msDS-Cached-Membership-horodatage
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514474"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="ee950-105">ms-DS-Cached-Membership-horodatage</span><span class="sxs-lookup"><span data-stu-id="ee950-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="ee950-106">L’attribut **ms-DS-Cached-Membership-Time-Stamp** est utilisé par le gestionnaire des comptes de sécurité pour l’extension du groupe lors de l’évaluation du jeton.</span><span class="sxs-lookup"><span data-stu-id="ee950-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="ee950-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-107">Entry</span></span> | <span data-ttu-id="ee950-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ee950-109">CN</span><span class="sxs-lookup"><span data-stu-id="ee950-109">CN</span></span>                | <span data-ttu-id="ee950-110">ms-DS-Cached-Membership-horodatage</span><span class="sxs-lookup"><span data-stu-id="ee950-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="ee950-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ee950-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ee950-112">msDS-Cached-Membership-horodatage</span><span class="sxs-lookup"><span data-stu-id="ee950-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="ee950-113">Taille</span><span class="sxs-lookup"><span data-stu-id="ee950-113">Size</span></span>              | <span data-ttu-id="ee950-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="ee950-114">8 bytes</span></span>                              |
| <span data-ttu-id="ee950-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ee950-115">Update Privilege</span></span>  | <span data-ttu-id="ee950-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ee950-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ee950-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ee950-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ee950-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-118">Attribute-Id</span></span>      | <span data-ttu-id="ee950-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="ee950-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="ee950-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ee950-120">System-Id-Guid</span></span>    | <span data-ttu-id="ee950-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="ee950-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="ee950-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee950-122">Syntax</span></span>            | [<span data-ttu-id="ee950-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="ee950-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ee950-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ee950-124">Implementations</span></span>

-   [<span data-ttu-id="ee950-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee950-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee950-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee950-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee950-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee950-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee950-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee950-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee950-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee950-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ee950-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee950-130">Windows Server 2003</span></span>



| <span data-ttu-id="ee950-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-131">Entry</span></span> | <span data-ttu-id="ee950-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee950-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ee950-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee950-135">System-Only</span></span>            | <span data-ttu-id="ee950-136">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-136">False</span></span>                             |
| <span data-ttu-id="ee950-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ee950-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ee950-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-138">True</span></span>                              |
| <span data-ttu-id="ee950-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ee950-139">Is Indexed</span></span>             | <span data-ttu-id="ee950-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-140">True</span></span>                              |
| <span data-ttu-id="ee950-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ee950-141">In Global Catalog</span></span>      | <span data-ttu-id="ee950-142">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-142">False</span></span>                             |
| <span data-ttu-id="ee950-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ee950-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee950-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ee950-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee950-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee950-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee950-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee950-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee950-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-147">Search-Flags</span></span>           | <span data-ttu-id="ee950-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee950-148">0x00000001</span></span>                        |
| <span data-ttu-id="ee950-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-149">System-Flags</span></span>           | <span data-ttu-id="ee950-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ee950-150">0x00000011</span></span>                        |
| <span data-ttu-id="ee950-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ee950-151">Classes used in</span></span>        | [<span data-ttu-id="ee950-152">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee950-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee950-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee950-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee950-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-154">Entry</span></span> | <span data-ttu-id="ee950-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee950-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ee950-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee950-158">System-Only</span></span>            | <span data-ttu-id="ee950-159">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-159">False</span></span>                             |
| <span data-ttu-id="ee950-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ee950-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ee950-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-161">True</span></span>                              |
| <span data-ttu-id="ee950-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ee950-162">Is Indexed</span></span>             | <span data-ttu-id="ee950-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-163">True</span></span>                              |
| <span data-ttu-id="ee950-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ee950-164">In Global Catalog</span></span>      | <span data-ttu-id="ee950-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-165">False</span></span>                             |
| <span data-ttu-id="ee950-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ee950-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee950-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ee950-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee950-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee950-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee950-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee950-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee950-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-170">Search-Flags</span></span>           | <span data-ttu-id="ee950-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee950-171">0x00000001</span></span>                        |
| <span data-ttu-id="ee950-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-172">System-Flags</span></span>           | <span data-ttu-id="ee950-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ee950-173">0x00000011</span></span>                        |
| <span data-ttu-id="ee950-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ee950-174">Classes used in</span></span>        | [<span data-ttu-id="ee950-175">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee950-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee950-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee950-176">Windows Server 2008</span></span>



| <span data-ttu-id="ee950-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-177">Entry</span></span> | <span data-ttu-id="ee950-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee950-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ee950-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee950-181">System-Only</span></span>            | <span data-ttu-id="ee950-182">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-182">False</span></span>                             |
| <span data-ttu-id="ee950-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ee950-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ee950-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-184">True</span></span>                              |
| <span data-ttu-id="ee950-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ee950-185">Is Indexed</span></span>             | <span data-ttu-id="ee950-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-186">True</span></span>                              |
| <span data-ttu-id="ee950-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ee950-187">In Global Catalog</span></span>      | <span data-ttu-id="ee950-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-188">False</span></span>                             |
| <span data-ttu-id="ee950-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ee950-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee950-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ee950-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee950-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee950-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee950-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee950-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee950-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-193">Search-Flags</span></span>           | <span data-ttu-id="ee950-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee950-194">0x00000001</span></span>                        |
| <span data-ttu-id="ee950-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-195">System-Flags</span></span>           | <span data-ttu-id="ee950-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ee950-196">0x00000011</span></span>                        |
| <span data-ttu-id="ee950-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ee950-197">Classes used in</span></span>        | [<span data-ttu-id="ee950-198">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee950-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee950-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee950-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee950-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-200">Entry</span></span> | <span data-ttu-id="ee950-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee950-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ee950-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee950-204">System-Only</span></span>            | <span data-ttu-id="ee950-205">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-205">False</span></span>                             |
| <span data-ttu-id="ee950-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ee950-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ee950-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-207">True</span></span>                              |
| <span data-ttu-id="ee950-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ee950-208">Is Indexed</span></span>             | <span data-ttu-id="ee950-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-209">True</span></span>                              |
| <span data-ttu-id="ee950-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ee950-210">In Global Catalog</span></span>      | <span data-ttu-id="ee950-211">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-211">False</span></span>                             |
| <span data-ttu-id="ee950-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ee950-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee950-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ee950-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee950-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee950-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee950-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee950-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee950-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-216">Search-Flags</span></span>           | <span data-ttu-id="ee950-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee950-217">0x00000001</span></span>                        |
| <span data-ttu-id="ee950-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-218">System-Flags</span></span>           | <span data-ttu-id="ee950-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ee950-219">0x00000011</span></span>                        |
| <span data-ttu-id="ee950-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ee950-220">Classes used in</span></span>        | [<span data-ttu-id="ee950-221">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee950-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee950-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee950-222">Windows Server 2012</span></span>



| <span data-ttu-id="ee950-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="ee950-223">Entry</span></span> | <span data-ttu-id="ee950-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee950-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee950-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ee950-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee950-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee950-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee950-227">System-Only</span></span>            | <span data-ttu-id="ee950-228">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-228">False</span></span>                             |
| <span data-ttu-id="ee950-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ee950-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ee950-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-230">True</span></span>                              |
| <span data-ttu-id="ee950-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ee950-231">Is Indexed</span></span>             | <span data-ttu-id="ee950-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="ee950-232">True</span></span>                              |
| <span data-ttu-id="ee950-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ee950-233">In Global Catalog</span></span>      | <span data-ttu-id="ee950-234">Faux</span><span class="sxs-lookup"><span data-stu-id="ee950-234">False</span></span>                             |
| <span data-ttu-id="ee950-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ee950-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee950-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ee950-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee950-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee950-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee950-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee950-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee950-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-239">Search-Flags</span></span>           | <span data-ttu-id="ee950-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee950-240">0x00000001</span></span>                        |
| <span data-ttu-id="ee950-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee950-241">System-Flags</span></span>           | <span data-ttu-id="ee950-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ee950-242">0x00000011</span></span>                        |
| <span data-ttu-id="ee950-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ee950-243">Classes used in</span></span>        | [<span data-ttu-id="ee950-244">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee950-244">**User**</span></span>](c-user.md)<br/> |



 

 





