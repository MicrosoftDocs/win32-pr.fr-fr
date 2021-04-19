---
title: MS-DS-par-utilisateur-confiance-Tombstone-attribut de quota
description: Utilisé pour appliquer un quota par utilisateur pour la suppression d’objets Trusted-Domain lorsque l’autorisation est basée sur la mise en correspondance du SID de l’utilisateur.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- MS-DS-per-utilisateur-Trust-Tombstone-Tombstone-attribut de quota AD (schéma)
- Schéma Active Directory de l’attribut msDS-PerUserTrustTombstonesQuota
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106517351"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="b5390-105">MS-DS-par-utilisateur-confiance-Tombstone-attribut de quota</span><span class="sxs-lookup"><span data-stu-id="b5390-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="b5390-106">Utilisé pour appliquer un quota par utilisateur pour la suppression d’objets Trusted-Domain lorsque l’autorisation est basée sur la mise en correspondance du SID de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5390-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="b5390-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-107">Entry</span></span> | <span data-ttu-id="b5390-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="b5390-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5390-109">CN</span></span>                | <span data-ttu-id="b5390-110">MS-DS-par-utilisateur-confiance-désactivation tombstone-quota</span><span class="sxs-lookup"><span data-stu-id="b5390-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="b5390-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b5390-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5390-112">msDS-PerUserTrustTombstonesQuota</span><span class="sxs-lookup"><span data-stu-id="b5390-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="b5390-113">Taille</span><span class="sxs-lookup"><span data-stu-id="b5390-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="b5390-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b5390-114">Update Privilege</span></span>  | <span data-ttu-id="b5390-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="b5390-115">Domain administrator</span></span>                      |
| <span data-ttu-id="b5390-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b5390-116">Update Frequency</span></span>  | <span data-ttu-id="b5390-117">À la création de la forêt et rarement après cela.</span><span class="sxs-lookup"><span data-stu-id="b5390-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="b5390-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-118">Attribute-Id</span></span>      | <span data-ttu-id="b5390-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="b5390-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="b5390-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5390-120">System-Id-Guid</span></span>    | <span data-ttu-id="b5390-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="b5390-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="b5390-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5390-122">Syntax</span></span>            | [<span data-ttu-id="b5390-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="b5390-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="b5390-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b5390-124">Implementations</span></span>

-   [<span data-ttu-id="b5390-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5390-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5390-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5390-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5390-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5390-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5390-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5390-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5390-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5390-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b5390-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5390-130">Windows Server 2003</span></span>



| <span data-ttu-id="b5390-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-131">Entry</span></span> | <span data-ttu-id="b5390-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b5390-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b5390-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5390-135">System-Only</span></span>            | <span data-ttu-id="b5390-136">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-136">False</span></span>                                        |
| <span data-ttu-id="b5390-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b5390-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b5390-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="b5390-138">True</span></span>                                         |
| <span data-ttu-id="b5390-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b5390-139">Is Indexed</span></span>             | <span data-ttu-id="b5390-140">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-140">False</span></span>                                        |
| <span data-ttu-id="b5390-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b5390-141">In Global Catalog</span></span>      | <span data-ttu-id="b5390-142">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-142">False</span></span>                                        |
| <span data-ttu-id="b5390-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b5390-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5390-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b5390-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b5390-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5390-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b5390-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5390-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b5390-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-147">Search-Flags</span></span>           | <span data-ttu-id="b5390-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5390-148">0x00000000</span></span>                                   |
| <span data-ttu-id="b5390-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-149">System-Flags</span></span>           | <span data-ttu-id="b5390-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5390-150">0x00000010</span></span>                                   |
| <span data-ttu-id="b5390-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b5390-151">Classes used in</span></span>        | [<span data-ttu-id="b5390-152">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="b5390-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5390-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5390-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5390-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-154">Entry</span></span> | <span data-ttu-id="b5390-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b5390-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b5390-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5390-158">System-Only</span></span>            | <span data-ttu-id="b5390-159">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-159">False</span></span>                                        |
| <span data-ttu-id="b5390-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b5390-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b5390-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="b5390-161">True</span></span>                                         |
| <span data-ttu-id="b5390-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b5390-162">Is Indexed</span></span>             | <span data-ttu-id="b5390-163">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-163">False</span></span>                                        |
| <span data-ttu-id="b5390-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b5390-164">In Global Catalog</span></span>      | <span data-ttu-id="b5390-165">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-165">False</span></span>                                        |
| <span data-ttu-id="b5390-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b5390-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5390-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b5390-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b5390-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5390-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b5390-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5390-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b5390-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-170">Search-Flags</span></span>           | <span data-ttu-id="b5390-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5390-171">0x00000000</span></span>                                   |
| <span data-ttu-id="b5390-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-172">System-Flags</span></span>           | <span data-ttu-id="b5390-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5390-173">0x00000010</span></span>                                   |
| <span data-ttu-id="b5390-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b5390-174">Classes used in</span></span>        | [<span data-ttu-id="b5390-175">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="b5390-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5390-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5390-176">Windows Server 2008</span></span>



| <span data-ttu-id="b5390-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-177">Entry</span></span> | <span data-ttu-id="b5390-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b5390-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b5390-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5390-181">System-Only</span></span>            | <span data-ttu-id="b5390-182">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-182">False</span></span>                                        |
| <span data-ttu-id="b5390-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b5390-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b5390-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="b5390-184">True</span></span>                                         |
| <span data-ttu-id="b5390-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b5390-185">Is Indexed</span></span>             | <span data-ttu-id="b5390-186">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-186">False</span></span>                                        |
| <span data-ttu-id="b5390-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b5390-187">In Global Catalog</span></span>      | <span data-ttu-id="b5390-188">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-188">False</span></span>                                        |
| <span data-ttu-id="b5390-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b5390-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5390-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b5390-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b5390-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5390-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b5390-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5390-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b5390-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-193">Search-Flags</span></span>           | <span data-ttu-id="b5390-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5390-194">0x00000000</span></span>                                   |
| <span data-ttu-id="b5390-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-195">System-Flags</span></span>           | <span data-ttu-id="b5390-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5390-196">0x00000010</span></span>                                   |
| <span data-ttu-id="b5390-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b5390-197">Classes used in</span></span>        | [<span data-ttu-id="b5390-198">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="b5390-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5390-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5390-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5390-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-200">Entry</span></span> | <span data-ttu-id="b5390-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b5390-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b5390-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5390-204">System-Only</span></span>            | <span data-ttu-id="b5390-205">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-205">False</span></span>                                        |
| <span data-ttu-id="b5390-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b5390-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b5390-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="b5390-207">True</span></span>                                         |
| <span data-ttu-id="b5390-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b5390-208">Is Indexed</span></span>             | <span data-ttu-id="b5390-209">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-209">False</span></span>                                        |
| <span data-ttu-id="b5390-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b5390-210">In Global Catalog</span></span>      | <span data-ttu-id="b5390-211">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-211">False</span></span>                                        |
| <span data-ttu-id="b5390-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b5390-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5390-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b5390-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b5390-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5390-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b5390-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5390-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b5390-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-216">Search-Flags</span></span>           | <span data-ttu-id="b5390-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5390-217">0x00000000</span></span>                                   |
| <span data-ttu-id="b5390-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-218">System-Flags</span></span>           | <span data-ttu-id="b5390-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5390-219">0x00000010</span></span>                                   |
| <span data-ttu-id="b5390-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b5390-220">Classes used in</span></span>        | [<span data-ttu-id="b5390-221">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="b5390-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5390-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5390-222">Windows Server 2012</span></span>



| <span data-ttu-id="b5390-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="b5390-223">Entry</span></span> | <span data-ttu-id="b5390-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5390-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b5390-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b5390-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5390-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b5390-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5390-227">System-Only</span></span>            | <span data-ttu-id="b5390-228">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-228">False</span></span>                                        |
| <span data-ttu-id="b5390-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b5390-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b5390-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="b5390-230">True</span></span>                                         |
| <span data-ttu-id="b5390-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b5390-231">Is Indexed</span></span>             | <span data-ttu-id="b5390-232">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-232">False</span></span>                                        |
| <span data-ttu-id="b5390-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b5390-233">In Global Catalog</span></span>      | <span data-ttu-id="b5390-234">Faux</span><span class="sxs-lookup"><span data-stu-id="b5390-234">False</span></span>                                        |
| <span data-ttu-id="b5390-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b5390-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5390-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b5390-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b5390-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5390-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b5390-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5390-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b5390-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-239">Search-Flags</span></span>           | <span data-ttu-id="b5390-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5390-240">0x00000000</span></span>                                   |
| <span data-ttu-id="b5390-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5390-241">System-Flags</span></span>           | <span data-ttu-id="b5390-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5390-242">0x00000010</span></span>                                   |
| <span data-ttu-id="b5390-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b5390-243">Classes used in</span></span>        | [<span data-ttu-id="b5390-244">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="b5390-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





