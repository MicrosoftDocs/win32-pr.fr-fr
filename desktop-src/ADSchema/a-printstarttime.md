---
title: Attribut Print-Start-Time
description: Heure à laquelle une file d’attente à l’impression commence à traiter les travaux.
ms.assetid: 748d98a7-cef8-4a6d-9310-1f14667b2912
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Print-Start-Time
- Schéma AD de l’attribut printStartTime
topic_type:
- apiref
api_name:
- Print-Start-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1898bace41a795231585505da3f15d208bde264
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744933"
---
# <a name="print-start-time-attribute"></a><span data-ttu-id="2a4f7-105">Attribut Print-Start-Time</span><span class="sxs-lookup"><span data-stu-id="2a4f7-105">Print-Start-Time attribute</span></span>

<span data-ttu-id="2a4f7-106">Heure à laquelle une file d’attente à l’impression commence à traiter les travaux.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-106">The time a print queue begins servicing jobs.</span></span>



| <span data-ttu-id="2a4f7-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-107">Entry</span></span> | <span data-ttu-id="2a4f7-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2a4f7-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a4f7-109">CN</span></span>                | <span data-ttu-id="2a4f7-110">Print-Start-Time</span><span class="sxs-lookup"><span data-stu-id="2a4f7-110">Print-Start-Time</span></span>                     |
| <span data-ttu-id="2a4f7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2a4f7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a4f7-112">printStartTime</span><span class="sxs-lookup"><span data-stu-id="2a4f7-112">printStartTime</span></span>                       |
| <span data-ttu-id="2a4f7-113">Taille</span><span class="sxs-lookup"><span data-stu-id="2a4f7-113">Size</span></span>              | <span data-ttu-id="2a4f7-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="2a4f7-114">4 bytes</span></span>                              |
| <span data-ttu-id="2a4f7-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2a4f7-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2a4f7-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2a4f7-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2a4f7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-117">Attribute-Id</span></span>      | <span data-ttu-id="2a4f7-118">1.2.840.113556.1.4.233</span><span class="sxs-lookup"><span data-stu-id="2a4f7-118">1.2.840.113556.1.4.233</span></span>               |
| <span data-ttu-id="2a4f7-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2a4f7-119">System-Id-Guid</span></span>    | <span data-ttu-id="2a4f7-120">281416c9-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2a4f7-120">281416c9-1968-11d0-a28f-00aa003049e2</span></span> |
| <span data-ttu-id="2a4f7-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a4f7-121">Syntax</span></span>            | [<span data-ttu-id="2a4f7-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2a4f7-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2a4f7-123">Implementations</span></span>

-   [<span data-ttu-id="2a4f7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a4f7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a4f7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a4f7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a4f7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a4f7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a4f7-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a4f7-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2a4f7-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-131">Entry</span></span> | <span data-ttu-id="2a4f7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-135">System-Only</span></span>            | <span data-ttu-id="2a4f7-136">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-136">False</span></span>                                          |
| <span data-ttu-id="2a4f7-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-138">True</span></span>                                           |
| <span data-ttu-id="2a4f7-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-139">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-140">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-140">False</span></span>                                          |
| <span data-ttu-id="2a4f7-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-141">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-142">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-142">False</span></span>                                          |
| <span data-ttu-id="2a4f7-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-147">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-148">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-149">System-Flags</span></span>           | <span data-ttu-id="2a4f7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-150">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-151">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-152">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a4f7-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a4f7-153">Windows Server 2003</span></span>



| <span data-ttu-id="2a4f7-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-154">Entry</span></span> | <span data-ttu-id="2a4f7-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-158">System-Only</span></span>            | <span data-ttu-id="2a4f7-159">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-159">False</span></span>                                          |
| <span data-ttu-id="2a4f7-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-161">True</span></span>                                           |
| <span data-ttu-id="2a4f7-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-162">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-163">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-163">False</span></span>                                          |
| <span data-ttu-id="2a4f7-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-164">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-165">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-165">False</span></span>                                          |
| <span data-ttu-id="2a4f7-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-170">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-171">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-172">System-Flags</span></span>           | <span data-ttu-id="2a4f7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-173">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-174">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-175">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a4f7-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a4f7-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a4f7-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-177">Entry</span></span> | <span data-ttu-id="2a4f7-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-181">System-Only</span></span>            | <span data-ttu-id="2a4f7-182">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-182">False</span></span>                                          |
| <span data-ttu-id="2a4f7-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-184">True</span></span>                                           |
| <span data-ttu-id="2a4f7-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-185">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-186">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-186">False</span></span>                                          |
| <span data-ttu-id="2a4f7-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-187">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-188">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-188">False</span></span>                                          |
| <span data-ttu-id="2a4f7-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-193">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-194">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-195">System-Flags</span></span>           | <span data-ttu-id="2a4f7-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-196">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-197">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-198">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a4f7-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a4f7-199">Windows Server 2008</span></span>



| <span data-ttu-id="2a4f7-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-200">Entry</span></span> | <span data-ttu-id="2a4f7-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-204">System-Only</span></span>            | <span data-ttu-id="2a4f7-205">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-205">False</span></span>                                          |
| <span data-ttu-id="2a4f7-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-207">True</span></span>                                           |
| <span data-ttu-id="2a4f7-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-208">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-209">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-209">False</span></span>                                          |
| <span data-ttu-id="2a4f7-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-210">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-211">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-211">False</span></span>                                          |
| <span data-ttu-id="2a4f7-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-216">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-217">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-218">System-Flags</span></span>           | <span data-ttu-id="2a4f7-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-219">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-220">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-221">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a4f7-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a4f7-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a4f7-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-223">Entry</span></span> | <span data-ttu-id="2a4f7-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-227">System-Only</span></span>            | <span data-ttu-id="2a4f7-228">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-228">False</span></span>                                          |
| <span data-ttu-id="2a4f7-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-230">True</span></span>                                           |
| <span data-ttu-id="2a4f7-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-231">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-232">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-232">False</span></span>                                          |
| <span data-ttu-id="2a4f7-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-233">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-234">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-234">False</span></span>                                          |
| <span data-ttu-id="2a4f7-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-239">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-240">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-241">System-Flags</span></span>           | <span data-ttu-id="2a4f7-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-242">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-243">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-244">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a4f7-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a4f7-245">Windows Server 2012</span></span>



| <span data-ttu-id="2a4f7-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4f7-246">Entry</span></span> | <span data-ttu-id="2a4f7-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f7-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="2a4f7-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4f7-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4f7-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="2a4f7-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4f7-250">System-Only</span></span>            | <span data-ttu-id="2a4f7-251">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-251">False</span></span>                                          |
| <span data-ttu-id="2a4f7-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4f7-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4f7-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4f7-253">True</span></span>                                           |
| <span data-ttu-id="2a4f7-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4f7-254">Is Indexed</span></span>             | <span data-ttu-id="2a4f7-255">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-255">False</span></span>                                          |
| <span data-ttu-id="2a4f7-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4f7-256">In Global Catalog</span></span>      | <span data-ttu-id="2a4f7-257">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4f7-257">False</span></span>                                          |
| <span data-ttu-id="2a4f7-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4f7-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4f7-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4f7-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="2a4f7-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4f7-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4f7-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="2a4f7-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-262">Search-Flags</span></span>           | <span data-ttu-id="2a4f7-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4f7-263">0x00000000</span></span>                                     |
| <span data-ttu-id="2a4f7-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4f7-264">System-Flags</span></span>           | <span data-ttu-id="2a4f7-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4f7-265">0x00000010</span></span>                                     |
| <span data-ttu-id="2a4f7-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4f7-266">Classes used in</span></span>        | [<span data-ttu-id="2a4f7-267">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="2a4f7-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





