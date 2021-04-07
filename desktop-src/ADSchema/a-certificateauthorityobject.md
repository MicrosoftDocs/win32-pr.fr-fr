---
title: Certificate-Authority-Object (attribut)
description: Référence à l’autorité de certification associée à un point de distribution de liste de révocation de certificats.
ms.assetid: 8dfd4441-6b45-4dc4-aed8-e33aa7fd099f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Certificate-Authority-Object
- Schéma AD de l’attribut certificateAuthorityObject
topic_type:
- apiref
api_name:
- Certificate-Authority-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65ffceb810cd6a4ef3033834dbf0f3c489f1506e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845614"
---
# <a name="certificate-authority-object-attribute"></a><span data-ttu-id="70750-105">Certificate-Authority-Object (attribut)</span><span class="sxs-lookup"><span data-stu-id="70750-105">Certificate-Authority-Object attribute</span></span>

<span data-ttu-id="70750-106">Référence à l’autorité de certification associée à un point de distribution de liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="70750-106">Reference to the certification authority associated with a Certificate Revocation List distribution point.</span></span>



| <span data-ttu-id="70750-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-107">Entry</span></span> | <span data-ttu-id="70750-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="70750-109">CN</span><span class="sxs-lookup"><span data-stu-id="70750-109">CN</span></span>                | <span data-ttu-id="70750-110">Certificate-Authority-Object</span><span class="sxs-lookup"><span data-stu-id="70750-110">Certificate-Authority-Object</span></span>            |
| <span data-ttu-id="70750-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="70750-111">Ldap-Display-Name</span></span> | <span data-ttu-id="70750-112">certificateAuthorityObject</span><span class="sxs-lookup"><span data-stu-id="70750-112">certificateAuthorityObject</span></span>              |
| <span data-ttu-id="70750-113">Taille</span><span class="sxs-lookup"><span data-stu-id="70750-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="70750-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="70750-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="70750-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="70750-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="70750-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="70750-116">Attribute-Id</span></span>      | <span data-ttu-id="70750-117">1.2.840.113556.1.4.684</span><span class="sxs-lookup"><span data-stu-id="70750-117">1.2.840.113556.1.4.684</span></span>                  |
| <span data-ttu-id="70750-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="70750-118">System-Id-Guid</span></span>    | <span data-ttu-id="70750-119">963d2732-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="70750-119">963d2732-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="70750-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70750-120">Syntax</span></span>            | [<span data-ttu-id="70750-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="70750-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="70750-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="70750-122">Implementations</span></span>

-   [<span data-ttu-id="70750-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="70750-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="70750-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="70750-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="70750-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="70750-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="70750-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="70750-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="70750-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="70750-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="70750-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="70750-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="70750-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="70750-129">Windows 2000 Server</span></span>



| <span data-ttu-id="70750-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-130">Entry</span></span> | <span data-ttu-id="70750-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-134">System-Only</span></span>            | <span data-ttu-id="70750-135">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-135">False</span></span>                                                               |
| <span data-ttu-id="70750-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-136">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-137">True</span></span>                                                                |
| <span data-ttu-id="70750-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-138">Is Indexed</span></span>             | <span data-ttu-id="70750-139">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-139">False</span></span>                                                               |
| <span data-ttu-id="70750-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-140">In Global Catalog</span></span>      | <span data-ttu-id="70750-141">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-141">False</span></span>                                                               |
| <span data-ttu-id="70750-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-146">Search-Flags</span></span>           | <span data-ttu-id="70750-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-148">System-Flags</span></span>           | <span data-ttu-id="70750-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-150">Classes used in</span></span>        | [<span data-ttu-id="70750-151">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="70750-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70750-152">Windows Server 2003</span></span>



| <span data-ttu-id="70750-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-153">Entry</span></span> | <span data-ttu-id="70750-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-157">System-Only</span></span>            | <span data-ttu-id="70750-158">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-158">False</span></span>                                                               |
| <span data-ttu-id="70750-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-159">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-160">True</span></span>                                                                |
| <span data-ttu-id="70750-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-161">Is Indexed</span></span>             | <span data-ttu-id="70750-162">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-162">False</span></span>                                                               |
| <span data-ttu-id="70750-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-163">In Global Catalog</span></span>      | <span data-ttu-id="70750-164">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-164">False</span></span>                                                               |
| <span data-ttu-id="70750-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-169">Search-Flags</span></span>           | <span data-ttu-id="70750-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-171">System-Flags</span></span>           | <span data-ttu-id="70750-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-173">Classes used in</span></span>        | [<span data-ttu-id="70750-174">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="70750-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="70750-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="70750-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-176">Entry</span></span> | <span data-ttu-id="70750-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-180">System-Only</span></span>            | <span data-ttu-id="70750-181">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-181">False</span></span>                                                               |
| <span data-ttu-id="70750-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-182">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-183">True</span></span>                                                                |
| <span data-ttu-id="70750-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-184">Is Indexed</span></span>             | <span data-ttu-id="70750-185">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-185">False</span></span>                                                               |
| <span data-ttu-id="70750-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-186">In Global Catalog</span></span>      | <span data-ttu-id="70750-187">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-187">False</span></span>                                                               |
| <span data-ttu-id="70750-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-192">Search-Flags</span></span>           | <span data-ttu-id="70750-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-194">System-Flags</span></span>           | <span data-ttu-id="70750-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-196">Classes used in</span></span>        | [<span data-ttu-id="70750-197">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="70750-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70750-198">Windows Server 2008</span></span>



| <span data-ttu-id="70750-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-199">Entry</span></span> | <span data-ttu-id="70750-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-203">System-Only</span></span>            | <span data-ttu-id="70750-204">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-204">False</span></span>                                                               |
| <span data-ttu-id="70750-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-205">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-206">True</span></span>                                                                |
| <span data-ttu-id="70750-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-207">Is Indexed</span></span>             | <span data-ttu-id="70750-208">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-208">False</span></span>                                                               |
| <span data-ttu-id="70750-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-209">In Global Catalog</span></span>      | <span data-ttu-id="70750-210">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-210">False</span></span>                                                               |
| <span data-ttu-id="70750-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-215">Search-Flags</span></span>           | <span data-ttu-id="70750-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-217">System-Flags</span></span>           | <span data-ttu-id="70750-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-219">Classes used in</span></span>        | [<span data-ttu-id="70750-220">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="70750-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70750-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="70750-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-222">Entry</span></span> | <span data-ttu-id="70750-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-226">System-Only</span></span>            | <span data-ttu-id="70750-227">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-227">False</span></span>                                                               |
| <span data-ttu-id="70750-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-228">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-229">True</span></span>                                                                |
| <span data-ttu-id="70750-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-230">Is Indexed</span></span>             | <span data-ttu-id="70750-231">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-231">False</span></span>                                                               |
| <span data-ttu-id="70750-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-232">In Global Catalog</span></span>      | <span data-ttu-id="70750-233">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-233">False</span></span>                                                               |
| <span data-ttu-id="70750-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-238">Search-Flags</span></span>           | <span data-ttu-id="70750-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-240">System-Flags</span></span>           | <span data-ttu-id="70750-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-242">Classes used in</span></span>        | [<span data-ttu-id="70750-243">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="70750-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70750-244">Windows Server 2012</span></span>



| <span data-ttu-id="70750-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="70750-245">Entry</span></span> | <span data-ttu-id="70750-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="70750-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70750-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="70750-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70750-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="70750-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="70750-249">System-Only</span></span>            | <span data-ttu-id="70750-250">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-250">False</span></span>                                                               |
| <span data-ttu-id="70750-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="70750-251">Is-Single-Valued</span></span>       | <span data-ttu-id="70750-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="70750-252">True</span></span>                                                                |
| <span data-ttu-id="70750-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="70750-253">Is Indexed</span></span>             | <span data-ttu-id="70750-254">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-254">False</span></span>                                                               |
| <span data-ttu-id="70750-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="70750-255">In Global Catalog</span></span>      | <span data-ttu-id="70750-256">Faux</span><span class="sxs-lookup"><span data-stu-id="70750-256">False</span></span>                                                               |
| <span data-ttu-id="70750-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="70750-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="70750-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="70750-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="70750-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70750-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70750-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="70750-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-261">Search-Flags</span></span>           | <span data-ttu-id="70750-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70750-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="70750-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70750-263">System-Flags</span></span>           | <span data-ttu-id="70750-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70750-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="70750-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="70750-265">Classes used in</span></span>        | [<span data-ttu-id="70750-266">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="70750-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





