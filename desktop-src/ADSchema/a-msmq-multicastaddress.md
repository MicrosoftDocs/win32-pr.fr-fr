---
title: Attribut MSMQ-Multicast-Address
description: Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties. Il détermine si MSMQ accepte les messages d’une adresse de multidiffusion.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MSMQ-Multicast-Address
- Schéma AD d’attribut MSMQ-MulticastAddress
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519770"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="9274f-106">Attribut MSMQ-Multicast-Address</span><span class="sxs-lookup"><span data-stu-id="9274f-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="9274f-107">Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="9274f-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="9274f-108">Il détermine si MSMQ accepte les messages d’une adresse de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="9274f-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="9274f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-109">Entry</span></span> | <span data-ttu-id="9274f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9274f-111">CN</span><span class="sxs-lookup"><span data-stu-id="9274f-111">CN</span></span>                | <span data-ttu-id="9274f-112">MSMQ-Multicast-Address</span><span class="sxs-lookup"><span data-stu-id="9274f-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="9274f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9274f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9274f-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="9274f-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="9274f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="9274f-115">Size</span></span>              | <span data-ttu-id="9274f-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="9274f-116">4 bytes</span></span>                                     |
| <span data-ttu-id="9274f-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9274f-117">Update Privilege</span></span>  | <span data-ttu-id="9274f-118">Propriétaire de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9274f-118">The queue owner.</span></span>                            |
| <span data-ttu-id="9274f-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9274f-119">Update Frequency</span></span>  | <span data-ttu-id="9274f-120">Lorsqu’une file d’attente est créée.</span><span class="sxs-lookup"><span data-stu-id="9274f-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="9274f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-121">Attribute-Id</span></span>      | <span data-ttu-id="9274f-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="9274f-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="9274f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9274f-123">System-Id-Guid</span></span>    | <span data-ttu-id="9274f-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="9274f-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="9274f-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9274f-125">Syntax</span></span>            | [<span data-ttu-id="9274f-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9274f-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9274f-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9274f-127">Implementations</span></span>

-   [<span data-ttu-id="9274f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9274f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9274f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9274f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9274f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9274f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9274f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9274f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9274f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9274f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9274f-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9274f-133">Windows Server 2003</span></span>



| <span data-ttu-id="9274f-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-134">Entry</span></span> | <span data-ttu-id="9274f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9274f-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9274f-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9274f-138">System-Only</span></span>            | <span data-ttu-id="9274f-139">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-139">False</span></span>                                        |
| <span data-ttu-id="9274f-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9274f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9274f-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-141">True</span></span>                                         |
| <span data-ttu-id="9274f-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9274f-142">Is Indexed</span></span>             | <span data-ttu-id="9274f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-143">False</span></span>                                        |
| <span data-ttu-id="9274f-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9274f-144">In Global Catalog</span></span>      | <span data-ttu-id="9274f-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-145">True</span></span>                                         |
| <span data-ttu-id="9274f-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9274f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9274f-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9274f-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9274f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9274f-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9274f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9274f-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9274f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-150">Search-Flags</span></span>           | <span data-ttu-id="9274f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9274f-151">0x00000000</span></span>                                   |
| <span data-ttu-id="9274f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-152">System-Flags</span></span>           | <span data-ttu-id="9274f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9274f-153">0x00000010</span></span>                                   |
| <span data-ttu-id="9274f-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9274f-154">Classes used in</span></span>        | [<span data-ttu-id="9274f-155">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9274f-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9274f-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9274f-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9274f-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-157">Entry</span></span> | <span data-ttu-id="9274f-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9274f-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9274f-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9274f-161">System-Only</span></span>            | <span data-ttu-id="9274f-162">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-162">False</span></span>                                        |
| <span data-ttu-id="9274f-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9274f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9274f-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-164">True</span></span>                                         |
| <span data-ttu-id="9274f-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9274f-165">Is Indexed</span></span>             | <span data-ttu-id="9274f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-166">False</span></span>                                        |
| <span data-ttu-id="9274f-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9274f-167">In Global Catalog</span></span>      | <span data-ttu-id="9274f-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-168">True</span></span>                                         |
| <span data-ttu-id="9274f-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9274f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9274f-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9274f-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9274f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9274f-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9274f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9274f-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9274f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-173">Search-Flags</span></span>           | <span data-ttu-id="9274f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9274f-174">0x00000000</span></span>                                   |
| <span data-ttu-id="9274f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-175">System-Flags</span></span>           | <span data-ttu-id="9274f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9274f-176">0x00000010</span></span>                                   |
| <span data-ttu-id="9274f-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9274f-177">Classes used in</span></span>        | [<span data-ttu-id="9274f-178">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9274f-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9274f-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9274f-179">Windows Server 2008</span></span>



| <span data-ttu-id="9274f-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-180">Entry</span></span> | <span data-ttu-id="9274f-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9274f-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9274f-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9274f-184">System-Only</span></span>            | <span data-ttu-id="9274f-185">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-185">False</span></span>                                        |
| <span data-ttu-id="9274f-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9274f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9274f-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-187">True</span></span>                                         |
| <span data-ttu-id="9274f-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9274f-188">Is Indexed</span></span>             | <span data-ttu-id="9274f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-189">False</span></span>                                        |
| <span data-ttu-id="9274f-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9274f-190">In Global Catalog</span></span>      | <span data-ttu-id="9274f-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-191">True</span></span>                                         |
| <span data-ttu-id="9274f-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9274f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9274f-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9274f-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9274f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9274f-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9274f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9274f-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9274f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-196">Search-Flags</span></span>           | <span data-ttu-id="9274f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9274f-197">0x00000000</span></span>                                   |
| <span data-ttu-id="9274f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-198">System-Flags</span></span>           | <span data-ttu-id="9274f-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9274f-199">0x00000010</span></span>                                   |
| <span data-ttu-id="9274f-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9274f-200">Classes used in</span></span>        | [<span data-ttu-id="9274f-201">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9274f-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9274f-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9274f-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9274f-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-203">Entry</span></span> | <span data-ttu-id="9274f-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9274f-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9274f-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9274f-207">System-Only</span></span>            | <span data-ttu-id="9274f-208">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-208">False</span></span>                                        |
| <span data-ttu-id="9274f-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9274f-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9274f-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-210">True</span></span>                                         |
| <span data-ttu-id="9274f-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9274f-211">Is Indexed</span></span>             | <span data-ttu-id="9274f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-212">False</span></span>                                        |
| <span data-ttu-id="9274f-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9274f-213">In Global Catalog</span></span>      | <span data-ttu-id="9274f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-214">True</span></span>                                         |
| <span data-ttu-id="9274f-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9274f-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9274f-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9274f-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9274f-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9274f-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9274f-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9274f-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9274f-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-219">Search-Flags</span></span>           | <span data-ttu-id="9274f-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9274f-220">0x00000000</span></span>                                   |
| <span data-ttu-id="9274f-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-221">System-Flags</span></span>           | <span data-ttu-id="9274f-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9274f-222">0x00000010</span></span>                                   |
| <span data-ttu-id="9274f-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9274f-223">Classes used in</span></span>        | [<span data-ttu-id="9274f-224">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9274f-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9274f-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9274f-225">Windows Server 2012</span></span>



| <span data-ttu-id="9274f-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="9274f-226">Entry</span></span> | <span data-ttu-id="9274f-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="9274f-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9274f-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9274f-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9274f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9274f-230">System-Only</span></span>            | <span data-ttu-id="9274f-231">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-231">False</span></span>                                        |
| <span data-ttu-id="9274f-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9274f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9274f-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-233">True</span></span>                                         |
| <span data-ttu-id="9274f-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9274f-234">Is Indexed</span></span>             | <span data-ttu-id="9274f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="9274f-235">False</span></span>                                        |
| <span data-ttu-id="9274f-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9274f-236">In Global Catalog</span></span>      | <span data-ttu-id="9274f-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="9274f-237">True</span></span>                                         |
| <span data-ttu-id="9274f-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9274f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9274f-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9274f-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9274f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9274f-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9274f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9274f-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9274f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-242">Search-Flags</span></span>           | <span data-ttu-id="9274f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9274f-243">0x00000000</span></span>                                   |
| <span data-ttu-id="9274f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9274f-244">System-Flags</span></span>           | <span data-ttu-id="9274f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9274f-245">0x00000010</span></span>                                   |
| <span data-ttu-id="9274f-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9274f-246">Classes used in</span></span>        | [<span data-ttu-id="9274f-247">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="9274f-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





