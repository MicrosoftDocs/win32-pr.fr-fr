---
title: attribut ms-FRS-Hub-Member
description: L’attribut ms-FRS-Hub-Member permet d’enregistrer les paramètres de topologie NTFRS par défaut.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-FRS-Hub-Member Attribute
- Schéma Active Directory msFRS-Hub-Member Attribute
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106512831"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="ff07a-105">attribut ms-FRS-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="ff07a-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="ff07a-106">L’attribut **MS-FRS-Hub-Member** permet d’enregistrer les paramètres de topologie NTFRS par défaut.</span><span class="sxs-lookup"><span data-stu-id="ff07a-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="ff07a-107">Lorsqu’un membre FRS est ajouté ou supprimé à un jeu de réplicas, ces attributs sont désignés et des ajustements appropriés sont effectués sur les connexions entre le reste des membres FRS dans le jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="ff07a-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="ff07a-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-108">Entry</span></span> | <span data-ttu-id="ff07a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ff07a-110">CN</span><span class="sxs-lookup"><span data-stu-id="ff07a-110">CN</span></span>                | <span data-ttu-id="ff07a-111">MS-FRS-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="ff07a-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="ff07a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ff07a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ff07a-113">msFRS-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="ff07a-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="ff07a-114">Taille</span><span class="sxs-lookup"><span data-stu-id="ff07a-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="ff07a-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ff07a-115">Update Privilege</span></span>  | <span data-ttu-id="ff07a-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="ff07a-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="ff07a-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ff07a-117">Update Frequency</span></span>  | <span data-ttu-id="ff07a-118">Lors de la création du jeu de réplicas ou de la modification de la topologie par défaut.</span><span class="sxs-lookup"><span data-stu-id="ff07a-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="ff07a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-119">Attribute-Id</span></span>      | <span data-ttu-id="ff07a-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="ff07a-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="ff07a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff07a-121">System-Id-Guid</span></span>    | <span data-ttu-id="ff07a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="ff07a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="ff07a-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff07a-123">Syntax</span></span>            | [<span data-ttu-id="ff07a-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ff07a-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="ff07a-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ff07a-125">Implementations</span></span>

-   [<span data-ttu-id="ff07a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff07a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff07a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff07a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff07a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff07a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff07a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff07a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff07a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff07a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ff07a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff07a-131">Windows Server 2003</span></span>



| <span data-ttu-id="ff07a-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-132">Entry</span></span> | <span data-ttu-id="ff07a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ff07a-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ff07a-134">Link-Id</span></span>                | <span data-ttu-id="ff07a-135">1046</span><span class="sxs-lookup"><span data-stu-id="ff07a-135">1046</span></span>                                                      |
| <span data-ttu-id="ff07a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="ff07a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff07a-137">System-Only</span></span>            | <span data-ttu-id="ff07a-138">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-138">False</span></span>                                                     |
| <span data-ttu-id="ff07a-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ff07a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ff07a-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ff07a-140">True</span></span>                                                      |
| <span data-ttu-id="ff07a-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ff07a-141">Is Indexed</span></span>             | <span data-ttu-id="ff07a-142">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-142">False</span></span>                                                     |
| <span data-ttu-id="ff07a-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ff07a-143">In Global Catalog</span></span>      | <span data-ttu-id="ff07a-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-144">False</span></span>                                                     |
| <span data-ttu-id="ff07a-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ff07a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff07a-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ff07a-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="ff07a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff07a-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff07a-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-149">Search-Flags</span></span>           | <span data-ttu-id="ff07a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-150">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-151">System-Flags</span></span>           | <span data-ttu-id="ff07a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-152">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ff07a-153">Classes used in</span></span>        | [<span data-ttu-id="ff07a-154">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="ff07a-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff07a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff07a-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff07a-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-156">Entry</span></span> | <span data-ttu-id="ff07a-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ff07a-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ff07a-158">Link-Id</span></span>                | <span data-ttu-id="ff07a-159">1046</span><span class="sxs-lookup"><span data-stu-id="ff07a-159">1046</span></span>                                                      |
| <span data-ttu-id="ff07a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="ff07a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff07a-161">System-Only</span></span>            | <span data-ttu-id="ff07a-162">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-162">False</span></span>                                                     |
| <span data-ttu-id="ff07a-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ff07a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ff07a-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="ff07a-164">True</span></span>                                                      |
| <span data-ttu-id="ff07a-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ff07a-165">Is Indexed</span></span>             | <span data-ttu-id="ff07a-166">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-166">False</span></span>                                                     |
| <span data-ttu-id="ff07a-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ff07a-167">In Global Catalog</span></span>      | <span data-ttu-id="ff07a-168">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-168">False</span></span>                                                     |
| <span data-ttu-id="ff07a-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ff07a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff07a-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ff07a-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="ff07a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff07a-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff07a-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-173">Search-Flags</span></span>           | <span data-ttu-id="ff07a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-174">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-175">System-Flags</span></span>           | <span data-ttu-id="ff07a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-176">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ff07a-177">Classes used in</span></span>        | [<span data-ttu-id="ff07a-178">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="ff07a-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff07a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff07a-179">Windows Server 2008</span></span>



| <span data-ttu-id="ff07a-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-180">Entry</span></span> | <span data-ttu-id="ff07a-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ff07a-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ff07a-182">Link-Id</span></span>                | <span data-ttu-id="ff07a-183">1046</span><span class="sxs-lookup"><span data-stu-id="ff07a-183">1046</span></span>                                                      |
| <span data-ttu-id="ff07a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="ff07a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff07a-185">System-Only</span></span>            | <span data-ttu-id="ff07a-186">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-186">False</span></span>                                                     |
| <span data-ttu-id="ff07a-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ff07a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ff07a-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="ff07a-188">True</span></span>                                                      |
| <span data-ttu-id="ff07a-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ff07a-189">Is Indexed</span></span>             | <span data-ttu-id="ff07a-190">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-190">False</span></span>                                                     |
| <span data-ttu-id="ff07a-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ff07a-191">In Global Catalog</span></span>      | <span data-ttu-id="ff07a-192">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-192">False</span></span>                                                     |
| <span data-ttu-id="ff07a-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ff07a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff07a-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ff07a-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="ff07a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff07a-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff07a-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-197">Search-Flags</span></span>           | <span data-ttu-id="ff07a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-198">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-199">System-Flags</span></span>           | <span data-ttu-id="ff07a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-200">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ff07a-201">Classes used in</span></span>        | [<span data-ttu-id="ff07a-202">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="ff07a-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff07a-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff07a-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff07a-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-204">Entry</span></span> | <span data-ttu-id="ff07a-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ff07a-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ff07a-206">Link-Id</span></span>                | <span data-ttu-id="ff07a-207">1046</span><span class="sxs-lookup"><span data-stu-id="ff07a-207">1046</span></span>                                                      |
| <span data-ttu-id="ff07a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="ff07a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff07a-209">System-Only</span></span>            | <span data-ttu-id="ff07a-210">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-210">False</span></span>                                                     |
| <span data-ttu-id="ff07a-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ff07a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ff07a-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="ff07a-212">True</span></span>                                                      |
| <span data-ttu-id="ff07a-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ff07a-213">Is Indexed</span></span>             | <span data-ttu-id="ff07a-214">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-214">False</span></span>                                                     |
| <span data-ttu-id="ff07a-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ff07a-215">In Global Catalog</span></span>      | <span data-ttu-id="ff07a-216">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-216">False</span></span>                                                     |
| <span data-ttu-id="ff07a-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ff07a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff07a-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ff07a-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="ff07a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff07a-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff07a-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-221">Search-Flags</span></span>           | <span data-ttu-id="ff07a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-222">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-223">System-Flags</span></span>           | <span data-ttu-id="ff07a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-224">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ff07a-225">Classes used in</span></span>        | [<span data-ttu-id="ff07a-226">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="ff07a-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff07a-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff07a-227">Windows Server 2012</span></span>



| <span data-ttu-id="ff07a-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="ff07a-228">Entry</span></span> | <span data-ttu-id="ff07a-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ff07a-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ff07a-230">Link-Id</span></span>                | <span data-ttu-id="ff07a-231">1046</span><span class="sxs-lookup"><span data-stu-id="ff07a-231">1046</span></span>                                                      |
| <span data-ttu-id="ff07a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff07a-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="ff07a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff07a-233">System-Only</span></span>            | <span data-ttu-id="ff07a-234">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-234">False</span></span>                                                     |
| <span data-ttu-id="ff07a-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ff07a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="ff07a-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="ff07a-236">True</span></span>                                                      |
| <span data-ttu-id="ff07a-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ff07a-237">Is Indexed</span></span>             | <span data-ttu-id="ff07a-238">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-238">False</span></span>                                                     |
| <span data-ttu-id="ff07a-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ff07a-239">In Global Catalog</span></span>      | <span data-ttu-id="ff07a-240">Faux</span><span class="sxs-lookup"><span data-stu-id="ff07a-240">False</span></span>                                                     |
| <span data-ttu-id="ff07a-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ff07a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff07a-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ff07a-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="ff07a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff07a-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff07a-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="ff07a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-245">Search-Flags</span></span>           | <span data-ttu-id="ff07a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-246">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff07a-247">System-Flags</span></span>           | <span data-ttu-id="ff07a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff07a-248">0x00000000</span></span>                                                |
| <span data-ttu-id="ff07a-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ff07a-249">Classes used in</span></span>        | [<span data-ttu-id="ff07a-250">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="ff07a-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ff07a-251">Notes</span><span class="sxs-lookup"><span data-stu-id="ff07a-251">Remarks</span></span>

<span data-ttu-id="ff07a-252">Il s’agit du nom unique complet d’un objet de [**membre NTFRS**](c-ntfrsmember.md) .</span><span class="sxs-lookup"><span data-stu-id="ff07a-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="ff07a-253">Le nom unique est au format « CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = volumes DFS, CN = service de réplication de fichiers, CN = System, DC =... »</span><span class="sxs-lookup"><span data-stu-id="ff07a-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





