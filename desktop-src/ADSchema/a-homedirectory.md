---
title: Attribut Home-Directory
description: Répertoire de départ du compte.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Home-Directory
- Schéma AD de l’attribut homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744852"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="a3c0d-105">Attribut Home-Directory</span><span class="sxs-lookup"><span data-stu-id="a3c0d-105">Home-Directory attribute</span></span>

<span data-ttu-id="a3c0d-106">Répertoire de départ du compte.</span><span class="sxs-lookup"><span data-stu-id="a3c0d-106">The home directory for the account.</span></span> <span data-ttu-id="a3c0d-107">Si [**le**](a-homedrive.md) lecteur de disque est défini et spécifie une lettre de lecteur, **HomeDirectory** doit être un chemin d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="a3c0d-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="a3c0d-108">Sinon, **HomeDirectory** est un chemin d’accès local complet incluant la lettre de lecteur (par exemple, \*DriveLetter \***: \\**_Directory_\* _\\_ \* _Folder_).</span><span class="sxs-lookup"><span data-stu-id="a3c0d-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="a3c0d-109">Cette valeur peut être une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="a3c0d-109">This value can be a null string.</span></span>



| <span data-ttu-id="a3c0d-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-110">Entry</span></span> | <span data-ttu-id="a3c0d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c0d-112">CN</span><span class="sxs-lookup"><span data-stu-id="a3c0d-112">CN</span></span>                | <span data-ttu-id="a3c0d-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="a3c0d-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="a3c0d-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a3c0d-114">Ldap-Display-Name</span></span> | <span data-ttu-id="a3c0d-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="a3c0d-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="a3c0d-116">Taille</span><span class="sxs-lookup"><span data-stu-id="a3c0d-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="a3c0d-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a3c0d-117">Update Privilege</span></span>  | <span data-ttu-id="a3c0d-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="a3c0d-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="a3c0d-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a3c0d-119">Update Frequency</span></span>  | <span data-ttu-id="a3c0d-120">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le répertoire de départ doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="a3c0d-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="a3c0d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-121">Attribute-Id</span></span>      | <span data-ttu-id="a3c0d-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="a3c0d-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="a3c0d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3c0d-123">System-Id-Guid</span></span>    | <span data-ttu-id="a3c0d-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a3c0d-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="a3c0d-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3c0d-125">Syntax</span></span>            | [<span data-ttu-id="a3c0d-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="a3c0d-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a3c0d-127">Implementations</span></span>

-   [<span data-ttu-id="a3c0d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3c0d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3c0d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3c0d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3c0d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3c0d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3c0d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3c0d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a3c0d-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-135">Entry</span></span> | <span data-ttu-id="a3c0d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3c0d-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3c0d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3c0d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-139">System-Only</span></span>            | <span data-ttu-id="a3c0d-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-140">False</span></span>                             |
| <span data-ttu-id="a3c0d-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-142">True</span></span>                              |
| <span data-ttu-id="a3c0d-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-143">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-144">False</span></span>                             |
| <span data-ttu-id="a3c0d-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-145">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-146">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-146">False</span></span>                             |
| <span data-ttu-id="a3c0d-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3c0d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3c0d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3c0d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-151">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-152">0x00000010</span></span>                        |
| <span data-ttu-id="a3c0d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-153">System-Flags</span></span>           | <span data-ttu-id="a3c0d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-154">0x00000010</span></span>                        |
| <span data-ttu-id="a3c0d-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-155">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3c0d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3c0d-157">Windows Server 2003</span></span>



| <span data-ttu-id="a3c0d-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-158">Entry</span></span> | <span data-ttu-id="a3c0d-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3c0d-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3c0d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3c0d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-162">System-Only</span></span>            | <span data-ttu-id="a3c0d-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-163">False</span></span>                             |
| <span data-ttu-id="a3c0d-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-165">True</span></span>                              |
| <span data-ttu-id="a3c0d-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-166">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-167">False</span></span>                             |
| <span data-ttu-id="a3c0d-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-168">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-169">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-169">False</span></span>                             |
| <span data-ttu-id="a3c0d-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3c0d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3c0d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3c0d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-174">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-175">0x00000010</span></span>                        |
| <span data-ttu-id="a3c0d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-176">System-Flags</span></span>           | <span data-ttu-id="a3c0d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-177">0x00000010</span></span>                        |
| <span data-ttu-id="a3c0d-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-178">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3c0d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3c0d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3c0d-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-181">Entry</span></span> | <span data-ttu-id="a3c0d-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c0d-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-185">System-Only</span></span>            | <span data-ttu-id="a3c0d-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-186">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-188">True</span></span>                                                                                |
| <span data-ttu-id="a3c0d-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-189">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-190">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-191">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-192">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a3c0d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-197">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-199">System-Flags</span></span>           | <span data-ttu-id="a3c0d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-201">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a3c0d-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3c0d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3c0d-204">Windows Server 2008</span></span>



| <span data-ttu-id="a3c0d-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-205">Entry</span></span> | <span data-ttu-id="a3c0d-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c0d-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-209">System-Only</span></span>            | <span data-ttu-id="a3c0d-210">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-210">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-212">True</span></span>                                                                                |
| <span data-ttu-id="a3c0d-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-213">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-214">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-214">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-215">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-216">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-216">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a3c0d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-221">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-223">System-Flags</span></span>           | <span data-ttu-id="a3c0d-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-225">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a3c0d-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3c0d-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3c0d-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3c0d-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-229">Entry</span></span> | <span data-ttu-id="a3c0d-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c0d-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-233">System-Only</span></span>            | <span data-ttu-id="a3c0d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-234">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-236">True</span></span>                                                                                |
| <span data-ttu-id="a3c0d-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-237">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-238">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-239">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-240">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-240">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a3c0d-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-245">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-247">System-Flags</span></span>           | <span data-ttu-id="a3c0d-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-249">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-250">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a3c0d-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3c0d-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3c0d-252">Windows Server 2012</span></span>



| <span data-ttu-id="a3c0d-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3c0d-253">Entry</span></span> | <span data-ttu-id="a3c0d-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3c0d-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c0d-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3c0d-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3c0d-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a3c0d-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3c0d-257">System-Only</span></span>            | <span data-ttu-id="a3c0d-258">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-258">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3c0d-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a3c0d-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3c0d-260">True</span></span>                                                                                |
| <span data-ttu-id="a3c0d-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3c0d-261">Is Indexed</span></span>             | <span data-ttu-id="a3c0d-262">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-262">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3c0d-263">In Global Catalog</span></span>      | <span data-ttu-id="a3c0d-264">Faux</span><span class="sxs-lookup"><span data-stu-id="a3c0d-264">False</span></span>                                                                               |
| <span data-ttu-id="a3c0d-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3c0d-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3c0d-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3c0d-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a3c0d-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3c0d-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3c0d-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a3c0d-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-269">Search-Flags</span></span>           | <span data-ttu-id="a3c0d-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3c0d-271">System-Flags</span></span>           | <span data-ttu-id="a3c0d-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3c0d-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a3c0d-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3c0d-273">Classes used in</span></span>        | [<span data-ttu-id="a3c0d-274">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a3c0d-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="a3c0d-276">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3c0d-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c0d-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="a3c0d-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





