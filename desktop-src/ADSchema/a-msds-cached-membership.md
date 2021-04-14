---
title: attribut d’appartenance en cache ms-DS
description: L’attribut ms-DS-Cached-membership est utilisé par le gestionnaire des comptes de sécurité pour l’extension du groupe lors de l’évaluation du jeton.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut d’appartenance en cache ms-DS
- Schéma AD d’attribut d’appartenance en cache msDS
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520177"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="61d85-105">attribut d’appartenance en cache ms-DS</span><span class="sxs-lookup"><span data-stu-id="61d85-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="61d85-106">L’attribut **ms-DS-Cached-Membership** est utilisé par le gestionnaire des comptes de sécurité pour l’extension du groupe lors de l’évaluation du jeton.</span><span class="sxs-lookup"><span data-stu-id="61d85-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="61d85-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-107">Entry</span></span> | <span data-ttu-id="61d85-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="61d85-109">CN</span><span class="sxs-lookup"><span data-stu-id="61d85-109">CN</span></span>                | <span data-ttu-id="61d85-110">ms-DS-mis en cache-appartenance</span><span class="sxs-lookup"><span data-stu-id="61d85-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="61d85-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="61d85-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61d85-112">msDS-Cached-Membership</span><span class="sxs-lookup"><span data-stu-id="61d85-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="61d85-113">Taille</span><span class="sxs-lookup"><span data-stu-id="61d85-113">Size</span></span>              | <span data-ttu-id="61d85-114">BLOB binaire pouvant atteindre jusqu’à 3 kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="61d85-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="61d85-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="61d85-115">Update Privilege</span></span>  | <span data-ttu-id="61d85-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="61d85-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="61d85-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="61d85-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="61d85-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-118">Attribute-Id</span></span>      | <span data-ttu-id="61d85-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="61d85-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="61d85-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="61d85-120">System-Id-Guid</span></span>    | <span data-ttu-id="61d85-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="61d85-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="61d85-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61d85-122">Syntax</span></span>            | [<span data-ttu-id="61d85-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="61d85-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="61d85-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="61d85-124">Implementations</span></span>

-   [<span data-ttu-id="61d85-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61d85-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61d85-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61d85-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61d85-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61d85-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61d85-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61d85-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61d85-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61d85-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="61d85-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61d85-130">Windows Server 2003</span></span>



| <span data-ttu-id="61d85-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-131">Entry</span></span> | <span data-ttu-id="61d85-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61d85-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61d85-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="61d85-135">System-Only</span></span>            | <span data-ttu-id="61d85-136">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-136">False</span></span>                             |
| <span data-ttu-id="61d85-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61d85-137">Is-Single-Valued</span></span>       | <span data-ttu-id="61d85-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="61d85-138">True</span></span>                              |
| <span data-ttu-id="61d85-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61d85-139">Is Indexed</span></span>             | <span data-ttu-id="61d85-140">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-140">False</span></span>                             |
| <span data-ttu-id="61d85-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61d85-141">In Global Catalog</span></span>      | <span data-ttu-id="61d85-142">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-142">False</span></span>                             |
| <span data-ttu-id="61d85-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61d85-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="61d85-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61d85-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61d85-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61d85-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="61d85-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61d85-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="61d85-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-147">Search-Flags</span></span>           | <span data-ttu-id="61d85-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d85-148">0x00000000</span></span>                        |
| <span data-ttu-id="61d85-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-149">System-Flags</span></span>           | <span data-ttu-id="61d85-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="61d85-150">0x00000011</span></span>                        |
| <span data-ttu-id="61d85-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61d85-151">Classes used in</span></span>        | [<span data-ttu-id="61d85-152">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="61d85-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61d85-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61d85-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61d85-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-154">Entry</span></span> | <span data-ttu-id="61d85-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61d85-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61d85-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="61d85-158">System-Only</span></span>            | <span data-ttu-id="61d85-159">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-159">False</span></span>                             |
| <span data-ttu-id="61d85-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61d85-160">Is-Single-Valued</span></span>       | <span data-ttu-id="61d85-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="61d85-161">True</span></span>                              |
| <span data-ttu-id="61d85-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61d85-162">Is Indexed</span></span>             | <span data-ttu-id="61d85-163">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-163">False</span></span>                             |
| <span data-ttu-id="61d85-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61d85-164">In Global Catalog</span></span>      | <span data-ttu-id="61d85-165">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-165">False</span></span>                             |
| <span data-ttu-id="61d85-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61d85-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="61d85-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61d85-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61d85-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61d85-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="61d85-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61d85-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="61d85-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-170">Search-Flags</span></span>           | <span data-ttu-id="61d85-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d85-171">0x00000000</span></span>                        |
| <span data-ttu-id="61d85-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-172">System-Flags</span></span>           | <span data-ttu-id="61d85-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="61d85-173">0x00000011</span></span>                        |
| <span data-ttu-id="61d85-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61d85-174">Classes used in</span></span>        | [<span data-ttu-id="61d85-175">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="61d85-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61d85-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61d85-176">Windows Server 2008</span></span>



| <span data-ttu-id="61d85-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-177">Entry</span></span> | <span data-ttu-id="61d85-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61d85-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61d85-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="61d85-181">System-Only</span></span>            | <span data-ttu-id="61d85-182">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-182">False</span></span>                             |
| <span data-ttu-id="61d85-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61d85-183">Is-Single-Valued</span></span>       | <span data-ttu-id="61d85-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="61d85-184">True</span></span>                              |
| <span data-ttu-id="61d85-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61d85-185">Is Indexed</span></span>             | <span data-ttu-id="61d85-186">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-186">False</span></span>                             |
| <span data-ttu-id="61d85-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61d85-187">In Global Catalog</span></span>      | <span data-ttu-id="61d85-188">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-188">False</span></span>                             |
| <span data-ttu-id="61d85-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61d85-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="61d85-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61d85-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61d85-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61d85-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="61d85-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61d85-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="61d85-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-193">Search-Flags</span></span>           | <span data-ttu-id="61d85-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d85-194">0x00000000</span></span>                        |
| <span data-ttu-id="61d85-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-195">System-Flags</span></span>           | <span data-ttu-id="61d85-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="61d85-196">0x00000011</span></span>                        |
| <span data-ttu-id="61d85-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61d85-197">Classes used in</span></span>        | [<span data-ttu-id="61d85-198">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="61d85-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61d85-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61d85-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61d85-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-200">Entry</span></span> | <span data-ttu-id="61d85-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61d85-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61d85-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="61d85-204">System-Only</span></span>            | <span data-ttu-id="61d85-205">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-205">False</span></span>                             |
| <span data-ttu-id="61d85-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61d85-206">Is-Single-Valued</span></span>       | <span data-ttu-id="61d85-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="61d85-207">True</span></span>                              |
| <span data-ttu-id="61d85-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61d85-208">Is Indexed</span></span>             | <span data-ttu-id="61d85-209">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-209">False</span></span>                             |
| <span data-ttu-id="61d85-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61d85-210">In Global Catalog</span></span>      | <span data-ttu-id="61d85-211">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-211">False</span></span>                             |
| <span data-ttu-id="61d85-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61d85-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="61d85-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61d85-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61d85-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61d85-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="61d85-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61d85-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="61d85-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-216">Search-Flags</span></span>           | <span data-ttu-id="61d85-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d85-217">0x00000000</span></span>                        |
| <span data-ttu-id="61d85-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-218">System-Flags</span></span>           | <span data-ttu-id="61d85-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="61d85-219">0x00000011</span></span>                        |
| <span data-ttu-id="61d85-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61d85-220">Classes used in</span></span>        | [<span data-ttu-id="61d85-221">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="61d85-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61d85-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61d85-222">Windows Server 2012</span></span>



| <span data-ttu-id="61d85-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="61d85-223">Entry</span></span> | <span data-ttu-id="61d85-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="61d85-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61d85-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61d85-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61d85-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61d85-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="61d85-227">System-Only</span></span>            | <span data-ttu-id="61d85-228">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-228">False</span></span>                             |
| <span data-ttu-id="61d85-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61d85-229">Is-Single-Valued</span></span>       | <span data-ttu-id="61d85-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="61d85-230">True</span></span>                              |
| <span data-ttu-id="61d85-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61d85-231">Is Indexed</span></span>             | <span data-ttu-id="61d85-232">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-232">False</span></span>                             |
| <span data-ttu-id="61d85-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61d85-233">In Global Catalog</span></span>      | <span data-ttu-id="61d85-234">Faux</span><span class="sxs-lookup"><span data-stu-id="61d85-234">False</span></span>                             |
| <span data-ttu-id="61d85-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61d85-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="61d85-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61d85-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61d85-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61d85-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="61d85-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61d85-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="61d85-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-239">Search-Flags</span></span>           | <span data-ttu-id="61d85-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d85-240">0x00000000</span></span>                        |
| <span data-ttu-id="61d85-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61d85-241">System-Flags</span></span>           | <span data-ttu-id="61d85-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="61d85-242">0x00000011</span></span>                        |
| <span data-ttu-id="61d85-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61d85-243">Classes used in</span></span>        | [<span data-ttu-id="61d85-244">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="61d85-244">**User**</span></span>](c-user.md)<br/> |



 

 





