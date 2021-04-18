---
title: Attribut de période de garbage-coll.
description: Cet attribut se trouve dans le service d’annuaire CN, CN Windows NT, CN Services, CN Configuration,... dessin. Il représente le temps, en heures, entre les exécutions de garbage collection du service d’annuaire.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de période de nettoyage de la mémoire
- Schéma AD de l’attribut garbageCollPeriod
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509143"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="03243-106">Attribut de période de garbage-coll.</span><span class="sxs-lookup"><span data-stu-id="03243-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="03243-107">Cet attribut se trouve dans le dossier CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration,... dessin.</span><span class="sxs-lookup"><span data-stu-id="03243-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="03243-108">Il représente le temps, en heures, entre les exécutions de garbage collection du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="03243-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="03243-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-109">Entry</span></span> | <span data-ttu-id="03243-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="03243-111">CN</span><span class="sxs-lookup"><span data-stu-id="03243-111">CN</span></span>                | <span data-ttu-id="03243-112">Garbage-coll-period</span><span class="sxs-lookup"><span data-stu-id="03243-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="03243-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03243-113">Ldap-Display-Name</span></span> | <span data-ttu-id="03243-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="03243-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="03243-115">Taille</span><span class="sxs-lookup"><span data-stu-id="03243-115">Size</span></span>              | <span data-ttu-id="03243-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="03243-116">4 bytes</span></span>                              |
| <span data-ttu-id="03243-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="03243-117">Update Privilege</span></span>  | <span data-ttu-id="03243-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="03243-118">Domain administrator</span></span>                 |
| <span data-ttu-id="03243-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="03243-119">Update Frequency</span></span>  | <span data-ttu-id="03243-120">Très rare.</span><span class="sxs-lookup"><span data-stu-id="03243-120">Very rare.</span></span>                           |
| <span data-ttu-id="03243-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03243-121">Attribute-Id</span></span>      | <span data-ttu-id="03243-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="03243-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="03243-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03243-123">System-Id-Guid</span></span>    | <span data-ttu-id="03243-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="03243-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="03243-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03243-125">Syntax</span></span>            | [<span data-ttu-id="03243-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03243-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="03243-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="03243-127">Implementations</span></span>

-   [<span data-ttu-id="03243-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03243-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03243-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03243-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03243-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="03243-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="03243-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03243-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03243-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03243-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03243-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03243-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03243-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03243-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03243-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03243-135">Windows 2000 Server</span></span>



| <span data-ttu-id="03243-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-136">Entry</span></span> | <span data-ttu-id="03243-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-139">MAPI-Id</span></span>                | <span data-ttu-id="03243-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-141">System-Only</span></span>            | <span data-ttu-id="03243-142">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-142">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-143">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-144">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-145">Is Indexed</span></span>             | <span data-ttu-id="03243-146">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-146">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-147">In Global Catalog</span></span>      | <span data-ttu-id="03243-148">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-148">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-153">Search-Flags</span></span>           | <span data-ttu-id="03243-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-155">System-Flags</span></span>           | <span data-ttu-id="03243-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-157">Classes used in</span></span>        | [<span data-ttu-id="03243-158">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-159">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03243-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03243-160">Windows Server 2003</span></span>



| <span data-ttu-id="03243-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-161">Entry</span></span> | <span data-ttu-id="03243-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-164">MAPI-Id</span></span>                | <span data-ttu-id="03243-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-166">System-Only</span></span>            | <span data-ttu-id="03243-167">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-167">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-168">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-169">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-170">Is Indexed</span></span>             | <span data-ttu-id="03243-171">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-171">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-172">In Global Catalog</span></span>      | <span data-ttu-id="03243-173">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-173">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-178">Search-Flags</span></span>           | <span data-ttu-id="03243-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-180">System-Flags</span></span>           | <span data-ttu-id="03243-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-182">Classes used in</span></span>        | [<span data-ttu-id="03243-183">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-184">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="03243-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="03243-185">ADAM</span></span>



| <span data-ttu-id="03243-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-186">Entry</span></span> | <span data-ttu-id="03243-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="03243-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="03243-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-189">MAPI-Id</span></span>                | <span data-ttu-id="03243-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-190">0x80AF</span></span>                                           |
| <span data-ttu-id="03243-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-191">System-Only</span></span>            | <span data-ttu-id="03243-192">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-192">False</span></span>                                            |
| <span data-ttu-id="03243-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-193">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-194">True</span></span>                                             |
| <span data-ttu-id="03243-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-195">Is Indexed</span></span>             | <span data-ttu-id="03243-196">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-196">False</span></span>                                            |
| <span data-ttu-id="03243-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-197">In Global Catalog</span></span>      | <span data-ttu-id="03243-198">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-198">False</span></span>                                            |
| <span data-ttu-id="03243-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="03243-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="03243-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="03243-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-203">Search-Flags</span></span>           | <span data-ttu-id="03243-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-204">0x00000000</span></span>                                       |
| <span data-ttu-id="03243-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-205">System-Flags</span></span>           | <span data-ttu-id="03243-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-206">0x00000010</span></span>                                       |
| <span data-ttu-id="03243-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-207">Classes used in</span></span>        | [<span data-ttu-id="03243-208">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03243-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03243-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03243-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-210">Entry</span></span> | <span data-ttu-id="03243-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-213">MAPI-Id</span></span>                | <span data-ttu-id="03243-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-215">System-Only</span></span>            | <span data-ttu-id="03243-216">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-216">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-217">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-218">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-219">Is Indexed</span></span>             | <span data-ttu-id="03243-220">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-220">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-221">In Global Catalog</span></span>      | <span data-ttu-id="03243-222">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-222">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-227">Search-Flags</span></span>           | <span data-ttu-id="03243-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-229">System-Flags</span></span>           | <span data-ttu-id="03243-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-231">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-231">Classes used in</span></span>        | [<span data-ttu-id="03243-232">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-233">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03243-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03243-234">Windows Server 2008</span></span>



| <span data-ttu-id="03243-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-235">Entry</span></span> | <span data-ttu-id="03243-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-238">MAPI-Id</span></span>                | <span data-ttu-id="03243-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-240">System-Only</span></span>            | <span data-ttu-id="03243-241">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-241">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-242">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-242">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-243">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-244">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-244">Is Indexed</span></span>             | <span data-ttu-id="03243-245">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-245">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-246">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-246">In Global Catalog</span></span>      | <span data-ttu-id="03243-247">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-247">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-248">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-249">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-252">Search-Flags</span></span>           | <span data-ttu-id="03243-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-254">System-Flags</span></span>           | <span data-ttu-id="03243-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-256">Classes used in</span></span>        | [<span data-ttu-id="03243-257">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-258">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03243-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03243-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03243-260">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-260">Entry</span></span> | <span data-ttu-id="03243-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-262">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-263">MAPI-Id</span></span>                | <span data-ttu-id="03243-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-265">System-Only</span></span>            | <span data-ttu-id="03243-266">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-266">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-267">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-267">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-268">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-269">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-269">Is Indexed</span></span>             | <span data-ttu-id="03243-270">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-270">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-271">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-271">In Global Catalog</span></span>      | <span data-ttu-id="03243-272">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-272">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-273">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-274">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-277">Search-Flags</span></span>           | <span data-ttu-id="03243-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-279">System-Flags</span></span>           | <span data-ttu-id="03243-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-281">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-281">Classes used in</span></span>        | [<span data-ttu-id="03243-282">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-283">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03243-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03243-284">Windows Server 2012</span></span>



| <span data-ttu-id="03243-285">Entrée</span><span class="sxs-lookup"><span data-stu-id="03243-285">Entry</span></span> | <span data-ttu-id="03243-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="03243-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03243-287">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03243-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="03243-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03243-288">MAPI-Id</span></span>                | <span data-ttu-id="03243-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="03243-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="03243-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="03243-290">System-Only</span></span>            | <span data-ttu-id="03243-291">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-291">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-292">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03243-292">Is-Single-Valued</span></span>       | <span data-ttu-id="03243-293">Vrai</span><span class="sxs-lookup"><span data-stu-id="03243-293">True</span></span>                                                                                                  |
| <span data-ttu-id="03243-294">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03243-294">Is Indexed</span></span>             | <span data-ttu-id="03243-295">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-295">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-296">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03243-296">In Global Catalog</span></span>      | <span data-ttu-id="03243-297">Faux</span><span class="sxs-lookup"><span data-stu-id="03243-297">False</span></span>                                                                                                 |
| <span data-ttu-id="03243-298">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03243-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="03243-299">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03243-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="03243-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03243-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03243-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="03243-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-302">Search-Flags</span></span>           | <span data-ttu-id="03243-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03243-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="03243-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03243-304">System-Flags</span></span>           | <span data-ttu-id="03243-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03243-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="03243-306">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03243-306">Classes used in</span></span>        | [<span data-ttu-id="03243-307">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="03243-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="03243-308">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="03243-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





