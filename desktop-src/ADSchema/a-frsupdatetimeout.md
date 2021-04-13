---
title: Attribut FRS-Update-Timeout
description: Durée maximale, en minutes, pendant laquelle attendre la fin de l’exécution d’une mise à jour.
ms.assetid: 0c06510e-d4a8-42f8-bf81-13a9f103e237
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut FRS-Update-Timeout
- Schéma AD de l’attribut fRSUpdateTimeout
topic_type:
- apiref
api_name:
- FRS-Update-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73730ec18942f98c07c0a4756bb8c7716e6abfd2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519930"
---
# <a name="frs-update-timeout-attribute"></a><span data-ttu-id="aebc1-105">Attribut FRS-Update-Timeout</span><span class="sxs-lookup"><span data-stu-id="aebc1-105">FRS-Update-Timeout attribute</span></span>

<span data-ttu-id="aebc1-106">Durée maximale, en minutes, pendant laquelle attendre la fin de l’exécution d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="aebc1-106">The maximum time, in minutes, to wait to complete an update before giving up.</span></span>



| <span data-ttu-id="aebc1-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-107">Entry</span></span> | <span data-ttu-id="aebc1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="aebc1-109">CN</span><span class="sxs-lookup"><span data-stu-id="aebc1-109">CN</span></span>                | <span data-ttu-id="aebc1-110">FRS-Update-Timeout</span><span class="sxs-lookup"><span data-stu-id="aebc1-110">FRS-Update-Timeout</span></span>                   |
| <span data-ttu-id="aebc1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aebc1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aebc1-112">fRSUpdateTimeout</span><span class="sxs-lookup"><span data-stu-id="aebc1-112">fRSUpdateTimeout</span></span>                     |
| <span data-ttu-id="aebc1-113">Taille</span><span class="sxs-lookup"><span data-stu-id="aebc1-113">Size</span></span>              | <span data-ttu-id="aebc1-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="aebc1-114">4 bytes</span></span>                              |
| <span data-ttu-id="aebc1-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="aebc1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="aebc1-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="aebc1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="aebc1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-117">Attribute-Id</span></span>      | <span data-ttu-id="aebc1-118">1.2.840.113556.1.4.485</span><span class="sxs-lookup"><span data-stu-id="aebc1-118">1.2.840.113556.1.4.485</span></span>               |
| <span data-ttu-id="aebc1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aebc1-119">System-Id-Guid</span></span>    | <span data-ttu-id="aebc1-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="aebc1-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span></span> |
| <span data-ttu-id="aebc1-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aebc1-121">Syntax</span></span>            | [<span data-ttu-id="aebc1-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="aebc1-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="aebc1-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="aebc1-123">Implementations</span></span>

-   [<span data-ttu-id="aebc1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aebc1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aebc1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aebc1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aebc1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aebc1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aebc1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aebc1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aebc1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aebc1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aebc1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aebc1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aebc1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aebc1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="aebc1-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-131">Entry</span></span> | <span data-ttu-id="aebc1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-133">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-134">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-135">System-Only</span></span>            | <span data-ttu-id="aebc1-136">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-136">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-138">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-139">Is Indexed</span></span>             | <span data-ttu-id="aebc1-140">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-140">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-141">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-142">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-142">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-144">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-145">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-146">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-147">Search-Flags</span></span>           | <span data-ttu-id="aebc1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-148">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-149">System-Flags</span></span>           | <span data-ttu-id="aebc1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-150">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-151">Classes used in</span></span>        | [<span data-ttu-id="aebc1-152">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-152">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-153">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-153">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aebc1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aebc1-154">Windows Server 2003</span></span>



| <span data-ttu-id="aebc1-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-155">Entry</span></span> | <span data-ttu-id="aebc1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-156">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-157">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-158">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-159">System-Only</span></span>            | <span data-ttu-id="aebc1-160">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-160">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-162">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-163">Is Indexed</span></span>             | <span data-ttu-id="aebc1-164">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-164">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-165">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-166">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-166">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-168">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-169">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-170">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-171">Search-Flags</span></span>           | <span data-ttu-id="aebc1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-172">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-173">System-Flags</span></span>           | <span data-ttu-id="aebc1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-174">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-175">Classes used in</span></span>        | [<span data-ttu-id="aebc1-176">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-176">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-177">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-177">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aebc1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aebc1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aebc1-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-179">Entry</span></span> | <span data-ttu-id="aebc1-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-180">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-181">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-182">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-183">System-Only</span></span>            | <span data-ttu-id="aebc1-184">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-184">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-186">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-187">Is Indexed</span></span>             | <span data-ttu-id="aebc1-188">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-188">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-189">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-190">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-190">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-192">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-193">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-194">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-195">Search-Flags</span></span>           | <span data-ttu-id="aebc1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-196">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-197">System-Flags</span></span>           | <span data-ttu-id="aebc1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-198">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-199">Classes used in</span></span>        | [<span data-ttu-id="aebc1-200">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-200">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-201">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-201">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aebc1-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aebc1-202">Windows Server 2008</span></span>



| <span data-ttu-id="aebc1-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-203">Entry</span></span> | <span data-ttu-id="aebc1-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-205">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-206">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-207">System-Only</span></span>            | <span data-ttu-id="aebc1-208">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-208">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-210">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-211">Is Indexed</span></span>             | <span data-ttu-id="aebc1-212">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-212">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-213">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-214">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-214">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-216">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-217">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-218">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-219">Search-Flags</span></span>           | <span data-ttu-id="aebc1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-220">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-221">System-Flags</span></span>           | <span data-ttu-id="aebc1-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-222">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-223">Classes used in</span></span>        | [<span data-ttu-id="aebc1-224">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-224">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-225">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-225">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aebc1-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aebc1-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aebc1-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-227">Entry</span></span> | <span data-ttu-id="aebc1-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-228">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-229">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-230">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-231">System-Only</span></span>            | <span data-ttu-id="aebc1-232">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-232">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-233">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-234">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-235">Is Indexed</span></span>             | <span data-ttu-id="aebc1-236">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-236">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-237">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-238">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-238">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-240">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-241">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-242">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-243">Search-Flags</span></span>           | <span data-ttu-id="aebc1-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-244">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-245">System-Flags</span></span>           | <span data-ttu-id="aebc1-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-246">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-247">Classes used in</span></span>        | [<span data-ttu-id="aebc1-248">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-248">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-249">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-249">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aebc1-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aebc1-250">Windows Server 2012</span></span>



| <span data-ttu-id="aebc1-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="aebc1-251">Entry</span></span> | <span data-ttu-id="aebc1-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebc1-252">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebc1-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aebc1-253">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aebc1-254">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="aebc1-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="aebc1-255">System-Only</span></span>            | <span data-ttu-id="aebc1-256">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-256">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aebc1-257">Is-Single-Valued</span></span>       | <span data-ttu-id="aebc1-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="aebc1-258">True</span></span>                                                                                                      |
| <span data-ttu-id="aebc1-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aebc1-259">Is Indexed</span></span>             | <span data-ttu-id="aebc1-260">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-260">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aebc1-261">In Global Catalog</span></span>      | <span data-ttu-id="aebc1-262">Faux</span><span class="sxs-lookup"><span data-stu-id="aebc1-262">False</span></span>                                                                                                     |
| <span data-ttu-id="aebc1-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aebc1-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="aebc1-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aebc1-264">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="aebc1-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aebc1-265">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aebc1-266">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="aebc1-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-267">Search-Flags</span></span>           | <span data-ttu-id="aebc1-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aebc1-268">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="aebc1-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aebc1-269">System-Flags</span></span>           | <span data-ttu-id="aebc1-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aebc1-270">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="aebc1-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aebc1-271">Classes used in</span></span>        | [<span data-ttu-id="aebc1-272">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="aebc1-272">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="aebc1-273">**NTFRS-abonné**</span><span class="sxs-lookup"><span data-stu-id="aebc1-273">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



 

 





