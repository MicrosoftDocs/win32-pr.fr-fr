---
title: attribut ms-DS-Trust-forêt-Trust-info
description: Contient les informations d’approbation de forêt (objet BLOB binaire) utilisées par le système pour un objet Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DS-Trust-forêt-Trust-info
- Schéma Active Directory de l’attribut msDS-TrustForestTrustInfo
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744677"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="e48f6-105">attribut ms-DS-Trust-forêt-Trust-info</span><span class="sxs-lookup"><span data-stu-id="e48f6-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="e48f6-106">Contient les informations d’approbation de forêt (objet BLOB binaire) utilisées par le système pour un objet Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="e48f6-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="e48f6-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-107">Entry</span></span> | <span data-ttu-id="e48f6-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e48f6-109">CN</span><span class="sxs-lookup"><span data-stu-id="e48f6-109">CN</span></span>                | <span data-ttu-id="e48f6-110">ms-DS-Trust-forêt-Trust-info</span><span class="sxs-lookup"><span data-stu-id="e48f6-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="e48f6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e48f6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e48f6-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="e48f6-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="e48f6-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e48f6-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="e48f6-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e48f6-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="e48f6-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e48f6-115">Update Frequency</span></span>  | <span data-ttu-id="e48f6-116">Uniquement lorsque la relation d’approbation entre les forêts change.</span><span class="sxs-lookup"><span data-stu-id="e48f6-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="e48f6-117">Cela peut se produire si la topologie d’une forêt approuvée change.</span><span class="sxs-lookup"><span data-stu-id="e48f6-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="e48f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-118">Attribute-Id</span></span>      | <span data-ttu-id="e48f6-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="e48f6-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="e48f6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e48f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="e48f6-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="e48f6-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="e48f6-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e48f6-122">Syntax</span></span>            | [<span data-ttu-id="e48f6-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e48f6-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="e48f6-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e48f6-124">Implementations</span></span>

-   [<span data-ttu-id="e48f6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e48f6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e48f6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e48f6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e48f6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e48f6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e48f6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e48f6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e48f6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e48f6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e48f6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e48f6-130">Windows Server 2003</span></span>



| <span data-ttu-id="e48f6-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-131">Entry</span></span> | <span data-ttu-id="e48f6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e48f6-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e48f6-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e48f6-135">System-Only</span></span>            | <span data-ttu-id="e48f6-136">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-136">False</span></span>                                                |
| <span data-ttu-id="e48f6-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e48f6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e48f6-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-138">True</span></span>                                                 |
| <span data-ttu-id="e48f6-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e48f6-139">Is Indexed</span></span>             | <span data-ttu-id="e48f6-140">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-140">False</span></span>                                                |
| <span data-ttu-id="e48f6-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e48f6-141">In Global Catalog</span></span>      | <span data-ttu-id="e48f6-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-142">True</span></span>                                                 |
| <span data-ttu-id="e48f6-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e48f6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e48f6-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e48f6-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e48f6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e48f6-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e48f6-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-147">Search-Flags</span></span>           | <span data-ttu-id="e48f6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e48f6-148">0x00000000</span></span>                                           |
| <span data-ttu-id="e48f6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-149">System-Flags</span></span>           | <span data-ttu-id="e48f6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e48f6-150">0x00000010</span></span>                                           |
| <span data-ttu-id="e48f6-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e48f6-151">Classes used in</span></span>        | [<span data-ttu-id="e48f6-152">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="e48f6-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e48f6-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e48f6-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e48f6-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-154">Entry</span></span> | <span data-ttu-id="e48f6-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e48f6-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e48f6-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e48f6-158">System-Only</span></span>            | <span data-ttu-id="e48f6-159">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-159">False</span></span>                                                |
| <span data-ttu-id="e48f6-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e48f6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e48f6-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-161">True</span></span>                                                 |
| <span data-ttu-id="e48f6-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e48f6-162">Is Indexed</span></span>             | <span data-ttu-id="e48f6-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-163">False</span></span>                                                |
| <span data-ttu-id="e48f6-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e48f6-164">In Global Catalog</span></span>      | <span data-ttu-id="e48f6-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-165">True</span></span>                                                 |
| <span data-ttu-id="e48f6-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e48f6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e48f6-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e48f6-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e48f6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e48f6-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e48f6-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-170">Search-Flags</span></span>           | <span data-ttu-id="e48f6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e48f6-171">0x00000000</span></span>                                           |
| <span data-ttu-id="e48f6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-172">System-Flags</span></span>           | <span data-ttu-id="e48f6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e48f6-173">0x00000010</span></span>                                           |
| <span data-ttu-id="e48f6-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e48f6-174">Classes used in</span></span>        | [<span data-ttu-id="e48f6-175">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="e48f6-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e48f6-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e48f6-176">Windows Server 2008</span></span>



| <span data-ttu-id="e48f6-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-177">Entry</span></span> | <span data-ttu-id="e48f6-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e48f6-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e48f6-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e48f6-181">System-Only</span></span>            | <span data-ttu-id="e48f6-182">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-182">False</span></span>                                                |
| <span data-ttu-id="e48f6-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e48f6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e48f6-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-184">True</span></span>                                                 |
| <span data-ttu-id="e48f6-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e48f6-185">Is Indexed</span></span>             | <span data-ttu-id="e48f6-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-186">False</span></span>                                                |
| <span data-ttu-id="e48f6-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e48f6-187">In Global Catalog</span></span>      | <span data-ttu-id="e48f6-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-188">True</span></span>                                                 |
| <span data-ttu-id="e48f6-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e48f6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e48f6-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e48f6-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e48f6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e48f6-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e48f6-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-193">Search-Flags</span></span>           | <span data-ttu-id="e48f6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e48f6-194">0x00000000</span></span>                                           |
| <span data-ttu-id="e48f6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-195">System-Flags</span></span>           | <span data-ttu-id="e48f6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e48f6-196">0x00000010</span></span>                                           |
| <span data-ttu-id="e48f6-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e48f6-197">Classes used in</span></span>        | [<span data-ttu-id="e48f6-198">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="e48f6-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e48f6-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e48f6-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e48f6-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-200">Entry</span></span> | <span data-ttu-id="e48f6-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e48f6-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e48f6-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e48f6-204">System-Only</span></span>            | <span data-ttu-id="e48f6-205">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-205">False</span></span>                                                |
| <span data-ttu-id="e48f6-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e48f6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e48f6-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-207">True</span></span>                                                 |
| <span data-ttu-id="e48f6-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e48f6-208">Is Indexed</span></span>             | <span data-ttu-id="e48f6-209">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-209">False</span></span>                                                |
| <span data-ttu-id="e48f6-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e48f6-210">In Global Catalog</span></span>      | <span data-ttu-id="e48f6-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-211">True</span></span>                                                 |
| <span data-ttu-id="e48f6-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e48f6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e48f6-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e48f6-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e48f6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e48f6-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e48f6-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-216">Search-Flags</span></span>           | <span data-ttu-id="e48f6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e48f6-217">0x00000000</span></span>                                           |
| <span data-ttu-id="e48f6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-218">System-Flags</span></span>           | <span data-ttu-id="e48f6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e48f6-219">0x00000010</span></span>                                           |
| <span data-ttu-id="e48f6-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e48f6-220">Classes used in</span></span>        | [<span data-ttu-id="e48f6-221">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="e48f6-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e48f6-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e48f6-222">Windows Server 2012</span></span>



| <span data-ttu-id="e48f6-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="e48f6-223">Entry</span></span> | <span data-ttu-id="e48f6-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f6-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e48f6-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e48f6-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e48f6-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e48f6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e48f6-227">System-Only</span></span>            | <span data-ttu-id="e48f6-228">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-228">False</span></span>                                                |
| <span data-ttu-id="e48f6-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e48f6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e48f6-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-230">True</span></span>                                                 |
| <span data-ttu-id="e48f6-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e48f6-231">Is Indexed</span></span>             | <span data-ttu-id="e48f6-232">Faux</span><span class="sxs-lookup"><span data-stu-id="e48f6-232">False</span></span>                                                |
| <span data-ttu-id="e48f6-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e48f6-233">In Global Catalog</span></span>      | <span data-ttu-id="e48f6-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="e48f6-234">True</span></span>                                                 |
| <span data-ttu-id="e48f6-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e48f6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e48f6-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e48f6-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e48f6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e48f6-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e48f6-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e48f6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-239">Search-Flags</span></span>           | <span data-ttu-id="e48f6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e48f6-240">0x00000000</span></span>                                           |
| <span data-ttu-id="e48f6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e48f6-241">System-Flags</span></span>           | <span data-ttu-id="e48f6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e48f6-242">0x00000010</span></span>                                           |
| <span data-ttu-id="e48f6-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e48f6-243">Classes used in</span></span>        | [<span data-ttu-id="e48f6-244">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="e48f6-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





