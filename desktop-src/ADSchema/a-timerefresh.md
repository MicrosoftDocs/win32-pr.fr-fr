---
title: Attribut Time-Refresh
description: Cet attribut présente l’intervalle pendant lequel un enregistrement de ressource contenu dans une zone intégrée Active Directory doit être actualisé pour le serveur DNS. L’intervalle par défaut est de 7 jours.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Time-Refresh
- Schéma AD de l’attribut timeRefresh
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943231"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="0bd69-106">Attribut Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="0bd69-106">Time-Refresh attribute</span></span>

<span data-ttu-id="0bd69-107">Cet attribut présente l’intervalle pendant lequel un enregistrement de ressource contenu dans une zone intégrée Active Directory doit être actualisé pour le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="0bd69-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="0bd69-108">L’intervalle par défaut est de 7 jours.</span><span class="sxs-lookup"><span data-stu-id="0bd69-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="0bd69-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-109">Entry</span></span> | <span data-ttu-id="0bd69-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0bd69-111">CN</span><span class="sxs-lookup"><span data-stu-id="0bd69-111">CN</span></span>                | <span data-ttu-id="0bd69-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="0bd69-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="0bd69-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0bd69-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0bd69-114">timeRefresh</span><span class="sxs-lookup"><span data-stu-id="0bd69-114">timeRefresh</span></span>                          |
| <span data-ttu-id="0bd69-115">Taille</span><span class="sxs-lookup"><span data-stu-id="0bd69-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="0bd69-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="0bd69-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0bd69-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="0bd69-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0bd69-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-118">Attribute-Id</span></span>      | <span data-ttu-id="0bd69-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="0bd69-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="0bd69-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0bd69-120">System-Id-Guid</span></span>    | <span data-ttu-id="0bd69-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="0bd69-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="0bd69-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd69-122">Syntax</span></span>            | [<span data-ttu-id="0bd69-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="0bd69-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0bd69-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="0bd69-124">Implementations</span></span>

-   [<span data-ttu-id="0bd69-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0bd69-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0bd69-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0bd69-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0bd69-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0bd69-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0bd69-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0bd69-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0bd69-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0bd69-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0bd69-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0bd69-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0bd69-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bd69-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0bd69-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-132">Entry</span></span> | <span data-ttu-id="0bd69-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-136">System-Only</span></span>            | <span data-ttu-id="0bd69-137">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-140">Is Indexed</span></span>             | <span data-ttu-id="0bd69-141">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-142">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-143">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-148">Search-Flags</span></span>           | <span data-ttu-id="0bd69-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-150">System-Flags</span></span>           | <span data-ttu-id="0bd69-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-152">Classes used in</span></span>        | [<span data-ttu-id="0bd69-153">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-154">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0bd69-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bd69-155">Windows Server 2003</span></span>



| <span data-ttu-id="0bd69-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-156">Entry</span></span> | <span data-ttu-id="0bd69-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-160">System-Only</span></span>            | <span data-ttu-id="0bd69-161">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-164">Is Indexed</span></span>             | <span data-ttu-id="0bd69-165">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-166">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-167">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-172">Search-Flags</span></span>           | <span data-ttu-id="0bd69-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-174">System-Flags</span></span>           | <span data-ttu-id="0bd69-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-176">Classes used in</span></span>        | [<span data-ttu-id="0bd69-177">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-178">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0bd69-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0bd69-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0bd69-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-180">Entry</span></span> | <span data-ttu-id="0bd69-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-184">System-Only</span></span>            | <span data-ttu-id="0bd69-185">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-188">Is Indexed</span></span>             | <span data-ttu-id="0bd69-189">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-190">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-191">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-196">Search-Flags</span></span>           | <span data-ttu-id="0bd69-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-198">System-Flags</span></span>           | <span data-ttu-id="0bd69-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-200">Classes used in</span></span>        | [<span data-ttu-id="0bd69-201">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-202">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0bd69-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bd69-203">Windows Server 2008</span></span>



| <span data-ttu-id="0bd69-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-204">Entry</span></span> | <span data-ttu-id="0bd69-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-208">System-Only</span></span>            | <span data-ttu-id="0bd69-209">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-212">Is Indexed</span></span>             | <span data-ttu-id="0bd69-213">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-214">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-215">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-220">Search-Flags</span></span>           | <span data-ttu-id="0bd69-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-222">System-Flags</span></span>           | <span data-ttu-id="0bd69-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-224">Classes used in</span></span>        | [<span data-ttu-id="0bd69-225">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-226">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0bd69-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bd69-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0bd69-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-228">Entry</span></span> | <span data-ttu-id="0bd69-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-232">System-Only</span></span>            | <span data-ttu-id="0bd69-233">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-236">Is Indexed</span></span>             | <span data-ttu-id="0bd69-237">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-238">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-239">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-244">Search-Flags</span></span>           | <span data-ttu-id="0bd69-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-246">System-Flags</span></span>           | <span data-ttu-id="0bd69-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-248">Classes used in</span></span>        | [<span data-ttu-id="0bd69-249">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-250">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0bd69-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bd69-251">Windows Server 2012</span></span>



| <span data-ttu-id="0bd69-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="0bd69-252">Entry</span></span> | <span data-ttu-id="0bd69-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd69-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd69-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0bd69-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bd69-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0bd69-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bd69-256">System-Only</span></span>            | <span data-ttu-id="0bd69-257">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0bd69-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0bd69-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="0bd69-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="0bd69-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0bd69-260">Is Indexed</span></span>             | <span data-ttu-id="0bd69-261">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0bd69-262">In Global Catalog</span></span>      | <span data-ttu-id="0bd69-263">Faux</span><span class="sxs-lookup"><span data-stu-id="0bd69-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="0bd69-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0bd69-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bd69-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0bd69-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0bd69-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bd69-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bd69-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0bd69-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-268">Search-Flags</span></span>           | <span data-ttu-id="0bd69-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bd69-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bd69-270">System-Flags</span></span>           | <span data-ttu-id="0bd69-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bd69-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0bd69-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0bd69-272">Classes used in</span></span>        | [<span data-ttu-id="0bd69-273">**Lien-Track-OMT-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="0bd69-274">**Lien-Track-vol-entrée**</span><span class="sxs-lookup"><span data-stu-id="0bd69-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





