---
title: Attribut Script-Path
description: Cet attribut spécifie le chemin d’accès pour le script d’ouverture de session de l’utilisateur. La chaîne peut être null.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Script-Path
- Schéma AD de l’attribut scriptPath
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107955"
---
# <a name="script-path-attribute"></a><span data-ttu-id="d2bfb-106">Attribut Script-Path</span><span class="sxs-lookup"><span data-stu-id="d2bfb-106">Script-Path attribute</span></span>

<span data-ttu-id="d2bfb-107">Cet attribut spécifie le chemin d’accès pour le script d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="d2bfb-108">La chaîne peut être null.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-108">The string can be null.</span></span>



| <span data-ttu-id="d2bfb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-109">Entry</span></span> | <span data-ttu-id="d2bfb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d2bfb-111">CN</span><span class="sxs-lookup"><span data-stu-id="d2bfb-111">CN</span></span>                | <span data-ttu-id="d2bfb-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="d2bfb-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="d2bfb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2bfb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d2bfb-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="d2bfb-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="d2bfb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="d2bfb-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="d2bfb-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d2bfb-116">Update Privilege</span></span>  | <span data-ttu-id="d2bfb-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="d2bfb-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d2bfb-118">Update Frequency</span></span>  | <span data-ttu-id="d2bfb-119">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le chemin d’accès doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="d2bfb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-120">Attribute-Id</span></span>      | <span data-ttu-id="d2bfb-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="d2bfb-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="d2bfb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2bfb-122">System-Id-Guid</span></span>    | <span data-ttu-id="d2bfb-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d2bfb-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="d2bfb-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2bfb-124">Syntax</span></span>            | [<span data-ttu-id="d2bfb-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="d2bfb-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d2bfb-126">Implementations</span></span>

-   [<span data-ttu-id="d2bfb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2bfb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2bfb-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2bfb-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2bfb-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2bfb-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2bfb-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2bfb-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d2bfb-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-134">Entry</span></span> | <span data-ttu-id="d2bfb-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-138">System-Only</span></span>            | <span data-ttu-id="d2bfb-139">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-139">False</span></span>                             |
| <span data-ttu-id="d2bfb-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-141">True</span></span>                              |
| <span data-ttu-id="d2bfb-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-142">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-143">False</span></span>                             |
| <span data-ttu-id="d2bfb-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-144">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-145">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-145">False</span></span>                             |
| <span data-ttu-id="d2bfb-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-150">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-151">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-152">System-Flags</span></span>           | <span data-ttu-id="d2bfb-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-153">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-154">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-155">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2bfb-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2bfb-156">Windows Server 2003</span></span>



| <span data-ttu-id="d2bfb-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-157">Entry</span></span> | <span data-ttu-id="d2bfb-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-161">System-Only</span></span>            | <span data-ttu-id="d2bfb-162">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-162">False</span></span>                             |
| <span data-ttu-id="d2bfb-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-164">True</span></span>                              |
| <span data-ttu-id="d2bfb-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-165">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-166">False</span></span>                             |
| <span data-ttu-id="d2bfb-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-167">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-168">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-168">False</span></span>                             |
| <span data-ttu-id="d2bfb-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-173">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-174">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-175">System-Flags</span></span>           | <span data-ttu-id="d2bfb-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-176">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-177">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-178">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2bfb-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2bfb-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2bfb-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-180">Entry</span></span> | <span data-ttu-id="d2bfb-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-184">System-Only</span></span>            | <span data-ttu-id="d2bfb-185">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-185">False</span></span>                             |
| <span data-ttu-id="d2bfb-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-187">True</span></span>                              |
| <span data-ttu-id="d2bfb-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-188">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-189">False</span></span>                             |
| <span data-ttu-id="d2bfb-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-190">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-191">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-191">False</span></span>                             |
| <span data-ttu-id="d2bfb-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-196">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-197">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-198">System-Flags</span></span>           | <span data-ttu-id="d2bfb-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-199">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-200">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-201">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2bfb-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2bfb-202">Windows Server 2008</span></span>



| <span data-ttu-id="d2bfb-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-203">Entry</span></span> | <span data-ttu-id="d2bfb-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-207">System-Only</span></span>            | <span data-ttu-id="d2bfb-208">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-208">False</span></span>                             |
| <span data-ttu-id="d2bfb-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-210">True</span></span>                              |
| <span data-ttu-id="d2bfb-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-211">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-212">False</span></span>                             |
| <span data-ttu-id="d2bfb-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-213">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-214">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-214">False</span></span>                             |
| <span data-ttu-id="d2bfb-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-219">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-220">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-221">System-Flags</span></span>           | <span data-ttu-id="d2bfb-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-222">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-223">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-224">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2bfb-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2bfb-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2bfb-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-226">Entry</span></span> | <span data-ttu-id="d2bfb-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-230">System-Only</span></span>            | <span data-ttu-id="d2bfb-231">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-231">False</span></span>                             |
| <span data-ttu-id="d2bfb-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-233">True</span></span>                              |
| <span data-ttu-id="d2bfb-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-234">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-235">False</span></span>                             |
| <span data-ttu-id="d2bfb-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-236">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-237">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-237">False</span></span>                             |
| <span data-ttu-id="d2bfb-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-242">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-243">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-244">System-Flags</span></span>           | <span data-ttu-id="d2bfb-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-245">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-246">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-247">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2bfb-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2bfb-248">Windows Server 2012</span></span>



| <span data-ttu-id="d2bfb-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="d2bfb-249">Entry</span></span> | <span data-ttu-id="d2bfb-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2bfb-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d2bfb-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d2bfb-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2bfb-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d2bfb-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2bfb-253">System-Only</span></span>            | <span data-ttu-id="d2bfb-254">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-254">False</span></span>                             |
| <span data-ttu-id="d2bfb-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d2bfb-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d2bfb-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2bfb-256">True</span></span>                              |
| <span data-ttu-id="d2bfb-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d2bfb-257">Is Indexed</span></span>             | <span data-ttu-id="d2bfb-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-258">False</span></span>                             |
| <span data-ttu-id="d2bfb-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d2bfb-259">In Global Catalog</span></span>      | <span data-ttu-id="d2bfb-260">Faux</span><span class="sxs-lookup"><span data-stu-id="d2bfb-260">False</span></span>                             |
| <span data-ttu-id="d2bfb-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d2bfb-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2bfb-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d2bfb-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d2bfb-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2bfb-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2bfb-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d2bfb-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-265">Search-Flags</span></span>           | <span data-ttu-id="d2bfb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-266">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2bfb-267">System-Flags</span></span>           | <span data-ttu-id="d2bfb-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2bfb-268">0x00000010</span></span>                        |
| <span data-ttu-id="d2bfb-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d2bfb-269">Classes used in</span></span>        | [<span data-ttu-id="d2bfb-270">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d2bfb-270">**User**</span></span>](c-user.md)<br/> |



 

 





