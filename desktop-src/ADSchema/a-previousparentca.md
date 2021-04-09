---
title: Attribut parent-CA précédent
description: Référence aux autorités de certification qui ont émis le dernier certificat expiré pour une autorité de certification.
ms.assetid: 9772d6cb-1105-426c-9982-473b4c1bf0d8
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut parent-CA précédent
- Schéma AD de l’attribut previousParentCA
topic_type:
- apiref
api_name:
- Previous-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a4c89652ef7ffffdc731614cfc57572b3edcde
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104033286"
---
# <a name="previous-parent-ca-attribute"></a><span data-ttu-id="c2d17-105">Attribut parent-CA précédent</span><span class="sxs-lookup"><span data-stu-id="c2d17-105">Previous-Parent-CA attribute</span></span>

<span data-ttu-id="c2d17-106">Référence aux autorités de certification qui ont émis le dernier certificat expiré pour une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="c2d17-106">Reference to the certification authorities that issued the last expired certificate for a certification authority.</span></span>



| <span data-ttu-id="c2d17-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-107">Entry</span></span> | <span data-ttu-id="c2d17-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c2d17-109">CN</span><span class="sxs-lookup"><span data-stu-id="c2d17-109">CN</span></span>                | <span data-ttu-id="c2d17-110">Previous-parent-CA</span><span class="sxs-lookup"><span data-stu-id="c2d17-110">Previous-Parent-CA</span></span>                      |
| <span data-ttu-id="c2d17-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c2d17-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c2d17-112">previousParentCA</span><span class="sxs-lookup"><span data-stu-id="c2d17-112">previousParentCA</span></span>                        |
| <span data-ttu-id="c2d17-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c2d17-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c2d17-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c2d17-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c2d17-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c2d17-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c2d17-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-116">Attribute-Id</span></span>      | <span data-ttu-id="c2d17-117">1.2.840.113556.1.4.694</span><span class="sxs-lookup"><span data-stu-id="c2d17-117">1.2.840.113556.1.4.694</span></span>                  |
| <span data-ttu-id="c2d17-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2d17-118">System-Id-Guid</span></span>    | <span data-ttu-id="c2d17-119">963d273d-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c2d17-119">963d273d-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="c2d17-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2d17-120">Syntax</span></span>            | [<span data-ttu-id="c2d17-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c2d17-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c2d17-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c2d17-122">Implementations</span></span>

-   [<span data-ttu-id="c2d17-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2d17-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2d17-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2d17-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2d17-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2d17-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2d17-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2d17-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2d17-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2d17-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2d17-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2d17-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2d17-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2d17-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c2d17-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-130">Entry</span></span> | <span data-ttu-id="c2d17-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-134">System-Only</span></span>            | <span data-ttu-id="c2d17-135">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-135">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-137">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-138">Is Indexed</span></span>             | <span data-ttu-id="c2d17-139">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-139">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-140">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-141">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-146">Search-Flags</span></span>           | <span data-ttu-id="c2d17-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-148">System-Flags</span></span>           | <span data-ttu-id="c2d17-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-150">Classes used in</span></span>        | [<span data-ttu-id="c2d17-151">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2d17-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2d17-152">Windows Server 2003</span></span>



| <span data-ttu-id="c2d17-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-153">Entry</span></span> | <span data-ttu-id="c2d17-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-157">System-Only</span></span>            | <span data-ttu-id="c2d17-158">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-158">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-160">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-160">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-161">Is Indexed</span></span>             | <span data-ttu-id="c2d17-162">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-162">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-163">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-164">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-169">Search-Flags</span></span>           | <span data-ttu-id="c2d17-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-171">System-Flags</span></span>           | <span data-ttu-id="c2d17-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-173">Classes used in</span></span>        | [<span data-ttu-id="c2d17-174">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2d17-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2d17-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2d17-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-176">Entry</span></span> | <span data-ttu-id="c2d17-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-180">System-Only</span></span>            | <span data-ttu-id="c2d17-181">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-181">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-183">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-183">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-184">Is Indexed</span></span>             | <span data-ttu-id="c2d17-185">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-185">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-186">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-187">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-187">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-192">Search-Flags</span></span>           | <span data-ttu-id="c2d17-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-194">System-Flags</span></span>           | <span data-ttu-id="c2d17-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-196">Classes used in</span></span>        | [<span data-ttu-id="c2d17-197">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2d17-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2d17-198">Windows Server 2008</span></span>



| <span data-ttu-id="c2d17-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-199">Entry</span></span> | <span data-ttu-id="c2d17-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-203">System-Only</span></span>            | <span data-ttu-id="c2d17-204">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-204">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-206">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-206">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-207">Is Indexed</span></span>             | <span data-ttu-id="c2d17-208">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-208">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-209">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-210">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-210">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-215">Search-Flags</span></span>           | <span data-ttu-id="c2d17-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-217">System-Flags</span></span>           | <span data-ttu-id="c2d17-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-219">Classes used in</span></span>        | [<span data-ttu-id="c2d17-220">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2d17-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2d17-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2d17-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-222">Entry</span></span> | <span data-ttu-id="c2d17-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-226">System-Only</span></span>            | <span data-ttu-id="c2d17-227">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-227">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-229">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-229">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-230">Is Indexed</span></span>             | <span data-ttu-id="c2d17-231">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-231">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-232">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-233">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-233">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-238">Search-Flags</span></span>           | <span data-ttu-id="c2d17-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-240">System-Flags</span></span>           | <span data-ttu-id="c2d17-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-242">Classes used in</span></span>        | [<span data-ttu-id="c2d17-243">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2d17-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2d17-244">Windows Server 2012</span></span>



| <span data-ttu-id="c2d17-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="c2d17-245">Entry</span></span> | <span data-ttu-id="c2d17-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d17-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c2d17-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2d17-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c2d17-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2d17-249">System-Only</span></span>            | <span data-ttu-id="c2d17-250">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-250">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c2d17-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c2d17-252">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-252">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c2d17-253">Is Indexed</span></span>             | <span data-ttu-id="c2d17-254">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-254">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c2d17-255">In Global Catalog</span></span>      | <span data-ttu-id="c2d17-256">Faux</span><span class="sxs-lookup"><span data-stu-id="c2d17-256">False</span></span>                                                                  |
| <span data-ttu-id="c2d17-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c2d17-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2d17-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c2d17-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c2d17-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2d17-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2d17-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c2d17-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-261">Search-Flags</span></span>           | <span data-ttu-id="c2d17-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2d17-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="c2d17-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2d17-263">System-Flags</span></span>           | <span data-ttu-id="c2d17-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2d17-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="c2d17-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c2d17-265">Classes used in</span></span>        | [<span data-ttu-id="c2d17-266">**Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="c2d17-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





