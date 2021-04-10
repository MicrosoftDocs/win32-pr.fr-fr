---
title: Attribut MSI-script-Path
description: Chemin d’accès au fichier de script de publication Microsoft installer pour cette application.
ms.assetid: 6ebe172c-42fc-4a36-940e-a48315d6496c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MSI-script-Path
- Schéma AD de l’attribut msiScriptPath
topic_type:
- apiref
api_name:
- Msi-Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ecce0bb7c082666136e69be8179cf3c5cdf7a6d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107752"
---
# <a name="msi-script-path-attribute"></a><span data-ttu-id="2a4ff-105">Attribut MSI-script-Path</span><span class="sxs-lookup"><span data-stu-id="2a4ff-105">Msi-Script-Path attribute</span></span>

<span data-ttu-id="2a4ff-106">Chemin d’accès au fichier de script de publication Microsoft installer pour cette application.</span><span class="sxs-lookup"><span data-stu-id="2a4ff-106">The file path for the Microsoft installer advertisement script file for this application.</span></span>



| <span data-ttu-id="2a4ff-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-107">Entry</span></span> | <span data-ttu-id="2a4ff-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2a4ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a4ff-109">CN</span></span>                | <span data-ttu-id="2a4ff-110">MSI-script-chemin</span><span class="sxs-lookup"><span data-stu-id="2a4ff-110">Msi-Script-Path</span></span>                             |
| <span data-ttu-id="2a4ff-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2a4ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a4ff-112">msiScriptPath</span><span class="sxs-lookup"><span data-stu-id="2a4ff-112">msiScriptPath</span></span>                               |
| <span data-ttu-id="2a4ff-113">Taille</span><span class="sxs-lookup"><span data-stu-id="2a4ff-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2a4ff-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2a4ff-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="2a4ff-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2a4ff-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2a4ff-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-116">Attribute-Id</span></span>      | <span data-ttu-id="2a4ff-117">1.2.840.113556.1.4.15</span><span class="sxs-lookup"><span data-stu-id="2a4ff-117">1.2.840.113556.1.4.15</span></span>                       |
| <span data-ttu-id="2a4ff-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2a4ff-118">System-Id-Guid</span></span>    | <span data-ttu-id="2a4ff-119">bf967937-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2a4ff-119">bf967937-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="2a4ff-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a4ff-120">Syntax</span></span>            | [<span data-ttu-id="2a4ff-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2a4ff-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2a4ff-122">Implementations</span></span>

-   [<span data-ttu-id="2a4ff-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a4ff-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a4ff-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a4ff-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a4ff-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a4ff-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a4ff-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a4ff-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2a4ff-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-130">Entry</span></span> | <span data-ttu-id="2a4ff-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-134">System-Only</span></span>            | <span data-ttu-id="2a4ff-135">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-135">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-137">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-138">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-139">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-139">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-140">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-141">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-141">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-146">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-148">System-Flags</span></span>           | <span data-ttu-id="2a4ff-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-150">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-151">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a4ff-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a4ff-152">Windows Server 2003</span></span>



| <span data-ttu-id="2a4ff-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-153">Entry</span></span> | <span data-ttu-id="2a4ff-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-157">System-Only</span></span>            | <span data-ttu-id="2a4ff-158">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-158">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-160">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-161">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-162">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-162">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-163">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-164">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-164">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-169">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-171">System-Flags</span></span>           | <span data-ttu-id="2a4ff-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-173">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-174">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a4ff-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a4ff-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a4ff-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-176">Entry</span></span> | <span data-ttu-id="2a4ff-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-180">System-Only</span></span>            | <span data-ttu-id="2a4ff-181">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-181">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-183">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-184">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-185">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-185">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-186">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-187">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-187">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-192">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-194">System-Flags</span></span>           | <span data-ttu-id="2a4ff-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-196">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-197">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a4ff-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a4ff-198">Windows Server 2008</span></span>



| <span data-ttu-id="2a4ff-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-199">Entry</span></span> | <span data-ttu-id="2a4ff-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-203">System-Only</span></span>            | <span data-ttu-id="2a4ff-204">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-204">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-206">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-207">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-208">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-208">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-209">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-210">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-210">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-215">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-217">System-Flags</span></span>           | <span data-ttu-id="2a4ff-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-219">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-220">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a4ff-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a4ff-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a4ff-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-222">Entry</span></span> | <span data-ttu-id="2a4ff-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-226">System-Only</span></span>            | <span data-ttu-id="2a4ff-227">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-227">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-229">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-230">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-231">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-231">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-232">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-233">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-233">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-238">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-240">System-Flags</span></span>           | <span data-ttu-id="2a4ff-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-242">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-243">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a4ff-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a4ff-244">Windows Server 2012</span></span>



| <span data-ttu-id="2a4ff-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a4ff-245">Entry</span></span> | <span data-ttu-id="2a4ff-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4ff-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2a4ff-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2a4ff-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a4ff-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2a4ff-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a4ff-249">System-Only</span></span>            | <span data-ttu-id="2a4ff-250">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-250">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2a4ff-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2a4ff-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="2a4ff-252">True</span></span>                                                             |
| <span data-ttu-id="2a4ff-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2a4ff-253">Is Indexed</span></span>             | <span data-ttu-id="2a4ff-254">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-254">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2a4ff-255">In Global Catalog</span></span>      | <span data-ttu-id="2a4ff-256">Faux</span><span class="sxs-lookup"><span data-stu-id="2a4ff-256">False</span></span>                                                            |
| <span data-ttu-id="2a4ff-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2a4ff-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a4ff-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2a4ff-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2a4ff-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a4ff-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a4ff-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2a4ff-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-261">Search-Flags</span></span>           | <span data-ttu-id="2a4ff-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a4ff-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="2a4ff-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a4ff-263">System-Flags</span></span>           | <span data-ttu-id="2a4ff-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a4ff-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="2a4ff-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2a4ff-265">Classes used in</span></span>        | [<span data-ttu-id="2a4ff-266">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="2a4ff-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





