---
title: Utilisateur-partagé-dossier-autre attribut
description: Spécifie un chemin d’accès UNC au dossier Documents partagés supplémentaire de l’utilisateur. Le chemin d’accès doit être un chemin d’accès UNC réseau au format \\ \\ Répertoire de partage du serveur \\ \\ . Cette valeur peut être une chaîne NULL.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- User-Shared-folder-autre attribut schéma Active Directory
- Schéma AD de l’attribut userSharedFolderOther
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744516"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="f7306-107">Utilisateur-partagé-dossier-autre attribut</span><span class="sxs-lookup"><span data-stu-id="f7306-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="f7306-108">Spécifie un chemin d’accès UNC au dossier Documents partagés supplémentaire de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7306-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="f7306-109">Le chemin d’accès doit être un chemin d’accès UNC réseau au format **\\\\** Répertoire de partage du _serveur_ *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="f7306-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="f7306-110">Cette valeur peut être une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="f7306-110">This value can be a null string.</span></span>



| <span data-ttu-id="f7306-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-111">Entry</span></span> | <span data-ttu-id="f7306-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f7306-113">CN</span><span class="sxs-lookup"><span data-stu-id="f7306-113">CN</span></span>                | <span data-ttu-id="f7306-114">Utilisateur-partagé-dossier-autre</span><span class="sxs-lookup"><span data-stu-id="f7306-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="f7306-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f7306-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f7306-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="f7306-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="f7306-117">Taille</span><span class="sxs-lookup"><span data-stu-id="f7306-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="f7306-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f7306-118">Update Privilege</span></span>  | <span data-ttu-id="f7306-119">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="f7306-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="f7306-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f7306-120">Update Frequency</span></span>  | <span data-ttu-id="f7306-121">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le dossier partagé doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="f7306-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="f7306-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-122">Attribute-Id</span></span>      | <span data-ttu-id="f7306-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="f7306-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="f7306-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7306-124">System-Id-Guid</span></span>    | <span data-ttu-id="f7306-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f7306-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="f7306-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7306-126">Syntax</span></span>            | [<span data-ttu-id="f7306-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f7306-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="f7306-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f7306-128">Implementations</span></span>

-   [<span data-ttu-id="f7306-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7306-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7306-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7306-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7306-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7306-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7306-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7306-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7306-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7306-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7306-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7306-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7306-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7306-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f7306-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-136">Entry</span></span> | <span data-ttu-id="f7306-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-140">System-Only</span></span>            | <span data-ttu-id="f7306-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-141">False</span></span>                             |
| <span data-ttu-id="f7306-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-143">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-143">False</span></span>                             |
| <span data-ttu-id="f7306-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-144">Is Indexed</span></span>             | <span data-ttu-id="f7306-145">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-145">False</span></span>                             |
| <span data-ttu-id="f7306-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-146">In Global Catalog</span></span>      | <span data-ttu-id="f7306-147">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-147">False</span></span>                             |
| <span data-ttu-id="f7306-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-152">Search-Flags</span></span>           | <span data-ttu-id="f7306-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-153">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-154">System-Flags</span></span>           | <span data-ttu-id="f7306-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-155">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-156">Classes used in</span></span>        | [<span data-ttu-id="f7306-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7306-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7306-158">Windows Server 2003</span></span>



| <span data-ttu-id="f7306-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-159">Entry</span></span> | <span data-ttu-id="f7306-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-163">System-Only</span></span>            | <span data-ttu-id="f7306-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-164">False</span></span>                             |
| <span data-ttu-id="f7306-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-166">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-166">False</span></span>                             |
| <span data-ttu-id="f7306-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-167">Is Indexed</span></span>             | <span data-ttu-id="f7306-168">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-168">False</span></span>                             |
| <span data-ttu-id="f7306-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-169">In Global Catalog</span></span>      | <span data-ttu-id="f7306-170">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-170">False</span></span>                             |
| <span data-ttu-id="f7306-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-175">Search-Flags</span></span>           | <span data-ttu-id="f7306-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-176">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-177">System-Flags</span></span>           | <span data-ttu-id="f7306-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-178">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-179">Classes used in</span></span>        | [<span data-ttu-id="f7306-180">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7306-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7306-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7306-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-182">Entry</span></span> | <span data-ttu-id="f7306-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-186">System-Only</span></span>            | <span data-ttu-id="f7306-187">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-187">False</span></span>                             |
| <span data-ttu-id="f7306-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-189">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-189">False</span></span>                             |
| <span data-ttu-id="f7306-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-190">Is Indexed</span></span>             | <span data-ttu-id="f7306-191">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-191">False</span></span>                             |
| <span data-ttu-id="f7306-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-192">In Global Catalog</span></span>      | <span data-ttu-id="f7306-193">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-193">False</span></span>                             |
| <span data-ttu-id="f7306-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-198">Search-Flags</span></span>           | <span data-ttu-id="f7306-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-199">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-200">System-Flags</span></span>           | <span data-ttu-id="f7306-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-201">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-202">Classes used in</span></span>        | [<span data-ttu-id="f7306-203">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7306-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7306-204">Windows Server 2008</span></span>



| <span data-ttu-id="f7306-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-205">Entry</span></span> | <span data-ttu-id="f7306-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-209">System-Only</span></span>            | <span data-ttu-id="f7306-210">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-210">False</span></span>                             |
| <span data-ttu-id="f7306-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-212">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-212">False</span></span>                             |
| <span data-ttu-id="f7306-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-213">Is Indexed</span></span>             | <span data-ttu-id="f7306-214">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-214">False</span></span>                             |
| <span data-ttu-id="f7306-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-215">In Global Catalog</span></span>      | <span data-ttu-id="f7306-216">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-216">False</span></span>                             |
| <span data-ttu-id="f7306-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-221">Search-Flags</span></span>           | <span data-ttu-id="f7306-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-222">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-223">System-Flags</span></span>           | <span data-ttu-id="f7306-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-224">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-225">Classes used in</span></span>        | [<span data-ttu-id="f7306-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7306-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7306-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7306-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-228">Entry</span></span> | <span data-ttu-id="f7306-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-232">System-Only</span></span>            | <span data-ttu-id="f7306-233">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-233">False</span></span>                             |
| <span data-ttu-id="f7306-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-235">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-235">False</span></span>                             |
| <span data-ttu-id="f7306-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-236">Is Indexed</span></span>             | <span data-ttu-id="f7306-237">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-237">False</span></span>                             |
| <span data-ttu-id="f7306-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-238">In Global Catalog</span></span>      | <span data-ttu-id="f7306-239">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-239">False</span></span>                             |
| <span data-ttu-id="f7306-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-244">Search-Flags</span></span>           | <span data-ttu-id="f7306-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-245">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-246">System-Flags</span></span>           | <span data-ttu-id="f7306-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-247">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-248">Classes used in</span></span>        | [<span data-ttu-id="f7306-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7306-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7306-250">Windows Server 2012</span></span>



| <span data-ttu-id="f7306-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7306-251">Entry</span></span> | <span data-ttu-id="f7306-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7306-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7306-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7306-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7306-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7306-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7306-255">System-Only</span></span>            | <span data-ttu-id="f7306-256">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-256">False</span></span>                             |
| <span data-ttu-id="f7306-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7306-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f7306-258">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-258">False</span></span>                             |
| <span data-ttu-id="f7306-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7306-259">Is Indexed</span></span>             | <span data-ttu-id="f7306-260">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-260">False</span></span>                             |
| <span data-ttu-id="f7306-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7306-261">In Global Catalog</span></span>      | <span data-ttu-id="f7306-262">Faux</span><span class="sxs-lookup"><span data-stu-id="f7306-262">False</span></span>                             |
| <span data-ttu-id="f7306-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7306-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7306-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7306-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7306-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7306-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7306-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7306-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7306-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-267">Search-Flags</span></span>           | <span data-ttu-id="f7306-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7306-268">0x00000000</span></span>                        |
| <span data-ttu-id="f7306-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7306-269">System-Flags</span></span>           | <span data-ttu-id="f7306-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7306-270">0x00000010</span></span>                        |
| <span data-ttu-id="f7306-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7306-271">Classes used in</span></span>        | [<span data-ttu-id="f7306-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f7306-272">**User**</span></span>](c-user.md)<br/> |



 

 





