---
title: Attribut Primary-Group-ID
description: Contient l’identificateur relatif (RID) pour le groupe principal de l’utilisateur. Par défaut, il s’agit du RID pour le groupe utilisateurs du domaine.
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Primary-Group-ID
- Schéma AD de l’attribut primaryGroupID
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744957"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="3b6ff-106">Attribut Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="3b6ff-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="3b6ff-107">Contient l’identificateur relatif (RID) pour le groupe principal de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3b6ff-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="3b6ff-108">Par défaut, il s’agit du RID pour le groupe utilisateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="3b6ff-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="3b6ff-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-109">Entry</span></span> | <span data-ttu-id="3b6ff-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3b6ff-111">CN</span><span class="sxs-lookup"><span data-stu-id="3b6ff-111">CN</span></span>                | <span data-ttu-id="3b6ff-112">ID de groupe principal</span><span class="sxs-lookup"><span data-stu-id="3b6ff-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="3b6ff-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3b6ff-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3b6ff-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="3b6ff-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="3b6ff-115">Taille</span><span class="sxs-lookup"><span data-stu-id="3b6ff-115">Size</span></span>              | <span data-ttu-id="3b6ff-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="3b6ff-116">4 bytes</span></span>                              |
| <span data-ttu-id="3b6ff-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3b6ff-117">Update Privilege</span></span>  | <span data-ttu-id="3b6ff-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="3b6ff-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="3b6ff-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3b6ff-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3b6ff-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-120">Attribute-Id</span></span>      | <span data-ttu-id="3b6ff-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="3b6ff-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="3b6ff-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3b6ff-122">System-Id-Guid</span></span>    | <span data-ttu-id="3b6ff-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3b6ff-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3b6ff-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b6ff-124">Syntax</span></span>            | [<span data-ttu-id="3b6ff-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3b6ff-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3b6ff-126">Implementations</span></span>

-   [<span data-ttu-id="3b6ff-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3b6ff-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3b6ff-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3b6ff-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3b6ff-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3b6ff-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3b6ff-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b6ff-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3b6ff-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-134">Entry</span></span> | <span data-ttu-id="3b6ff-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-138">System-Only</span></span>            | <span data-ttu-id="3b6ff-139">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-139">False</span></span>                             |
| <span data-ttu-id="3b6ff-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-141">True</span></span>                              |
| <span data-ttu-id="3b6ff-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-142">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-143">True</span></span>                              |
| <span data-ttu-id="3b6ff-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-144">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-145">True</span></span>                              |
| <span data-ttu-id="3b6ff-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-150">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-151">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-152">System-Flags</span></span>           | <span data-ttu-id="3b6ff-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-153">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-154">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-155">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3b6ff-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b6ff-156">Windows Server 2003</span></span>



| <span data-ttu-id="3b6ff-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-157">Entry</span></span> | <span data-ttu-id="3b6ff-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-161">System-Only</span></span>            | <span data-ttu-id="3b6ff-162">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-162">False</span></span>                             |
| <span data-ttu-id="3b6ff-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-164">True</span></span>                              |
| <span data-ttu-id="3b6ff-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-165">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-166">True</span></span>                              |
| <span data-ttu-id="3b6ff-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-167">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-168">True</span></span>                              |
| <span data-ttu-id="3b6ff-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-173">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-174">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-175">System-Flags</span></span>           | <span data-ttu-id="3b6ff-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-176">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-177">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-178">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3b6ff-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3b6ff-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3b6ff-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-180">Entry</span></span> | <span data-ttu-id="3b6ff-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-184">System-Only</span></span>            | <span data-ttu-id="3b6ff-185">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-185">False</span></span>                             |
| <span data-ttu-id="3b6ff-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-187">True</span></span>                              |
| <span data-ttu-id="3b6ff-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-188">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-189">True</span></span>                              |
| <span data-ttu-id="3b6ff-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-190">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-191">True</span></span>                              |
| <span data-ttu-id="3b6ff-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-196">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-197">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-198">System-Flags</span></span>           | <span data-ttu-id="3b6ff-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-199">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-200">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-201">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3b6ff-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b6ff-202">Windows Server 2008</span></span>



| <span data-ttu-id="3b6ff-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-203">Entry</span></span> | <span data-ttu-id="3b6ff-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-207">System-Only</span></span>            | <span data-ttu-id="3b6ff-208">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-208">False</span></span>                             |
| <span data-ttu-id="3b6ff-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-210">True</span></span>                              |
| <span data-ttu-id="3b6ff-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-211">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-212">True</span></span>                              |
| <span data-ttu-id="3b6ff-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-213">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-214">True</span></span>                              |
| <span data-ttu-id="3b6ff-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-219">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-220">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-221">System-Flags</span></span>           | <span data-ttu-id="3b6ff-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-222">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-223">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-224">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3b6ff-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b6ff-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3b6ff-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-226">Entry</span></span> | <span data-ttu-id="3b6ff-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-230">System-Only</span></span>            | <span data-ttu-id="3b6ff-231">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-231">False</span></span>                             |
| <span data-ttu-id="3b6ff-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-233">True</span></span>                              |
| <span data-ttu-id="3b6ff-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-234">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-235">True</span></span>                              |
| <span data-ttu-id="3b6ff-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-236">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-237">True</span></span>                              |
| <span data-ttu-id="3b6ff-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-242">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-243">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-244">System-Flags</span></span>           | <span data-ttu-id="3b6ff-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-245">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-246">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-247">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3b6ff-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-248">Windows Server 2012</span></span>



| <span data-ttu-id="3b6ff-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="3b6ff-249">Entry</span></span> | <span data-ttu-id="3b6ff-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6ff-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3b6ff-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3b6ff-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b6ff-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3b6ff-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b6ff-253">System-Only</span></span>            | <span data-ttu-id="3b6ff-254">Faux</span><span class="sxs-lookup"><span data-stu-id="3b6ff-254">False</span></span>                             |
| <span data-ttu-id="3b6ff-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3b6ff-255">Is-Single-Valued</span></span>       | <span data-ttu-id="3b6ff-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-256">True</span></span>                              |
| <span data-ttu-id="3b6ff-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3b6ff-257">Is Indexed</span></span>             | <span data-ttu-id="3b6ff-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-258">True</span></span>                              |
| <span data-ttu-id="3b6ff-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3b6ff-259">In Global Catalog</span></span>      | <span data-ttu-id="3b6ff-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="3b6ff-260">True</span></span>                              |
| <span data-ttu-id="3b6ff-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3b6ff-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b6ff-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3b6ff-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3b6ff-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b6ff-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b6ff-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="3b6ff-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-265">Search-Flags</span></span>           | <span data-ttu-id="3b6ff-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3b6ff-266">0x00000011</span></span>                        |
| <span data-ttu-id="3b6ff-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b6ff-267">System-Flags</span></span>           | <span data-ttu-id="3b6ff-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3b6ff-268">0x00000012</span></span>                        |
| <span data-ttu-id="3b6ff-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3b6ff-269">Classes used in</span></span>        | [<span data-ttu-id="3b6ff-270">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3b6ff-270">**User**</span></span>](c-user.md)<br/> |



 

 





