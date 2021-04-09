---
title: A-attribut-partiel-réplica-NC
description: Frère vers a-Master-NC. Contient-partial-Replica-NC reflète le nom unique de tous les autres NC de domaine qui ont été répliqués dans un catalogue global.
ms.assetid: 2501bbb3-74b5-4604-b0c0-8653fc092e1c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut a-partial-Replica-NC
- Schéma AD de l’attribut hasPartialReplicaNCs
topic_type:
- apiref
api_name:
- Has-Partial-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f284df094c909b01b88a4853ed7c4a41dee9f31a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744220"
---
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="f50b1-106">A-attribut-partiel-réplica-NC</span><span class="sxs-lookup"><span data-stu-id="f50b1-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="f50b1-107">Frère vers a-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="f50b1-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="f50b1-108">Contient-partial-Replica-NC reflète le nom unique de tous les autres NC de domaine qui ont été répliqués dans un catalogue global.</span><span class="sxs-lookup"><span data-stu-id="f50b1-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="f50b1-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-109">Entry</span></span> | <span data-ttu-id="f50b1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f50b1-111">CN</span><span class="sxs-lookup"><span data-stu-id="f50b1-111">CN</span></span>                | <span data-ttu-id="f50b1-112">Contient-partiel-conplica-NC</span><span class="sxs-lookup"><span data-stu-id="f50b1-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="f50b1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f50b1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f50b1-114">hasPartialReplicaNCs</span><span class="sxs-lookup"><span data-stu-id="f50b1-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="f50b1-115">Taille</span><span class="sxs-lookup"><span data-stu-id="f50b1-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="f50b1-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f50b1-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f50b1-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f50b1-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f50b1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-118">Attribute-Id</span></span>      | <span data-ttu-id="f50b1-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="f50b1-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="f50b1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f50b1-120">System-Id-Guid</span></span>    | <span data-ttu-id="f50b1-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f50b1-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="f50b1-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f50b1-122">Syntax</span></span>            | [<span data-ttu-id="f50b1-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f50b1-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f50b1-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f50b1-124">Implementations</span></span>

-   [<span data-ttu-id="f50b1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f50b1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f50b1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f50b1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f50b1-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f50b1-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f50b1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f50b1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f50b1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f50b1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f50b1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f50b1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f50b1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f50b1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f50b1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f50b1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f50b1-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-133">Entry</span></span> | <span data-ttu-id="f50b1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-135">Link-Id</span></span>                | <span data-ttu-id="f50b1-136">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-136">74</span></span>                                       |
| <span data-ttu-id="f50b1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-137">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-138">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-138">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-139">System-Only</span></span>            | <span data-ttu-id="f50b1-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-140">True</span></span>                                     |
| <span data-ttu-id="f50b1-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-142">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-142">False</span></span>                                    |
| <span data-ttu-id="f50b1-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-143">Is Indexed</span></span>             | <span data-ttu-id="f50b1-144">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-144">False</span></span>                                    |
| <span data-ttu-id="f50b1-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-145">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-146">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-146">False</span></span>                                    |
| <span data-ttu-id="f50b1-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-151">Search-Flags</span></span>           | <span data-ttu-id="f50b1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-152">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-153">System-Flags</span></span>           | <span data-ttu-id="f50b1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-154">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-155">Classes used in</span></span>        | [<span data-ttu-id="f50b1-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f50b1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f50b1-157">Windows Server 2003</span></span>



| <span data-ttu-id="f50b1-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-158">Entry</span></span> | <span data-ttu-id="f50b1-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-160">Link-Id</span></span>                | <span data-ttu-id="f50b1-161">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-161">74</span></span>                                       |
| <span data-ttu-id="f50b1-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-162">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-163">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-163">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-164">System-Only</span></span>            | <span data-ttu-id="f50b1-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-165">True</span></span>                                     |
| <span data-ttu-id="f50b1-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-167">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-167">False</span></span>                                    |
| <span data-ttu-id="f50b1-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-168">Is Indexed</span></span>             | <span data-ttu-id="f50b1-169">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-169">False</span></span>                                    |
| <span data-ttu-id="f50b1-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-170">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-171">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-171">False</span></span>                                    |
| <span data-ttu-id="f50b1-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-176">Search-Flags</span></span>           | <span data-ttu-id="f50b1-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-177">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-178">System-Flags</span></span>           | <span data-ttu-id="f50b1-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-179">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-180">Classes used in</span></span>        | [<span data-ttu-id="f50b1-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f50b1-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="f50b1-182">ADAM</span></span>



| <span data-ttu-id="f50b1-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-183">Entry</span></span> | <span data-ttu-id="f50b1-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-185">Link-Id</span></span>                | <span data-ttu-id="f50b1-186">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-186">74</span></span>                                       |
| <span data-ttu-id="f50b1-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-187">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-188">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-188">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-189">System-Only</span></span>            | <span data-ttu-id="f50b1-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-190">True</span></span>                                     |
| <span data-ttu-id="f50b1-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-192">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-192">False</span></span>                                    |
| <span data-ttu-id="f50b1-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-193">Is Indexed</span></span>             | <span data-ttu-id="f50b1-194">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-194">False</span></span>                                    |
| <span data-ttu-id="f50b1-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-195">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-196">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-196">False</span></span>                                    |
| <span data-ttu-id="f50b1-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-201">Search-Flags</span></span>           | <span data-ttu-id="f50b1-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-202">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-203">System-Flags</span></span>           | <span data-ttu-id="f50b1-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-204">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-205">Classes used in</span></span>        | [<span data-ttu-id="f50b1-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f50b1-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f50b1-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f50b1-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-208">Entry</span></span> | <span data-ttu-id="f50b1-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-210">Link-Id</span></span>                | <span data-ttu-id="f50b1-211">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-211">74</span></span>                                       |
| <span data-ttu-id="f50b1-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-212">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-213">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-213">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-214">System-Only</span></span>            | <span data-ttu-id="f50b1-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-215">True</span></span>                                     |
| <span data-ttu-id="f50b1-216">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-216">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-217">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-217">False</span></span>                                    |
| <span data-ttu-id="f50b1-218">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-218">Is Indexed</span></span>             | <span data-ttu-id="f50b1-219">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-219">False</span></span>                                    |
| <span data-ttu-id="f50b1-220">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-220">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-221">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-221">False</span></span>                                    |
| <span data-ttu-id="f50b1-222">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-223">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-226">Search-Flags</span></span>           | <span data-ttu-id="f50b1-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-227">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-228">System-Flags</span></span>           | <span data-ttu-id="f50b1-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-229">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-230">Classes used in</span></span>        | [<span data-ttu-id="f50b1-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f50b1-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f50b1-232">Windows Server 2008</span></span>



| <span data-ttu-id="f50b1-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-233">Entry</span></span> | <span data-ttu-id="f50b1-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-235">Link-Id</span></span>                | <span data-ttu-id="f50b1-236">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-236">74</span></span>                                       |
| <span data-ttu-id="f50b1-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-237">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-238">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-238">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-239">System-Only</span></span>            | <span data-ttu-id="f50b1-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-240">True</span></span>                                     |
| <span data-ttu-id="f50b1-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-241">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-242">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-242">False</span></span>                                    |
| <span data-ttu-id="f50b1-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-243">Is Indexed</span></span>             | <span data-ttu-id="f50b1-244">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-244">False</span></span>                                    |
| <span data-ttu-id="f50b1-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-245">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-246">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-246">False</span></span>                                    |
| <span data-ttu-id="f50b1-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-251">Search-Flags</span></span>           | <span data-ttu-id="f50b1-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-252">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-253">System-Flags</span></span>           | <span data-ttu-id="f50b1-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-254">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-255">Classes used in</span></span>        | [<span data-ttu-id="f50b1-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f50b1-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f50b1-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f50b1-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-258">Entry</span></span> | <span data-ttu-id="f50b1-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-260">Link-Id</span></span>                | <span data-ttu-id="f50b1-261">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-261">74</span></span>                                       |
| <span data-ttu-id="f50b1-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-262">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-263">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-263">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-264">System-Only</span></span>            | <span data-ttu-id="f50b1-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-265">True</span></span>                                     |
| <span data-ttu-id="f50b1-266">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-266">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-267">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-267">False</span></span>                                    |
| <span data-ttu-id="f50b1-268">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-268">Is Indexed</span></span>             | <span data-ttu-id="f50b1-269">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-269">False</span></span>                                    |
| <span data-ttu-id="f50b1-270">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-270">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-271">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-271">False</span></span>                                    |
| <span data-ttu-id="f50b1-272">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-273">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-276">Search-Flags</span></span>           | <span data-ttu-id="f50b1-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-277">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-278">System-Flags</span></span>           | <span data-ttu-id="f50b1-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-279">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-280">Classes used in</span></span>        | [<span data-ttu-id="f50b1-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f50b1-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f50b1-282">Windows Server 2012</span></span>



| <span data-ttu-id="f50b1-283">Entrée</span><span class="sxs-lookup"><span data-stu-id="f50b1-283">Entry</span></span> | <span data-ttu-id="f50b1-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50b1-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f50b1-285">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f50b1-285">Link-Id</span></span>                | <span data-ttu-id="f50b1-286">74</span><span class="sxs-lookup"><span data-stu-id="f50b1-286">74</span></span>                                       |
| <span data-ttu-id="f50b1-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f50b1-287">MAPI-Id</span></span>                | <span data-ttu-id="f50b1-288">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f50b1-288">0x80B5</span></span>                                   |
| <span data-ttu-id="f50b1-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="f50b1-289">System-Only</span></span>            | <span data-ttu-id="f50b1-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="f50b1-290">True</span></span>                                     |
| <span data-ttu-id="f50b1-291">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f50b1-291">Is-Single-Valued</span></span>       | <span data-ttu-id="f50b1-292">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-292">False</span></span>                                    |
| <span data-ttu-id="f50b1-293">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f50b1-293">Is Indexed</span></span>             | <span data-ttu-id="f50b1-294">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-294">False</span></span>                                    |
| <span data-ttu-id="f50b1-295">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f50b1-295">In Global Catalog</span></span>      | <span data-ttu-id="f50b1-296">Faux</span><span class="sxs-lookup"><span data-stu-id="f50b1-296">False</span></span>                                    |
| <span data-ttu-id="f50b1-297">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f50b1-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="f50b1-298">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f50b1-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f50b1-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f50b1-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f50b1-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f50b1-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-301">Search-Flags</span></span>           | <span data-ttu-id="f50b1-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f50b1-302">0x00000000</span></span>                               |
| <span data-ttu-id="f50b1-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f50b1-303">System-Flags</span></span>           | <span data-ttu-id="f50b1-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50b1-304">0x00000010</span></span>                               |
| <span data-ttu-id="f50b1-305">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f50b1-305">Classes used in</span></span>        | [<span data-ttu-id="f50b1-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f50b1-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





