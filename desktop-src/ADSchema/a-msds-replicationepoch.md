---
title: attribut ms-DS-ReplicationEpoch
description: Cela permet de conserver l’époque de réplication de tous les contrôleurs de domaines. Une époque est la période pendant laquelle un domaine a un nom spécifique. Une nouvelle époque commence lorsqu’un changement de nom de domaine se produit.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-ReplicationEpoch
- Schéma Active Directory de l’attribut msDS-ReplicationEpoch
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519809"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="06800-107">attribut ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="06800-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="06800-108">Cela permet de conserver l’époque de réplication de tous les contrôleurs de domaines.</span><span class="sxs-lookup"><span data-stu-id="06800-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="06800-109">Une époque est la période pendant laquelle un domaine a un nom spécifique.</span><span class="sxs-lookup"><span data-stu-id="06800-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="06800-110">Une nouvelle époque commence lorsqu’un changement de nom de domaine se produit.</span><span class="sxs-lookup"><span data-stu-id="06800-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="06800-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-111">Entry</span></span> | <span data-ttu-id="06800-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="06800-113">CN</span><span class="sxs-lookup"><span data-stu-id="06800-113">CN</span></span>                | <span data-ttu-id="06800-114">ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="06800-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="06800-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="06800-115">Ldap-Display-Name</span></span> | <span data-ttu-id="06800-116">msDS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="06800-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="06800-117">Taille</span><span class="sxs-lookup"><span data-stu-id="06800-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="06800-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="06800-118">Update Privilege</span></span>  | <span data-ttu-id="06800-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="06800-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="06800-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="06800-120">Update Frequency</span></span>  | <span data-ttu-id="06800-121">Uniquement pendant la restructuration de domaine.</span><span class="sxs-lookup"><span data-stu-id="06800-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="06800-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06800-122">Attribute-Id</span></span>      | <span data-ttu-id="06800-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="06800-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="06800-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="06800-124">System-Id-Guid</span></span>    | <span data-ttu-id="06800-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="06800-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="06800-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06800-126">Syntax</span></span>            | [<span data-ttu-id="06800-127">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="06800-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="06800-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="06800-128">Implementations</span></span>

-   [<span data-ttu-id="06800-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06800-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06800-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="06800-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="06800-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06800-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06800-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06800-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06800-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06800-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06800-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06800-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="06800-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06800-135">Windows Server 2003</span></span>



| <span data-ttu-id="06800-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-136">Entry</span></span> | <span data-ttu-id="06800-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-140">System-Only</span></span>            | <span data-ttu-id="06800-141">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-141">False</span></span>                                    |
| <span data-ttu-id="06800-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-142">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-143">True</span></span>                                     |
| <span data-ttu-id="06800-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-144">Is Indexed</span></span>             | <span data-ttu-id="06800-145">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-145">False</span></span>                                    |
| <span data-ttu-id="06800-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-146">In Global Catalog</span></span>      | <span data-ttu-id="06800-147">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-147">False</span></span>                                    |
| <span data-ttu-id="06800-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-152">Search-Flags</span></span>           | <span data-ttu-id="06800-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-153">0x00000000</span></span>                               |
| <span data-ttu-id="06800-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-154">System-Flags</span></span>           | <span data-ttu-id="06800-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-155">0x00000011</span></span>                               |
| <span data-ttu-id="06800-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-156">Classes used in</span></span>        | [<span data-ttu-id="06800-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="06800-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="06800-158">ADAM</span></span>



| <span data-ttu-id="06800-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-159">Entry</span></span> | <span data-ttu-id="06800-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-163">System-Only</span></span>            | <span data-ttu-id="06800-164">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-164">False</span></span>                                    |
| <span data-ttu-id="06800-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-165">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-166">True</span></span>                                     |
| <span data-ttu-id="06800-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-167">Is Indexed</span></span>             | <span data-ttu-id="06800-168">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-168">False</span></span>                                    |
| <span data-ttu-id="06800-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-169">In Global Catalog</span></span>      | <span data-ttu-id="06800-170">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-170">False</span></span>                                    |
| <span data-ttu-id="06800-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-175">Search-Flags</span></span>           | <span data-ttu-id="06800-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-176">0x00000000</span></span>                               |
| <span data-ttu-id="06800-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-177">System-Flags</span></span>           | <span data-ttu-id="06800-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-178">0x00000011</span></span>                               |
| <span data-ttu-id="06800-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-179">Classes used in</span></span>        | [<span data-ttu-id="06800-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06800-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06800-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06800-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-182">Entry</span></span> | <span data-ttu-id="06800-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-186">System-Only</span></span>            | <span data-ttu-id="06800-187">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-187">False</span></span>                                    |
| <span data-ttu-id="06800-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-188">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-189">True</span></span>                                     |
| <span data-ttu-id="06800-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-190">Is Indexed</span></span>             | <span data-ttu-id="06800-191">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-191">False</span></span>                                    |
| <span data-ttu-id="06800-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-192">In Global Catalog</span></span>      | <span data-ttu-id="06800-193">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-193">False</span></span>                                    |
| <span data-ttu-id="06800-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-198">Search-Flags</span></span>           | <span data-ttu-id="06800-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-199">0x00000000</span></span>                               |
| <span data-ttu-id="06800-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-200">System-Flags</span></span>           | <span data-ttu-id="06800-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-201">0x00000011</span></span>                               |
| <span data-ttu-id="06800-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-202">Classes used in</span></span>        | [<span data-ttu-id="06800-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06800-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06800-204">Windows Server 2008</span></span>



| <span data-ttu-id="06800-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-205">Entry</span></span> | <span data-ttu-id="06800-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-209">System-Only</span></span>            | <span data-ttu-id="06800-210">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-210">False</span></span>                                    |
| <span data-ttu-id="06800-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-211">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-212">True</span></span>                                     |
| <span data-ttu-id="06800-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-213">Is Indexed</span></span>             | <span data-ttu-id="06800-214">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-214">False</span></span>                                    |
| <span data-ttu-id="06800-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-215">In Global Catalog</span></span>      | <span data-ttu-id="06800-216">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-216">False</span></span>                                    |
| <span data-ttu-id="06800-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-221">Search-Flags</span></span>           | <span data-ttu-id="06800-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-222">0x00000000</span></span>                               |
| <span data-ttu-id="06800-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-223">System-Flags</span></span>           | <span data-ttu-id="06800-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-224">0x00000011</span></span>                               |
| <span data-ttu-id="06800-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-225">Classes used in</span></span>        | [<span data-ttu-id="06800-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06800-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06800-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06800-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-228">Entry</span></span> | <span data-ttu-id="06800-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-232">System-Only</span></span>            | <span data-ttu-id="06800-233">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-233">False</span></span>                                    |
| <span data-ttu-id="06800-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-234">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-235">True</span></span>                                     |
| <span data-ttu-id="06800-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-236">Is Indexed</span></span>             | <span data-ttu-id="06800-237">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-237">False</span></span>                                    |
| <span data-ttu-id="06800-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-238">In Global Catalog</span></span>      | <span data-ttu-id="06800-239">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-239">False</span></span>                                    |
| <span data-ttu-id="06800-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-244">Search-Flags</span></span>           | <span data-ttu-id="06800-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-245">0x00000000</span></span>                               |
| <span data-ttu-id="06800-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-246">System-Flags</span></span>           | <span data-ttu-id="06800-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-247">0x00000011</span></span>                               |
| <span data-ttu-id="06800-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-248">Classes used in</span></span>        | [<span data-ttu-id="06800-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06800-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06800-250">Windows Server 2012</span></span>



| <span data-ttu-id="06800-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="06800-251">Entry</span></span> | <span data-ttu-id="06800-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="06800-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="06800-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="06800-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06800-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="06800-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="06800-255">System-Only</span></span>            | <span data-ttu-id="06800-256">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-256">False</span></span>                                    |
| <span data-ttu-id="06800-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="06800-257">Is-Single-Valued</span></span>       | <span data-ttu-id="06800-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="06800-258">True</span></span>                                     |
| <span data-ttu-id="06800-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="06800-259">Is Indexed</span></span>             | <span data-ttu-id="06800-260">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-260">False</span></span>                                    |
| <span data-ttu-id="06800-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="06800-261">In Global Catalog</span></span>      | <span data-ttu-id="06800-262">Faux</span><span class="sxs-lookup"><span data-stu-id="06800-262">False</span></span>                                    |
| <span data-ttu-id="06800-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="06800-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="06800-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="06800-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="06800-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06800-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="06800-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06800-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="06800-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-267">Search-Flags</span></span>           | <span data-ttu-id="06800-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06800-268">0x00000000</span></span>                               |
| <span data-ttu-id="06800-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06800-269">System-Flags</span></span>           | <span data-ttu-id="06800-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06800-270">0x00000011</span></span>                               |
| <span data-ttu-id="06800-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="06800-271">Classes used in</span></span>        | [<span data-ttu-id="06800-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="06800-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





