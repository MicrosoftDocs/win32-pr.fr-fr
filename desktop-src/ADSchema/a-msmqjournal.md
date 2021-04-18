---
title: Attribut MSMQ-Journal
description: Indique si les messages récupérés à partir de la file d’attente doivent être conservés dans le journal.
ms.assetid: fb1f73eb-57f4-413f-bd7a-9dfd5e5c797f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut MSMQ-Journal
- Schéma AD de l’attribut mSMQJournal
topic_type:
- apiref
api_name:
- MSMQ-Journal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a28e7740e41f8209e37345e934a36d10512bc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516125"
---
# <a name="msmq-journal-attribute"></a><span data-ttu-id="53256-105">Attribut MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="53256-105">MSMQ-Journal attribute</span></span>

<span data-ttu-id="53256-106">Indique si les messages récupérés à partir de la file d’attente doivent être conservés dans le journal.</span><span class="sxs-lookup"><span data-stu-id="53256-106">Indicates whether messages retrieved form the queue should be kept in journal.</span></span>



| <span data-ttu-id="53256-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-107">Entry</span></span> | <span data-ttu-id="53256-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="53256-109">CN</span><span class="sxs-lookup"><span data-stu-id="53256-109">CN</span></span>                | <span data-ttu-id="53256-110">MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="53256-110">MSMQ-Journal</span></span>                         |
| <span data-ttu-id="53256-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53256-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53256-112">mSMQJournal</span><span class="sxs-lookup"><span data-stu-id="53256-112">mSMQJournal</span></span>                          |
| <span data-ttu-id="53256-113">Taille</span><span class="sxs-lookup"><span data-stu-id="53256-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="53256-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="53256-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="53256-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="53256-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="53256-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53256-116">Attribute-Id</span></span>      | <span data-ttu-id="53256-117">1.2.840.113556.1.4.918</span><span class="sxs-lookup"><span data-stu-id="53256-117">1.2.840.113556.1.4.918</span></span>               |
| <span data-ttu-id="53256-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53256-118">System-Id-Guid</span></span>    | <span data-ttu-id="53256-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="53256-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="53256-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53256-120">Syntax</span></span>            | [<span data-ttu-id="53256-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="53256-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="53256-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="53256-122">Implementations</span></span>

-   [<span data-ttu-id="53256-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53256-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53256-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53256-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53256-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53256-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53256-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53256-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53256-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53256-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53256-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53256-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53256-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53256-129">Windows 2000 Server</span></span>



| <span data-ttu-id="53256-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-130">Entry</span></span> | <span data-ttu-id="53256-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-134">System-Only</span></span>            | <span data-ttu-id="53256-135">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-135">False</span></span>                                        |
| <span data-ttu-id="53256-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-136">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-137">True</span></span>                                         |
| <span data-ttu-id="53256-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-138">Is Indexed</span></span>             | <span data-ttu-id="53256-139">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-139">False</span></span>                                        |
| <span data-ttu-id="53256-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-140">In Global Catalog</span></span>      | <span data-ttu-id="53256-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-141">True</span></span>                                         |
| <span data-ttu-id="53256-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-146">Search-Flags</span></span>           | <span data-ttu-id="53256-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-147">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-148">System-Flags</span></span>           | <span data-ttu-id="53256-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-149">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-150">Classes used in</span></span>        | [<span data-ttu-id="53256-151">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53256-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53256-152">Windows Server 2003</span></span>



| <span data-ttu-id="53256-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-153">Entry</span></span> | <span data-ttu-id="53256-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-157">System-Only</span></span>            | <span data-ttu-id="53256-158">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-158">False</span></span>                                        |
| <span data-ttu-id="53256-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-159">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-160">True</span></span>                                         |
| <span data-ttu-id="53256-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-161">Is Indexed</span></span>             | <span data-ttu-id="53256-162">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-162">False</span></span>                                        |
| <span data-ttu-id="53256-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-163">In Global Catalog</span></span>      | <span data-ttu-id="53256-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-164">True</span></span>                                         |
| <span data-ttu-id="53256-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-169">Search-Flags</span></span>           | <span data-ttu-id="53256-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-170">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-171">System-Flags</span></span>           | <span data-ttu-id="53256-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-172">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-173">Classes used in</span></span>        | [<span data-ttu-id="53256-174">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53256-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53256-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53256-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-176">Entry</span></span> | <span data-ttu-id="53256-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-180">System-Only</span></span>            | <span data-ttu-id="53256-181">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-181">False</span></span>                                        |
| <span data-ttu-id="53256-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-182">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-183">True</span></span>                                         |
| <span data-ttu-id="53256-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-184">Is Indexed</span></span>             | <span data-ttu-id="53256-185">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-185">False</span></span>                                        |
| <span data-ttu-id="53256-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-186">In Global Catalog</span></span>      | <span data-ttu-id="53256-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-187">True</span></span>                                         |
| <span data-ttu-id="53256-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-192">Search-Flags</span></span>           | <span data-ttu-id="53256-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-193">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-194">System-Flags</span></span>           | <span data-ttu-id="53256-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-195">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-196">Classes used in</span></span>        | [<span data-ttu-id="53256-197">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53256-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53256-198">Windows Server 2008</span></span>



| <span data-ttu-id="53256-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-199">Entry</span></span> | <span data-ttu-id="53256-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-203">System-Only</span></span>            | <span data-ttu-id="53256-204">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-204">False</span></span>                                        |
| <span data-ttu-id="53256-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-205">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-206">True</span></span>                                         |
| <span data-ttu-id="53256-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-207">Is Indexed</span></span>             | <span data-ttu-id="53256-208">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-208">False</span></span>                                        |
| <span data-ttu-id="53256-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-209">In Global Catalog</span></span>      | <span data-ttu-id="53256-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-210">True</span></span>                                         |
| <span data-ttu-id="53256-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-215">Search-Flags</span></span>           | <span data-ttu-id="53256-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-216">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-217">System-Flags</span></span>           | <span data-ttu-id="53256-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-218">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-219">Classes used in</span></span>        | [<span data-ttu-id="53256-220">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53256-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53256-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53256-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-222">Entry</span></span> | <span data-ttu-id="53256-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-226">System-Only</span></span>            | <span data-ttu-id="53256-227">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-227">False</span></span>                                        |
| <span data-ttu-id="53256-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-228">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-229">True</span></span>                                         |
| <span data-ttu-id="53256-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-230">Is Indexed</span></span>             | <span data-ttu-id="53256-231">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-231">False</span></span>                                        |
| <span data-ttu-id="53256-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-232">In Global Catalog</span></span>      | <span data-ttu-id="53256-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-233">True</span></span>                                         |
| <span data-ttu-id="53256-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-238">Search-Flags</span></span>           | <span data-ttu-id="53256-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-239">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-240">System-Flags</span></span>           | <span data-ttu-id="53256-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-241">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-242">Classes used in</span></span>        | [<span data-ttu-id="53256-243">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53256-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53256-244">Windows Server 2012</span></span>



| <span data-ttu-id="53256-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="53256-245">Entry</span></span> | <span data-ttu-id="53256-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="53256-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53256-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53256-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53256-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53256-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="53256-249">System-Only</span></span>            | <span data-ttu-id="53256-250">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-250">False</span></span>                                        |
| <span data-ttu-id="53256-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53256-251">Is-Single-Valued</span></span>       | <span data-ttu-id="53256-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-252">True</span></span>                                         |
| <span data-ttu-id="53256-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53256-253">Is Indexed</span></span>             | <span data-ttu-id="53256-254">Faux</span><span class="sxs-lookup"><span data-stu-id="53256-254">False</span></span>                                        |
| <span data-ttu-id="53256-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53256-255">In Global Catalog</span></span>      | <span data-ttu-id="53256-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="53256-256">True</span></span>                                         |
| <span data-ttu-id="53256-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53256-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="53256-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53256-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53256-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53256-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53256-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53256-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53256-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-261">Search-Flags</span></span>           | <span data-ttu-id="53256-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53256-262">0x00000000</span></span>                                   |
| <span data-ttu-id="53256-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53256-263">System-Flags</span></span>           | <span data-ttu-id="53256-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53256-264">0x00000010</span></span>                                   |
| <span data-ttu-id="53256-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53256-265">Classes used in</span></span>        | [<span data-ttu-id="53256-266">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="53256-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





