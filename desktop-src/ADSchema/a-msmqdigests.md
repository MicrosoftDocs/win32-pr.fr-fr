---
title: Attribut MSMQ-Digests
description: Tableau des résumés des certificats correspondants dans l’attribut mSMQ-Sign-Certificates. Ils sont utilisés pour mapper un résumé dans un certificat.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut MSMQ-Digests
- Schéma AD de l’attribut mSMQDigests
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106513075"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="b41b2-106">Attribut MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="b41b2-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="b41b2-107">Tableau des résumés des certificats correspondants dans l’attribut mSMQ-Sign-Certificates.</span><span class="sxs-lookup"><span data-stu-id="b41b2-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="b41b2-108">Ils sont utilisés pour mapper un résumé dans un certificat.</span><span class="sxs-lookup"><span data-stu-id="b41b2-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="b41b2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-109">Entry</span></span> | <span data-ttu-id="b41b2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b41b2-111">CN</span><span class="sxs-lookup"><span data-stu-id="b41b2-111">CN</span></span>                | <span data-ttu-id="b41b2-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="b41b2-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="b41b2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b41b2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b41b2-114">mSMQDigests</span><span class="sxs-lookup"><span data-stu-id="b41b2-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="b41b2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="b41b2-115">Size</span></span>              | <span data-ttu-id="b41b2-116">Chaque condensé est de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="b41b2-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="b41b2-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b41b2-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b41b2-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b41b2-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b41b2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-119">Attribute-Id</span></span>      | <span data-ttu-id="b41b2-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="b41b2-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="b41b2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b41b2-121">System-Id-Guid</span></span>    | <span data-ttu-id="b41b2-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b41b2-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="b41b2-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b41b2-123">Syntax</span></span>            | [<span data-ttu-id="b41b2-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b41b2-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b41b2-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b41b2-125">Implementations</span></span>

-   [<span data-ttu-id="b41b2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b41b2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b41b2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b41b2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b41b2-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b41b2-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b41b2-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b41b2-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b41b2-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b41b2-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b41b2-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b41b2-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b41b2-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b41b2-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b41b2-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-133">Entry</span></span> | <span data-ttu-id="b41b2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-137">System-Only</span></span>            | <span data-ttu-id="b41b2-138">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-138">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-140">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-141">Is Indexed</span></span>             | <span data-ttu-id="b41b2-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-142">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-143">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-144">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-147">Range-Lower</span></span>            | <span data-ttu-id="b41b2-148">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-148">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-149">Range-Upper</span></span>            | <span data-ttu-id="b41b2-150">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-150">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-151">Search-Flags</span></span>           | <span data-ttu-id="b41b2-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-153">System-Flags</span></span>           | <span data-ttu-id="b41b2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-155">Classes used in</span></span>        | [<span data-ttu-id="b41b2-156">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b41b2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b41b2-158">Windows Server 2003</span></span>



| <span data-ttu-id="b41b2-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-159">Entry</span></span> | <span data-ttu-id="b41b2-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-163">System-Only</span></span>            | <span data-ttu-id="b41b2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-164">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-166">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-167">Is Indexed</span></span>             | <span data-ttu-id="b41b2-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-168">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-169">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-170">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-173">Range-Lower</span></span>            | <span data-ttu-id="b41b2-174">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-174">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-175">Range-Upper</span></span>            | <span data-ttu-id="b41b2-176">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-176">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-177">Search-Flags</span></span>           | <span data-ttu-id="b41b2-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-179">System-Flags</span></span>           | <span data-ttu-id="b41b2-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-181">Classes used in</span></span>        | [<span data-ttu-id="b41b2-182">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-183">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b41b2-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b41b2-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b41b2-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-185">Entry</span></span> | <span data-ttu-id="b41b2-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-189">System-Only</span></span>            | <span data-ttu-id="b41b2-190">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-190">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-191">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-192">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-192">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-193">Is Indexed</span></span>             | <span data-ttu-id="b41b2-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-194">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-195">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-196">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-199">Range-Lower</span></span>            | <span data-ttu-id="b41b2-200">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-200">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-201">Range-Upper</span></span>            | <span data-ttu-id="b41b2-202">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-202">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-203">Search-Flags</span></span>           | <span data-ttu-id="b41b2-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-205">System-Flags</span></span>           | <span data-ttu-id="b41b2-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-207">Classes used in</span></span>        | [<span data-ttu-id="b41b2-208">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-209">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b41b2-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b41b2-210">Windows Server 2008</span></span>



| <span data-ttu-id="b41b2-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-211">Entry</span></span> | <span data-ttu-id="b41b2-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-215">System-Only</span></span>            | <span data-ttu-id="b41b2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-216">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-218">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-218">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-219">Is Indexed</span></span>             | <span data-ttu-id="b41b2-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-220">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-221">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-222">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-222">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-225">Range-Lower</span></span>            | <span data-ttu-id="b41b2-226">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-226">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-227">Range-Upper</span></span>            | <span data-ttu-id="b41b2-228">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-228">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-229">Search-Flags</span></span>           | <span data-ttu-id="b41b2-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-231">System-Flags</span></span>           | <span data-ttu-id="b41b2-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-233">Classes used in</span></span>        | [<span data-ttu-id="b41b2-234">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-235">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b41b2-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b41b2-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b41b2-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-237">Entry</span></span> | <span data-ttu-id="b41b2-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-241">System-Only</span></span>            | <span data-ttu-id="b41b2-242">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-242">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-243">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-244">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-244">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-245">Is Indexed</span></span>             | <span data-ttu-id="b41b2-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-246">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-247">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-248">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-251">Range-Lower</span></span>            | <span data-ttu-id="b41b2-252">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-252">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-253">Range-Upper</span></span>            | <span data-ttu-id="b41b2-254">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-254">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-255">Search-Flags</span></span>           | <span data-ttu-id="b41b2-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-257">System-Flags</span></span>           | <span data-ttu-id="b41b2-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-259">Classes used in</span></span>        | [<span data-ttu-id="b41b2-260">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-261">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b41b2-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b41b2-262">Windows Server 2012</span></span>



| <span data-ttu-id="b41b2-263">Entrée</span><span class="sxs-lookup"><span data-stu-id="b41b2-263">Entry</span></span> | <span data-ttu-id="b41b2-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41b2-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b2-265">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b41b2-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b41b2-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="b41b2-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="b41b2-267">System-Only</span></span>            | <span data-ttu-id="b41b2-268">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-268">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-269">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b41b2-269">Is-Single-Valued</span></span>       | <span data-ttu-id="b41b2-270">Faux</span><span class="sxs-lookup"><span data-stu-id="b41b2-270">False</span></span>                                                                                         |
| <span data-ttu-id="b41b2-271">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b41b2-271">Is Indexed</span></span>             | <span data-ttu-id="b41b2-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-272">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-273">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b41b2-273">In Global Catalog</span></span>      | <span data-ttu-id="b41b2-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="b41b2-274">True</span></span>                                                                                          |
| <span data-ttu-id="b41b2-275">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b41b2-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="b41b2-276">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b41b2-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="b41b2-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b41b2-277">Range-Lower</span></span>            | <span data-ttu-id="b41b2-278">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-278">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b41b2-279">Range-Upper</span></span>            | <span data-ttu-id="b41b2-280">16</span><span class="sxs-lookup"><span data-stu-id="b41b2-280">16</span></span>                                                                                            |
| <span data-ttu-id="b41b2-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-281">Search-Flags</span></span>           | <span data-ttu-id="b41b2-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b41b2-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="b41b2-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b41b2-283">System-Flags</span></span>           | <span data-ttu-id="b41b2-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b41b2-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="b41b2-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b41b2-285">Classes used in</span></span>        | [<span data-ttu-id="b41b2-286">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="b41b2-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="b41b2-287">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b41b2-287">**User**</span></span>](c-user.md)<br/> |



 

 





