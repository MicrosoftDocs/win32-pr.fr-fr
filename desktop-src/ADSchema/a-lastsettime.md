---
title: Attribut Last-Set-Time
description: Heure de la dernière modification de la clé secrète.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Last-Set-Time
- Schéma AD de l’attribut lastSetTime
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385415"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="c2a5a-105">Attribut Last-Set-Time</span><span class="sxs-lookup"><span data-stu-id="c2a5a-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="c2a5a-106">Heure de la dernière modification de la clé secrète.</span><span class="sxs-lookup"><span data-stu-id="c2a5a-106">The last time the secret was changed.</span></span> <span data-ttu-id="c2a5a-107">Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="c2a5a-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="c2a5a-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-108">Entry</span></span> | <span data-ttu-id="c2a5a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c2a5a-110">CN</span><span class="sxs-lookup"><span data-stu-id="c2a5a-110">CN</span></span>                | <span data-ttu-id="c2a5a-111">Last-Set-Time</span><span class="sxs-lookup"><span data-stu-id="c2a5a-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="c2a5a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c2a5a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c2a5a-113">lastSetTime</span><span class="sxs-lookup"><span data-stu-id="c2a5a-113">lastSetTime</span></span>                          |
| <span data-ttu-id="c2a5a-114">Taille</span><span class="sxs-lookup"><span data-stu-id="c2a5a-114">Size</span></span>              | <span data-ttu-id="c2a5a-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="c2a5a-115">8 bytes</span></span>                              |
| <span data-ttu-id="c2a5a-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c2a5a-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c2a5a-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c2a5a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c2a5a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-118">Attribute-Id</span></span>      | <span data-ttu-id="c2a5a-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="c2a5a-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="c2a5a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2a5a-120">System-Id-Guid</span></span>    | <span data-ttu-id="c2a5a-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c2a5a-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c2a5a-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2a5a-122">Syntax</span></span>            | [<span data-ttu-id="c2a5a-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c2a5a-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c2a5a-124">Implementations</span></span>

-   [<span data-ttu-id="c2a5a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2a5a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2a5a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2a5a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2a5a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2a5a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2a5a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2a5a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c2a5a-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-132">Entry</span></span> | <span data-ttu-id="c2a5a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-136">System-Only</span></span>            | <span data-ttu-id="c2a5a-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-137">False</span></span>                                 |
| <span data-ttu-id="c2a5a-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-139">True</span></span>                                  |
| <span data-ttu-id="c2a5a-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-140">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-141">False</span></span>                                 |
| <span data-ttu-id="c2a5a-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-142">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-143">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-143">False</span></span>                                 |
| <span data-ttu-id="c2a5a-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-148">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-149">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-150">System-Flags</span></span>           | <span data-ttu-id="c2a5a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-151">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-152">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-153">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2a5a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2a5a-154">Windows Server 2003</span></span>



| <span data-ttu-id="c2a5a-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-155">Entry</span></span> | <span data-ttu-id="c2a5a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-159">System-Only</span></span>            | <span data-ttu-id="c2a5a-160">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-160">False</span></span>                                 |
| <span data-ttu-id="c2a5a-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-162">True</span></span>                                  |
| <span data-ttu-id="c2a5a-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-163">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-164">False</span></span>                                 |
| <span data-ttu-id="c2a5a-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-165">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-166">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-166">False</span></span>                                 |
| <span data-ttu-id="c2a5a-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-171">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-172">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-173">System-Flags</span></span>           | <span data-ttu-id="c2a5a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-174">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-175">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-176">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2a5a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2a5a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2a5a-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-178">Entry</span></span> | <span data-ttu-id="c2a5a-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-182">System-Only</span></span>            | <span data-ttu-id="c2a5a-183">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-183">False</span></span>                                 |
| <span data-ttu-id="c2a5a-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-185">True</span></span>                                  |
| <span data-ttu-id="c2a5a-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-186">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-187">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-187">False</span></span>                                 |
| <span data-ttu-id="c2a5a-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-188">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-189">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-189">False</span></span>                                 |
| <span data-ttu-id="c2a5a-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-194">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-195">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-196">System-Flags</span></span>           | <span data-ttu-id="c2a5a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-197">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-198">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-199">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2a5a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2a5a-200">Windows Server 2008</span></span>



| <span data-ttu-id="c2a5a-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-201">Entry</span></span> | <span data-ttu-id="c2a5a-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-205">System-Only</span></span>            | <span data-ttu-id="c2a5a-206">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-206">False</span></span>                                 |
| <span data-ttu-id="c2a5a-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-208">True</span></span>                                  |
| <span data-ttu-id="c2a5a-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-209">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-210">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-210">False</span></span>                                 |
| <span data-ttu-id="c2a5a-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-211">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-212">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-212">False</span></span>                                 |
| <span data-ttu-id="c2a5a-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-217">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-218">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-219">System-Flags</span></span>           | <span data-ttu-id="c2a5a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-220">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-221">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-222">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2a5a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2a5a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2a5a-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-224">Entry</span></span> | <span data-ttu-id="c2a5a-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-228">System-Only</span></span>            | <span data-ttu-id="c2a5a-229">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-229">False</span></span>                                 |
| <span data-ttu-id="c2a5a-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-231">True</span></span>                                  |
| <span data-ttu-id="c2a5a-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-232">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-233">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-233">False</span></span>                                 |
| <span data-ttu-id="c2a5a-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-234">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-235">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-235">False</span></span>                                 |
| <span data-ttu-id="c2a5a-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-240">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-241">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-242">System-Flags</span></span>           | <span data-ttu-id="c2a5a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-243">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-244">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-245">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2a5a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2a5a-246">Windows Server 2012</span></span>



| <span data-ttu-id="c2a5a-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2a5a-247">Entry</span></span> | <span data-ttu-id="c2a5a-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5a-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c2a5a-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2a5a-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a5a-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c2a5a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a5a-251">System-Only</span></span>            | <span data-ttu-id="c2a5a-252">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-252">False</span></span>                                 |
| <span data-ttu-id="c2a5a-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2a5a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a5a-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="c2a5a-254">True</span></span>                                  |
| <span data-ttu-id="c2a5a-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2a5a-255">Is Indexed</span></span>             | <span data-ttu-id="c2a5a-256">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-256">False</span></span>                                 |
| <span data-ttu-id="c2a5a-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2a5a-257">In Global Catalog</span></span>      | <span data-ttu-id="c2a5a-258">Faux</span><span class="sxs-lookup"><span data-stu-id="c2a5a-258">False</span></span>                                 |
| <span data-ttu-id="c2a5a-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2a5a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a5a-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2a5a-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c2a5a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a5a-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a5a-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="c2a5a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-263">Search-Flags</span></span>           | <span data-ttu-id="c2a5a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a5a-264">0x00000000</span></span>                            |
| <span data-ttu-id="c2a5a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a5a-265">System-Flags</span></span>           | <span data-ttu-id="c2a5a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a5a-266">0x00000010</span></span>                            |
| <span data-ttu-id="c2a5a-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2a5a-267">Classes used in</span></span>        | [<span data-ttu-id="c2a5a-268">**Secret**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





