---
title: attribut ms-DS-Top-quota-usage
description: Liste des premiers utilisateurs du quota actuellement dans la base de données d’annuaire, classés en diminuant l’utilisation du quota.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-Top-quota-usage
- Schéma Active Directory de l’attribut msDS-TopQuotaUsage
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516529"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="f4bde-105">attribut ms-DS-Top-quota-usage</span><span class="sxs-lookup"><span data-stu-id="f4bde-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="f4bde-106">Liste des premiers utilisateurs du quota actuellement dans la base de données d’annuaire, classés en diminuant l’utilisation du quota.</span><span class="sxs-lookup"><span data-stu-id="f4bde-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="f4bde-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-107">Entry</span></span> | <span data-ttu-id="f4bde-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f4bde-109">CN</span><span class="sxs-lookup"><span data-stu-id="f4bde-109">CN</span></span>                | <span data-ttu-id="f4bde-110">ms-DS-Top-quota-utilisation</span><span class="sxs-lookup"><span data-stu-id="f4bde-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="f4bde-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f4bde-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f4bde-112">msDS-TopQuotaUsage</span><span class="sxs-lookup"><span data-stu-id="f4bde-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="f4bde-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f4bde-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f4bde-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f4bde-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f4bde-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f4bde-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f4bde-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-116">Attribute-Id</span></span>      | <span data-ttu-id="f4bde-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="f4bde-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="f4bde-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f4bde-118">System-Id-Guid</span></span>    | <span data-ttu-id="f4bde-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="f4bde-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="f4bde-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4bde-120">Syntax</span></span>            | [<span data-ttu-id="f4bde-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f4bde-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f4bde-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f4bde-122">Implementations</span></span>

-   [<span data-ttu-id="f4bde-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4bde-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4bde-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f4bde-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f4bde-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4bde-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4bde-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4bde-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4bde-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4bde-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4bde-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4bde-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f4bde-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4bde-129">Windows Server 2003</span></span>



| <span data-ttu-id="f4bde-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-130">Entry</span></span> | <span data-ttu-id="f4bde-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-134">System-Only</span></span>            | <span data-ttu-id="f4bde-135">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-135">False</span></span>                                                             |
| <span data-ttu-id="f4bde-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-137">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-137">False</span></span>                                                             |
| <span data-ttu-id="f4bde-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-138">Is Indexed</span></span>             | <span data-ttu-id="f4bde-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-139">False</span></span>                                                             |
| <span data-ttu-id="f4bde-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-140">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-141">False</span></span>                                                             |
| <span data-ttu-id="f4bde-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-146">Search-Flags</span></span>           | <span data-ttu-id="f4bde-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-148">System-Flags</span></span>           | <span data-ttu-id="f4bde-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-150">Classes used in</span></span>        | [<span data-ttu-id="f4bde-151">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f4bde-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="f4bde-152">ADAM</span></span>



| <span data-ttu-id="f4bde-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-153">Entry</span></span> | <span data-ttu-id="f4bde-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-157">System-Only</span></span>            | <span data-ttu-id="f4bde-158">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-158">False</span></span>                                                             |
| <span data-ttu-id="f4bde-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-160">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-160">False</span></span>                                                             |
| <span data-ttu-id="f4bde-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-161">Is Indexed</span></span>             | <span data-ttu-id="f4bde-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-162">False</span></span>                                                             |
| <span data-ttu-id="f4bde-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-163">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-164">False</span></span>                                                             |
| <span data-ttu-id="f4bde-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-169">Search-Flags</span></span>           | <span data-ttu-id="f4bde-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-171">System-Flags</span></span>           | <span data-ttu-id="f4bde-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-173">Classes used in</span></span>        | [<span data-ttu-id="f4bde-174">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4bde-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4bde-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4bde-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-176">Entry</span></span> | <span data-ttu-id="f4bde-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-180">System-Only</span></span>            | <span data-ttu-id="f4bde-181">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-181">False</span></span>                                                             |
| <span data-ttu-id="f4bde-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-183">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-183">False</span></span>                                                             |
| <span data-ttu-id="f4bde-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-184">Is Indexed</span></span>             | <span data-ttu-id="f4bde-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-185">False</span></span>                                                             |
| <span data-ttu-id="f4bde-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-186">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-187">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-187">False</span></span>                                                             |
| <span data-ttu-id="f4bde-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-192">Search-Flags</span></span>           | <span data-ttu-id="f4bde-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-194">System-Flags</span></span>           | <span data-ttu-id="f4bde-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-196">Classes used in</span></span>        | [<span data-ttu-id="f4bde-197">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4bde-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4bde-198">Windows Server 2008</span></span>



| <span data-ttu-id="f4bde-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-199">Entry</span></span> | <span data-ttu-id="f4bde-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-203">System-Only</span></span>            | <span data-ttu-id="f4bde-204">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-204">False</span></span>                                                             |
| <span data-ttu-id="f4bde-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-206">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-206">False</span></span>                                                             |
| <span data-ttu-id="f4bde-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-207">Is Indexed</span></span>             | <span data-ttu-id="f4bde-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-208">False</span></span>                                                             |
| <span data-ttu-id="f4bde-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-209">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-210">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-210">False</span></span>                                                             |
| <span data-ttu-id="f4bde-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-215">Search-Flags</span></span>           | <span data-ttu-id="f4bde-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-217">System-Flags</span></span>           | <span data-ttu-id="f4bde-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-219">Classes used in</span></span>        | [<span data-ttu-id="f4bde-220">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4bde-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4bde-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4bde-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-222">Entry</span></span> | <span data-ttu-id="f4bde-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-226">System-Only</span></span>            | <span data-ttu-id="f4bde-227">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-227">False</span></span>                                                             |
| <span data-ttu-id="f4bde-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-229">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-229">False</span></span>                                                             |
| <span data-ttu-id="f4bde-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-230">Is Indexed</span></span>             | <span data-ttu-id="f4bde-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-231">False</span></span>                                                             |
| <span data-ttu-id="f4bde-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-232">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-233">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-233">False</span></span>                                                             |
| <span data-ttu-id="f4bde-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-238">Search-Flags</span></span>           | <span data-ttu-id="f4bde-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-240">System-Flags</span></span>           | <span data-ttu-id="f4bde-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-242">Classes used in</span></span>        | [<span data-ttu-id="f4bde-243">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4bde-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4bde-244">Windows Server 2012</span></span>



| <span data-ttu-id="f4bde-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4bde-245">Entry</span></span> | <span data-ttu-id="f4bde-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4bde-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4bde-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4bde-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4bde-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4bde-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4bde-249">System-Only</span></span>            | <span data-ttu-id="f4bde-250">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-250">False</span></span>                                                             |
| <span data-ttu-id="f4bde-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4bde-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f4bde-252">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-252">False</span></span>                                                             |
| <span data-ttu-id="f4bde-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4bde-253">Is Indexed</span></span>             | <span data-ttu-id="f4bde-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-254">False</span></span>                                                             |
| <span data-ttu-id="f4bde-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4bde-255">In Global Catalog</span></span>      | <span data-ttu-id="f4bde-256">Faux</span><span class="sxs-lookup"><span data-stu-id="f4bde-256">False</span></span>                                                             |
| <span data-ttu-id="f4bde-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4bde-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4bde-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4bde-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4bde-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4bde-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4bde-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4bde-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-261">Search-Flags</span></span>           | <span data-ttu-id="f4bde-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4bde-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4bde-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4bde-263">System-Flags</span></span>           | <span data-ttu-id="f4bde-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f4bde-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="f4bde-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4bde-265">Classes used in</span></span>        | [<span data-ttu-id="f4bde-266">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4bde-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





