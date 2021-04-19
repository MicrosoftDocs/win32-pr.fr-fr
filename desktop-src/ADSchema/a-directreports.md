---
title: Attribut de rapports
description: Contient la liste des utilisateurs qui sont directement signalés à l’utilisateur. Les utilisateurs répertoriés comme rapports sont ceux dont la propriété gestionnaire de propriétés est définie sur cet utilisateur. Chaque élément de la liste est une référence liée à l’objet qui représente l’utilisateur.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs de rapports
- Schéma AD de l’attribut directReports
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514486"
---
# <a name="reports-attribute"></a><span data-ttu-id="4688f-107">Attribut de rapports</span><span class="sxs-lookup"><span data-stu-id="4688f-107">Reports attribute</span></span>

<span data-ttu-id="4688f-108">Contient la liste des utilisateurs qui sont directement signalés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4688f-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="4688f-109">Les utilisateurs répertoriés comme rapports sont ceux dont la propriété gestionnaire de propriétés est définie sur cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4688f-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="4688f-110">Chaque élément de la liste est une référence liée à l’objet qui représente l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4688f-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="4688f-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-111">Entry</span></span> | <span data-ttu-id="4688f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="4688f-113">CN</span><span class="sxs-lookup"><span data-stu-id="4688f-113">CN</span></span>                | <span data-ttu-id="4688f-114">Rapports</span><span class="sxs-lookup"><span data-stu-id="4688f-114">Reports</span></span>                                         |
| <span data-ttu-id="4688f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4688f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4688f-116">directReports</span><span class="sxs-lookup"><span data-stu-id="4688f-116">directReports</span></span>                                   |
| <span data-ttu-id="4688f-117">Taille</span><span class="sxs-lookup"><span data-stu-id="4688f-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="4688f-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4688f-118">Update Privilege</span></span>  | <span data-ttu-id="4688f-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="4688f-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="4688f-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4688f-120">Update Frequency</span></span>  | <span data-ttu-id="4688f-121">Chaque fois que les rapports directs d’un utilisateur changent.</span><span class="sxs-lookup"><span data-stu-id="4688f-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="4688f-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-122">Attribute-Id</span></span>      | <span data-ttu-id="4688f-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="4688f-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="4688f-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4688f-124">System-Id-Guid</span></span>    | <span data-ttu-id="4688f-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4688f-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="4688f-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4688f-126">Syntax</span></span>            | [<span data-ttu-id="4688f-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4688f-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="4688f-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4688f-128">Implementations</span></span>

-   [<span data-ttu-id="4688f-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4688f-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4688f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4688f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4688f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4688f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4688f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4688f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4688f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4688f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4688f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4688f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4688f-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4688f-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4688f-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-136">Entry</span></span> | <span data-ttu-id="4688f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-138">Link-Id</span></span>                | <span data-ttu-id="4688f-139">43</span><span class="sxs-lookup"><span data-stu-id="4688f-139">43</span></span>                              |
| <span data-ttu-id="4688f-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-140">MAPI-Id</span></span>                | <span data-ttu-id="4688f-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-141">0x800E</span></span>                          |
| <span data-ttu-id="4688f-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-142">System-Only</span></span>            | <span data-ttu-id="4688f-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-143">True</span></span>                            |
| <span data-ttu-id="4688f-144">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-144">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-145">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-145">False</span></span>                           |
| <span data-ttu-id="4688f-146">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-146">Is Indexed</span></span>             | <span data-ttu-id="4688f-147">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-147">False</span></span>                           |
| <span data-ttu-id="4688f-148">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-148">In Global Catalog</span></span>      | <span data-ttu-id="4688f-149">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-149">False</span></span>                           |
| <span data-ttu-id="4688f-150">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-151">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-154">Search-Flags</span></span>           | <span data-ttu-id="4688f-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-155">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-156">System-Flags</span></span>           | <span data-ttu-id="4688f-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-157">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-158">Classes used in</span></span>        | [<span data-ttu-id="4688f-159">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4688f-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4688f-160">Windows Server 2003</span></span>



| <span data-ttu-id="4688f-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-161">Entry</span></span> | <span data-ttu-id="4688f-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-163">Link-Id</span></span>                | <span data-ttu-id="4688f-164">43</span><span class="sxs-lookup"><span data-stu-id="4688f-164">43</span></span>                              |
| <span data-ttu-id="4688f-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-165">MAPI-Id</span></span>                | <span data-ttu-id="4688f-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-166">0x800E</span></span>                          |
| <span data-ttu-id="4688f-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-167">System-Only</span></span>            | <span data-ttu-id="4688f-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-168">True</span></span>                            |
| <span data-ttu-id="4688f-169">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-169">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-170">False</span></span>                           |
| <span data-ttu-id="4688f-171">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-171">Is Indexed</span></span>             | <span data-ttu-id="4688f-172">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-172">False</span></span>                           |
| <span data-ttu-id="4688f-173">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-173">In Global Catalog</span></span>      | <span data-ttu-id="4688f-174">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-174">False</span></span>                           |
| <span data-ttu-id="4688f-175">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-176">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-179">Search-Flags</span></span>           | <span data-ttu-id="4688f-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-180">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-181">System-Flags</span></span>           | <span data-ttu-id="4688f-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-182">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-183">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-183">Classes used in</span></span>        | [<span data-ttu-id="4688f-184">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4688f-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4688f-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4688f-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-186">Entry</span></span> | <span data-ttu-id="4688f-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-188">Link-Id</span></span>                | <span data-ttu-id="4688f-189">43</span><span class="sxs-lookup"><span data-stu-id="4688f-189">43</span></span>                              |
| <span data-ttu-id="4688f-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-190">MAPI-Id</span></span>                | <span data-ttu-id="4688f-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-191">0x800E</span></span>                          |
| <span data-ttu-id="4688f-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-192">System-Only</span></span>            | <span data-ttu-id="4688f-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-193">True</span></span>                            |
| <span data-ttu-id="4688f-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-194">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-195">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-195">False</span></span>                           |
| <span data-ttu-id="4688f-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-196">Is Indexed</span></span>             | <span data-ttu-id="4688f-197">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-197">False</span></span>                           |
| <span data-ttu-id="4688f-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-198">In Global Catalog</span></span>      | <span data-ttu-id="4688f-199">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-199">False</span></span>                           |
| <span data-ttu-id="4688f-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-204">Search-Flags</span></span>           | <span data-ttu-id="4688f-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-205">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-206">System-Flags</span></span>           | <span data-ttu-id="4688f-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-207">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-208">Classes used in</span></span>        | [<span data-ttu-id="4688f-209">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4688f-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4688f-210">Windows Server 2008</span></span>



| <span data-ttu-id="4688f-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-211">Entry</span></span> | <span data-ttu-id="4688f-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-213">Link-Id</span></span>                | <span data-ttu-id="4688f-214">43</span><span class="sxs-lookup"><span data-stu-id="4688f-214">43</span></span>                              |
| <span data-ttu-id="4688f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-215">MAPI-Id</span></span>                | <span data-ttu-id="4688f-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-216">0x800E</span></span>                          |
| <span data-ttu-id="4688f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-217">System-Only</span></span>            | <span data-ttu-id="4688f-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-218">True</span></span>                            |
| <span data-ttu-id="4688f-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-220">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-220">False</span></span>                           |
| <span data-ttu-id="4688f-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-221">Is Indexed</span></span>             | <span data-ttu-id="4688f-222">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-222">False</span></span>                           |
| <span data-ttu-id="4688f-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-223">In Global Catalog</span></span>      | <span data-ttu-id="4688f-224">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-224">False</span></span>                           |
| <span data-ttu-id="4688f-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-229">Search-Flags</span></span>           | <span data-ttu-id="4688f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-230">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-231">System-Flags</span></span>           | <span data-ttu-id="4688f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-232">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-233">Classes used in</span></span>        | [<span data-ttu-id="4688f-234">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4688f-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4688f-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4688f-236">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-236">Entry</span></span> | <span data-ttu-id="4688f-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-238">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-238">Link-Id</span></span>                | <span data-ttu-id="4688f-239">43</span><span class="sxs-lookup"><span data-stu-id="4688f-239">43</span></span>                              |
| <span data-ttu-id="4688f-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-240">MAPI-Id</span></span>                | <span data-ttu-id="4688f-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-241">0x800E</span></span>                          |
| <span data-ttu-id="4688f-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-242">System-Only</span></span>            | <span data-ttu-id="4688f-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-243">True</span></span>                            |
| <span data-ttu-id="4688f-244">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-244">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-245">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-245">False</span></span>                           |
| <span data-ttu-id="4688f-246">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-246">Is Indexed</span></span>             | <span data-ttu-id="4688f-247">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-247">False</span></span>                           |
| <span data-ttu-id="4688f-248">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-248">In Global Catalog</span></span>      | <span data-ttu-id="4688f-249">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-249">False</span></span>                           |
| <span data-ttu-id="4688f-250">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-251">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-254">Search-Flags</span></span>           | <span data-ttu-id="4688f-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-255">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-256">System-Flags</span></span>           | <span data-ttu-id="4688f-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-257">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-258">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-258">Classes used in</span></span>        | [<span data-ttu-id="4688f-259">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4688f-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4688f-260">Windows Server 2012</span></span>



| <span data-ttu-id="4688f-261">Entrée</span><span class="sxs-lookup"><span data-stu-id="4688f-261">Entry</span></span> | <span data-ttu-id="4688f-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="4688f-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4688f-263">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4688f-263">Link-Id</span></span>                | <span data-ttu-id="4688f-264">43</span><span class="sxs-lookup"><span data-stu-id="4688f-264">43</span></span>                              |
| <span data-ttu-id="4688f-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4688f-265">MAPI-Id</span></span>                | <span data-ttu-id="4688f-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="4688f-266">0x800E</span></span>                          |
| <span data-ttu-id="4688f-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="4688f-267">System-Only</span></span>            | <span data-ttu-id="4688f-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="4688f-268">True</span></span>                            |
| <span data-ttu-id="4688f-269">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4688f-269">Is-Single-Valued</span></span>       | <span data-ttu-id="4688f-270">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-270">False</span></span>                           |
| <span data-ttu-id="4688f-271">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4688f-271">Is Indexed</span></span>             | <span data-ttu-id="4688f-272">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-272">False</span></span>                           |
| <span data-ttu-id="4688f-273">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4688f-273">In Global Catalog</span></span>      | <span data-ttu-id="4688f-274">Faux</span><span class="sxs-lookup"><span data-stu-id="4688f-274">False</span></span>                           |
| <span data-ttu-id="4688f-275">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4688f-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="4688f-276">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4688f-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4688f-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4688f-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4688f-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4688f-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4688f-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-279">Search-Flags</span></span>           | <span data-ttu-id="4688f-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4688f-280">0x00000000</span></span>                      |
| <span data-ttu-id="4688f-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4688f-281">System-Flags</span></span>           | <span data-ttu-id="4688f-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4688f-282">0x00000010</span></span>                      |
| <span data-ttu-id="4688f-283">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4688f-283">Classes used in</span></span>        | [<span data-ttu-id="4688f-284">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="4688f-284">**Top**</span></span>](c-top.md)<br/> |



 

 





