---
title: Attribut Repl-Interval
description: Attribut des objets Site-Link qui définit l’intervalle, en minutes, entre les cycles de réplication entre les sites de la liste de sites.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Repl-Interval
- Schéma AD de l’attribut replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107590"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="a76d2-105">Attribut Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="a76d2-105">Repl-Interval attribute</span></span>

<span data-ttu-id="a76d2-106">Attribut des objets Site-Link qui définit l’intervalle, en minutes, entre les cycles de réplication entre les sites de la liste de sites.</span><span class="sxs-lookup"><span data-stu-id="a76d2-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="a76d2-107">Doit être un multiple de 15 minutes (granularité de la réplication des services de domaine intersites), un minimum de 15 minutes et un maximum de 10 080 minutes (une semaine).</span><span class="sxs-lookup"><span data-stu-id="a76d2-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="a76d2-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-108">Entry</span></span> | <span data-ttu-id="a76d2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="a76d2-110">CN</span><span class="sxs-lookup"><span data-stu-id="a76d2-110">CN</span></span>                | <span data-ttu-id="a76d2-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="a76d2-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="a76d2-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a76d2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a76d2-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="a76d2-113">replInterval</span></span>                                   |
| <span data-ttu-id="a76d2-114">Taille</span><span class="sxs-lookup"><span data-stu-id="a76d2-114">Size</span></span>              | <span data-ttu-id="a76d2-115">4 octets</span><span class="sxs-lookup"><span data-stu-id="a76d2-115">4 bytes</span></span>                                        |
| <span data-ttu-id="a76d2-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a76d2-116">Update Privilege</span></span>  | <span data-ttu-id="a76d2-117">Administrateur d’entreprise</span><span class="sxs-lookup"><span data-stu-id="a76d2-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="a76d2-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a76d2-118">Update Frequency</span></span>  | <span data-ttu-id="a76d2-119">Lorsque l’intervalle de réplication doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="a76d2-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="a76d2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-120">Attribute-Id</span></span>      | <span data-ttu-id="a76d2-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="a76d2-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="a76d2-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a76d2-122">System-Id-Guid</span></span>    | <span data-ttu-id="a76d2-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="a76d2-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="a76d2-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a76d2-124">Syntax</span></span>            | [<span data-ttu-id="a76d2-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a76d2-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="a76d2-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a76d2-126">Implementations</span></span>

-   [<span data-ttu-id="a76d2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a76d2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a76d2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a76d2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a76d2-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a76d2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a76d2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a76d2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a76d2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a76d2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a76d2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a76d2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a76d2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a76d2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a76d2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a76d2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a76d2-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-135">Entry</span></span> | <span data-ttu-id="a76d2-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-139">System-Only</span></span>            | <span data-ttu-id="a76d2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-140">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-142">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-143">Is Indexed</span></span>             | <span data-ttu-id="a76d2-144">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-144">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-145">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-146">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-146">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-151">Search-Flags</span></span>           | <span data-ttu-id="a76d2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-153">System-Flags</span></span>           | <span data-ttu-id="a76d2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-155">Classes used in</span></span>        | [<span data-ttu-id="a76d2-156">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-157">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a76d2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a76d2-158">Windows Server 2003</span></span>



| <span data-ttu-id="a76d2-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-159">Entry</span></span> | <span data-ttu-id="a76d2-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-163">System-Only</span></span>            | <span data-ttu-id="a76d2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-164">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-166">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-167">Is Indexed</span></span>             | <span data-ttu-id="a76d2-168">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-168">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-169">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-170">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-170">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-175">Search-Flags</span></span>           | <span data-ttu-id="a76d2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-177">System-Flags</span></span>           | <span data-ttu-id="a76d2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-179">Classes used in</span></span>        | [<span data-ttu-id="a76d2-180">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-181">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a76d2-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="a76d2-182">ADAM</span></span>



| <span data-ttu-id="a76d2-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-183">Entry</span></span> | <span data-ttu-id="a76d2-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-187">System-Only</span></span>            | <span data-ttu-id="a76d2-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-188">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-190">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-191">Is Indexed</span></span>             | <span data-ttu-id="a76d2-192">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-192">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-193">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-194">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-194">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-199">Search-Flags</span></span>           | <span data-ttu-id="a76d2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-201">System-Flags</span></span>           | <span data-ttu-id="a76d2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-203">Classes used in</span></span>        | [<span data-ttu-id="a76d2-204">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-205">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a76d2-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a76d2-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a76d2-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-207">Entry</span></span> | <span data-ttu-id="a76d2-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-211">System-Only</span></span>            | <span data-ttu-id="a76d2-212">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-212">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-214">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-215">Is Indexed</span></span>             | <span data-ttu-id="a76d2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-216">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-217">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-218">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-218">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-223">Search-Flags</span></span>           | <span data-ttu-id="a76d2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-225">System-Flags</span></span>           | <span data-ttu-id="a76d2-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-227">Classes used in</span></span>        | [<span data-ttu-id="a76d2-228">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-229">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a76d2-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a76d2-230">Windows Server 2008</span></span>



| <span data-ttu-id="a76d2-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-231">Entry</span></span> | <span data-ttu-id="a76d2-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-235">System-Only</span></span>            | <span data-ttu-id="a76d2-236">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-236">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-238">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-239">Is Indexed</span></span>             | <span data-ttu-id="a76d2-240">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-240">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-241">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-242">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-242">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-247">Search-Flags</span></span>           | <span data-ttu-id="a76d2-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-249">System-Flags</span></span>           | <span data-ttu-id="a76d2-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-251">Classes used in</span></span>        | [<span data-ttu-id="a76d2-252">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-253">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a76d2-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a76d2-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a76d2-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-255">Entry</span></span> | <span data-ttu-id="a76d2-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-259">System-Only</span></span>            | <span data-ttu-id="a76d2-260">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-260">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-261">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-262">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-263">Is Indexed</span></span>             | <span data-ttu-id="a76d2-264">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-264">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-265">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-266">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-266">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-271">Search-Flags</span></span>           | <span data-ttu-id="a76d2-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-273">System-Flags</span></span>           | <span data-ttu-id="a76d2-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-275">Classes used in</span></span>        | [<span data-ttu-id="a76d2-276">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-277">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a76d2-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a76d2-278">Windows Server 2012</span></span>



| <span data-ttu-id="a76d2-279">Entrée</span><span class="sxs-lookup"><span data-stu-id="a76d2-279">Entry</span></span> | <span data-ttu-id="a76d2-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76d2-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d2-281">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a76d2-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a76d2-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="a76d2-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="a76d2-283">System-Only</span></span>            | <span data-ttu-id="a76d2-284">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-284">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a76d2-285">Is-Single-Valued</span></span>       | <span data-ttu-id="a76d2-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="a76d2-286">True</span></span>                                                                                                       |
| <span data-ttu-id="a76d2-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a76d2-287">Is Indexed</span></span>             | <span data-ttu-id="a76d2-288">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-288">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a76d2-289">In Global Catalog</span></span>      | <span data-ttu-id="a76d2-290">Faux</span><span class="sxs-lookup"><span data-stu-id="a76d2-290">False</span></span>                                                                                                      |
| <span data-ttu-id="a76d2-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a76d2-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="a76d2-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a76d2-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="a76d2-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a76d2-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a76d2-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="a76d2-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-295">Search-Flags</span></span>           | <span data-ttu-id="a76d2-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a76d2-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a76d2-297">System-Flags</span></span>           | <span data-ttu-id="a76d2-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a76d2-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="a76d2-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a76d2-299">Classes used in</span></span>        | [<span data-ttu-id="a76d2-300">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="a76d2-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="a76d2-301">**Lien de site**</span><span class="sxs-lookup"><span data-stu-id="a76d2-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





