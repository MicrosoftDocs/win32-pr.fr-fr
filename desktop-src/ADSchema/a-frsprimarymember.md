---
title: FRS-attribut de membre principal
description: Référence au membre principal d’un jeu de réplicas.
ms.assetid: a6b8017d-6700-43f3-a170-f4d56009c8f7
ms.tgt_platform: multiple
keywords:
- Schéma AD FRS-attribut de membre principal
- Schéma AD de l’attribut fRSPrimaryMember
topic_type:
- apiref
api_name:
- FRS-Primary-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d34113856fca12e21278ea405eb444d37494d8c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107080"
---
# <a name="frs-primary-member-attribute"></a><span data-ttu-id="dcccb-105">FRS-attribut de membre principal</span><span class="sxs-lookup"><span data-stu-id="dcccb-105">FRS-Primary-Member attribute</span></span>

<span data-ttu-id="dcccb-106">Référence au membre principal d’un jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="dcccb-106">Reference to the primary member of a replica set.</span></span>



| <span data-ttu-id="dcccb-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-107">Entry</span></span> | <span data-ttu-id="dcccb-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dcccb-109">CN</span><span class="sxs-lookup"><span data-stu-id="dcccb-109">CN</span></span>                | <span data-ttu-id="dcccb-110">FRS-principal-membre</span><span class="sxs-lookup"><span data-stu-id="dcccb-110">FRS-Primary-Member</span></span>                      |
| <span data-ttu-id="dcccb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dcccb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dcccb-112">fRSPrimaryMember</span><span class="sxs-lookup"><span data-stu-id="dcccb-112">fRSPrimaryMember</span></span>                        |
| <span data-ttu-id="dcccb-113">Taille</span><span class="sxs-lookup"><span data-stu-id="dcccb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="dcccb-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="dcccb-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="dcccb-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="dcccb-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dcccb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-116">Attribute-Id</span></span>      | <span data-ttu-id="dcccb-117">1.2.840.113556.1.4.878</span><span class="sxs-lookup"><span data-stu-id="dcccb-117">1.2.840.113556.1.4.878</span></span>                  |
| <span data-ttu-id="dcccb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dcccb-118">System-Id-Guid</span></span>    | <span data-ttu-id="dcccb-119">2a132581-9373-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="dcccb-119">2a132581-9373-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="dcccb-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcccb-120">Syntax</span></span>            | [<span data-ttu-id="dcccb-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dcccb-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dcccb-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="dcccb-122">Implementations</span></span>

-   [<span data-ttu-id="dcccb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dcccb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dcccb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dcccb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dcccb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dcccb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dcccb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dcccb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dcccb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dcccb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dcccb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dcccb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dcccb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dcccb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="dcccb-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-130">Entry</span></span> | <span data-ttu-id="dcccb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-132">Link-Id</span></span>                | <span data-ttu-id="dcccb-133">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-133">106</span></span>                                                       |
| <span data-ttu-id="dcccb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-135">System-Only</span></span>            | <span data-ttu-id="dcccb-136">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-136">False</span></span>                                                     |
| <span data-ttu-id="dcccb-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-138">True</span></span>                                                      |
| <span data-ttu-id="dcccb-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-139">Is Indexed</span></span>             | <span data-ttu-id="dcccb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-140">False</span></span>                                                     |
| <span data-ttu-id="dcccb-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-141">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-142">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-142">False</span></span>                                                     |
| <span data-ttu-id="dcccb-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-147">Search-Flags</span></span>           | <span data-ttu-id="dcccb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-148">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-149">System-Flags</span></span>           | <span data-ttu-id="dcccb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-150">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-151">Classes used in</span></span>        | [<span data-ttu-id="dcccb-152">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dcccb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dcccb-153">Windows Server 2003</span></span>



| <span data-ttu-id="dcccb-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-154">Entry</span></span> | <span data-ttu-id="dcccb-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-156">Link-Id</span></span>                | <span data-ttu-id="dcccb-157">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-157">106</span></span>                                                       |
| <span data-ttu-id="dcccb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-159">System-Only</span></span>            | <span data-ttu-id="dcccb-160">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-160">False</span></span>                                                     |
| <span data-ttu-id="dcccb-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-162">True</span></span>                                                      |
| <span data-ttu-id="dcccb-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-163">Is Indexed</span></span>             | <span data-ttu-id="dcccb-164">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-164">False</span></span>                                                     |
| <span data-ttu-id="dcccb-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-165">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-166">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-166">False</span></span>                                                     |
| <span data-ttu-id="dcccb-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-171">Search-Flags</span></span>           | <span data-ttu-id="dcccb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-172">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-173">System-Flags</span></span>           | <span data-ttu-id="dcccb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-174">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-175">Classes used in</span></span>        | [<span data-ttu-id="dcccb-176">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-176">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dcccb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dcccb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dcccb-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-178">Entry</span></span> | <span data-ttu-id="dcccb-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-180">Link-Id</span></span>                | <span data-ttu-id="dcccb-181">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-181">106</span></span>                                                       |
| <span data-ttu-id="dcccb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-183">System-Only</span></span>            | <span data-ttu-id="dcccb-184">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-184">False</span></span>                                                     |
| <span data-ttu-id="dcccb-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-186">True</span></span>                                                      |
| <span data-ttu-id="dcccb-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-187">Is Indexed</span></span>             | <span data-ttu-id="dcccb-188">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-188">False</span></span>                                                     |
| <span data-ttu-id="dcccb-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-189">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-190">False</span></span>                                                     |
| <span data-ttu-id="dcccb-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-195">Search-Flags</span></span>           | <span data-ttu-id="dcccb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-196">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-197">System-Flags</span></span>           | <span data-ttu-id="dcccb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-198">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-199">Classes used in</span></span>        | [<span data-ttu-id="dcccb-200">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-200">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dcccb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcccb-201">Windows Server 2008</span></span>



| <span data-ttu-id="dcccb-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-202">Entry</span></span> | <span data-ttu-id="dcccb-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-204">Link-Id</span></span>                | <span data-ttu-id="dcccb-205">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-205">106</span></span>                                                       |
| <span data-ttu-id="dcccb-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-207">System-Only</span></span>            | <span data-ttu-id="dcccb-208">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-208">False</span></span>                                                     |
| <span data-ttu-id="dcccb-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-209">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-210">True</span></span>                                                      |
| <span data-ttu-id="dcccb-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-211">Is Indexed</span></span>             | <span data-ttu-id="dcccb-212">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-212">False</span></span>                                                     |
| <span data-ttu-id="dcccb-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-213">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-214">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-214">False</span></span>                                                     |
| <span data-ttu-id="dcccb-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-219">Search-Flags</span></span>           | <span data-ttu-id="dcccb-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-220">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-221">System-Flags</span></span>           | <span data-ttu-id="dcccb-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-222">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-223">Classes used in</span></span>        | [<span data-ttu-id="dcccb-224">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-224">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dcccb-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dcccb-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dcccb-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-226">Entry</span></span> | <span data-ttu-id="dcccb-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-228">Link-Id</span></span>                | <span data-ttu-id="dcccb-229">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-229">106</span></span>                                                       |
| <span data-ttu-id="dcccb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-230">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-231">System-Only</span></span>            | <span data-ttu-id="dcccb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-232">False</span></span>                                                     |
| <span data-ttu-id="dcccb-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-234">True</span></span>                                                      |
| <span data-ttu-id="dcccb-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-235">Is Indexed</span></span>             | <span data-ttu-id="dcccb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-236">False</span></span>                                                     |
| <span data-ttu-id="dcccb-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-237">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-238">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-238">False</span></span>                                                     |
| <span data-ttu-id="dcccb-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-240">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-241">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-242">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-243">Search-Flags</span></span>           | <span data-ttu-id="dcccb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-244">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-245">System-Flags</span></span>           | <span data-ttu-id="dcccb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-246">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-247">Classes used in</span></span>        | [<span data-ttu-id="dcccb-248">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-248">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dcccb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dcccb-249">Windows Server 2012</span></span>



| <span data-ttu-id="dcccb-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="dcccb-250">Entry</span></span> | <span data-ttu-id="dcccb-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcccb-251">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dcccb-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dcccb-252">Link-Id</span></span>                | <span data-ttu-id="dcccb-253">106</span><span class="sxs-lookup"><span data-stu-id="dcccb-253">106</span></span>                                                       |
| <span data-ttu-id="dcccb-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcccb-254">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dcccb-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcccb-255">System-Only</span></span>            | <span data-ttu-id="dcccb-256">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-256">False</span></span>                                                     |
| <span data-ttu-id="dcccb-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dcccb-257">Is-Single-Valued</span></span>       | <span data-ttu-id="dcccb-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="dcccb-258">True</span></span>                                                      |
| <span data-ttu-id="dcccb-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dcccb-259">Is Indexed</span></span>             | <span data-ttu-id="dcccb-260">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-260">False</span></span>                                                     |
| <span data-ttu-id="dcccb-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dcccb-261">In Global Catalog</span></span>      | <span data-ttu-id="dcccb-262">Faux</span><span class="sxs-lookup"><span data-stu-id="dcccb-262">False</span></span>                                                     |
| <span data-ttu-id="dcccb-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dcccb-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcccb-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dcccb-264">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dcccb-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcccb-265">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcccb-266">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dcccb-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-267">Search-Flags</span></span>           | <span data-ttu-id="dcccb-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcccb-268">0x00000000</span></span>                                                |
| <span data-ttu-id="dcccb-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcccb-269">System-Flags</span></span>           | <span data-ttu-id="dcccb-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcccb-270">0x00000010</span></span>                                                |
| <span data-ttu-id="dcccb-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dcccb-271">Classes used in</span></span>        | [<span data-ttu-id="dcccb-272">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="dcccb-272">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





