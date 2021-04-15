---
title: Attribut User-Parameters
description: Paramètres de l’utilisateur.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut User-Parameters
- Schéma AD de l’attribut userParameters
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519961"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="890de-105">Attribut User-Parameters</span><span class="sxs-lookup"><span data-stu-id="890de-105">User-Parameters attribute</span></span>

<span data-ttu-id="890de-106">Paramètres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="890de-106">Parameters of the user.</span></span> <span data-ttu-id="890de-107">Pointe vers une chaîne Unicode qui est réservée à une utilisation par des applications.</span><span class="sxs-lookup"><span data-stu-id="890de-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="890de-108">Cette chaîne peut être une chaîne NULL, ou elle peut contenir un nombre quelconque de caractères avant le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="890de-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="890de-109">Les produits Microsoft utilisent ce membre pour stocker des données utilisateur spécifiques au programme individuel.</span><span class="sxs-lookup"><span data-stu-id="890de-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="890de-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-110">Entry</span></span> | <span data-ttu-id="890de-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="890de-112">CN</span><span class="sxs-lookup"><span data-stu-id="890de-112">CN</span></span>                | <span data-ttu-id="890de-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="890de-113">User-Parameters</span></span>                             |
| <span data-ttu-id="890de-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="890de-114">Ldap-Display-Name</span></span> | <span data-ttu-id="890de-115">userParameters</span><span class="sxs-lookup"><span data-stu-id="890de-115">userParameters</span></span>                              |
| <span data-ttu-id="890de-116">Taille</span><span class="sxs-lookup"><span data-stu-id="890de-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="890de-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="890de-117">Update Privilege</span></span>  | <span data-ttu-id="890de-118">Modifié par les applications.</span><span class="sxs-lookup"><span data-stu-id="890de-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="890de-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="890de-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="890de-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="890de-120">Attribute-Id</span></span>      | <span data-ttu-id="890de-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="890de-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="890de-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="890de-122">System-Id-Guid</span></span>    | <span data-ttu-id="890de-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="890de-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="890de-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="890de-124">Syntax</span></span>            | [<span data-ttu-id="890de-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="890de-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="890de-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="890de-126">Implementations</span></span>

-   [<span data-ttu-id="890de-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="890de-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="890de-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="890de-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="890de-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="890de-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="890de-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="890de-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="890de-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="890de-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="890de-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="890de-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="890de-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="890de-133">Windows 2000 Server</span></span>



| <span data-ttu-id="890de-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-134">Entry</span></span> | <span data-ttu-id="890de-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-138">System-Only</span></span>            | <span data-ttu-id="890de-139">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-139">False</span></span>                             |
| <span data-ttu-id="890de-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-140">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-141">True</span></span>                              |
| <span data-ttu-id="890de-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-142">Is Indexed</span></span>             | <span data-ttu-id="890de-143">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-143">False</span></span>                             |
| <span data-ttu-id="890de-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-144">In Global Catalog</span></span>      | <span data-ttu-id="890de-145">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-145">False</span></span>                             |
| <span data-ttu-id="890de-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-148">Range-Lower</span></span>            | <span data-ttu-id="890de-149">0</span><span class="sxs-lookup"><span data-stu-id="890de-149">0</span></span>                                 |
| <span data-ttu-id="890de-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-150">Range-Upper</span></span>            | <span data-ttu-id="890de-151">32767</span><span class="sxs-lookup"><span data-stu-id="890de-151">32767</span></span>                             |
| <span data-ttu-id="890de-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-152">Search-Flags</span></span>           | <span data-ttu-id="890de-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-153">0x00000000</span></span>                        |
| <span data-ttu-id="890de-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-154">System-Flags</span></span>           | <span data-ttu-id="890de-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-155">0x00000010</span></span>                        |
| <span data-ttu-id="890de-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-156">Classes used in</span></span>        | [<span data-ttu-id="890de-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="890de-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="890de-158">Windows Server 2003</span></span>



| <span data-ttu-id="890de-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-159">Entry</span></span> | <span data-ttu-id="890de-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-163">System-Only</span></span>            | <span data-ttu-id="890de-164">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-164">False</span></span>                             |
| <span data-ttu-id="890de-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-165">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-166">True</span></span>                              |
| <span data-ttu-id="890de-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-167">Is Indexed</span></span>             | <span data-ttu-id="890de-168">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-168">False</span></span>                             |
| <span data-ttu-id="890de-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-169">In Global Catalog</span></span>      | <span data-ttu-id="890de-170">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-170">False</span></span>                             |
| <span data-ttu-id="890de-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-173">Range-Lower</span></span>            | <span data-ttu-id="890de-174">0</span><span class="sxs-lookup"><span data-stu-id="890de-174">0</span></span>                                 |
| <span data-ttu-id="890de-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-175">Range-Upper</span></span>            | <span data-ttu-id="890de-176">32767</span><span class="sxs-lookup"><span data-stu-id="890de-176">32767</span></span>                             |
| <span data-ttu-id="890de-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-177">Search-Flags</span></span>           | <span data-ttu-id="890de-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-178">0x00000000</span></span>                        |
| <span data-ttu-id="890de-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-179">System-Flags</span></span>           | <span data-ttu-id="890de-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-180">0x00000010</span></span>                        |
| <span data-ttu-id="890de-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-181">Classes used in</span></span>        | [<span data-ttu-id="890de-182">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="890de-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="890de-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="890de-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-184">Entry</span></span> | <span data-ttu-id="890de-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-188">System-Only</span></span>            | <span data-ttu-id="890de-189">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-189">False</span></span>                             |
| <span data-ttu-id="890de-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-190">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-191">True</span></span>                              |
| <span data-ttu-id="890de-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-192">Is Indexed</span></span>             | <span data-ttu-id="890de-193">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-193">False</span></span>                             |
| <span data-ttu-id="890de-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-194">In Global Catalog</span></span>      | <span data-ttu-id="890de-195">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-195">False</span></span>                             |
| <span data-ttu-id="890de-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-198">Range-Lower</span></span>            | <span data-ttu-id="890de-199">0</span><span class="sxs-lookup"><span data-stu-id="890de-199">0</span></span>                                 |
| <span data-ttu-id="890de-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-200">Range-Upper</span></span>            | <span data-ttu-id="890de-201">32767</span><span class="sxs-lookup"><span data-stu-id="890de-201">32767</span></span>                             |
| <span data-ttu-id="890de-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-202">Search-Flags</span></span>           | <span data-ttu-id="890de-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-203">0x00000000</span></span>                        |
| <span data-ttu-id="890de-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-204">System-Flags</span></span>           | <span data-ttu-id="890de-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-205">0x00000010</span></span>                        |
| <span data-ttu-id="890de-206">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-206">Classes used in</span></span>        | [<span data-ttu-id="890de-207">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="890de-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="890de-208">Windows Server 2008</span></span>



| <span data-ttu-id="890de-209">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-209">Entry</span></span> | <span data-ttu-id="890de-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-211">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-213">System-Only</span></span>            | <span data-ttu-id="890de-214">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-214">False</span></span>                             |
| <span data-ttu-id="890de-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-215">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-216">True</span></span>                              |
| <span data-ttu-id="890de-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-217">Is Indexed</span></span>             | <span data-ttu-id="890de-218">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-218">False</span></span>                             |
| <span data-ttu-id="890de-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-219">In Global Catalog</span></span>      | <span data-ttu-id="890de-220">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-220">False</span></span>                             |
| <span data-ttu-id="890de-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-223">Range-Lower</span></span>            | <span data-ttu-id="890de-224">0</span><span class="sxs-lookup"><span data-stu-id="890de-224">0</span></span>                                 |
| <span data-ttu-id="890de-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-225">Range-Upper</span></span>            | <span data-ttu-id="890de-226">32767</span><span class="sxs-lookup"><span data-stu-id="890de-226">32767</span></span>                             |
| <span data-ttu-id="890de-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-227">Search-Flags</span></span>           | <span data-ttu-id="890de-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-228">0x00000000</span></span>                        |
| <span data-ttu-id="890de-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-229">System-Flags</span></span>           | <span data-ttu-id="890de-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-230">0x00000010</span></span>                        |
| <span data-ttu-id="890de-231">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-231">Classes used in</span></span>        | [<span data-ttu-id="890de-232">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="890de-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="890de-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="890de-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-234">Entry</span></span> | <span data-ttu-id="890de-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-238">System-Only</span></span>            | <span data-ttu-id="890de-239">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-239">False</span></span>                             |
| <span data-ttu-id="890de-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-240">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-241">True</span></span>                              |
| <span data-ttu-id="890de-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-242">Is Indexed</span></span>             | <span data-ttu-id="890de-243">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-243">False</span></span>                             |
| <span data-ttu-id="890de-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-244">In Global Catalog</span></span>      | <span data-ttu-id="890de-245">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-245">False</span></span>                             |
| <span data-ttu-id="890de-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-248">Range-Lower</span></span>            | <span data-ttu-id="890de-249">0</span><span class="sxs-lookup"><span data-stu-id="890de-249">0</span></span>                                 |
| <span data-ttu-id="890de-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-250">Range-Upper</span></span>            | <span data-ttu-id="890de-251">32767</span><span class="sxs-lookup"><span data-stu-id="890de-251">32767</span></span>                             |
| <span data-ttu-id="890de-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-252">Search-Flags</span></span>           | <span data-ttu-id="890de-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-253">0x00000000</span></span>                        |
| <span data-ttu-id="890de-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-254">System-Flags</span></span>           | <span data-ttu-id="890de-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-255">0x00000010</span></span>                        |
| <span data-ttu-id="890de-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-256">Classes used in</span></span>        | [<span data-ttu-id="890de-257">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="890de-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="890de-258">Windows Server 2012</span></span>



| <span data-ttu-id="890de-259">Entrée</span><span class="sxs-lookup"><span data-stu-id="890de-259">Entry</span></span> | <span data-ttu-id="890de-260">Valeur</span><span class="sxs-lookup"><span data-stu-id="890de-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="890de-261">ID de lien</span><span class="sxs-lookup"><span data-stu-id="890de-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="890de-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="890de-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="890de-263">System-Only</span></span>            | <span data-ttu-id="890de-264">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-264">False</span></span>                             |
| <span data-ttu-id="890de-265">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="890de-265">Is-Single-Valued</span></span>       | <span data-ttu-id="890de-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="890de-266">True</span></span>                              |
| <span data-ttu-id="890de-267">Est indexé</span><span class="sxs-lookup"><span data-stu-id="890de-267">Is Indexed</span></span>             | <span data-ttu-id="890de-268">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-268">False</span></span>                             |
| <span data-ttu-id="890de-269">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="890de-269">In Global Catalog</span></span>      | <span data-ttu-id="890de-270">Faux</span><span class="sxs-lookup"><span data-stu-id="890de-270">False</span></span>                             |
| <span data-ttu-id="890de-271">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="890de-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="890de-272">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="890de-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="890de-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="890de-273">Range-Lower</span></span>            | <span data-ttu-id="890de-274">0</span><span class="sxs-lookup"><span data-stu-id="890de-274">0</span></span>                                 |
| <span data-ttu-id="890de-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="890de-275">Range-Upper</span></span>            | <span data-ttu-id="890de-276">32767</span><span class="sxs-lookup"><span data-stu-id="890de-276">32767</span></span>                             |
| <span data-ttu-id="890de-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-277">Search-Flags</span></span>           | <span data-ttu-id="890de-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890de-278">0x00000000</span></span>                        |
| <span data-ttu-id="890de-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="890de-279">System-Flags</span></span>           | <span data-ttu-id="890de-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="890de-280">0x00000010</span></span>                        |
| <span data-ttu-id="890de-281">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="890de-281">Classes used in</span></span>        | [<span data-ttu-id="890de-282">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="890de-282">**User**</span></span>](c-user.md)<br/> |



 

 





