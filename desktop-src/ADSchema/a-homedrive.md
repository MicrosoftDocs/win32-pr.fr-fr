---
title: Attribut Home-Drive
description: Spécifie la lettre de lecteur à laquelle mapper le chemin d’accès UNC spécifié par homeDirectory.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Home-Drive
- Schéma AD de l’attribut homeDrive
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106517344"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="c43e0-105">Attribut Home-Drive</span><span class="sxs-lookup"><span data-stu-id="c43e0-105">Home-Drive attribute</span></span>

<span data-ttu-id="c43e0-106">Spécifie la lettre de lecteur à laquelle mapper le chemin d’accès UNC spécifié par [**HomeDirectory**](a-homedirectory.md).</span><span class="sxs-lookup"><span data-stu-id="c43e0-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="c43e0-107">La lettre de lecteur doit être spécifiée sous la forme *LettreLecteur \* \* * :** où *LettreLecteur* est la lettre du lecteur à mapper.</span><span class="sxs-lookup"><span data-stu-id="c43e0-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="c43e0-108">Le *LettreLecteur* doit être une seule lettre majuscule et le signe deux-points ( :) est requis.</span><span class="sxs-lookup"><span data-stu-id="c43e0-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="c43e0-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-109">Entry</span></span> | <span data-ttu-id="c43e0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c43e0-111">CN</span><span class="sxs-lookup"><span data-stu-id="c43e0-111">CN</span></span>                | <span data-ttu-id="c43e0-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="c43e0-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="c43e0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c43e0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c43e0-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="c43e0-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="c43e0-115">Taille</span><span class="sxs-lookup"><span data-stu-id="c43e0-115">Size</span></span>              | <span data-ttu-id="c43e0-116">2 octets</span><span class="sxs-lookup"><span data-stu-id="c43e0-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="c43e0-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c43e0-117">Update Privilege</span></span>  | <span data-ttu-id="c43e0-118">L’administrateur de domaine définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c43e0-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="c43e0-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c43e0-119">Update Frequency</span></span>  | <span data-ttu-id="c43e0-120">Lorsque l’enregistrement d’un utilisateur est créé et chaque fois que le lecteur de démarrage doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="c43e0-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="c43e0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-121">Attribute-Id</span></span>      | <span data-ttu-id="c43e0-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="c43e0-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="c43e0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c43e0-123">System-Id-Guid</span></span>    | <span data-ttu-id="c43e0-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c43e0-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="c43e0-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c43e0-125">Syntax</span></span>            | [<span data-ttu-id="c43e0-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c43e0-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="c43e0-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c43e0-127">Implementations</span></span>

-   [<span data-ttu-id="c43e0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c43e0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c43e0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c43e0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c43e0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c43e0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c43e0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c43e0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c43e0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c43e0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c43e0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c43e0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c43e0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c43e0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c43e0-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-135">Entry</span></span> | <span data-ttu-id="c43e0-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-139">System-Only</span></span>            | <span data-ttu-id="c43e0-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-140">False</span></span>                             |
| <span data-ttu-id="c43e0-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-142">True</span></span>                              |
| <span data-ttu-id="c43e0-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-143">Is Indexed</span></span>             | <span data-ttu-id="c43e0-144">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-144">False</span></span>                             |
| <span data-ttu-id="c43e0-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-145">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-146">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-146">False</span></span>                             |
| <span data-ttu-id="c43e0-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-151">Search-Flags</span></span>           | <span data-ttu-id="c43e0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-152">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-153">System-Flags</span></span>           | <span data-ttu-id="c43e0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-154">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-155">Classes used in</span></span>        | [<span data-ttu-id="c43e0-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c43e0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c43e0-157">Windows Server 2003</span></span>



| <span data-ttu-id="c43e0-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-158">Entry</span></span> | <span data-ttu-id="c43e0-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-162">System-Only</span></span>            | <span data-ttu-id="c43e0-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-163">False</span></span>                             |
| <span data-ttu-id="c43e0-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-165">True</span></span>                              |
| <span data-ttu-id="c43e0-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-166">Is Indexed</span></span>             | <span data-ttu-id="c43e0-167">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-167">False</span></span>                             |
| <span data-ttu-id="c43e0-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-168">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-169">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-169">False</span></span>                             |
| <span data-ttu-id="c43e0-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-174">Search-Flags</span></span>           | <span data-ttu-id="c43e0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-175">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-176">System-Flags</span></span>           | <span data-ttu-id="c43e0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-177">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-178">Classes used in</span></span>        | [<span data-ttu-id="c43e0-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c43e0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c43e0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c43e0-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-181">Entry</span></span> | <span data-ttu-id="c43e0-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-185">System-Only</span></span>            | <span data-ttu-id="c43e0-186">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-186">False</span></span>                             |
| <span data-ttu-id="c43e0-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-188">True</span></span>                              |
| <span data-ttu-id="c43e0-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-189">Is Indexed</span></span>             | <span data-ttu-id="c43e0-190">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-190">False</span></span>                             |
| <span data-ttu-id="c43e0-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-191">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-192">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-192">False</span></span>                             |
| <span data-ttu-id="c43e0-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-197">Search-Flags</span></span>           | <span data-ttu-id="c43e0-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-198">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-199">System-Flags</span></span>           | <span data-ttu-id="c43e0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-200">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-201">Classes used in</span></span>        | [<span data-ttu-id="c43e0-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c43e0-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c43e0-203">Windows Server 2008</span></span>



| <span data-ttu-id="c43e0-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-204">Entry</span></span> | <span data-ttu-id="c43e0-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-208">System-Only</span></span>            | <span data-ttu-id="c43e0-209">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-209">False</span></span>                             |
| <span data-ttu-id="c43e0-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-211">True</span></span>                              |
| <span data-ttu-id="c43e0-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-212">Is Indexed</span></span>             | <span data-ttu-id="c43e0-213">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-213">False</span></span>                             |
| <span data-ttu-id="c43e0-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-214">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-215">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-215">False</span></span>                             |
| <span data-ttu-id="c43e0-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-220">Search-Flags</span></span>           | <span data-ttu-id="c43e0-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-221">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-222">System-Flags</span></span>           | <span data-ttu-id="c43e0-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-223">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-224">Classes used in</span></span>        | [<span data-ttu-id="c43e0-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c43e0-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c43e0-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c43e0-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-227">Entry</span></span> | <span data-ttu-id="c43e0-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-231">System-Only</span></span>            | <span data-ttu-id="c43e0-232">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-232">False</span></span>                             |
| <span data-ttu-id="c43e0-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-234">True</span></span>                              |
| <span data-ttu-id="c43e0-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-235">Is Indexed</span></span>             | <span data-ttu-id="c43e0-236">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-236">False</span></span>                             |
| <span data-ttu-id="c43e0-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-237">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-238">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-238">False</span></span>                             |
| <span data-ttu-id="c43e0-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-243">Search-Flags</span></span>           | <span data-ttu-id="c43e0-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-244">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-245">System-Flags</span></span>           | <span data-ttu-id="c43e0-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-246">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-247">Classes used in</span></span>        | [<span data-ttu-id="c43e0-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c43e0-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c43e0-249">Windows Server 2012</span></span>



| <span data-ttu-id="c43e0-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="c43e0-250">Entry</span></span> | <span data-ttu-id="c43e0-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43e0-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c43e0-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c43e0-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43e0-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c43e0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43e0-254">System-Only</span></span>            | <span data-ttu-id="c43e0-255">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-255">False</span></span>                             |
| <span data-ttu-id="c43e0-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c43e0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c43e0-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="c43e0-257">True</span></span>                              |
| <span data-ttu-id="c43e0-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c43e0-258">Is Indexed</span></span>             | <span data-ttu-id="c43e0-259">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-259">False</span></span>                             |
| <span data-ttu-id="c43e0-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c43e0-260">In Global Catalog</span></span>      | <span data-ttu-id="c43e0-261">Faux</span><span class="sxs-lookup"><span data-stu-id="c43e0-261">False</span></span>                             |
| <span data-ttu-id="c43e0-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c43e0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43e0-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c43e0-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c43e0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43e0-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c43e0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43e0-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c43e0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-266">Search-Flags</span></span>           | <span data-ttu-id="c43e0-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-267">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43e0-268">System-Flags</span></span>           | <span data-ttu-id="c43e0-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43e0-269">0x00000010</span></span>                        |
| <span data-ttu-id="c43e0-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c43e0-270">Classes used in</span></span>        | [<span data-ttu-id="c43e0-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c43e0-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="c43e0-272">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c43e0-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43e0-273">**homeDirectory**</span><span class="sxs-lookup"><span data-stu-id="c43e0-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





