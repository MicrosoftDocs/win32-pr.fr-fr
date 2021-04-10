---
title: Attribut Seq-Notification
description: Cet attribut contient un compteur qui est incrémenté quotidiennement. Cette valeur de compteur est donnée au service de suivi des liaisons qui ajoute la valeur à ses volumes et aux fichiers sources de liaison lorsqu’ils sont actualisés. Le contrôleur de domaine gère cette valeur.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Seq-Notification
- Schéma AD de l’attribut seqNotification
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107536"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="f1d05-107">Attribut Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="f1d05-107">Seq-Notification attribute</span></span>

<span data-ttu-id="f1d05-108">Cet attribut contient un compteur qui est incrémenté quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="f1d05-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="f1d05-109">Cette valeur de compteur est donnée au service de suivi des liaisons qui ajoute la valeur à ses volumes et aux fichiers sources de liaison lorsqu’ils sont actualisés.</span><span class="sxs-lookup"><span data-stu-id="f1d05-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="f1d05-110">Le contrôleur de domaine gère cette valeur.</span><span class="sxs-lookup"><span data-stu-id="f1d05-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="f1d05-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-111">Entry</span></span> | <span data-ttu-id="f1d05-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f1d05-113">CN</span><span class="sxs-lookup"><span data-stu-id="f1d05-113">CN</span></span>                | <span data-ttu-id="f1d05-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="f1d05-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="f1d05-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1d05-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f1d05-116">seqNotification</span><span class="sxs-lookup"><span data-stu-id="f1d05-116">seqNotification</span></span>                      |
| <span data-ttu-id="f1d05-117">Taille</span><span class="sxs-lookup"><span data-stu-id="f1d05-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="f1d05-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f1d05-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f1d05-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f1d05-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f1d05-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-120">Attribute-Id</span></span>      | <span data-ttu-id="f1d05-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="f1d05-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="f1d05-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1d05-122">System-Id-Guid</span></span>    | <span data-ttu-id="f1d05-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f1d05-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="f1d05-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1d05-124">Syntax</span></span>            | [<span data-ttu-id="f1d05-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f1d05-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f1d05-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f1d05-126">Implementations</span></span>

-   [<span data-ttu-id="f1d05-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1d05-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1d05-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1d05-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1d05-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1d05-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1d05-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1d05-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1d05-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1d05-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1d05-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1d05-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1d05-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1d05-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f1d05-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-134">Entry</span></span> | <span data-ttu-id="f1d05-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-138">System-Only</span></span>            | <span data-ttu-id="f1d05-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-139">False</span></span>                                                          |
| <span data-ttu-id="f1d05-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-141">True</span></span>                                                           |
| <span data-ttu-id="f1d05-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-142">Is Indexed</span></span>             | <span data-ttu-id="f1d05-143">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-143">False</span></span>                                                          |
| <span data-ttu-id="f1d05-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-144">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-145">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-145">False</span></span>                                                          |
| <span data-ttu-id="f1d05-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-150">Search-Flags</span></span>           | <span data-ttu-id="f1d05-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-152">System-Flags</span></span>           | <span data-ttu-id="f1d05-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-154">Classes used in</span></span>        | [<span data-ttu-id="f1d05-155">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1d05-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1d05-156">Windows Server 2003</span></span>



| <span data-ttu-id="f1d05-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-157">Entry</span></span> | <span data-ttu-id="f1d05-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-161">System-Only</span></span>            | <span data-ttu-id="f1d05-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-162">False</span></span>                                                          |
| <span data-ttu-id="f1d05-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-164">True</span></span>                                                           |
| <span data-ttu-id="f1d05-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-165">Is Indexed</span></span>             | <span data-ttu-id="f1d05-166">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-166">False</span></span>                                                          |
| <span data-ttu-id="f1d05-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-167">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-168">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-168">False</span></span>                                                          |
| <span data-ttu-id="f1d05-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-173">Search-Flags</span></span>           | <span data-ttu-id="f1d05-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-175">System-Flags</span></span>           | <span data-ttu-id="f1d05-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-177">Classes used in</span></span>        | [<span data-ttu-id="f1d05-178">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1d05-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1d05-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1d05-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-180">Entry</span></span> | <span data-ttu-id="f1d05-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-184">System-Only</span></span>            | <span data-ttu-id="f1d05-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-185">False</span></span>                                                          |
| <span data-ttu-id="f1d05-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-187">True</span></span>                                                           |
| <span data-ttu-id="f1d05-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-188">Is Indexed</span></span>             | <span data-ttu-id="f1d05-189">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-189">False</span></span>                                                          |
| <span data-ttu-id="f1d05-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-190">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-191">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-191">False</span></span>                                                          |
| <span data-ttu-id="f1d05-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-196">Search-Flags</span></span>           | <span data-ttu-id="f1d05-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-198">System-Flags</span></span>           | <span data-ttu-id="f1d05-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-200">Classes used in</span></span>        | [<span data-ttu-id="f1d05-201">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1d05-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1d05-202">Windows Server 2008</span></span>



| <span data-ttu-id="f1d05-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-203">Entry</span></span> | <span data-ttu-id="f1d05-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-207">System-Only</span></span>            | <span data-ttu-id="f1d05-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-208">False</span></span>                                                          |
| <span data-ttu-id="f1d05-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-210">True</span></span>                                                           |
| <span data-ttu-id="f1d05-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-211">Is Indexed</span></span>             | <span data-ttu-id="f1d05-212">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-212">False</span></span>                                                          |
| <span data-ttu-id="f1d05-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-213">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-214">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-214">False</span></span>                                                          |
| <span data-ttu-id="f1d05-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-219">Search-Flags</span></span>           | <span data-ttu-id="f1d05-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-221">System-Flags</span></span>           | <span data-ttu-id="f1d05-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-223">Classes used in</span></span>        | [<span data-ttu-id="f1d05-224">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1d05-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1d05-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1d05-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-226">Entry</span></span> | <span data-ttu-id="f1d05-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-230">System-Only</span></span>            | <span data-ttu-id="f1d05-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-231">False</span></span>                                                          |
| <span data-ttu-id="f1d05-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-233">True</span></span>                                                           |
| <span data-ttu-id="f1d05-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-234">Is Indexed</span></span>             | <span data-ttu-id="f1d05-235">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-235">False</span></span>                                                          |
| <span data-ttu-id="f1d05-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-236">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-237">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-237">False</span></span>                                                          |
| <span data-ttu-id="f1d05-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-242">Search-Flags</span></span>           | <span data-ttu-id="f1d05-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-244">System-Flags</span></span>           | <span data-ttu-id="f1d05-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-246">Classes used in</span></span>        | [<span data-ttu-id="f1d05-247">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1d05-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1d05-248">Windows Server 2012</span></span>



| <span data-ttu-id="f1d05-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1d05-249">Entry</span></span> | <span data-ttu-id="f1d05-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d05-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f1d05-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1d05-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1d05-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f1d05-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1d05-253">System-Only</span></span>            | <span data-ttu-id="f1d05-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-254">False</span></span>                                                          |
| <span data-ttu-id="f1d05-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1d05-255">Is-Single-Valued</span></span>       | <span data-ttu-id="f1d05-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1d05-256">True</span></span>                                                           |
| <span data-ttu-id="f1d05-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1d05-257">Is Indexed</span></span>             | <span data-ttu-id="f1d05-258">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-258">False</span></span>                                                          |
| <span data-ttu-id="f1d05-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1d05-259">In Global Catalog</span></span>      | <span data-ttu-id="f1d05-260">Faux</span><span class="sxs-lookup"><span data-stu-id="f1d05-260">False</span></span>                                                          |
| <span data-ttu-id="f1d05-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1d05-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1d05-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1d05-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f1d05-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1d05-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1d05-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="f1d05-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-265">Search-Flags</span></span>           | <span data-ttu-id="f1d05-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1d05-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="f1d05-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1d05-267">System-Flags</span></span>           | <span data-ttu-id="f1d05-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1d05-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="f1d05-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1d05-269">Classes used in</span></span>        | [<span data-ttu-id="f1d05-270">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="f1d05-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





