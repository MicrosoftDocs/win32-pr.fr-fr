---
title: Attribut de membre
description: Liste des utilisateurs qui appartiennent au groupe.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Attribut de membre schéma Active Directory
- attribut de membre schéma Active Directory
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106538619"
---
# <a name="member-attribute"></a><span data-ttu-id="9fc05-105">Attribut de membre</span><span class="sxs-lookup"><span data-stu-id="9fc05-105">Member attribute</span></span>

<span data-ttu-id="9fc05-106">Liste des utilisateurs qui appartiennent au groupe.</span><span class="sxs-lookup"><span data-stu-id="9fc05-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="9fc05-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-107">Entry</span></span> | <span data-ttu-id="9fc05-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9fc05-109">CN</span><span class="sxs-lookup"><span data-stu-id="9fc05-109">CN</span></span>                | <span data-ttu-id="9fc05-110">Membre</span><span class="sxs-lookup"><span data-stu-id="9fc05-110">Member</span></span>                                                |
| <span data-ttu-id="9fc05-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9fc05-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9fc05-112">member</span><span class="sxs-lookup"><span data-stu-id="9fc05-112">member</span></span>                                                |
| <span data-ttu-id="9fc05-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9fc05-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9fc05-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9fc05-114">Update Privilege</span></span>  | <span data-ttu-id="9fc05-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="9fc05-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="9fc05-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9fc05-116">Update Frequency</span></span>  | <span data-ttu-id="9fc05-117">Chaque fois qu’un utilisateur est ajouté à un groupe ou en est supprimé.</span><span class="sxs-lookup"><span data-stu-id="9fc05-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="9fc05-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-118">Attribute-Id</span></span>      | <span data-ttu-id="9fc05-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="9fc05-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="9fc05-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9fc05-120">System-Id-Guid</span></span>    | <span data-ttu-id="9fc05-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9fc05-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="9fc05-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fc05-122">Syntax</span></span>            | [<span data-ttu-id="9fc05-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9fc05-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="9fc05-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9fc05-124">Implementations</span></span>

-   [<span data-ttu-id="9fc05-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9fc05-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9fc05-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9fc05-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9fc05-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9fc05-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9fc05-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9fc05-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9fc05-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9fc05-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9fc05-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9fc05-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9fc05-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9fc05-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9fc05-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9fc05-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9fc05-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-133">Entry</span></span> | <span data-ttu-id="9fc05-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-135">Link-Id</span></span>                | <span data-ttu-id="9fc05-136">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-136">2</span></span>                                                                                       |
| <span data-ttu-id="9fc05-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-137">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="9fc05-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-139">System-Only</span></span>            | <span data-ttu-id="9fc05-140">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-140">False</span></span>                                                                                   |
| <span data-ttu-id="9fc05-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-142">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-142">False</span></span>                                                                                   |
| <span data-ttu-id="9fc05-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-143">Is Indexed</span></span>             | <span data-ttu-id="9fc05-144">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-144">False</span></span>                                                                                   |
| <span data-ttu-id="9fc05-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-145">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-146">True</span></span>                                                                                    |
| <span data-ttu-id="9fc05-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="9fc05-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="9fc05-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="9fc05-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-151">Search-Flags</span></span>           | <span data-ttu-id="9fc05-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="9fc05-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-153">System-Flags</span></span>           | <span data-ttu-id="9fc05-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="9fc05-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-155">Classes used in</span></span>        | [<span data-ttu-id="9fc05-156">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-157">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9fc05-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fc05-158">Windows Server 2003</span></span>



| <span data-ttu-id="9fc05-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-159">Entry</span></span> | <span data-ttu-id="9fc05-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-161">Link-Id</span></span>                | <span data-ttu-id="9fc05-162">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="9fc05-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-163">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="9fc05-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-165">System-Only</span></span>            | <span data-ttu-id="9fc05-166">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-167">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-168">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-169">Is Indexed</span></span>             | <span data-ttu-id="9fc05-170">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-171">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="9fc05-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="9fc05-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-177">Search-Flags</span></span>           | <span data-ttu-id="9fc05-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-179">System-Flags</span></span>           | <span data-ttu-id="9fc05-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-181">Classes used in</span></span>        | [<span data-ttu-id="9fc05-182">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-183">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="9fc05-184">**Groupe MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9fc05-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9fc05-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="9fc05-185">ADAM</span></span>



| <span data-ttu-id="9fc05-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-186">Entry</span></span> | <span data-ttu-id="9fc05-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9fc05-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-188">Link-Id</span></span>                | <span data-ttu-id="9fc05-189">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-189">2</span></span>                                   |
| <span data-ttu-id="9fc05-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-190">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-191">0x8009</span></span>                              |
| <span data-ttu-id="9fc05-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-192">System-Only</span></span>            | <span data-ttu-id="9fc05-193">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-193">False</span></span>                               |
| <span data-ttu-id="9fc05-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-194">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-195">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-195">False</span></span>                               |
| <span data-ttu-id="9fc05-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-196">Is Indexed</span></span>             | <span data-ttu-id="9fc05-197">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-197">False</span></span>                               |
| <span data-ttu-id="9fc05-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-198">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-199">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-199">True</span></span>                                |
| <span data-ttu-id="9fc05-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9fc05-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9fc05-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9fc05-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-204">Search-Flags</span></span>           | <span data-ttu-id="9fc05-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-205">0x00000000</span></span>                          |
| <span data-ttu-id="9fc05-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-206">System-Flags</span></span>           | <span data-ttu-id="9fc05-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-207">0x00000012</span></span>                          |
| <span data-ttu-id="9fc05-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-208">Classes used in</span></span>        | [<span data-ttu-id="9fc05-209">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9fc05-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9fc05-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9fc05-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-211">Entry</span></span> | <span data-ttu-id="9fc05-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-213">Link-Id</span></span>                | <span data-ttu-id="9fc05-214">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="9fc05-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-215">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="9fc05-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-217">System-Only</span></span>            | <span data-ttu-id="9fc05-218">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-219">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-220">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-221">Is Indexed</span></span>             | <span data-ttu-id="9fc05-222">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-223">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-224">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="9fc05-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="9fc05-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-229">Search-Flags</span></span>           | <span data-ttu-id="9fc05-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-231">System-Flags</span></span>           | <span data-ttu-id="9fc05-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-233">Classes used in</span></span>        | [<span data-ttu-id="9fc05-234">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-235">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="9fc05-236">**Groupe MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9fc05-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9fc05-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc05-237">Windows Server 2008</span></span>



| <span data-ttu-id="9fc05-238">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-238">Entry</span></span> | <span data-ttu-id="9fc05-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-240">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-240">Link-Id</span></span>                | <span data-ttu-id="9fc05-241">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="9fc05-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-242">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="9fc05-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-244">System-Only</span></span>            | <span data-ttu-id="9fc05-245">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-246">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-247">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-248">Is Indexed</span></span>             | <span data-ttu-id="9fc05-249">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-250">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="9fc05-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="9fc05-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-256">Search-Flags</span></span>           | <span data-ttu-id="9fc05-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-258">System-Flags</span></span>           | <span data-ttu-id="9fc05-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-260">Classes used in</span></span>        | [<span data-ttu-id="9fc05-261">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-262">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="9fc05-263">**Groupe MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9fc05-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9fc05-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9fc05-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9fc05-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-265">Entry</span></span> | <span data-ttu-id="9fc05-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-267">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-267">Link-Id</span></span>                | <span data-ttu-id="9fc05-268">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="9fc05-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-269">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="9fc05-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-271">System-Only</span></span>            | <span data-ttu-id="9fc05-272">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-273">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-273">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-274">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-275">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-275">Is Indexed</span></span>             | <span data-ttu-id="9fc05-276">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-277">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-277">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="9fc05-279">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-280">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="9fc05-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-283">Search-Flags</span></span>           | <span data-ttu-id="9fc05-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-285">System-Flags</span></span>           | <span data-ttu-id="9fc05-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-287">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-287">Classes used in</span></span>        | [<span data-ttu-id="9fc05-288">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-289">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="9fc05-290">**Groupe MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9fc05-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9fc05-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9fc05-291">Windows Server 2012</span></span>



| <span data-ttu-id="9fc05-292">Entrée</span><span class="sxs-lookup"><span data-stu-id="9fc05-292">Entry</span></span> | <span data-ttu-id="9fc05-293">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc05-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc05-294">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9fc05-294">Link-Id</span></span>                | <span data-ttu-id="9fc05-295">2</span><span class="sxs-lookup"><span data-stu-id="9fc05-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="9fc05-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fc05-296">MAPI-Id</span></span>                | <span data-ttu-id="9fc05-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="9fc05-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="9fc05-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fc05-298">System-Only</span></span>            | <span data-ttu-id="9fc05-299">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-300">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9fc05-300">Is-Single-Valued</span></span>       | <span data-ttu-id="9fc05-301">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-302">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9fc05-302">Is Indexed</span></span>             | <span data-ttu-id="9fc05-303">Faux</span><span class="sxs-lookup"><span data-stu-id="9fc05-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="9fc05-304">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9fc05-304">In Global Catalog</span></span>      | <span data-ttu-id="9fc05-305">Vrai</span><span class="sxs-lookup"><span data-stu-id="9fc05-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="9fc05-306">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9fc05-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fc05-307">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9fc05-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="9fc05-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fc05-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fc05-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="9fc05-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-310">Search-Flags</span></span>           | <span data-ttu-id="9fc05-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fc05-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fc05-312">System-Flags</span></span>           | <span data-ttu-id="9fc05-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9fc05-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="9fc05-314">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9fc05-314">Classes used in</span></span>        | [<span data-ttu-id="9fc05-315">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9fc05-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="9fc05-316">**Groupes de noms**</span><span class="sxs-lookup"><span data-stu-id="9fc05-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="9fc05-317">**Groupe MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9fc05-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





