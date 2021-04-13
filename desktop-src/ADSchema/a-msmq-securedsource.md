---
title: MSMQ-Secured-attribut source
description: Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties. Il détermine si MSMQ accepte uniquement les messages provenant d’une source sécurisée (https, par exemple) pour cette file d’attente.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de source sécurisé MSMQ-
- Schéma AD d’attribut MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519769"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="af149-106">MSMQ-Secured-attribut source</span><span class="sxs-lookup"><span data-stu-id="af149-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="af149-107">Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="af149-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="af149-108">Il détermine si MSMQ accepte uniquement les messages provenant d’une source sécurisée (https, par exemple) pour cette file d’attente.</span><span class="sxs-lookup"><span data-stu-id="af149-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="af149-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-109">Entry</span></span> | <span data-ttu-id="af149-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="af149-111">CN</span><span class="sxs-lookup"><span data-stu-id="af149-111">CN</span></span>                | <span data-ttu-id="af149-112">MSMQ-sécurisé-source</span><span class="sxs-lookup"><span data-stu-id="af149-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="af149-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="af149-113">Ldap-Display-Name</span></span> | <span data-ttu-id="af149-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="af149-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="af149-115">Taille</span><span class="sxs-lookup"><span data-stu-id="af149-115">Size</span></span>              | <span data-ttu-id="af149-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="af149-116">4 bytes</span></span>                              |
| <span data-ttu-id="af149-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="af149-117">Update Privilege</span></span>  | <span data-ttu-id="af149-118">Propriétaire de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="af149-118">The queue owner.</span></span>                     |
| <span data-ttu-id="af149-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="af149-119">Update Frequency</span></span>  | <span data-ttu-id="af149-120">Lorsqu’une file d’attente est créée.</span><span class="sxs-lookup"><span data-stu-id="af149-120">When a queue is created.</span></span>             |
| <span data-ttu-id="af149-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af149-121">Attribute-Id</span></span>      | <span data-ttu-id="af149-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="af149-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="af149-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="af149-123">System-Id-Guid</span></span>    | <span data-ttu-id="af149-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="af149-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="af149-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af149-125">Syntax</span></span>            | [<span data-ttu-id="af149-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="af149-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="af149-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="af149-127">Implementations</span></span>

-   [<span data-ttu-id="af149-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af149-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af149-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af149-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af149-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af149-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af149-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af149-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af149-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af149-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="af149-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af149-133">Windows Server 2003</span></span>



| <span data-ttu-id="af149-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-134">Entry</span></span> | <span data-ttu-id="af149-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="af149-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="af149-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af149-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="af149-138">System-Only</span></span>            | <span data-ttu-id="af149-139">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-139">False</span></span>                                        |
| <span data-ttu-id="af149-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="af149-140">Is-Single-Valued</span></span>       | <span data-ttu-id="af149-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-141">True</span></span>                                         |
| <span data-ttu-id="af149-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="af149-142">Is Indexed</span></span>             | <span data-ttu-id="af149-143">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-143">False</span></span>                                        |
| <span data-ttu-id="af149-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="af149-144">In Global Catalog</span></span>      | <span data-ttu-id="af149-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-145">True</span></span>                                         |
| <span data-ttu-id="af149-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="af149-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="af149-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="af149-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="af149-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af149-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="af149-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af149-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="af149-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-150">Search-Flags</span></span>           | <span data-ttu-id="af149-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af149-151">0x00000000</span></span>                                   |
| <span data-ttu-id="af149-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-152">System-Flags</span></span>           | <span data-ttu-id="af149-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af149-153">0x00000010</span></span>                                   |
| <span data-ttu-id="af149-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="af149-154">Classes used in</span></span>        | [<span data-ttu-id="af149-155">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="af149-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af149-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af149-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af149-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-157">Entry</span></span> | <span data-ttu-id="af149-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="af149-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="af149-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af149-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="af149-161">System-Only</span></span>            | <span data-ttu-id="af149-162">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-162">False</span></span>                                        |
| <span data-ttu-id="af149-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="af149-163">Is-Single-Valued</span></span>       | <span data-ttu-id="af149-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-164">True</span></span>                                         |
| <span data-ttu-id="af149-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="af149-165">Is Indexed</span></span>             | <span data-ttu-id="af149-166">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-166">False</span></span>                                        |
| <span data-ttu-id="af149-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="af149-167">In Global Catalog</span></span>      | <span data-ttu-id="af149-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-168">True</span></span>                                         |
| <span data-ttu-id="af149-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="af149-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="af149-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="af149-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="af149-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af149-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="af149-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af149-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="af149-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-173">Search-Flags</span></span>           | <span data-ttu-id="af149-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af149-174">0x00000000</span></span>                                   |
| <span data-ttu-id="af149-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-175">System-Flags</span></span>           | <span data-ttu-id="af149-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af149-176">0x00000010</span></span>                                   |
| <span data-ttu-id="af149-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="af149-177">Classes used in</span></span>        | [<span data-ttu-id="af149-178">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="af149-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af149-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af149-179">Windows Server 2008</span></span>



| <span data-ttu-id="af149-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-180">Entry</span></span> | <span data-ttu-id="af149-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="af149-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="af149-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af149-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="af149-184">System-Only</span></span>            | <span data-ttu-id="af149-185">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-185">False</span></span>                                        |
| <span data-ttu-id="af149-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="af149-186">Is-Single-Valued</span></span>       | <span data-ttu-id="af149-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-187">True</span></span>                                         |
| <span data-ttu-id="af149-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="af149-188">Is Indexed</span></span>             | <span data-ttu-id="af149-189">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-189">False</span></span>                                        |
| <span data-ttu-id="af149-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="af149-190">In Global Catalog</span></span>      | <span data-ttu-id="af149-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-191">True</span></span>                                         |
| <span data-ttu-id="af149-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="af149-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="af149-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="af149-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="af149-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af149-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="af149-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af149-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="af149-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-196">Search-Flags</span></span>           | <span data-ttu-id="af149-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af149-197">0x00000000</span></span>                                   |
| <span data-ttu-id="af149-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-198">System-Flags</span></span>           | <span data-ttu-id="af149-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af149-199">0x00000010</span></span>                                   |
| <span data-ttu-id="af149-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="af149-200">Classes used in</span></span>        | [<span data-ttu-id="af149-201">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="af149-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af149-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af149-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af149-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-203">Entry</span></span> | <span data-ttu-id="af149-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="af149-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="af149-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af149-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="af149-207">System-Only</span></span>            | <span data-ttu-id="af149-208">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-208">False</span></span>                                        |
| <span data-ttu-id="af149-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="af149-209">Is-Single-Valued</span></span>       | <span data-ttu-id="af149-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-210">True</span></span>                                         |
| <span data-ttu-id="af149-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="af149-211">Is Indexed</span></span>             | <span data-ttu-id="af149-212">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-212">False</span></span>                                        |
| <span data-ttu-id="af149-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="af149-213">In Global Catalog</span></span>      | <span data-ttu-id="af149-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-214">True</span></span>                                         |
| <span data-ttu-id="af149-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="af149-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="af149-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="af149-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="af149-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af149-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="af149-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af149-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="af149-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-219">Search-Flags</span></span>           | <span data-ttu-id="af149-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af149-220">0x00000000</span></span>                                   |
| <span data-ttu-id="af149-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-221">System-Flags</span></span>           | <span data-ttu-id="af149-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af149-222">0x00000010</span></span>                                   |
| <span data-ttu-id="af149-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="af149-223">Classes used in</span></span>        | [<span data-ttu-id="af149-224">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="af149-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af149-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af149-225">Windows Server 2012</span></span>



| <span data-ttu-id="af149-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="af149-226">Entry</span></span> | <span data-ttu-id="af149-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="af149-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="af149-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="af149-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af149-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="af149-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="af149-230">System-Only</span></span>            | <span data-ttu-id="af149-231">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-231">False</span></span>                                        |
| <span data-ttu-id="af149-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="af149-232">Is-Single-Valued</span></span>       | <span data-ttu-id="af149-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-233">True</span></span>                                         |
| <span data-ttu-id="af149-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="af149-234">Is Indexed</span></span>             | <span data-ttu-id="af149-235">Faux</span><span class="sxs-lookup"><span data-stu-id="af149-235">False</span></span>                                        |
| <span data-ttu-id="af149-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="af149-236">In Global Catalog</span></span>      | <span data-ttu-id="af149-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="af149-237">True</span></span>                                         |
| <span data-ttu-id="af149-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="af149-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="af149-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="af149-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="af149-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af149-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="af149-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af149-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="af149-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-242">Search-Flags</span></span>           | <span data-ttu-id="af149-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af149-243">0x00000000</span></span>                                   |
| <span data-ttu-id="af149-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af149-244">System-Flags</span></span>           | <span data-ttu-id="af149-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af149-245">0x00000010</span></span>                                   |
| <span data-ttu-id="af149-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="af149-246">Classes used in</span></span>        | [<span data-ttu-id="af149-247">**MSMQ-file d’attente**</span><span class="sxs-lookup"><span data-stu-id="af149-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





