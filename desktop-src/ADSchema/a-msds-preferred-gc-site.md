---
title: ms-DS-Preferred-attribut-GC-site
description: L’attribut ms-DS-Preferred-GC-site est utilisé par le gestionnaire de comptes de sécurité pour l’extension de groupe lors de l’évaluation du jeton.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-Preferred-GC-site
- Schéma AD de l’attribut msDS-Preferred-GC-site
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104200609"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="526d2-105">ms-DS-Preferred-attribut-GC-site</span><span class="sxs-lookup"><span data-stu-id="526d2-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="526d2-106">L’attribut **ms-DS-Preferred-gc-site** est utilisé par le gestionnaire de comptes de sécurité pour l’extension de groupe lors de l’évaluation du jeton.</span><span class="sxs-lookup"><span data-stu-id="526d2-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="526d2-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-107">Entry</span></span> | <span data-ttu-id="526d2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="526d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="526d2-109">CN</span></span>                | <span data-ttu-id="526d2-110">ms-DS-préféré-GC-site</span><span class="sxs-lookup"><span data-stu-id="526d2-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="526d2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="526d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="526d2-112">msDS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="526d2-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="526d2-113">Taille</span><span class="sxs-lookup"><span data-stu-id="526d2-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="526d2-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="526d2-114">Update Privilege</span></span>  | <span data-ttu-id="526d2-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="526d2-115">Domain administrator</span></span>                    |
| <span data-ttu-id="526d2-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="526d2-116">Update Frequency</span></span>  | <span data-ttu-id="526d2-117">À la discrétion de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="526d2-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="526d2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-118">Attribute-Id</span></span>      | <span data-ttu-id="526d2-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="526d2-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="526d2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="526d2-120">System-Id-Guid</span></span>    | <span data-ttu-id="526d2-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="526d2-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="526d2-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="526d2-122">Syntax</span></span>            | [<span data-ttu-id="526d2-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="526d2-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="526d2-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="526d2-124">Implementations</span></span>

-   [<span data-ttu-id="526d2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="526d2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="526d2-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="526d2-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="526d2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="526d2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="526d2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="526d2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="526d2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="526d2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="526d2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="526d2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="526d2-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="526d2-131">Windows Server 2003</span></span>



| <span data-ttu-id="526d2-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-132">Entry</span></span> | <span data-ttu-id="526d2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-136">System-Only</span></span>            | <span data-ttu-id="526d2-137">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-137">False</span></span>                                                       |
| <span data-ttu-id="526d2-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-139">True</span></span>                                                        |
| <span data-ttu-id="526d2-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-140">Is Indexed</span></span>             | <span data-ttu-id="526d2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-141">False</span></span>                                                       |
| <span data-ttu-id="526d2-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-142">In Global Catalog</span></span>      | <span data-ttu-id="526d2-143">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-143">False</span></span>                                                       |
| <span data-ttu-id="526d2-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-148">Search-Flags</span></span>           | <span data-ttu-id="526d2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-150">System-Flags</span></span>           | <span data-ttu-id="526d2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-152">Classes used in</span></span>        | [<span data-ttu-id="526d2-153">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="526d2-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="526d2-154">ADAM</span></span>



| <span data-ttu-id="526d2-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-155">Entry</span></span> | <span data-ttu-id="526d2-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-159">System-Only</span></span>            | <span data-ttu-id="526d2-160">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-160">False</span></span>                                                       |
| <span data-ttu-id="526d2-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-162">True</span></span>                                                        |
| <span data-ttu-id="526d2-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-163">Is Indexed</span></span>             | <span data-ttu-id="526d2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-164">False</span></span>                                                       |
| <span data-ttu-id="526d2-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-165">In Global Catalog</span></span>      | <span data-ttu-id="526d2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-166">False</span></span>                                                       |
| <span data-ttu-id="526d2-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-171">Search-Flags</span></span>           | <span data-ttu-id="526d2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-173">System-Flags</span></span>           | <span data-ttu-id="526d2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-175">Classes used in</span></span>        | [<span data-ttu-id="526d2-176">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="526d2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="526d2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="526d2-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-178">Entry</span></span> | <span data-ttu-id="526d2-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-182">System-Only</span></span>            | <span data-ttu-id="526d2-183">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-183">False</span></span>                                                       |
| <span data-ttu-id="526d2-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-185">True</span></span>                                                        |
| <span data-ttu-id="526d2-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-186">Is Indexed</span></span>             | <span data-ttu-id="526d2-187">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-187">False</span></span>                                                       |
| <span data-ttu-id="526d2-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-188">In Global Catalog</span></span>      | <span data-ttu-id="526d2-189">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-189">False</span></span>                                                       |
| <span data-ttu-id="526d2-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-194">Search-Flags</span></span>           | <span data-ttu-id="526d2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-196">System-Flags</span></span>           | <span data-ttu-id="526d2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-198">Classes used in</span></span>        | [<span data-ttu-id="526d2-199">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="526d2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="526d2-200">Windows Server 2008</span></span>



| <span data-ttu-id="526d2-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-201">Entry</span></span> | <span data-ttu-id="526d2-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-205">System-Only</span></span>            | <span data-ttu-id="526d2-206">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-206">False</span></span>                                                       |
| <span data-ttu-id="526d2-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-208">True</span></span>                                                        |
| <span data-ttu-id="526d2-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-209">Is Indexed</span></span>             | <span data-ttu-id="526d2-210">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-210">False</span></span>                                                       |
| <span data-ttu-id="526d2-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-211">In Global Catalog</span></span>      | <span data-ttu-id="526d2-212">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-212">False</span></span>                                                       |
| <span data-ttu-id="526d2-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-217">Search-Flags</span></span>           | <span data-ttu-id="526d2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-219">System-Flags</span></span>           | <span data-ttu-id="526d2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-221">Classes used in</span></span>        | [<span data-ttu-id="526d2-222">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="526d2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="526d2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="526d2-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-224">Entry</span></span> | <span data-ttu-id="526d2-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-228">System-Only</span></span>            | <span data-ttu-id="526d2-229">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-229">False</span></span>                                                       |
| <span data-ttu-id="526d2-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-231">True</span></span>                                                        |
| <span data-ttu-id="526d2-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-232">Is Indexed</span></span>             | <span data-ttu-id="526d2-233">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-233">False</span></span>                                                       |
| <span data-ttu-id="526d2-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-234">In Global Catalog</span></span>      | <span data-ttu-id="526d2-235">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-235">False</span></span>                                                       |
| <span data-ttu-id="526d2-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-240">Search-Flags</span></span>           | <span data-ttu-id="526d2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-242">System-Flags</span></span>           | <span data-ttu-id="526d2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-244">Classes used in</span></span>        | [<span data-ttu-id="526d2-245">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="526d2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="526d2-246">Windows Server 2012</span></span>



| <span data-ttu-id="526d2-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="526d2-247">Entry</span></span> | <span data-ttu-id="526d2-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="526d2-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="526d2-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="526d2-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="526d2-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="526d2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="526d2-251">System-Only</span></span>            | <span data-ttu-id="526d2-252">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-252">False</span></span>                                                       |
| <span data-ttu-id="526d2-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="526d2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="526d2-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="526d2-254">True</span></span>                                                        |
| <span data-ttu-id="526d2-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="526d2-255">Is Indexed</span></span>             | <span data-ttu-id="526d2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-256">False</span></span>                                                       |
| <span data-ttu-id="526d2-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="526d2-257">In Global Catalog</span></span>      | <span data-ttu-id="526d2-258">Faux</span><span class="sxs-lookup"><span data-stu-id="526d2-258">False</span></span>                                                       |
| <span data-ttu-id="526d2-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="526d2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="526d2-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="526d2-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="526d2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="526d2-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="526d2-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="526d2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-263">Search-Flags</span></span>           | <span data-ttu-id="526d2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="526d2-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="526d2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="526d2-265">System-Flags</span></span>           | <span data-ttu-id="526d2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="526d2-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="526d2-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="526d2-267">Classes used in</span></span>        | [<span data-ttu-id="526d2-268">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="526d2-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





