---
title: Attribut Profile-Path
description: Spécifie un chemin d’accès au profil de l’utilisateur. Cette valeur peut être une chaîne NULL, un chemin d’accès absolu local ou un chemin d’accès UNC.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Profile-Path
- Schéma AD de l’attribut profilePath
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949840"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="38b0d-106">Attribut Profile-Path</span><span class="sxs-lookup"><span data-stu-id="38b0d-106">Profile-Path attribute</span></span>

<span data-ttu-id="38b0d-107">Spécifie un chemin d’accès au profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38b0d-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="38b0d-108">Cette valeur peut être une chaîne NULL, un chemin d’accès absolu local ou un chemin d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="38b0d-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="38b0d-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-109">Entry</span></span> | <span data-ttu-id="38b0d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="38b0d-111">CN</span><span class="sxs-lookup"><span data-stu-id="38b0d-111">CN</span></span>                | <span data-ttu-id="38b0d-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="38b0d-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="38b0d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="38b0d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="38b0d-114">profilePath</span><span class="sxs-lookup"><span data-stu-id="38b0d-114">profilePath</span></span>                                                              |
| <span data-ttu-id="38b0d-115">Taille</span><span class="sxs-lookup"><span data-stu-id="38b0d-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="38b0d-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="38b0d-116">Update Privilege</span></span>  | <span data-ttu-id="38b0d-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="38b0d-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="38b0d-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="38b0d-118">Update Frequency</span></span>  | <span data-ttu-id="38b0d-119">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le chemin d’accès doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="38b0d-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="38b0d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-120">Attribute-Id</span></span>      | <span data-ttu-id="38b0d-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="38b0d-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="38b0d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38b0d-122">System-Id-Guid</span></span>    | <span data-ttu-id="38b0d-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="38b0d-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="38b0d-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38b0d-124">Syntax</span></span>            | [<span data-ttu-id="38b0d-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="38b0d-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="38b0d-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="38b0d-126">Implementations</span></span>

-   [<span data-ttu-id="38b0d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38b0d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38b0d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38b0d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38b0d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38b0d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38b0d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38b0d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38b0d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38b0d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38b0d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38b0d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38b0d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38b0d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="38b0d-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-134">Entry</span></span> | <span data-ttu-id="38b0d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-138">System-Only</span></span>            | <span data-ttu-id="38b0d-139">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-139">False</span></span>                             |
| <span data-ttu-id="38b0d-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-141">True</span></span>                              |
| <span data-ttu-id="38b0d-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-142">Is Indexed</span></span>             | <span data-ttu-id="38b0d-143">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-143">False</span></span>                             |
| <span data-ttu-id="38b0d-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-144">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-145">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-145">False</span></span>                             |
| <span data-ttu-id="38b0d-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-150">Search-Flags</span></span>           | <span data-ttu-id="38b0d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-151">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-152">System-Flags</span></span>           | <span data-ttu-id="38b0d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-153">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-154">Classes used in</span></span>        | [<span data-ttu-id="38b0d-155">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38b0d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38b0d-156">Windows Server 2003</span></span>



| <span data-ttu-id="38b0d-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-157">Entry</span></span> | <span data-ttu-id="38b0d-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-161">System-Only</span></span>            | <span data-ttu-id="38b0d-162">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-162">False</span></span>                             |
| <span data-ttu-id="38b0d-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-164">True</span></span>                              |
| <span data-ttu-id="38b0d-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-165">Is Indexed</span></span>             | <span data-ttu-id="38b0d-166">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-166">False</span></span>                             |
| <span data-ttu-id="38b0d-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-167">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-168">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-168">False</span></span>                             |
| <span data-ttu-id="38b0d-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-173">Search-Flags</span></span>           | <span data-ttu-id="38b0d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-174">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-175">System-Flags</span></span>           | <span data-ttu-id="38b0d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-176">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-177">Classes used in</span></span>        | [<span data-ttu-id="38b0d-178">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38b0d-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38b0d-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38b0d-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-180">Entry</span></span> | <span data-ttu-id="38b0d-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-184">System-Only</span></span>            | <span data-ttu-id="38b0d-185">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-185">False</span></span>                             |
| <span data-ttu-id="38b0d-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-187">True</span></span>                              |
| <span data-ttu-id="38b0d-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-188">Is Indexed</span></span>             | <span data-ttu-id="38b0d-189">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-189">False</span></span>                             |
| <span data-ttu-id="38b0d-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-190">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-191">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-191">False</span></span>                             |
| <span data-ttu-id="38b0d-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-196">Search-Flags</span></span>           | <span data-ttu-id="38b0d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-197">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-198">System-Flags</span></span>           | <span data-ttu-id="38b0d-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-199">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-200">Classes used in</span></span>        | [<span data-ttu-id="38b0d-201">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38b0d-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38b0d-202">Windows Server 2008</span></span>



| <span data-ttu-id="38b0d-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-203">Entry</span></span> | <span data-ttu-id="38b0d-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-207">System-Only</span></span>            | <span data-ttu-id="38b0d-208">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-208">False</span></span>                             |
| <span data-ttu-id="38b0d-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-210">True</span></span>                              |
| <span data-ttu-id="38b0d-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-211">Is Indexed</span></span>             | <span data-ttu-id="38b0d-212">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-212">False</span></span>                             |
| <span data-ttu-id="38b0d-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-213">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-214">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-214">False</span></span>                             |
| <span data-ttu-id="38b0d-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-219">Search-Flags</span></span>           | <span data-ttu-id="38b0d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-220">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-221">System-Flags</span></span>           | <span data-ttu-id="38b0d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-222">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-223">Classes used in</span></span>        | [<span data-ttu-id="38b0d-224">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38b0d-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38b0d-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38b0d-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-226">Entry</span></span> | <span data-ttu-id="38b0d-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-230">System-Only</span></span>            | <span data-ttu-id="38b0d-231">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-231">False</span></span>                             |
| <span data-ttu-id="38b0d-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-232">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-233">True</span></span>                              |
| <span data-ttu-id="38b0d-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-234">Is Indexed</span></span>             | <span data-ttu-id="38b0d-235">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-235">False</span></span>                             |
| <span data-ttu-id="38b0d-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-236">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-237">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-237">False</span></span>                             |
| <span data-ttu-id="38b0d-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-242">Search-Flags</span></span>           | <span data-ttu-id="38b0d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-243">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-244">System-Flags</span></span>           | <span data-ttu-id="38b0d-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-245">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-246">Classes used in</span></span>        | [<span data-ttu-id="38b0d-247">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38b0d-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38b0d-248">Windows Server 2012</span></span>



| <span data-ttu-id="38b0d-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="38b0d-249">Entry</span></span> | <span data-ttu-id="38b0d-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b0d-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38b0d-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="38b0d-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b0d-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38b0d-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b0d-253">System-Only</span></span>            | <span data-ttu-id="38b0d-254">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-254">False</span></span>                             |
| <span data-ttu-id="38b0d-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="38b0d-255">Is-Single-Valued</span></span>       | <span data-ttu-id="38b0d-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="38b0d-256">True</span></span>                              |
| <span data-ttu-id="38b0d-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="38b0d-257">Is Indexed</span></span>             | <span data-ttu-id="38b0d-258">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-258">False</span></span>                             |
| <span data-ttu-id="38b0d-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="38b0d-259">In Global Catalog</span></span>      | <span data-ttu-id="38b0d-260">Faux</span><span class="sxs-lookup"><span data-stu-id="38b0d-260">False</span></span>                             |
| <span data-ttu-id="38b0d-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="38b0d-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b0d-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="38b0d-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38b0d-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b0d-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38b0d-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b0d-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38b0d-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-265">Search-Flags</span></span>           | <span data-ttu-id="38b0d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-266">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b0d-267">System-Flags</span></span>           | <span data-ttu-id="38b0d-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b0d-268">0x00000010</span></span>                        |
| <span data-ttu-id="38b0d-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="38b0d-269">Classes used in</span></span>        | [<span data-ttu-id="38b0d-270">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="38b0d-270">**User**</span></span>](c-user.md)<br/> |



 

 





