---
title: MS-IEEE-80211-attribut de données
description: Stocke une liste de configurations réseau préférées dans stratégie de groupe pour les réseaux sans fil.
ms.assetid: 8e5ae2c6-c048-419d-a684-e450a2445a0e
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de données MS-IEEE-80211
- msieee80211-schéma AD d’attribut de données
topic_type:
- apiref
api_name:
- ms-ieee-80211-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a53138e15a15e4fafecb998b87ef8b4df71fb2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519786"
---
# <a name="ms-ieee-80211-data-attribute"></a><span data-ttu-id="08fd7-105">MS-IEEE-80211-attribut de données</span><span class="sxs-lookup"><span data-stu-id="08fd7-105">ms-ieee-80211-Data attribute</span></span>

<span data-ttu-id="08fd7-106">Stocke une liste de configurations réseau préférées dans stratégie de groupe pour les réseaux sans fil.</span><span class="sxs-lookup"><span data-stu-id="08fd7-106">Stores a list of preferred network configurations in Group Policy for wireless networks.</span></span>



| <span data-ttu-id="08fd7-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-107">Entry</span></span> | <span data-ttu-id="08fd7-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08fd7-109">CN</span><span class="sxs-lookup"><span data-stu-id="08fd7-109">CN</span></span>                | <span data-ttu-id="08fd7-110">MS-IEEE-80211-données</span><span class="sxs-lookup"><span data-stu-id="08fd7-110">ms-ieee-80211-Data</span></span>                                                               |
| <span data-ttu-id="08fd7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="08fd7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="08fd7-112">msieee80211-données</span><span class="sxs-lookup"><span data-stu-id="08fd7-112">msieee80211-Data</span></span>                                                                 |
| <span data-ttu-id="08fd7-113">Taille</span><span class="sxs-lookup"><span data-stu-id="08fd7-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="08fd7-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="08fd7-114">Update Privilege</span></span>  | <span data-ttu-id="08fd7-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="08fd7-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="08fd7-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="08fd7-116">Update Frequency</span></span>  | <span data-ttu-id="08fd7-117">Chaque fois qu’un administrateur de domaine modifie la stratégie de réseau sans fil pour un domaine ou une unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="08fd7-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="08fd7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-118">Attribute-Id</span></span>      | <span data-ttu-id="08fd7-119">1.2.840.113556.1.4.1821</span><span class="sxs-lookup"><span data-stu-id="08fd7-119">1.2.840.113556.1.4.1821</span></span>                                                          |
| <span data-ttu-id="08fd7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="08fd7-120">System-Id-Guid</span></span>    | <span data-ttu-id="08fd7-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span><span class="sxs-lookup"><span data-stu-id="08fd7-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span></span>                                             |
| <span data-ttu-id="08fd7-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08fd7-122">Syntax</span></span>            | [<span data-ttu-id="08fd7-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="08fd7-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                            |



## <a name="implementations"></a><span data-ttu-id="08fd7-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="08fd7-124">Implementations</span></span>

-   [<span data-ttu-id="08fd7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="08fd7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="08fd7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="08fd7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="08fd7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="08fd7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="08fd7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="08fd7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="08fd7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="08fd7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="08fd7-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08fd7-130">Windows Server 2003</span></span>



| <span data-ttu-id="08fd7-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-131">Entry</span></span> | <span data-ttu-id="08fd7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="08fd7-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="08fd7-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="08fd7-135">System-Only</span></span>            | <span data-ttu-id="08fd7-136">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-136">False</span></span>                                                           |
| <span data-ttu-id="08fd7-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="08fd7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="08fd7-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="08fd7-138">True</span></span>                                                            |
| <span data-ttu-id="08fd7-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="08fd7-139">Is Indexed</span></span>             | <span data-ttu-id="08fd7-140">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-140">False</span></span>                                                           |
| <span data-ttu-id="08fd7-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="08fd7-141">In Global Catalog</span></span>      | <span data-ttu-id="08fd7-142">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-142">False</span></span>                                                           |
| <span data-ttu-id="08fd7-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="08fd7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="08fd7-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="08fd7-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="08fd7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08fd7-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08fd7-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-147">Search-Flags</span></span>           | <span data-ttu-id="08fd7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08fd7-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="08fd7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-149">System-Flags</span></span>           | <span data-ttu-id="08fd7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08fd7-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="08fd7-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="08fd7-151">Classes used in</span></span>        | [<span data-ttu-id="08fd7-152">**MS-IEEE-80211-stratégie**</span><span class="sxs-lookup"><span data-stu-id="08fd7-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="08fd7-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="08fd7-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="08fd7-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-154">Entry</span></span> | <span data-ttu-id="08fd7-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="08fd7-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="08fd7-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="08fd7-158">System-Only</span></span>            | <span data-ttu-id="08fd7-159">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-159">False</span></span>                                                           |
| <span data-ttu-id="08fd7-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="08fd7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="08fd7-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="08fd7-161">True</span></span>                                                            |
| <span data-ttu-id="08fd7-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="08fd7-162">Is Indexed</span></span>             | <span data-ttu-id="08fd7-163">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-163">False</span></span>                                                           |
| <span data-ttu-id="08fd7-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="08fd7-164">In Global Catalog</span></span>      | <span data-ttu-id="08fd7-165">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-165">False</span></span>                                                           |
| <span data-ttu-id="08fd7-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="08fd7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="08fd7-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="08fd7-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="08fd7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08fd7-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08fd7-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-170">Search-Flags</span></span>           | <span data-ttu-id="08fd7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08fd7-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="08fd7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-172">System-Flags</span></span>           | <span data-ttu-id="08fd7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08fd7-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="08fd7-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="08fd7-174">Classes used in</span></span>        | [<span data-ttu-id="08fd7-175">**MS-IEEE-80211-stratégie**</span><span class="sxs-lookup"><span data-stu-id="08fd7-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="08fd7-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08fd7-176">Windows Server 2008</span></span>



| <span data-ttu-id="08fd7-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-177">Entry</span></span> | <span data-ttu-id="08fd7-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="08fd7-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="08fd7-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="08fd7-181">System-Only</span></span>            | <span data-ttu-id="08fd7-182">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-182">False</span></span>                                                           |
| <span data-ttu-id="08fd7-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="08fd7-183">Is-Single-Valued</span></span>       | <span data-ttu-id="08fd7-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="08fd7-184">True</span></span>                                                            |
| <span data-ttu-id="08fd7-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="08fd7-185">Is Indexed</span></span>             | <span data-ttu-id="08fd7-186">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-186">False</span></span>                                                           |
| <span data-ttu-id="08fd7-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="08fd7-187">In Global Catalog</span></span>      | <span data-ttu-id="08fd7-188">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-188">False</span></span>                                                           |
| <span data-ttu-id="08fd7-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="08fd7-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="08fd7-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="08fd7-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="08fd7-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08fd7-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08fd7-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-193">Search-Flags</span></span>           | <span data-ttu-id="08fd7-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08fd7-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="08fd7-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-195">System-Flags</span></span>           | <span data-ttu-id="08fd7-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08fd7-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="08fd7-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="08fd7-197">Classes used in</span></span>        | [<span data-ttu-id="08fd7-198">**MS-IEEE-80211-stratégie**</span><span class="sxs-lookup"><span data-stu-id="08fd7-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="08fd7-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08fd7-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="08fd7-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-200">Entry</span></span> | <span data-ttu-id="08fd7-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="08fd7-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="08fd7-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="08fd7-204">System-Only</span></span>            | <span data-ttu-id="08fd7-205">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-205">False</span></span>                                                           |
| <span data-ttu-id="08fd7-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="08fd7-206">Is-Single-Valued</span></span>       | <span data-ttu-id="08fd7-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="08fd7-207">True</span></span>                                                            |
| <span data-ttu-id="08fd7-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="08fd7-208">Is Indexed</span></span>             | <span data-ttu-id="08fd7-209">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-209">False</span></span>                                                           |
| <span data-ttu-id="08fd7-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="08fd7-210">In Global Catalog</span></span>      | <span data-ttu-id="08fd7-211">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-211">False</span></span>                                                           |
| <span data-ttu-id="08fd7-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="08fd7-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="08fd7-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="08fd7-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="08fd7-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08fd7-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08fd7-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-216">Search-Flags</span></span>           | <span data-ttu-id="08fd7-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08fd7-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="08fd7-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-218">System-Flags</span></span>           | <span data-ttu-id="08fd7-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08fd7-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="08fd7-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="08fd7-220">Classes used in</span></span>        | [<span data-ttu-id="08fd7-221">**MS-IEEE-80211-stratégie**</span><span class="sxs-lookup"><span data-stu-id="08fd7-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="08fd7-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08fd7-222">Windows Server 2012</span></span>



| <span data-ttu-id="08fd7-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="08fd7-223">Entry</span></span> | <span data-ttu-id="08fd7-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="08fd7-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="08fd7-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="08fd7-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08fd7-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="08fd7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="08fd7-227">System-Only</span></span>            | <span data-ttu-id="08fd7-228">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-228">False</span></span>                                                           |
| <span data-ttu-id="08fd7-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="08fd7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="08fd7-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="08fd7-230">True</span></span>                                                            |
| <span data-ttu-id="08fd7-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="08fd7-231">Is Indexed</span></span>             | <span data-ttu-id="08fd7-232">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-232">False</span></span>                                                           |
| <span data-ttu-id="08fd7-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="08fd7-233">In Global Catalog</span></span>      | <span data-ttu-id="08fd7-234">Faux</span><span class="sxs-lookup"><span data-stu-id="08fd7-234">False</span></span>                                                           |
| <span data-ttu-id="08fd7-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="08fd7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="08fd7-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="08fd7-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="08fd7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08fd7-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08fd7-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="08fd7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-239">Search-Flags</span></span>           | <span data-ttu-id="08fd7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08fd7-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="08fd7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08fd7-241">System-Flags</span></span>           | <span data-ttu-id="08fd7-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08fd7-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="08fd7-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="08fd7-243">Classes used in</span></span>        | [<span data-ttu-id="08fd7-244">**MS-IEEE-80211-stratégie**</span><span class="sxs-lookup"><span data-stu-id="08fd7-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





