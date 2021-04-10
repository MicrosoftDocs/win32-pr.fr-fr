---
title: ms-DS-AZ-LDAP-Query (attribut)
description: Chaîne qui définit la requête LDAP (longueur maximale 4096) qui détermine l’appartenance d’un objet utilisateur au groupe.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-AZ-LDAP-Query Attribute
- Schéma Active Directory de l’attribut msDS-AzLDAPQuery
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107842"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="18a76-105">ms-DS-AZ-LDAP-Query (attribut)</span><span class="sxs-lookup"><span data-stu-id="18a76-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="18a76-106">Chaîne qui définit la requête LDAP (longueur maximale 4096) qui détermine l’appartenance d’un objet utilisateur au groupe.</span><span class="sxs-lookup"><span data-stu-id="18a76-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="18a76-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-107">Entry</span></span> | <span data-ttu-id="18a76-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="18a76-109">CN</span><span class="sxs-lookup"><span data-stu-id="18a76-109">CN</span></span>                | <span data-ttu-id="18a76-110">ms-DS-AZ-LDAP-requête</span><span class="sxs-lookup"><span data-stu-id="18a76-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="18a76-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="18a76-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18a76-112">msDS-AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="18a76-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="18a76-113">Taille</span><span class="sxs-lookup"><span data-stu-id="18a76-113">Size</span></span>              | <span data-ttu-id="18a76-114">4096 caractères</span><span class="sxs-lookup"><span data-stu-id="18a76-114">4096 characters</span></span>                             |
| <span data-ttu-id="18a76-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="18a76-115">Update Privilege</span></span>  | <span data-ttu-id="18a76-116">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="18a76-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="18a76-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="18a76-117">Update Frequency</span></span>  | <span data-ttu-id="18a76-118">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="18a76-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="18a76-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-119">Attribute-Id</span></span>      | <span data-ttu-id="18a76-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="18a76-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="18a76-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18a76-121">System-Id-Guid</span></span>    | <span data-ttu-id="18a76-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="18a76-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="18a76-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18a76-123">Syntax</span></span>            | [<span data-ttu-id="18a76-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="18a76-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="18a76-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="18a76-125">Implementations</span></span>

-   [<span data-ttu-id="18a76-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18a76-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18a76-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18a76-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18a76-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18a76-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18a76-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18a76-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18a76-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18a76-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="18a76-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18a76-131">Windows Server 2003</span></span>



| <span data-ttu-id="18a76-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-132">Entry</span></span> | <span data-ttu-id="18a76-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="18a76-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18a76-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="18a76-136">System-Only</span></span>            | <span data-ttu-id="18a76-137">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-137">False</span></span>                               |
| <span data-ttu-id="18a76-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18a76-138">Is-Single-Valued</span></span>       | <span data-ttu-id="18a76-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="18a76-139">True</span></span>                                |
| <span data-ttu-id="18a76-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18a76-140">Is Indexed</span></span>             | <span data-ttu-id="18a76-141">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-141">False</span></span>                               |
| <span data-ttu-id="18a76-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18a76-142">In Global Catalog</span></span>      | <span data-ttu-id="18a76-143">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-143">False</span></span>                               |
| <span data-ttu-id="18a76-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18a76-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="18a76-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18a76-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="18a76-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18a76-146">Range-Lower</span></span>            | <span data-ttu-id="18a76-147">0</span><span class="sxs-lookup"><span data-stu-id="18a76-147">0</span></span>                                   |
| <span data-ttu-id="18a76-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18a76-148">Range-Upper</span></span>            | <span data-ttu-id="18a76-149">4096</span><span class="sxs-lookup"><span data-stu-id="18a76-149">4096</span></span>                                |
| <span data-ttu-id="18a76-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-150">Search-Flags</span></span>           | <span data-ttu-id="18a76-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18a76-151">0x00000000</span></span>                          |
| <span data-ttu-id="18a76-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-152">System-Flags</span></span>           | <span data-ttu-id="18a76-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a76-153">0x00000010</span></span>                          |
| <span data-ttu-id="18a76-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18a76-154">Classes used in</span></span>        | [<span data-ttu-id="18a76-155">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="18a76-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18a76-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18a76-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18a76-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-157">Entry</span></span> | <span data-ttu-id="18a76-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="18a76-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18a76-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="18a76-161">System-Only</span></span>            | <span data-ttu-id="18a76-162">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-162">False</span></span>                               |
| <span data-ttu-id="18a76-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18a76-163">Is-Single-Valued</span></span>       | <span data-ttu-id="18a76-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="18a76-164">True</span></span>                                |
| <span data-ttu-id="18a76-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18a76-165">Is Indexed</span></span>             | <span data-ttu-id="18a76-166">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-166">False</span></span>                               |
| <span data-ttu-id="18a76-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18a76-167">In Global Catalog</span></span>      | <span data-ttu-id="18a76-168">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-168">False</span></span>                               |
| <span data-ttu-id="18a76-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18a76-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="18a76-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18a76-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="18a76-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18a76-171">Range-Lower</span></span>            | <span data-ttu-id="18a76-172">0</span><span class="sxs-lookup"><span data-stu-id="18a76-172">0</span></span>                                   |
| <span data-ttu-id="18a76-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18a76-173">Range-Upper</span></span>            | <span data-ttu-id="18a76-174">4096</span><span class="sxs-lookup"><span data-stu-id="18a76-174">4096</span></span>                                |
| <span data-ttu-id="18a76-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-175">Search-Flags</span></span>           | <span data-ttu-id="18a76-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18a76-176">0x00000000</span></span>                          |
| <span data-ttu-id="18a76-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-177">System-Flags</span></span>           | <span data-ttu-id="18a76-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a76-178">0x00000010</span></span>                          |
| <span data-ttu-id="18a76-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18a76-179">Classes used in</span></span>        | [<span data-ttu-id="18a76-180">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="18a76-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18a76-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18a76-181">Windows Server 2008</span></span>



| <span data-ttu-id="18a76-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-182">Entry</span></span> | <span data-ttu-id="18a76-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="18a76-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18a76-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="18a76-186">System-Only</span></span>            | <span data-ttu-id="18a76-187">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-187">False</span></span>                               |
| <span data-ttu-id="18a76-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18a76-188">Is-Single-Valued</span></span>       | <span data-ttu-id="18a76-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="18a76-189">True</span></span>                                |
| <span data-ttu-id="18a76-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18a76-190">Is Indexed</span></span>             | <span data-ttu-id="18a76-191">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-191">False</span></span>                               |
| <span data-ttu-id="18a76-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18a76-192">In Global Catalog</span></span>      | <span data-ttu-id="18a76-193">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-193">False</span></span>                               |
| <span data-ttu-id="18a76-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18a76-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="18a76-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18a76-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="18a76-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18a76-196">Range-Lower</span></span>            | <span data-ttu-id="18a76-197">0</span><span class="sxs-lookup"><span data-stu-id="18a76-197">0</span></span>                                   |
| <span data-ttu-id="18a76-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18a76-198">Range-Upper</span></span>            | <span data-ttu-id="18a76-199">4096</span><span class="sxs-lookup"><span data-stu-id="18a76-199">4096</span></span>                                |
| <span data-ttu-id="18a76-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-200">Search-Flags</span></span>           | <span data-ttu-id="18a76-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18a76-201">0x00000000</span></span>                          |
| <span data-ttu-id="18a76-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-202">System-Flags</span></span>           | <span data-ttu-id="18a76-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a76-203">0x00000010</span></span>                          |
| <span data-ttu-id="18a76-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18a76-204">Classes used in</span></span>        | [<span data-ttu-id="18a76-205">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="18a76-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18a76-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18a76-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18a76-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-207">Entry</span></span> | <span data-ttu-id="18a76-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="18a76-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18a76-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="18a76-211">System-Only</span></span>            | <span data-ttu-id="18a76-212">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-212">False</span></span>                               |
| <span data-ttu-id="18a76-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18a76-213">Is-Single-Valued</span></span>       | <span data-ttu-id="18a76-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="18a76-214">True</span></span>                                |
| <span data-ttu-id="18a76-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18a76-215">Is Indexed</span></span>             | <span data-ttu-id="18a76-216">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-216">False</span></span>                               |
| <span data-ttu-id="18a76-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18a76-217">In Global Catalog</span></span>      | <span data-ttu-id="18a76-218">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-218">False</span></span>                               |
| <span data-ttu-id="18a76-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18a76-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="18a76-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18a76-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="18a76-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18a76-221">Range-Lower</span></span>            | <span data-ttu-id="18a76-222">0</span><span class="sxs-lookup"><span data-stu-id="18a76-222">0</span></span>                                   |
| <span data-ttu-id="18a76-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18a76-223">Range-Upper</span></span>            | <span data-ttu-id="18a76-224">4096</span><span class="sxs-lookup"><span data-stu-id="18a76-224">4096</span></span>                                |
| <span data-ttu-id="18a76-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-225">Search-Flags</span></span>           | <span data-ttu-id="18a76-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18a76-226">0x00000000</span></span>                          |
| <span data-ttu-id="18a76-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-227">System-Flags</span></span>           | <span data-ttu-id="18a76-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a76-228">0x00000010</span></span>                          |
| <span data-ttu-id="18a76-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18a76-229">Classes used in</span></span>        | [<span data-ttu-id="18a76-230">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="18a76-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18a76-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18a76-231">Windows Server 2012</span></span>



| <span data-ttu-id="18a76-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="18a76-232">Entry</span></span> | <span data-ttu-id="18a76-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a76-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="18a76-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18a76-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18a76-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="18a76-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="18a76-236">System-Only</span></span>            | <span data-ttu-id="18a76-237">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-237">False</span></span>                               |
| <span data-ttu-id="18a76-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18a76-238">Is-Single-Valued</span></span>       | <span data-ttu-id="18a76-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="18a76-239">True</span></span>                                |
| <span data-ttu-id="18a76-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18a76-240">Is Indexed</span></span>             | <span data-ttu-id="18a76-241">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-241">False</span></span>                               |
| <span data-ttu-id="18a76-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18a76-242">In Global Catalog</span></span>      | <span data-ttu-id="18a76-243">Faux</span><span class="sxs-lookup"><span data-stu-id="18a76-243">False</span></span>                               |
| <span data-ttu-id="18a76-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18a76-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="18a76-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18a76-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="18a76-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18a76-246">Range-Lower</span></span>            | <span data-ttu-id="18a76-247">0</span><span class="sxs-lookup"><span data-stu-id="18a76-247">0</span></span>                                   |
| <span data-ttu-id="18a76-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18a76-248">Range-Upper</span></span>            | <span data-ttu-id="18a76-249">4096</span><span class="sxs-lookup"><span data-stu-id="18a76-249">4096</span></span>                                |
| <span data-ttu-id="18a76-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-250">Search-Flags</span></span>           | <span data-ttu-id="18a76-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18a76-251">0x00000000</span></span>                          |
| <span data-ttu-id="18a76-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18a76-252">System-Flags</span></span>           | <span data-ttu-id="18a76-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a76-253">0x00000010</span></span>                          |
| <span data-ttu-id="18a76-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18a76-254">Classes used in</span></span>        | [<span data-ttu-id="18a76-255">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="18a76-255">**Group**</span></span>](c-group.md)<br/> |



 

 





