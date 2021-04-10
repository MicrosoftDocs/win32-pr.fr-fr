---
title: GPC-WQL-Filter (attribut)
description: Utilisé pour stocker une chaîne qui contient un GUID pour le filtre et un chemin d’accès d’espace de noms WMI.
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- Schéma AD GPC-WQL-Filter Attribute
- Schéma AD de l’attribut gPCWQLFilter
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845246"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="cfe92-105">GPC-WQL-Filter (attribut)</span><span class="sxs-lookup"><span data-stu-id="cfe92-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="cfe92-106">Utilisé pour stocker une chaîne qui contient un GUID pour le filtre et un chemin d’accès d’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="cfe92-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="cfe92-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-107">Entry</span></span> | <span data-ttu-id="cfe92-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="cfe92-109">CN</span><span class="sxs-lookup"><span data-stu-id="cfe92-109">CN</span></span>                | <span data-ttu-id="cfe92-110">GPC-WQL-Filter</span><span class="sxs-lookup"><span data-stu-id="cfe92-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="cfe92-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cfe92-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cfe92-112">gPCWQLFilter</span><span class="sxs-lookup"><span data-stu-id="cfe92-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="cfe92-113">Taille</span><span class="sxs-lookup"><span data-stu-id="cfe92-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="cfe92-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cfe92-114">Update Privilege</span></span>  | <span data-ttu-id="cfe92-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="cfe92-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="cfe92-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cfe92-116">Update Frequency</span></span>  | <span data-ttu-id="cfe92-117">Uniquement lorsque l’administrateur modifie la propriété de filtre dans l’interface utilisateur stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cfe92-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="cfe92-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-118">Attribute-Id</span></span>      | <span data-ttu-id="cfe92-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="cfe92-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="cfe92-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cfe92-120">System-Id-Guid</span></span>    | <span data-ttu-id="cfe92-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="cfe92-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="cfe92-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfe92-122">Syntax</span></span>            | [<span data-ttu-id="cfe92-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cfe92-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="cfe92-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cfe92-124">Implementations</span></span>

-   [<span data-ttu-id="cfe92-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cfe92-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cfe92-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cfe92-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cfe92-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cfe92-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cfe92-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cfe92-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cfe92-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cfe92-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cfe92-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfe92-130">Windows Server 2003</span></span>



| <span data-ttu-id="cfe92-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-131">Entry</span></span> | <span data-ttu-id="cfe92-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfe92-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cfe92-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfe92-135">System-Only</span></span>            | <span data-ttu-id="cfe92-136">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-136">False</span></span>                                                               |
| <span data-ttu-id="cfe92-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cfe92-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cfe92-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="cfe92-138">True</span></span>                                                                |
| <span data-ttu-id="cfe92-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cfe92-139">Is Indexed</span></span>             | <span data-ttu-id="cfe92-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-140">False</span></span>                                                               |
| <span data-ttu-id="cfe92-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cfe92-141">In Global Catalog</span></span>      | <span data-ttu-id="cfe92-142">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-142">False</span></span>                                                               |
| <span data-ttu-id="cfe92-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cfe92-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfe92-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cfe92-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cfe92-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfe92-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfe92-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-147">Search-Flags</span></span>           | <span data-ttu-id="cfe92-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfe92-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="cfe92-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-149">System-Flags</span></span>           | <span data-ttu-id="cfe92-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfe92-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="cfe92-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cfe92-151">Classes used in</span></span>        | [<span data-ttu-id="cfe92-152">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="cfe92-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cfe92-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfe92-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cfe92-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-154">Entry</span></span> | <span data-ttu-id="cfe92-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfe92-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cfe92-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfe92-158">System-Only</span></span>            | <span data-ttu-id="cfe92-159">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-159">False</span></span>                                                               |
| <span data-ttu-id="cfe92-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cfe92-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cfe92-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="cfe92-161">True</span></span>                                                                |
| <span data-ttu-id="cfe92-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cfe92-162">Is Indexed</span></span>             | <span data-ttu-id="cfe92-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-163">False</span></span>                                                               |
| <span data-ttu-id="cfe92-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cfe92-164">In Global Catalog</span></span>      | <span data-ttu-id="cfe92-165">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-165">False</span></span>                                                               |
| <span data-ttu-id="cfe92-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cfe92-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfe92-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cfe92-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cfe92-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfe92-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfe92-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-170">Search-Flags</span></span>           | <span data-ttu-id="cfe92-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfe92-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="cfe92-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-172">System-Flags</span></span>           | <span data-ttu-id="cfe92-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfe92-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="cfe92-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cfe92-174">Classes used in</span></span>        | [<span data-ttu-id="cfe92-175">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="cfe92-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cfe92-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfe92-176">Windows Server 2008</span></span>



| <span data-ttu-id="cfe92-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-177">Entry</span></span> | <span data-ttu-id="cfe92-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfe92-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cfe92-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfe92-181">System-Only</span></span>            | <span data-ttu-id="cfe92-182">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-182">False</span></span>                                                               |
| <span data-ttu-id="cfe92-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cfe92-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cfe92-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="cfe92-184">True</span></span>                                                                |
| <span data-ttu-id="cfe92-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cfe92-185">Is Indexed</span></span>             | <span data-ttu-id="cfe92-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-186">False</span></span>                                                               |
| <span data-ttu-id="cfe92-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cfe92-187">In Global Catalog</span></span>      | <span data-ttu-id="cfe92-188">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-188">False</span></span>                                                               |
| <span data-ttu-id="cfe92-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cfe92-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfe92-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cfe92-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cfe92-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfe92-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfe92-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-193">Search-Flags</span></span>           | <span data-ttu-id="cfe92-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfe92-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="cfe92-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-195">System-Flags</span></span>           | <span data-ttu-id="cfe92-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfe92-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="cfe92-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cfe92-197">Classes used in</span></span>        | [<span data-ttu-id="cfe92-198">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="cfe92-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cfe92-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfe92-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cfe92-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-200">Entry</span></span> | <span data-ttu-id="cfe92-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfe92-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cfe92-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfe92-204">System-Only</span></span>            | <span data-ttu-id="cfe92-205">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-205">False</span></span>                                                               |
| <span data-ttu-id="cfe92-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cfe92-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cfe92-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="cfe92-207">True</span></span>                                                                |
| <span data-ttu-id="cfe92-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cfe92-208">Is Indexed</span></span>             | <span data-ttu-id="cfe92-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-209">False</span></span>                                                               |
| <span data-ttu-id="cfe92-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cfe92-210">In Global Catalog</span></span>      | <span data-ttu-id="cfe92-211">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-211">False</span></span>                                                               |
| <span data-ttu-id="cfe92-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cfe92-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfe92-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cfe92-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cfe92-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfe92-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfe92-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-216">Search-Flags</span></span>           | <span data-ttu-id="cfe92-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfe92-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="cfe92-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-218">System-Flags</span></span>           | <span data-ttu-id="cfe92-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfe92-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="cfe92-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cfe92-220">Classes used in</span></span>        | [<span data-ttu-id="cfe92-221">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="cfe92-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cfe92-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfe92-222">Windows Server 2012</span></span>



| <span data-ttu-id="cfe92-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="cfe92-223">Entry</span></span> | <span data-ttu-id="cfe92-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe92-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfe92-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cfe92-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfe92-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cfe92-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfe92-227">System-Only</span></span>            | <span data-ttu-id="cfe92-228">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-228">False</span></span>                                                               |
| <span data-ttu-id="cfe92-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cfe92-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cfe92-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="cfe92-230">True</span></span>                                                                |
| <span data-ttu-id="cfe92-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cfe92-231">Is Indexed</span></span>             | <span data-ttu-id="cfe92-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-232">False</span></span>                                                               |
| <span data-ttu-id="cfe92-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cfe92-233">In Global Catalog</span></span>      | <span data-ttu-id="cfe92-234">Faux</span><span class="sxs-lookup"><span data-stu-id="cfe92-234">False</span></span>                                                               |
| <span data-ttu-id="cfe92-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cfe92-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfe92-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cfe92-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cfe92-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfe92-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfe92-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cfe92-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-239">Search-Flags</span></span>           | <span data-ttu-id="cfe92-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfe92-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="cfe92-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfe92-241">System-Flags</span></span>           | <span data-ttu-id="cfe92-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfe92-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="cfe92-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cfe92-243">Classes used in</span></span>        | [<span data-ttu-id="cfe92-244">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="cfe92-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





