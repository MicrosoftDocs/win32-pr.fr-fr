---
title: Attribut de liste de révocation de certificats
description: Représente une liste de certificats qui ont été révoqués.
ms.assetid: fb7b4888-15c0-475b-a87a-7cb0656963bb
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de liste de révocation de certificats
- Schéma AD de l’attribut certificateRevocationList
topic_type:
- apiref
api_name:
- Certificate-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae77265ffeeae76ae07d608845723b1828772f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107266"
---
# <a name="certificate-revocation-list-attribute"></a><span data-ttu-id="586ca-105">Attribut de liste de révocation de certificats</span><span class="sxs-lookup"><span data-stu-id="586ca-105">Certificate-Revocation-List attribute</span></span>

<span data-ttu-id="586ca-106">Représente une liste de certificats qui ont été révoqués.</span><span class="sxs-lookup"><span data-stu-id="586ca-106">Represents a list of certificates that have been revoked.</span></span>



| <span data-ttu-id="586ca-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-107">Entry</span></span> | <span data-ttu-id="586ca-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="586ca-109">CN</span><span class="sxs-lookup"><span data-stu-id="586ca-109">CN</span></span>                | <span data-ttu-id="586ca-110">Certificat-révocation-liste</span><span class="sxs-lookup"><span data-stu-id="586ca-110">Certificate-Revocation-List</span></span>                           |
| <span data-ttu-id="586ca-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="586ca-111">Ldap-Display-Name</span></span> | <span data-ttu-id="586ca-112">certificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="586ca-112">certificateRevocationList</span></span>                             |
| <span data-ttu-id="586ca-113">Taille</span><span class="sxs-lookup"><span data-stu-id="586ca-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="586ca-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="586ca-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="586ca-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="586ca-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="586ca-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-116">Attribute-Id</span></span>      | <span data-ttu-id="586ca-117">2.5.4.39</span><span class="sxs-lookup"><span data-stu-id="586ca-117">2.5.4.39</span></span>                                              |
| <span data-ttu-id="586ca-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="586ca-118">System-Id-Guid</span></span>    | <span data-ttu-id="586ca-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="586ca-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="586ca-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="586ca-120">Syntax</span></span>            | [<span data-ttu-id="586ca-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="586ca-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="586ca-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="586ca-122">Implementations</span></span>

-   [<span data-ttu-id="586ca-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="586ca-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="586ca-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="586ca-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="586ca-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="586ca-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="586ca-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="586ca-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="586ca-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="586ca-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="586ca-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="586ca-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="586ca-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="586ca-129">Windows 2000 Server</span></span>



| <span data-ttu-id="586ca-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-130">Entry</span></span> | <span data-ttu-id="586ca-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-133">MAPI-Id</span></span>                | <span data-ttu-id="586ca-134">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-134">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-135">System-Only</span></span>            | <span data-ttu-id="586ca-136">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-137">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-138">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-139">Is Indexed</span></span>             | <span data-ttu-id="586ca-140">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-141">In Global Catalog</span></span>      | <span data-ttu-id="586ca-142">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-147">Search-Flags</span></span>           | <span data-ttu-id="586ca-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-149">System-Flags</span></span>           | <span data-ttu-id="586ca-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-151">Classes used in</span></span>        | [<span data-ttu-id="586ca-152">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-153">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="586ca-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="586ca-154">Windows Server 2003</span></span>



| <span data-ttu-id="586ca-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-155">Entry</span></span> | <span data-ttu-id="586ca-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-158">MAPI-Id</span></span>                | <span data-ttu-id="586ca-159">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-159">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-160">System-Only</span></span>            | <span data-ttu-id="586ca-161">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-162">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-163">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-164">Is Indexed</span></span>             | <span data-ttu-id="586ca-165">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-166">In Global Catalog</span></span>      | <span data-ttu-id="586ca-167">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-172">Search-Flags</span></span>           | <span data-ttu-id="586ca-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-174">System-Flags</span></span>           | <span data-ttu-id="586ca-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-176">Classes used in</span></span>        | [<span data-ttu-id="586ca-177">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-178">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="586ca-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="586ca-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="586ca-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-180">Entry</span></span> | <span data-ttu-id="586ca-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-183">MAPI-Id</span></span>                | <span data-ttu-id="586ca-184">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-184">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-185">System-Only</span></span>            | <span data-ttu-id="586ca-186">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-187">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-188">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-189">Is Indexed</span></span>             | <span data-ttu-id="586ca-190">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-191">In Global Catalog</span></span>      | <span data-ttu-id="586ca-192">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-197">Search-Flags</span></span>           | <span data-ttu-id="586ca-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-199">System-Flags</span></span>           | <span data-ttu-id="586ca-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-201">Classes used in</span></span>        | [<span data-ttu-id="586ca-202">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-203">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="586ca-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="586ca-204">Windows Server 2008</span></span>



| <span data-ttu-id="586ca-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-205">Entry</span></span> | <span data-ttu-id="586ca-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-208">MAPI-Id</span></span>                | <span data-ttu-id="586ca-209">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-209">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-210">System-Only</span></span>            | <span data-ttu-id="586ca-211">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-212">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-214">Is Indexed</span></span>             | <span data-ttu-id="586ca-215">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-216">In Global Catalog</span></span>      | <span data-ttu-id="586ca-217">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-222">Search-Flags</span></span>           | <span data-ttu-id="586ca-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-224">System-Flags</span></span>           | <span data-ttu-id="586ca-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-226">Classes used in</span></span>        | [<span data-ttu-id="586ca-227">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-228">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="586ca-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="586ca-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="586ca-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-230">Entry</span></span> | <span data-ttu-id="586ca-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-233">MAPI-Id</span></span>                | <span data-ttu-id="586ca-234">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-234">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-235">System-Only</span></span>            | <span data-ttu-id="586ca-236">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-237">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-238">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-239">Is Indexed</span></span>             | <span data-ttu-id="586ca-240">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-241">In Global Catalog</span></span>      | <span data-ttu-id="586ca-242">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-247">Search-Flags</span></span>           | <span data-ttu-id="586ca-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-249">System-Flags</span></span>           | <span data-ttu-id="586ca-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-251">Classes used in</span></span>        | [<span data-ttu-id="586ca-252">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-253">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="586ca-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="586ca-254">Windows Server 2012</span></span>



| <span data-ttu-id="586ca-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="586ca-255">Entry</span></span> | <span data-ttu-id="586ca-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="586ca-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ca-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="586ca-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="586ca-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586ca-258">MAPI-Id</span></span>                | <span data-ttu-id="586ca-259">0x8016</span><span class="sxs-lookup"><span data-stu-id="586ca-259">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="586ca-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="586ca-260">System-Only</span></span>            | <span data-ttu-id="586ca-261">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-262">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="586ca-262">Is-Single-Valued</span></span>       | <span data-ttu-id="586ca-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="586ca-263">True</span></span>                                                                                                                                       |
| <span data-ttu-id="586ca-264">Est indexé</span><span class="sxs-lookup"><span data-stu-id="586ca-264">Is Indexed</span></span>             | <span data-ttu-id="586ca-265">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-266">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="586ca-266">In Global Catalog</span></span>      | <span data-ttu-id="586ca-267">Faux</span><span class="sxs-lookup"><span data-stu-id="586ca-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="586ca-268">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="586ca-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="586ca-269">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="586ca-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="586ca-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586ca-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586ca-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="586ca-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-272">Search-Flags</span></span>           | <span data-ttu-id="586ca-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="586ca-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586ca-274">System-Flags</span></span>           | <span data-ttu-id="586ca-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="586ca-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="586ca-276">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="586ca-276">Classes used in</span></span>        | [<span data-ttu-id="586ca-277">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="586ca-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="586ca-278">**Point de distribution de liste de révocation de certificats**</span><span class="sxs-lookup"><span data-stu-id="586ca-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





