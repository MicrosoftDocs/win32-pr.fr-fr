---
title: ms-DS-site-attribut Affinity
description: L’attribut ms-DS-site-Affinity est utilisé par le gestionnaire de comptes de sécurité pour l’extension de groupe lors de l’évaluation du jeton.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-site-Affinity
- Schéma AD de l’attribut msDS-site-Affinity
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845453"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="67944-105">ms-DS-site-attribut Affinity</span><span class="sxs-lookup"><span data-stu-id="67944-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="67944-106">L’attribut **ms-DS-site-Affinity** est utilisé par le gestionnaire de comptes de sécurité pour l’extension de groupe lors de l’évaluation du jeton.</span><span class="sxs-lookup"><span data-stu-id="67944-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="67944-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-107">Entry</span></span> | <span data-ttu-id="67944-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67944-109">CN</span><span class="sxs-lookup"><span data-stu-id="67944-109">CN</span></span>                | <span data-ttu-id="67944-110">ms-DS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="67944-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="67944-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="67944-111">Ldap-Display-Name</span></span> | <span data-ttu-id="67944-112">msDS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="67944-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="67944-113">Taille</span><span class="sxs-lookup"><span data-stu-id="67944-113">Size</span></span>              | <span data-ttu-id="67944-114">Objet BLOB binaire à valeurs multiples, où chaque valeur est sizeof (GUID) + sizeof ( \_ entier long).</span><span class="sxs-lookup"><span data-stu-id="67944-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="67944-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="67944-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="67944-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="67944-116">Update Frequency</span></span>  | <span data-ttu-id="67944-117">Par défaut, une fois tous les trois mois.</span><span class="sxs-lookup"><span data-stu-id="67944-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="67944-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="67944-118">Attribute-Id</span></span>      | <span data-ttu-id="67944-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="67944-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="67944-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="67944-120">System-Id-Guid</span></span>    | <span data-ttu-id="67944-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="67944-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="67944-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67944-122">Syntax</span></span>            | [<span data-ttu-id="67944-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="67944-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="67944-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="67944-124">Implementations</span></span>

-   [<span data-ttu-id="67944-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="67944-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="67944-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="67944-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="67944-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="67944-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="67944-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="67944-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="67944-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="67944-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="67944-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67944-130">Windows Server 2003</span></span>



| <span data-ttu-id="67944-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-131">Entry</span></span> | <span data-ttu-id="67944-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67944-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="67944-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67944-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="67944-135">System-Only</span></span>            | <span data-ttu-id="67944-136">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-136">False</span></span>                             |
| <span data-ttu-id="67944-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="67944-137">Is-Single-Valued</span></span>       | <span data-ttu-id="67944-138">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-138">False</span></span>                             |
| <span data-ttu-id="67944-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="67944-139">Is Indexed</span></span>             | <span data-ttu-id="67944-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="67944-140">True</span></span>                              |
| <span data-ttu-id="67944-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="67944-141">In Global Catalog</span></span>      | <span data-ttu-id="67944-142">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-142">False</span></span>                             |
| <span data-ttu-id="67944-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="67944-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="67944-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="67944-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67944-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67944-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67944-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67944-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67944-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-147">Search-Flags</span></span>           | <span data-ttu-id="67944-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="67944-148">0x00000001</span></span>                        |
| <span data-ttu-id="67944-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-149">System-Flags</span></span>           | <span data-ttu-id="67944-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67944-150">0x00000010</span></span>                        |
| <span data-ttu-id="67944-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="67944-151">Classes used in</span></span>        | [<span data-ttu-id="67944-152">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="67944-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="67944-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="67944-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="67944-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-154">Entry</span></span> | <span data-ttu-id="67944-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67944-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="67944-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67944-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="67944-158">System-Only</span></span>            | <span data-ttu-id="67944-159">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-159">False</span></span>                             |
| <span data-ttu-id="67944-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="67944-160">Is-Single-Valued</span></span>       | <span data-ttu-id="67944-161">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-161">False</span></span>                             |
| <span data-ttu-id="67944-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="67944-162">Is Indexed</span></span>             | <span data-ttu-id="67944-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="67944-163">True</span></span>                              |
| <span data-ttu-id="67944-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="67944-164">In Global Catalog</span></span>      | <span data-ttu-id="67944-165">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-165">False</span></span>                             |
| <span data-ttu-id="67944-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="67944-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="67944-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="67944-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67944-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67944-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67944-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67944-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67944-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-170">Search-Flags</span></span>           | <span data-ttu-id="67944-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="67944-171">0x00000001</span></span>                        |
| <span data-ttu-id="67944-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-172">System-Flags</span></span>           | <span data-ttu-id="67944-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67944-173">0x00000010</span></span>                        |
| <span data-ttu-id="67944-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="67944-174">Classes used in</span></span>        | [<span data-ttu-id="67944-175">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="67944-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="67944-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67944-176">Windows Server 2008</span></span>



| <span data-ttu-id="67944-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-177">Entry</span></span> | <span data-ttu-id="67944-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67944-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="67944-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67944-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="67944-181">System-Only</span></span>            | <span data-ttu-id="67944-182">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-182">False</span></span>                             |
| <span data-ttu-id="67944-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="67944-183">Is-Single-Valued</span></span>       | <span data-ttu-id="67944-184">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-184">False</span></span>                             |
| <span data-ttu-id="67944-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="67944-185">Is Indexed</span></span>             | <span data-ttu-id="67944-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="67944-186">True</span></span>                              |
| <span data-ttu-id="67944-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="67944-187">In Global Catalog</span></span>      | <span data-ttu-id="67944-188">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-188">False</span></span>                             |
| <span data-ttu-id="67944-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="67944-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="67944-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="67944-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67944-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67944-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67944-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67944-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67944-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-193">Search-Flags</span></span>           | <span data-ttu-id="67944-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="67944-194">0x00000001</span></span>                        |
| <span data-ttu-id="67944-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-195">System-Flags</span></span>           | <span data-ttu-id="67944-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67944-196">0x00000010</span></span>                        |
| <span data-ttu-id="67944-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="67944-197">Classes used in</span></span>        | [<span data-ttu-id="67944-198">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="67944-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="67944-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67944-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="67944-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-200">Entry</span></span> | <span data-ttu-id="67944-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67944-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="67944-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67944-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="67944-204">System-Only</span></span>            | <span data-ttu-id="67944-205">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-205">False</span></span>                             |
| <span data-ttu-id="67944-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="67944-206">Is-Single-Valued</span></span>       | <span data-ttu-id="67944-207">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-207">False</span></span>                             |
| <span data-ttu-id="67944-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="67944-208">Is Indexed</span></span>             | <span data-ttu-id="67944-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="67944-209">True</span></span>                              |
| <span data-ttu-id="67944-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="67944-210">In Global Catalog</span></span>      | <span data-ttu-id="67944-211">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-211">False</span></span>                             |
| <span data-ttu-id="67944-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="67944-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="67944-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="67944-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67944-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67944-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67944-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67944-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67944-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-216">Search-Flags</span></span>           | <span data-ttu-id="67944-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="67944-217">0x00000001</span></span>                        |
| <span data-ttu-id="67944-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-218">System-Flags</span></span>           | <span data-ttu-id="67944-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67944-219">0x00000010</span></span>                        |
| <span data-ttu-id="67944-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="67944-220">Classes used in</span></span>        | [<span data-ttu-id="67944-221">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="67944-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="67944-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67944-222">Windows Server 2012</span></span>



| <span data-ttu-id="67944-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="67944-223">Entry</span></span> | <span data-ttu-id="67944-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="67944-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67944-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="67944-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67944-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67944-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="67944-227">System-Only</span></span>            | <span data-ttu-id="67944-228">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-228">False</span></span>                             |
| <span data-ttu-id="67944-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="67944-229">Is-Single-Valued</span></span>       | <span data-ttu-id="67944-230">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-230">False</span></span>                             |
| <span data-ttu-id="67944-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="67944-231">Is Indexed</span></span>             | <span data-ttu-id="67944-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="67944-232">True</span></span>                              |
| <span data-ttu-id="67944-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="67944-233">In Global Catalog</span></span>      | <span data-ttu-id="67944-234">Faux</span><span class="sxs-lookup"><span data-stu-id="67944-234">False</span></span>                             |
| <span data-ttu-id="67944-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="67944-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="67944-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="67944-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67944-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67944-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67944-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67944-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67944-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-239">Search-Flags</span></span>           | <span data-ttu-id="67944-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="67944-240">0x00000001</span></span>                        |
| <span data-ttu-id="67944-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67944-241">System-Flags</span></span>           | <span data-ttu-id="67944-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67944-242">0x00000010</span></span>                        |
| <span data-ttu-id="67944-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="67944-243">Classes used in</span></span>        | [<span data-ttu-id="67944-244">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="67944-244">**User**</span></span>](c-user.md)<br/> |



 

 





