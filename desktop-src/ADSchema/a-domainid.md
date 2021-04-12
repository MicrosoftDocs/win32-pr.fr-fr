---
title: Attribut de nom de domaine
description: Référence à un domaine associé à une autorité de certification.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut d’ID de domaine
- Schéma AD de l’attribut domaine
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c321fdea062ccbca907e22a2d72b06c26110ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385359"
---
# <a name="domain-id-attribute"></a><span data-ttu-id="350d3-105">Attribut de nom de domaine</span><span class="sxs-lookup"><span data-stu-id="350d3-105">Domain-ID attribute</span></span>

<span data-ttu-id="350d3-106">Référence à un domaine associé à une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="350d3-106">Reference to a domain that is associated with a certification authority.</span></span>



| <span data-ttu-id="350d3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-107">Entry</span></span> | <span data-ttu-id="350d3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="350d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="350d3-109">CN</span></span>                | <span data-ttu-id="350d3-110">ID de domaine</span><span class="sxs-lookup"><span data-stu-id="350d3-110">Domain-ID</span></span>                               |
| <span data-ttu-id="350d3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="350d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="350d3-112">Domaine</span><span class="sxs-lookup"><span data-stu-id="350d3-112">domainID</span></span>                                |
| <span data-ttu-id="350d3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="350d3-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="350d3-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="350d3-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="350d3-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="350d3-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="350d3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-116">Attribute-Id</span></span>      | <span data-ttu-id="350d3-117">1.2.840.113556.1.4.686</span><span class="sxs-lookup"><span data-stu-id="350d3-117">1.2.840.113556.1.4.686</span></span>                  |
| <span data-ttu-id="350d3-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="350d3-118">System-Id-Guid</span></span>    | <span data-ttu-id="350d3-119">963d2734-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="350d3-119">963d2734-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="350d3-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="350d3-120">Syntax</span></span>            | [<span data-ttu-id="350d3-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="350d3-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="350d3-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="350d3-122">Implementations</span></span>

-   [<span data-ttu-id="350d3-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="350d3-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="350d3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="350d3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="350d3-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="350d3-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="350d3-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="350d3-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="350d3-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="350d3-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="350d3-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="350d3-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="350d3-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="350d3-129">Windows 2000 Server</span></span>



| <span data-ttu-id="350d3-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-130">Entry</span></span> | <span data-ttu-id="350d3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-134">System-Only</span></span>            | <span data-ttu-id="350d3-135">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-135">False</span></span>                                                                  |
| <span data-ttu-id="350d3-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-136">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-137">True</span></span>                                                                   |
| <span data-ttu-id="350d3-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-138">Is Indexed</span></span>             | <span data-ttu-id="350d3-139">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-139">False</span></span>                                                                  |
| <span data-ttu-id="350d3-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-140">In Global Catalog</span></span>      | <span data-ttu-id="350d3-141">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-141">False</span></span>                                                                  |
| <span data-ttu-id="350d3-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-146">Search-Flags</span></span>           | <span data-ttu-id="350d3-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-148">System-Flags</span></span>           | <span data-ttu-id="350d3-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-150">Classes used in</span></span>        | [<span data-ttu-id="350d3-151">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="350d3-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="350d3-152">Windows Server 2003</span></span>



| <span data-ttu-id="350d3-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-153">Entry</span></span> | <span data-ttu-id="350d3-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-157">System-Only</span></span>            | <span data-ttu-id="350d3-158">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-158">False</span></span>                                                                  |
| <span data-ttu-id="350d3-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-159">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-160">True</span></span>                                                                   |
| <span data-ttu-id="350d3-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-161">Is Indexed</span></span>             | <span data-ttu-id="350d3-162">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-162">False</span></span>                                                                  |
| <span data-ttu-id="350d3-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-163">In Global Catalog</span></span>      | <span data-ttu-id="350d3-164">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-164">False</span></span>                                                                  |
| <span data-ttu-id="350d3-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-169">Search-Flags</span></span>           | <span data-ttu-id="350d3-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-171">System-Flags</span></span>           | <span data-ttu-id="350d3-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-173">Classes used in</span></span>        | [<span data-ttu-id="350d3-174">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="350d3-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="350d3-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="350d3-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-176">Entry</span></span> | <span data-ttu-id="350d3-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-180">System-Only</span></span>            | <span data-ttu-id="350d3-181">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-181">False</span></span>                                                                  |
| <span data-ttu-id="350d3-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-182">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-183">True</span></span>                                                                   |
| <span data-ttu-id="350d3-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-184">Is Indexed</span></span>             | <span data-ttu-id="350d3-185">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-185">False</span></span>                                                                  |
| <span data-ttu-id="350d3-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-186">In Global Catalog</span></span>      | <span data-ttu-id="350d3-187">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-187">False</span></span>                                                                  |
| <span data-ttu-id="350d3-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-192">Search-Flags</span></span>           | <span data-ttu-id="350d3-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-194">System-Flags</span></span>           | <span data-ttu-id="350d3-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-196">Classes used in</span></span>        | [<span data-ttu-id="350d3-197">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="350d3-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="350d3-198">Windows Server 2008</span></span>



| <span data-ttu-id="350d3-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-199">Entry</span></span> | <span data-ttu-id="350d3-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-203">System-Only</span></span>            | <span data-ttu-id="350d3-204">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-204">False</span></span>                                                                  |
| <span data-ttu-id="350d3-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-205">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-206">True</span></span>                                                                   |
| <span data-ttu-id="350d3-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-207">Is Indexed</span></span>             | <span data-ttu-id="350d3-208">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-208">False</span></span>                                                                  |
| <span data-ttu-id="350d3-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-209">In Global Catalog</span></span>      | <span data-ttu-id="350d3-210">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-210">False</span></span>                                                                  |
| <span data-ttu-id="350d3-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-215">Search-Flags</span></span>           | <span data-ttu-id="350d3-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-217">System-Flags</span></span>           | <span data-ttu-id="350d3-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-219">Classes used in</span></span>        | [<span data-ttu-id="350d3-220">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="350d3-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="350d3-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="350d3-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-222">Entry</span></span> | <span data-ttu-id="350d3-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-226">System-Only</span></span>            | <span data-ttu-id="350d3-227">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-227">False</span></span>                                                                  |
| <span data-ttu-id="350d3-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-228">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-229">True</span></span>                                                                   |
| <span data-ttu-id="350d3-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-230">Is Indexed</span></span>             | <span data-ttu-id="350d3-231">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-231">False</span></span>                                                                  |
| <span data-ttu-id="350d3-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-232">In Global Catalog</span></span>      | <span data-ttu-id="350d3-233">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-233">False</span></span>                                                                  |
| <span data-ttu-id="350d3-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-238">Search-Flags</span></span>           | <span data-ttu-id="350d3-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-240">System-Flags</span></span>           | <span data-ttu-id="350d3-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-242">Classes used in</span></span>        | [<span data-ttu-id="350d3-243">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="350d3-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="350d3-244">Windows Server 2012</span></span>



| <span data-ttu-id="350d3-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="350d3-245">Entry</span></span> | <span data-ttu-id="350d3-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="350d3-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="350d3-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="350d3-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350d3-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="350d3-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="350d3-249">System-Only</span></span>            | <span data-ttu-id="350d3-250">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-250">False</span></span>                                                                  |
| <span data-ttu-id="350d3-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="350d3-251">Is-Single-Valued</span></span>       | <span data-ttu-id="350d3-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="350d3-252">True</span></span>                                                                   |
| <span data-ttu-id="350d3-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="350d3-253">Is Indexed</span></span>             | <span data-ttu-id="350d3-254">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-254">False</span></span>                                                                  |
| <span data-ttu-id="350d3-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="350d3-255">In Global Catalog</span></span>      | <span data-ttu-id="350d3-256">Faux</span><span class="sxs-lookup"><span data-stu-id="350d3-256">False</span></span>                                                                  |
| <span data-ttu-id="350d3-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="350d3-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="350d3-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="350d3-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="350d3-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350d3-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350d3-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="350d3-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-261">Search-Flags</span></span>           | <span data-ttu-id="350d3-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350d3-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="350d3-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350d3-263">System-Flags</span></span>           | <span data-ttu-id="350d3-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350d3-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="350d3-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="350d3-265">Classes used in</span></span>        | [<span data-ttu-id="350d3-266">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="350d3-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





