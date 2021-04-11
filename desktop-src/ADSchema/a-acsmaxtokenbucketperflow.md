---
title: ACS-attribut Max-Token-Bucket-par-Flow
description: L’attribut ACS-Max-Token-compartiment-per-Flow est destiné à un usage interne uniquement.
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ACS-Token-Token-per-Flow
- Schéma AD de l’attribut aCSMaxTokenBucketPerFlow
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108311"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="24e4e-105">ACS-attribut Max-Token-Bucket-par-Flow</span><span class="sxs-lookup"><span data-stu-id="24e4e-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="24e4e-106">L’attribut **ACS-Max-Token-compartiment-per-Flow** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="24e4e-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="24e4e-107">Basé sur RFC2210.</span><span class="sxs-lookup"><span data-stu-id="24e4e-107">Based on RFC2210.</span></span>



| <span data-ttu-id="24e4e-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-108">Entry</span></span> | <span data-ttu-id="24e4e-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="24e4e-110">CN</span><span class="sxs-lookup"><span data-stu-id="24e4e-110">CN</span></span>                | <span data-ttu-id="24e4e-111">ACS-Max-Token-Bucket par Flow</span><span class="sxs-lookup"><span data-stu-id="24e4e-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="24e4e-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="24e4e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="24e4e-113">aCSMaxTokenBucketPerFlow</span><span class="sxs-lookup"><span data-stu-id="24e4e-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="24e4e-114">Taille</span><span class="sxs-lookup"><span data-stu-id="24e4e-114">Size</span></span>              | <span data-ttu-id="24e4e-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="24e4e-115">8 bytes</span></span>                              |
| <span data-ttu-id="24e4e-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="24e4e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="24e4e-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="24e4e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="24e4e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-118">Attribute-Id</span></span>      | <span data-ttu-id="24e4e-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="24e4e-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="24e4e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="24e4e-120">System-Id-Guid</span></span>    | <span data-ttu-id="24e4e-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="24e4e-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="24e4e-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24e4e-122">Syntax</span></span>            | [<span data-ttu-id="24e4e-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="24e4e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="24e4e-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="24e4e-124">Implementations</span></span>

-   [<span data-ttu-id="24e4e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="24e4e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="24e4e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="24e4e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="24e4e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="24e4e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="24e4e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="24e4e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="24e4e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="24e4e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="24e4e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="24e4e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="24e4e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="24e4e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="24e4e-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-132">Entry</span></span> | <span data-ttu-id="24e4e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-136">System-Only</span></span>            | <span data-ttu-id="24e4e-137">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-137">False</span></span>                                        |
| <span data-ttu-id="24e4e-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-139">True</span></span>                                         |
| <span data-ttu-id="24e4e-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-140">Is Indexed</span></span>             | <span data-ttu-id="24e4e-141">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-141">False</span></span>                                        |
| <span data-ttu-id="24e4e-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-142">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-143">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-143">False</span></span>                                        |
| <span data-ttu-id="24e4e-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-148">Search-Flags</span></span>           | <span data-ttu-id="24e4e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-149">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-150">System-Flags</span></span>           | <span data-ttu-id="24e4e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-151">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-152">Classes used in</span></span>        | [<span data-ttu-id="24e4e-153">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="24e4e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24e4e-154">Windows Server 2003</span></span>



| <span data-ttu-id="24e4e-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-155">Entry</span></span> | <span data-ttu-id="24e4e-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-159">System-Only</span></span>            | <span data-ttu-id="24e4e-160">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-160">False</span></span>                                        |
| <span data-ttu-id="24e4e-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-162">True</span></span>                                         |
| <span data-ttu-id="24e4e-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-163">Is Indexed</span></span>             | <span data-ttu-id="24e4e-164">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-164">False</span></span>                                        |
| <span data-ttu-id="24e4e-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-165">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-166">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-166">False</span></span>                                        |
| <span data-ttu-id="24e4e-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-171">Search-Flags</span></span>           | <span data-ttu-id="24e4e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-172">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-173">System-Flags</span></span>           | <span data-ttu-id="24e4e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-174">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-175">Classes used in</span></span>        | [<span data-ttu-id="24e4e-176">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="24e4e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="24e4e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="24e4e-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-178">Entry</span></span> | <span data-ttu-id="24e4e-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-182">System-Only</span></span>            | <span data-ttu-id="24e4e-183">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-183">False</span></span>                                        |
| <span data-ttu-id="24e4e-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-185">True</span></span>                                         |
| <span data-ttu-id="24e4e-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-186">Is Indexed</span></span>             | <span data-ttu-id="24e4e-187">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-187">False</span></span>                                        |
| <span data-ttu-id="24e4e-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-188">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-189">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-189">False</span></span>                                        |
| <span data-ttu-id="24e4e-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-194">Search-Flags</span></span>           | <span data-ttu-id="24e4e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-195">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-196">System-Flags</span></span>           | <span data-ttu-id="24e4e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-197">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-198">Classes used in</span></span>        | [<span data-ttu-id="24e4e-199">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="24e4e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24e4e-200">Windows Server 2008</span></span>



| <span data-ttu-id="24e4e-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-201">Entry</span></span> | <span data-ttu-id="24e4e-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-205">System-Only</span></span>            | <span data-ttu-id="24e4e-206">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-206">False</span></span>                                        |
| <span data-ttu-id="24e4e-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-208">True</span></span>                                         |
| <span data-ttu-id="24e4e-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-209">Is Indexed</span></span>             | <span data-ttu-id="24e4e-210">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-210">False</span></span>                                        |
| <span data-ttu-id="24e4e-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-211">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-212">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-212">False</span></span>                                        |
| <span data-ttu-id="24e4e-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-217">Search-Flags</span></span>           | <span data-ttu-id="24e4e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-218">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-219">System-Flags</span></span>           | <span data-ttu-id="24e4e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-220">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-221">Classes used in</span></span>        | [<span data-ttu-id="24e4e-222">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="24e4e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24e4e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="24e4e-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-224">Entry</span></span> | <span data-ttu-id="24e4e-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-228">System-Only</span></span>            | <span data-ttu-id="24e4e-229">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-229">False</span></span>                                        |
| <span data-ttu-id="24e4e-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-231">True</span></span>                                         |
| <span data-ttu-id="24e4e-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-232">Is Indexed</span></span>             | <span data-ttu-id="24e4e-233">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-233">False</span></span>                                        |
| <span data-ttu-id="24e4e-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-234">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-235">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-235">False</span></span>                                        |
| <span data-ttu-id="24e4e-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-240">Search-Flags</span></span>           | <span data-ttu-id="24e4e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-241">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-242">System-Flags</span></span>           | <span data-ttu-id="24e4e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-243">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-244">Classes used in</span></span>        | [<span data-ttu-id="24e4e-245">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="24e4e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24e4e-246">Windows Server 2012</span></span>



| <span data-ttu-id="24e4e-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="24e4e-247">Entry</span></span> | <span data-ttu-id="24e4e-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e4e-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="24e4e-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="24e4e-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="24e4e-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="24e4e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="24e4e-251">System-Only</span></span>            | <span data-ttu-id="24e4e-252">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-252">False</span></span>                                        |
| <span data-ttu-id="24e4e-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="24e4e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="24e4e-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="24e4e-254">True</span></span>                                         |
| <span data-ttu-id="24e4e-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="24e4e-255">Is Indexed</span></span>             | <span data-ttu-id="24e4e-256">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-256">False</span></span>                                        |
| <span data-ttu-id="24e4e-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="24e4e-257">In Global Catalog</span></span>      | <span data-ttu-id="24e4e-258">Faux</span><span class="sxs-lookup"><span data-stu-id="24e4e-258">False</span></span>                                        |
| <span data-ttu-id="24e4e-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="24e4e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="24e4e-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="24e4e-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="24e4e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="24e4e-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="24e4e-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="24e4e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-263">Search-Flags</span></span>           | <span data-ttu-id="24e4e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24e4e-264">0x00000000</span></span>                                   |
| <span data-ttu-id="24e4e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="24e4e-265">System-Flags</span></span>           | <span data-ttu-id="24e4e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24e4e-266">0x00000010</span></span>                                   |
| <span data-ttu-id="24e4e-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="24e4e-267">Classes used in</span></span>        | [<span data-ttu-id="24e4e-268">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="24e4e-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





