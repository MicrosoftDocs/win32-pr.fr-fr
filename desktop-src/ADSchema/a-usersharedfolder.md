---
title: Attribut User-Shared-folder
description: Spécifie un chemin d’accès UNC au dossier Documents partagés de l’utilisateur. Le chemin d’accès doit être un chemin d’accès UNC réseau au format \\ \\ Répertoire de partage du serveur \\ \\ . Cette valeur peut être une chaîne NULL.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut User-Shared-folder
- Schéma AD de l’attribut userSharedFolder
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943225"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="4943f-107">Attribut User-Shared-folder</span><span class="sxs-lookup"><span data-stu-id="4943f-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="4943f-108">Spécifie un chemin d’accès UNC au dossier Documents partagés de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4943f-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="4943f-109">Le chemin d’accès doit être un chemin d’accès UNC réseau au format **\\\\** Répertoire de partage du _serveur_ *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="4943f-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="4943f-110">Cette valeur peut être une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="4943f-110">This value can be a null string.</span></span>



| <span data-ttu-id="4943f-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-111">Entry</span></span> | <span data-ttu-id="4943f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4943f-113">CN</span><span class="sxs-lookup"><span data-stu-id="4943f-113">CN</span></span>                | <span data-ttu-id="4943f-114">User-Shared-folder</span><span class="sxs-lookup"><span data-stu-id="4943f-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="4943f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4943f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4943f-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="4943f-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="4943f-117">Taille</span><span class="sxs-lookup"><span data-stu-id="4943f-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="4943f-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4943f-118">Update Privilege</span></span>  | <span data-ttu-id="4943f-119">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="4943f-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="4943f-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4943f-120">Update Frequency</span></span>  | <span data-ttu-id="4943f-121">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le dossier partagé doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="4943f-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="4943f-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-122">Attribute-Id</span></span>      | <span data-ttu-id="4943f-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="4943f-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="4943f-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4943f-124">System-Id-Guid</span></span>    | <span data-ttu-id="4943f-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4943f-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="4943f-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4943f-126">Syntax</span></span>            | [<span data-ttu-id="4943f-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4943f-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="4943f-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4943f-128">Implementations</span></span>

-   [<span data-ttu-id="4943f-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4943f-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4943f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4943f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4943f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4943f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4943f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4943f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4943f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4943f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4943f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4943f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4943f-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4943f-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4943f-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-136">Entry</span></span> | <span data-ttu-id="4943f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-140">System-Only</span></span>            | <span data-ttu-id="4943f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-141">False</span></span>                             |
| <span data-ttu-id="4943f-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-143">True</span></span>                              |
| <span data-ttu-id="4943f-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-144">Is Indexed</span></span>             | <span data-ttu-id="4943f-145">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-145">False</span></span>                             |
| <span data-ttu-id="4943f-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-146">In Global Catalog</span></span>      | <span data-ttu-id="4943f-147">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-147">False</span></span>                             |
| <span data-ttu-id="4943f-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-152">Search-Flags</span></span>           | <span data-ttu-id="4943f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-153">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-154">System-Flags</span></span>           | <span data-ttu-id="4943f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-155">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-156">Classes used in</span></span>        | [<span data-ttu-id="4943f-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4943f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4943f-158">Windows Server 2003</span></span>



| <span data-ttu-id="4943f-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-159">Entry</span></span> | <span data-ttu-id="4943f-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-163">System-Only</span></span>            | <span data-ttu-id="4943f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-164">False</span></span>                             |
| <span data-ttu-id="4943f-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-166">True</span></span>                              |
| <span data-ttu-id="4943f-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-167">Is Indexed</span></span>             | <span data-ttu-id="4943f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-168">False</span></span>                             |
| <span data-ttu-id="4943f-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-169">In Global Catalog</span></span>      | <span data-ttu-id="4943f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-170">False</span></span>                             |
| <span data-ttu-id="4943f-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-175">Search-Flags</span></span>           | <span data-ttu-id="4943f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-176">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-177">System-Flags</span></span>           | <span data-ttu-id="4943f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-178">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-179">Classes used in</span></span>        | [<span data-ttu-id="4943f-180">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4943f-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4943f-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4943f-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-182">Entry</span></span> | <span data-ttu-id="4943f-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-186">System-Only</span></span>            | <span data-ttu-id="4943f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-187">False</span></span>                             |
| <span data-ttu-id="4943f-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-189">True</span></span>                              |
| <span data-ttu-id="4943f-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-190">Is Indexed</span></span>             | <span data-ttu-id="4943f-191">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-191">False</span></span>                             |
| <span data-ttu-id="4943f-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-192">In Global Catalog</span></span>      | <span data-ttu-id="4943f-193">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-193">False</span></span>                             |
| <span data-ttu-id="4943f-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-198">Search-Flags</span></span>           | <span data-ttu-id="4943f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-199">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-200">System-Flags</span></span>           | <span data-ttu-id="4943f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-201">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-202">Classes used in</span></span>        | [<span data-ttu-id="4943f-203">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4943f-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4943f-204">Windows Server 2008</span></span>



| <span data-ttu-id="4943f-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-205">Entry</span></span> | <span data-ttu-id="4943f-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-209">System-Only</span></span>            | <span data-ttu-id="4943f-210">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-210">False</span></span>                             |
| <span data-ttu-id="4943f-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-212">True</span></span>                              |
| <span data-ttu-id="4943f-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-213">Is Indexed</span></span>             | <span data-ttu-id="4943f-214">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-214">False</span></span>                             |
| <span data-ttu-id="4943f-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-215">In Global Catalog</span></span>      | <span data-ttu-id="4943f-216">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-216">False</span></span>                             |
| <span data-ttu-id="4943f-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-221">Search-Flags</span></span>           | <span data-ttu-id="4943f-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-222">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-223">System-Flags</span></span>           | <span data-ttu-id="4943f-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-224">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-225">Classes used in</span></span>        | [<span data-ttu-id="4943f-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4943f-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4943f-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4943f-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-228">Entry</span></span> | <span data-ttu-id="4943f-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-232">System-Only</span></span>            | <span data-ttu-id="4943f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-233">False</span></span>                             |
| <span data-ttu-id="4943f-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-235">True</span></span>                              |
| <span data-ttu-id="4943f-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-236">Is Indexed</span></span>             | <span data-ttu-id="4943f-237">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-237">False</span></span>                             |
| <span data-ttu-id="4943f-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-238">In Global Catalog</span></span>      | <span data-ttu-id="4943f-239">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-239">False</span></span>                             |
| <span data-ttu-id="4943f-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-244">Search-Flags</span></span>           | <span data-ttu-id="4943f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-245">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-246">System-Flags</span></span>           | <span data-ttu-id="4943f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-247">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-248">Classes used in</span></span>        | [<span data-ttu-id="4943f-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4943f-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4943f-250">Windows Server 2012</span></span>



| <span data-ttu-id="4943f-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="4943f-251">Entry</span></span> | <span data-ttu-id="4943f-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="4943f-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4943f-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4943f-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4943f-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4943f-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="4943f-255">System-Only</span></span>            | <span data-ttu-id="4943f-256">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-256">False</span></span>                             |
| <span data-ttu-id="4943f-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4943f-257">Is-Single-Valued</span></span>       | <span data-ttu-id="4943f-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="4943f-258">True</span></span>                              |
| <span data-ttu-id="4943f-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4943f-259">Is Indexed</span></span>             | <span data-ttu-id="4943f-260">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-260">False</span></span>                             |
| <span data-ttu-id="4943f-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4943f-261">In Global Catalog</span></span>      | <span data-ttu-id="4943f-262">Faux</span><span class="sxs-lookup"><span data-stu-id="4943f-262">False</span></span>                             |
| <span data-ttu-id="4943f-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4943f-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="4943f-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4943f-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4943f-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4943f-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4943f-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4943f-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4943f-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-267">Search-Flags</span></span>           | <span data-ttu-id="4943f-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4943f-268">0x00000000</span></span>                        |
| <span data-ttu-id="4943f-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4943f-269">System-Flags</span></span>           | <span data-ttu-id="4943f-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4943f-270">0x00000010</span></span>                        |
| <span data-ttu-id="4943f-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4943f-271">Classes used in</span></span>        | [<span data-ttu-id="4943f-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4943f-272">**User**</span></span>](c-user.md)<br/> |



 

 





