---
title: Attribut de membre de non-sécurité
description: Membres non-sécurité d’un groupe. Utilisé pour les listes de distribution Exchange.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de non-sécurité d’attribut de membre
- Schéma AD de l’attribut nonSecurityMember
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949849"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="8d877-106">Attribut de membre de non-sécurité</span><span class="sxs-lookup"><span data-stu-id="8d877-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="8d877-107">Membres non-sécurité d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="8d877-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="8d877-108">Utilisé pour les listes de distribution Exchange.</span><span class="sxs-lookup"><span data-stu-id="8d877-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="8d877-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-109">Entry</span></span> | <span data-ttu-id="8d877-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="8d877-111">CN</span><span class="sxs-lookup"><span data-stu-id="8d877-111">CN</span></span>                | <span data-ttu-id="8d877-112">Membre non de sécurité</span><span class="sxs-lookup"><span data-stu-id="8d877-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="8d877-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8d877-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8d877-114">nonSecurityMember</span><span class="sxs-lookup"><span data-stu-id="8d877-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="8d877-115">Taille</span><span class="sxs-lookup"><span data-stu-id="8d877-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="8d877-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8d877-116">Update Privilege</span></span>  | <span data-ttu-id="8d877-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="8d877-117">Domain administrator</span></span>                             |
| <span data-ttu-id="8d877-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8d877-118">Update Frequency</span></span>  | <span data-ttu-id="8d877-119">Chaque fois qu’un utilisateur est ajouté ou supprimé de la LD.</span><span class="sxs-lookup"><span data-stu-id="8d877-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="8d877-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-120">Attribute-Id</span></span>      | <span data-ttu-id="8d877-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="8d877-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="8d877-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8d877-122">System-Id-Guid</span></span>    | <span data-ttu-id="8d877-123">52458018-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8d877-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="8d877-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d877-124">Syntax</span></span>            | [<span data-ttu-id="8d877-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8d877-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="8d877-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8d877-126">Implementations</span></span>

-   [<span data-ttu-id="8d877-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8d877-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8d877-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8d877-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8d877-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8d877-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8d877-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8d877-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8d877-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d877-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8d877-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8d877-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8d877-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d877-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8d877-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-134">Entry</span></span> | <span data-ttu-id="8d877-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-136">Link-Id</span></span>                | <span data-ttu-id="8d877-137">50</span><span class="sxs-lookup"><span data-stu-id="8d877-137">50</span></span>                                  |
| <span data-ttu-id="8d877-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-139">System-Only</span></span>            | <span data-ttu-id="8d877-140">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-140">False</span></span>                               |
| <span data-ttu-id="8d877-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-142">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-142">False</span></span>                               |
| <span data-ttu-id="8d877-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-143">Is Indexed</span></span>             | <span data-ttu-id="8d877-144">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-144">False</span></span>                               |
| <span data-ttu-id="8d877-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-145">In Global Catalog</span></span>      | <span data-ttu-id="8d877-146">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-146">False</span></span>                               |
| <span data-ttu-id="8d877-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-151">Search-Flags</span></span>           | <span data-ttu-id="8d877-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-152">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-153">System-Flags</span></span>           | <span data-ttu-id="8d877-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-154">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-155">Classes used in</span></span>        | [<span data-ttu-id="8d877-156">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8d877-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d877-157">Windows Server 2003</span></span>



| <span data-ttu-id="8d877-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-158">Entry</span></span> | <span data-ttu-id="8d877-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-160">Link-Id</span></span>                | <span data-ttu-id="8d877-161">50</span><span class="sxs-lookup"><span data-stu-id="8d877-161">50</span></span>                                  |
| <span data-ttu-id="8d877-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-163">System-Only</span></span>            | <span data-ttu-id="8d877-164">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-164">False</span></span>                               |
| <span data-ttu-id="8d877-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-166">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-166">False</span></span>                               |
| <span data-ttu-id="8d877-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-167">Is Indexed</span></span>             | <span data-ttu-id="8d877-168">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-168">False</span></span>                               |
| <span data-ttu-id="8d877-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-169">In Global Catalog</span></span>      | <span data-ttu-id="8d877-170">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-170">False</span></span>                               |
| <span data-ttu-id="8d877-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-175">Search-Flags</span></span>           | <span data-ttu-id="8d877-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-176">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-177">System-Flags</span></span>           | <span data-ttu-id="8d877-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-178">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-179">Classes used in</span></span>        | [<span data-ttu-id="8d877-180">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8d877-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8d877-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8d877-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-182">Entry</span></span> | <span data-ttu-id="8d877-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-184">Link-Id</span></span>                | <span data-ttu-id="8d877-185">50</span><span class="sxs-lookup"><span data-stu-id="8d877-185">50</span></span>                                  |
| <span data-ttu-id="8d877-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-187">System-Only</span></span>            | <span data-ttu-id="8d877-188">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-188">False</span></span>                               |
| <span data-ttu-id="8d877-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-190">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-190">False</span></span>                               |
| <span data-ttu-id="8d877-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-191">Is Indexed</span></span>             | <span data-ttu-id="8d877-192">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-192">False</span></span>                               |
| <span data-ttu-id="8d877-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-193">In Global Catalog</span></span>      | <span data-ttu-id="8d877-194">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-194">False</span></span>                               |
| <span data-ttu-id="8d877-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-199">Search-Flags</span></span>           | <span data-ttu-id="8d877-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-200">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-201">System-Flags</span></span>           | <span data-ttu-id="8d877-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-202">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-203">Classes used in</span></span>        | [<span data-ttu-id="8d877-204">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8d877-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d877-205">Windows Server 2008</span></span>



| <span data-ttu-id="8d877-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-206">Entry</span></span> | <span data-ttu-id="8d877-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-208">Link-Id</span></span>                | <span data-ttu-id="8d877-209">50</span><span class="sxs-lookup"><span data-stu-id="8d877-209">50</span></span>                                  |
| <span data-ttu-id="8d877-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-211">System-Only</span></span>            | <span data-ttu-id="8d877-212">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-212">False</span></span>                               |
| <span data-ttu-id="8d877-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-214">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-214">False</span></span>                               |
| <span data-ttu-id="8d877-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-215">Is Indexed</span></span>             | <span data-ttu-id="8d877-216">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-216">False</span></span>                               |
| <span data-ttu-id="8d877-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-217">In Global Catalog</span></span>      | <span data-ttu-id="8d877-218">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-218">False</span></span>                               |
| <span data-ttu-id="8d877-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-223">Search-Flags</span></span>           | <span data-ttu-id="8d877-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-224">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-225">System-Flags</span></span>           | <span data-ttu-id="8d877-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-226">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-227">Classes used in</span></span>        | [<span data-ttu-id="8d877-228">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8d877-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d877-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8d877-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-230">Entry</span></span> | <span data-ttu-id="8d877-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-232">Link-Id</span></span>                | <span data-ttu-id="8d877-233">50</span><span class="sxs-lookup"><span data-stu-id="8d877-233">50</span></span>                                  |
| <span data-ttu-id="8d877-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-235">System-Only</span></span>            | <span data-ttu-id="8d877-236">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-236">False</span></span>                               |
| <span data-ttu-id="8d877-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-238">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-238">False</span></span>                               |
| <span data-ttu-id="8d877-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-239">Is Indexed</span></span>             | <span data-ttu-id="8d877-240">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-240">False</span></span>                               |
| <span data-ttu-id="8d877-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-241">In Global Catalog</span></span>      | <span data-ttu-id="8d877-242">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-242">False</span></span>                               |
| <span data-ttu-id="8d877-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-247">Search-Flags</span></span>           | <span data-ttu-id="8d877-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-248">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-249">System-Flags</span></span>           | <span data-ttu-id="8d877-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-250">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-251">Classes used in</span></span>        | [<span data-ttu-id="8d877-252">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8d877-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d877-253">Windows Server 2012</span></span>



| <span data-ttu-id="8d877-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="8d877-254">Entry</span></span> | <span data-ttu-id="8d877-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d877-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8d877-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8d877-256">Link-Id</span></span>                | <span data-ttu-id="8d877-257">50</span><span class="sxs-lookup"><span data-stu-id="8d877-257">50</span></span>                                  |
| <span data-ttu-id="8d877-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d877-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8d877-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d877-259">System-Only</span></span>            | <span data-ttu-id="8d877-260">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-260">False</span></span>                               |
| <span data-ttu-id="8d877-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8d877-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8d877-262">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-262">False</span></span>                               |
| <span data-ttu-id="8d877-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8d877-263">Is Indexed</span></span>             | <span data-ttu-id="8d877-264">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-264">False</span></span>                               |
| <span data-ttu-id="8d877-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8d877-265">In Global Catalog</span></span>      | <span data-ttu-id="8d877-266">Faux</span><span class="sxs-lookup"><span data-stu-id="8d877-266">False</span></span>                               |
| <span data-ttu-id="8d877-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8d877-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d877-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8d877-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8d877-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d877-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8d877-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d877-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8d877-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-271">Search-Flags</span></span>           | <span data-ttu-id="8d877-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d877-272">0x00000000</span></span>                          |
| <span data-ttu-id="8d877-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d877-273">System-Flags</span></span>           | <span data-ttu-id="8d877-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d877-274">0x00000010</span></span>                          |
| <span data-ttu-id="8d877-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8d877-275">Classes used in</span></span>        | [<span data-ttu-id="8d877-276">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8d877-276">**Group**</span></span>](c-group.md)<br/> |



 

 





