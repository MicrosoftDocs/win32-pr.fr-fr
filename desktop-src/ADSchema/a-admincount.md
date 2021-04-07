---
title: Attribut Admin-Count
description: Indique qu’un objet donné a fait passer ses ACL à une valeur plus sécurisée par le système, car il était membre de l’un des groupes d’administration (directement ou transitivement).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Admin-Count
- Schéma AD de l’attribut adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745308"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="8168d-105">Attribut Admin-Count</span><span class="sxs-lookup"><span data-stu-id="8168d-105">Admin-Count attribute</span></span>

<span data-ttu-id="8168d-106">Indique qu’un objet donné a fait passer ses ACL à une valeur plus sécurisée par le système, car il était membre de l’un des groupes d’administration (directement ou transitivement).</span><span class="sxs-lookup"><span data-stu-id="8168d-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="8168d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-107">Entry</span></span> | <span data-ttu-id="8168d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="8168d-109">CN</span><span class="sxs-lookup"><span data-stu-id="8168d-109">CN</span></span>                | <span data-ttu-id="8168d-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="8168d-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="8168d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8168d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8168d-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="8168d-112">adminCount</span></span>                                          |
| <span data-ttu-id="8168d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="8168d-113">Size</span></span>              | <span data-ttu-id="8168d-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="8168d-114">4 bytes</span></span>                                             |
| <span data-ttu-id="8168d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8168d-115">Update Privilege</span></span>  | <span data-ttu-id="8168d-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="8168d-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="8168d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8168d-117">Update Frequency</span></span>  | <span data-ttu-id="8168d-118">Lorsqu’un objet est ajouté à un groupe d’administration.</span><span class="sxs-lookup"><span data-stu-id="8168d-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="8168d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-119">Attribute-Id</span></span>      | <span data-ttu-id="8168d-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="8168d-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="8168d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8168d-121">System-Id-Guid</span></span>    | <span data-ttu-id="8168d-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8168d-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="8168d-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8168d-123">Syntax</span></span>            | [<span data-ttu-id="8168d-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="8168d-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="8168d-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8168d-125">Implementations</span></span>

-   [<span data-ttu-id="8168d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8168d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8168d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8168d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8168d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8168d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8168d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8168d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8168d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8168d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8168d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8168d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8168d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8168d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8168d-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-133">Entry</span></span> | <span data-ttu-id="8168d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-137">System-Only</span></span>            | <span data-ttu-id="8168d-138">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-138">False</span></span>                                                                 |
| <span data-ttu-id="8168d-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-140">True</span></span>                                                                  |
| <span data-ttu-id="8168d-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-141">Is Indexed</span></span>             | <span data-ttu-id="8168d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-142">False</span></span>                                                                 |
| <span data-ttu-id="8168d-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-143">In Global Catalog</span></span>      | <span data-ttu-id="8168d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-144">False</span></span>                                                                 |
| <span data-ttu-id="8168d-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-149">Search-Flags</span></span>           | <span data-ttu-id="8168d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-151">System-Flags</span></span>           | <span data-ttu-id="8168d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-153">Classes used in</span></span>        | [<span data-ttu-id="8168d-154">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-155">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8168d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8168d-156">Windows Server 2003</span></span>



| <span data-ttu-id="8168d-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-157">Entry</span></span> | <span data-ttu-id="8168d-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-161">System-Only</span></span>            | <span data-ttu-id="8168d-162">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-162">False</span></span>                                                                 |
| <span data-ttu-id="8168d-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-164">True</span></span>                                                                  |
| <span data-ttu-id="8168d-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-165">Is Indexed</span></span>             | <span data-ttu-id="8168d-166">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-166">False</span></span>                                                                 |
| <span data-ttu-id="8168d-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-167">In Global Catalog</span></span>      | <span data-ttu-id="8168d-168">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-168">False</span></span>                                                                 |
| <span data-ttu-id="8168d-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-173">Search-Flags</span></span>           | <span data-ttu-id="8168d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-175">System-Flags</span></span>           | <span data-ttu-id="8168d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-177">Classes used in</span></span>        | [<span data-ttu-id="8168d-178">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8168d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8168d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8168d-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-181">Entry</span></span> | <span data-ttu-id="8168d-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-185">System-Only</span></span>            | <span data-ttu-id="8168d-186">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-186">False</span></span>                                                                 |
| <span data-ttu-id="8168d-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-188">True</span></span>                                                                  |
| <span data-ttu-id="8168d-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-189">Is Indexed</span></span>             | <span data-ttu-id="8168d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-190">False</span></span>                                                                 |
| <span data-ttu-id="8168d-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-191">In Global Catalog</span></span>      | <span data-ttu-id="8168d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-192">False</span></span>                                                                 |
| <span data-ttu-id="8168d-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-197">Search-Flags</span></span>           | <span data-ttu-id="8168d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-199">System-Flags</span></span>           | <span data-ttu-id="8168d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-201">Classes used in</span></span>        | [<span data-ttu-id="8168d-202">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-203">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8168d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8168d-204">Windows Server 2008</span></span>



| <span data-ttu-id="8168d-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-205">Entry</span></span> | <span data-ttu-id="8168d-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-209">System-Only</span></span>            | <span data-ttu-id="8168d-210">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-210">False</span></span>                                                                 |
| <span data-ttu-id="8168d-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-212">True</span></span>                                                                  |
| <span data-ttu-id="8168d-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-213">Is Indexed</span></span>             | <span data-ttu-id="8168d-214">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-214">False</span></span>                                                                 |
| <span data-ttu-id="8168d-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-215">In Global Catalog</span></span>      | <span data-ttu-id="8168d-216">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-216">False</span></span>                                                                 |
| <span data-ttu-id="8168d-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-221">Search-Flags</span></span>           | <span data-ttu-id="8168d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-223">System-Flags</span></span>           | <span data-ttu-id="8168d-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-225">Classes used in</span></span>        | [<span data-ttu-id="8168d-226">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-227">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8168d-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8168d-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8168d-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-229">Entry</span></span> | <span data-ttu-id="8168d-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-233">System-Only</span></span>            | <span data-ttu-id="8168d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-234">False</span></span>                                                                 |
| <span data-ttu-id="8168d-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-235">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-236">True</span></span>                                                                  |
| <span data-ttu-id="8168d-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-237">Is Indexed</span></span>             | <span data-ttu-id="8168d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-238">False</span></span>                                                                 |
| <span data-ttu-id="8168d-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-239">In Global Catalog</span></span>      | <span data-ttu-id="8168d-240">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-240">False</span></span>                                                                 |
| <span data-ttu-id="8168d-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-245">Search-Flags</span></span>           | <span data-ttu-id="8168d-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-247">System-Flags</span></span>           | <span data-ttu-id="8168d-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-249">Classes used in</span></span>        | [<span data-ttu-id="8168d-250">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-251">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8168d-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8168d-252">Windows Server 2012</span></span>



| <span data-ttu-id="8168d-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="8168d-253">Entry</span></span> | <span data-ttu-id="8168d-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="8168d-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8168d-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8168d-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8168d-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="8168d-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="8168d-257">System-Only</span></span>            | <span data-ttu-id="8168d-258">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-258">False</span></span>                                                                 |
| <span data-ttu-id="8168d-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8168d-259">Is-Single-Valued</span></span>       | <span data-ttu-id="8168d-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="8168d-260">True</span></span>                                                                  |
| <span data-ttu-id="8168d-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8168d-261">Is Indexed</span></span>             | <span data-ttu-id="8168d-262">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-262">False</span></span>                                                                 |
| <span data-ttu-id="8168d-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8168d-263">In Global Catalog</span></span>      | <span data-ttu-id="8168d-264">Faux</span><span class="sxs-lookup"><span data-stu-id="8168d-264">False</span></span>                                                                 |
| <span data-ttu-id="8168d-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8168d-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="8168d-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8168d-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="8168d-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8168d-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8168d-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="8168d-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-269">Search-Flags</span></span>           | <span data-ttu-id="8168d-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8168d-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="8168d-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8168d-271">System-Flags</span></span>           | <span data-ttu-id="8168d-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8168d-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="8168d-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8168d-273">Classes used in</span></span>        | [<span data-ttu-id="8168d-274">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8168d-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="8168d-275">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8168d-275">**User**</span></span>](c-user.md)<br/> |



 

 





