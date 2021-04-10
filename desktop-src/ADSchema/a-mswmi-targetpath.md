---
title: MS-WMI-TargetPath (attribut)
description: Liste de paires clé/valeur permettant d’identifier de façon unique un objet WMI.
ms.assetid: b5d6c718-86f6-40a5-8fb1-e3ed4821ac62
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-WMI-TargetPath
- Schéma AD de l’attribut msWMI-TargetPath
topic_type:
- apiref
api_name:
- ms-WMI-TargetPath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9818125d757716970cff538167d5d737a8354555
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943126"
---
# <a name="ms-wmi-targetpath-attribute"></a><span data-ttu-id="cd1e8-105">MS-WMI-TargetPath (attribut)</span><span class="sxs-lookup"><span data-stu-id="cd1e8-105">ms-WMI-TargetPath attribute</span></span>

<span data-ttu-id="cd1e8-106">Liste de paires clé/valeur permettant d’identifier de façon unique un objet WMI.</span><span class="sxs-lookup"><span data-stu-id="cd1e8-106">List of key/value pairs for uniquely identifying a WMI object.</span></span>



| <span data-ttu-id="cd1e8-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-107">Entry</span></span> | <span data-ttu-id="cd1e8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cd1e8-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd1e8-109">CN</span></span>                | <span data-ttu-id="cd1e8-110">MS-WMI-TargetPath</span><span class="sxs-lookup"><span data-stu-id="cd1e8-110">ms-WMI-TargetPath</span></span>                           |
| <span data-ttu-id="cd1e8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cd1e8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd1e8-112">msWMI-TargetPath</span><span class="sxs-lookup"><span data-stu-id="cd1e8-112">msWMI-TargetPath</span></span>                            |
| <span data-ttu-id="cd1e8-113">Taille</span><span class="sxs-lookup"><span data-stu-id="cd1e8-113">Size</span></span>              | <span data-ttu-id="cd1e8-114">Moins de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="cd1e8-114">Less than 100 characters.</span></span>                   |
| <span data-ttu-id="cd1e8-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cd1e8-115">Update Privilege</span></span>  | <span data-ttu-id="cd1e8-116">Administrateur stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cd1e8-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="cd1e8-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cd1e8-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cd1e8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-118">Attribute-Id</span></span>      | <span data-ttu-id="cd1e8-119">1.2.840.113556.1.4.1648</span><span class="sxs-lookup"><span data-stu-id="cd1e8-119">1.2.840.113556.1.4.1648</span></span>                     |
| <span data-ttu-id="cd1e8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd1e8-120">System-Id-Guid</span></span>    | <span data-ttu-id="cd1e8-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span><span class="sxs-lookup"><span data-stu-id="cd1e8-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span></span>        |
| <span data-ttu-id="cd1e8-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd1e8-122">Syntax</span></span>            | [<span data-ttu-id="cd1e8-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cd1e8-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cd1e8-124">Implementations</span></span>

-   [<span data-ttu-id="cd1e8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd1e8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd1e8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd1e8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd1e8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cd1e8-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd1e8-130">Windows Server 2003</span></span>



| <span data-ttu-id="cd1e8-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-131">Entry</span></span> | <span data-ttu-id="cd1e8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd1e8-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd1e8-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1e8-135">System-Only</span></span>            | <span data-ttu-id="cd1e8-136">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-136">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd1e8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1e8-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd1e8-138">True</span></span>                                                               |
| <span data-ttu-id="cd1e8-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd1e8-139">Is Indexed</span></span>             | <span data-ttu-id="cd1e8-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-140">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd1e8-141">In Global Catalog</span></span>      | <span data-ttu-id="cd1e8-142">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-142">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd1e8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1e8-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd1e8-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd1e8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1e8-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1e8-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-147">Search-Flags</span></span>           | <span data-ttu-id="cd1e8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1e8-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd1e8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-149">System-Flags</span></span>           | <span data-ttu-id="cd1e8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1e8-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd1e8-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd1e8-151">Classes used in</span></span>        | [<span data-ttu-id="cd1e8-152">**MS-WMI-modèle policytemplate**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-152">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd1e8-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd1e8-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd1e8-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-154">Entry</span></span> | <span data-ttu-id="cd1e8-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd1e8-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd1e8-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1e8-158">System-Only</span></span>            | <span data-ttu-id="cd1e8-159">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-159">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd1e8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1e8-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd1e8-161">True</span></span>                                                               |
| <span data-ttu-id="cd1e8-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd1e8-162">Is Indexed</span></span>             | <span data-ttu-id="cd1e8-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-163">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd1e8-164">In Global Catalog</span></span>      | <span data-ttu-id="cd1e8-165">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-165">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd1e8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1e8-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd1e8-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd1e8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1e8-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1e8-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-170">Search-Flags</span></span>           | <span data-ttu-id="cd1e8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1e8-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd1e8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-172">System-Flags</span></span>           | <span data-ttu-id="cd1e8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1e8-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd1e8-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd1e8-174">Classes used in</span></span>        | [<span data-ttu-id="cd1e8-175">**MS-WMI-modèle policytemplate**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-175">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd1e8-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd1e8-176">Windows Server 2008</span></span>



| <span data-ttu-id="cd1e8-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-177">Entry</span></span> | <span data-ttu-id="cd1e8-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd1e8-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd1e8-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1e8-181">System-Only</span></span>            | <span data-ttu-id="cd1e8-182">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-182">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd1e8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1e8-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd1e8-184">True</span></span>                                                               |
| <span data-ttu-id="cd1e8-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd1e8-185">Is Indexed</span></span>             | <span data-ttu-id="cd1e8-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-186">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd1e8-187">In Global Catalog</span></span>      | <span data-ttu-id="cd1e8-188">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-188">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd1e8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1e8-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd1e8-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd1e8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1e8-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1e8-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-193">Search-Flags</span></span>           | <span data-ttu-id="cd1e8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1e8-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd1e8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-195">System-Flags</span></span>           | <span data-ttu-id="cd1e8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1e8-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd1e8-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd1e8-197">Classes used in</span></span>        | [<span data-ttu-id="cd1e8-198">**MS-WMI-modèle policytemplate**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-198">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd1e8-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd1e8-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd1e8-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-200">Entry</span></span> | <span data-ttu-id="cd1e8-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd1e8-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd1e8-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1e8-204">System-Only</span></span>            | <span data-ttu-id="cd1e8-205">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-205">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd1e8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1e8-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd1e8-207">True</span></span>                                                               |
| <span data-ttu-id="cd1e8-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd1e8-208">Is Indexed</span></span>             | <span data-ttu-id="cd1e8-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-209">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd1e8-210">In Global Catalog</span></span>      | <span data-ttu-id="cd1e8-211">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-211">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd1e8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1e8-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd1e8-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd1e8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1e8-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1e8-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-216">Search-Flags</span></span>           | <span data-ttu-id="cd1e8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1e8-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd1e8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-218">System-Flags</span></span>           | <span data-ttu-id="cd1e8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1e8-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd1e8-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd1e8-220">Classes used in</span></span>        | [<span data-ttu-id="cd1e8-221">**MS-WMI-modèle policytemplate**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-221">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd1e8-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd1e8-222">Windows Server 2012</span></span>



| <span data-ttu-id="cd1e8-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd1e8-223">Entry</span></span> | <span data-ttu-id="cd1e8-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd1e8-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd1e8-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd1e8-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1e8-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd1e8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1e8-227">System-Only</span></span>            | <span data-ttu-id="cd1e8-228">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-228">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd1e8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1e8-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd1e8-230">True</span></span>                                                               |
| <span data-ttu-id="cd1e8-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd1e8-231">Is Indexed</span></span>             | <span data-ttu-id="cd1e8-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-232">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd1e8-233">In Global Catalog</span></span>      | <span data-ttu-id="cd1e8-234">Faux</span><span class="sxs-lookup"><span data-stu-id="cd1e8-234">False</span></span>                                                              |
| <span data-ttu-id="cd1e8-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd1e8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1e8-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd1e8-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd1e8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1e8-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1e8-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd1e8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-239">Search-Flags</span></span>           | <span data-ttu-id="cd1e8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1e8-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd1e8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1e8-241">System-Flags</span></span>           | <span data-ttu-id="cd1e8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1e8-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd1e8-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd1e8-243">Classes used in</span></span>        | [<span data-ttu-id="cd1e8-244">**MS-WMI-modèle policytemplate**</span><span class="sxs-lookup"><span data-stu-id="cd1e8-244">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



 

 





