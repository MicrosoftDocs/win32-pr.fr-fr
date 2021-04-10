---
title: Attribut Invocation-Id
description: Utilisé pour identifier de manière unique chaque annuaire Microsoft Exchange Server dans l’organisation.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Invocation-Id
- Schéma AD de l’attribut d’invocation
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107029"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="8b861-105">Attribut Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-105">Invocation-Id attribute</span></span>

<span data-ttu-id="8b861-106">Utilisé pour identifier de manière unique chaque annuaire Microsoft Exchange Server dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8b861-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="8b861-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-107">Entry</span></span> | <span data-ttu-id="8b861-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="8b861-109">CN</span><span class="sxs-lookup"><span data-stu-id="8b861-109">CN</span></span>                | <span data-ttu-id="8b861-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="8b861-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8b861-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8b861-112">invocationId</span><span class="sxs-lookup"><span data-stu-id="8b861-112">invocationId</span></span>                                          |
| <span data-ttu-id="8b861-113">Taille</span><span class="sxs-lookup"><span data-stu-id="8b861-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="8b861-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8b861-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="8b861-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8b861-115">Update Frequency</span></span>  | <span data-ttu-id="8b861-116">Lors de l’installation du serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="8b861-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="8b861-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-117">Attribute-Id</span></span>      | <span data-ttu-id="8b861-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="8b861-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="8b861-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b861-119">System-Id-Guid</span></span>    | <span data-ttu-id="8b861-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8b861-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="8b861-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b861-121">Syntax</span></span>            | [<span data-ttu-id="8b861-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="8b861-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="8b861-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8b861-123">Implementations</span></span>

-   [<span data-ttu-id="8b861-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b861-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b861-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b861-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b861-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8b861-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8b861-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b861-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b861-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b861-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b861-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b861-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b861-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b861-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b861-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b861-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8b861-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-132">Entry</span></span> | <span data-ttu-id="8b861-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-135">MAPI-Id</span></span>                | <span data-ttu-id="8b861-136">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-136">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-137">System-Only</span></span>            | <span data-ttu-id="8b861-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-138">True</span></span>                                     |
| <span data-ttu-id="8b861-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-140">True</span></span>                                     |
| <span data-ttu-id="8b861-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-141">Is Indexed</span></span>             | <span data-ttu-id="8b861-142">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-142">False</span></span>                                    |
| <span data-ttu-id="8b861-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-143">In Global Catalog</span></span>      | <span data-ttu-id="8b861-144">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-144">False</span></span>                                    |
| <span data-ttu-id="8b861-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-149">Search-Flags</span></span>           | <span data-ttu-id="8b861-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b861-150">0x00000000</span></span>                               |
| <span data-ttu-id="8b861-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-151">System-Flags</span></span>           | <span data-ttu-id="8b861-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-152">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-153">Classes used in</span></span>        | [<span data-ttu-id="8b861-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b861-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b861-155">Windows Server 2003</span></span>



| <span data-ttu-id="8b861-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-156">Entry</span></span> | <span data-ttu-id="8b861-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-159">MAPI-Id</span></span>                | <span data-ttu-id="8b861-160">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-160">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-161">System-Only</span></span>            | <span data-ttu-id="8b861-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-162">True</span></span>                                     |
| <span data-ttu-id="8b861-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-164">True</span></span>                                     |
| <span data-ttu-id="8b861-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-165">Is Indexed</span></span>             | <span data-ttu-id="8b861-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-166">True</span></span>                                     |
| <span data-ttu-id="8b861-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-167">In Global Catalog</span></span>      | <span data-ttu-id="8b861-168">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-168">False</span></span>                                    |
| <span data-ttu-id="8b861-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-173">Search-Flags</span></span>           | <span data-ttu-id="8b861-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-174">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-175">System-Flags</span></span>           | <span data-ttu-id="8b861-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-176">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-177">Classes used in</span></span>        | [<span data-ttu-id="8b861-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8b861-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="8b861-179">ADAM</span></span>



| <span data-ttu-id="8b861-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-180">Entry</span></span> | <span data-ttu-id="8b861-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-183">MAPI-Id</span></span>                | <span data-ttu-id="8b861-184">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-184">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-185">System-Only</span></span>            | <span data-ttu-id="8b861-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-186">True</span></span>                                     |
| <span data-ttu-id="8b861-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-188">True</span></span>                                     |
| <span data-ttu-id="8b861-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-189">Is Indexed</span></span>             | <span data-ttu-id="8b861-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-190">True</span></span>                                     |
| <span data-ttu-id="8b861-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-191">In Global Catalog</span></span>      | <span data-ttu-id="8b861-192">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-192">False</span></span>                                    |
| <span data-ttu-id="8b861-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-197">Search-Flags</span></span>           | <span data-ttu-id="8b861-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-198">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-199">System-Flags</span></span>           | <span data-ttu-id="8b861-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-200">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-201">Classes used in</span></span>        | [<span data-ttu-id="8b861-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b861-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b861-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b861-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-204">Entry</span></span> | <span data-ttu-id="8b861-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-207">MAPI-Id</span></span>                | <span data-ttu-id="8b861-208">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-208">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-209">System-Only</span></span>            | <span data-ttu-id="8b861-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-210">True</span></span>                                     |
| <span data-ttu-id="8b861-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-212">True</span></span>                                     |
| <span data-ttu-id="8b861-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-213">Is Indexed</span></span>             | <span data-ttu-id="8b861-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-214">True</span></span>                                     |
| <span data-ttu-id="8b861-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-215">In Global Catalog</span></span>      | <span data-ttu-id="8b861-216">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-216">False</span></span>                                    |
| <span data-ttu-id="8b861-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-221">Search-Flags</span></span>           | <span data-ttu-id="8b861-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-222">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-223">System-Flags</span></span>           | <span data-ttu-id="8b861-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-224">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-225">Classes used in</span></span>        | [<span data-ttu-id="8b861-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b861-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b861-227">Windows Server 2008</span></span>



| <span data-ttu-id="8b861-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-228">Entry</span></span> | <span data-ttu-id="8b861-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-231">MAPI-Id</span></span>                | <span data-ttu-id="8b861-232">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-232">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-233">System-Only</span></span>            | <span data-ttu-id="8b861-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-234">True</span></span>                                     |
| <span data-ttu-id="8b861-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-235">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-236">True</span></span>                                     |
| <span data-ttu-id="8b861-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-237">Is Indexed</span></span>             | <span data-ttu-id="8b861-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-238">True</span></span>                                     |
| <span data-ttu-id="8b861-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-239">In Global Catalog</span></span>      | <span data-ttu-id="8b861-240">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-240">False</span></span>                                    |
| <span data-ttu-id="8b861-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-245">Search-Flags</span></span>           | <span data-ttu-id="8b861-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-246">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-247">System-Flags</span></span>           | <span data-ttu-id="8b861-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-248">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-249">Classes used in</span></span>        | [<span data-ttu-id="8b861-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b861-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b861-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b861-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-252">Entry</span></span> | <span data-ttu-id="8b861-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-255">MAPI-Id</span></span>                | <span data-ttu-id="8b861-256">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-256">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-257">System-Only</span></span>            | <span data-ttu-id="8b861-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-258">True</span></span>                                     |
| <span data-ttu-id="8b861-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-259">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-260">True</span></span>                                     |
| <span data-ttu-id="8b861-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-261">Is Indexed</span></span>             | <span data-ttu-id="8b861-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-262">True</span></span>                                     |
| <span data-ttu-id="8b861-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-263">In Global Catalog</span></span>      | <span data-ttu-id="8b861-264">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-264">False</span></span>                                    |
| <span data-ttu-id="8b861-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-269">Search-Flags</span></span>           | <span data-ttu-id="8b861-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-270">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-271">System-Flags</span></span>           | <span data-ttu-id="8b861-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-272">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-273">Classes used in</span></span>        | [<span data-ttu-id="8b861-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b861-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b861-275">Windows Server 2012</span></span>



| <span data-ttu-id="8b861-276">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b861-276">Entry</span></span> | <span data-ttu-id="8b861-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b861-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b861-278">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b861-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b861-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b861-279">MAPI-Id</span></span>                | <span data-ttu-id="8b861-280">0x80BF</span><span class="sxs-lookup"><span data-stu-id="8b861-280">0x80BF</span></span>                                   |
| <span data-ttu-id="8b861-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b861-281">System-Only</span></span>            | <span data-ttu-id="8b861-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-282">True</span></span>                                     |
| <span data-ttu-id="8b861-283">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b861-283">Is-Single-Valued</span></span>       | <span data-ttu-id="8b861-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-284">True</span></span>                                     |
| <span data-ttu-id="8b861-285">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b861-285">Is Indexed</span></span>             | <span data-ttu-id="8b861-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b861-286">True</span></span>                                     |
| <span data-ttu-id="8b861-287">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b861-287">In Global Catalog</span></span>      | <span data-ttu-id="8b861-288">Faux</span><span class="sxs-lookup"><span data-stu-id="8b861-288">False</span></span>                                    |
| <span data-ttu-id="8b861-289">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b861-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b861-290">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b861-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b861-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b861-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b861-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b861-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b861-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-293">Search-Flags</span></span>           | <span data-ttu-id="8b861-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b861-294">0x00000001</span></span>                               |
| <span data-ttu-id="8b861-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b861-295">System-Flags</span></span>           | <span data-ttu-id="8b861-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b861-296">0x00000010</span></span>                               |
| <span data-ttu-id="8b861-297">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b861-297">Classes used in</span></span>        | [<span data-ttu-id="8b861-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b861-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





