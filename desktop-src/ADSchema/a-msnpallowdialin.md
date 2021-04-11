---
title: attribut msNPAllowDialin
description: Indique si le compte a l’autorisation de se connecter au serveur RAS.
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut msNPAllowDialin
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108078"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="a9791-104">attribut msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a9791-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="a9791-105">Indique si le compte a l’autorisation de se connecter au serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="a9791-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="a9791-106">Ne modifiez pas cette valeur directement.</span><span class="sxs-lookup"><span data-stu-id="a9791-106">Do not modify this value directly.</span></span> <span data-ttu-id="a9791-107">Utilisez la [fonction d’administration RAS](/windows/desktop/RRAS/ras-administration-functions) appropriée pour modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a9791-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="a9791-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-108">Entry</span></span> | <span data-ttu-id="a9791-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a9791-110">CN</span><span class="sxs-lookup"><span data-stu-id="a9791-110">CN</span></span>                | <span data-ttu-id="a9791-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a9791-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="a9791-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a9791-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a9791-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a9791-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="a9791-114">Taille</span><span class="sxs-lookup"><span data-stu-id="a9791-114">Size</span></span>              | <span data-ttu-id="a9791-115">4 octets</span><span class="sxs-lookup"><span data-stu-id="a9791-115">4 bytes</span></span>                              |
| <span data-ttu-id="a9791-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a9791-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a9791-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a9791-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a9791-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-118">Attribute-Id</span></span>      | <span data-ttu-id="a9791-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="a9791-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="a9791-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a9791-120">System-Id-Guid</span></span>    | <span data-ttu-id="a9791-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="a9791-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="a9791-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9791-122">Syntax</span></span>            | [<span data-ttu-id="a9791-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9791-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a9791-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a9791-124">Implementations</span></span>

-   [<span data-ttu-id="a9791-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9791-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9791-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9791-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9791-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9791-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9791-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9791-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9791-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9791-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9791-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9791-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9791-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9791-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a9791-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-132">Entry</span></span> | <span data-ttu-id="a9791-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-136">System-Only</span></span>            | <span data-ttu-id="a9791-137">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-137">False</span></span>                             |
| <span data-ttu-id="a9791-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-139">True</span></span>                              |
| <span data-ttu-id="a9791-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-140">Is Indexed</span></span>             | <span data-ttu-id="a9791-141">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-141">False</span></span>                             |
| <span data-ttu-id="a9791-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-142">In Global Catalog</span></span>      | <span data-ttu-id="a9791-143">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-143">False</span></span>                             |
| <span data-ttu-id="a9791-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-148">Search-Flags</span></span>           | <span data-ttu-id="a9791-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9791-149">0x00000000</span></span>                        |
| <span data-ttu-id="a9791-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-150">System-Flags</span></span>           | <span data-ttu-id="a9791-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-151">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-152">Classes used in</span></span>        | [<span data-ttu-id="a9791-153">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9791-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9791-154">Windows Server 2003</span></span>



| <span data-ttu-id="a9791-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-155">Entry</span></span> | <span data-ttu-id="a9791-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-159">System-Only</span></span>            | <span data-ttu-id="a9791-160">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-160">False</span></span>                             |
| <span data-ttu-id="a9791-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-162">True</span></span>                              |
| <span data-ttu-id="a9791-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-163">Is Indexed</span></span>             | <span data-ttu-id="a9791-164">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-164">False</span></span>                             |
| <span data-ttu-id="a9791-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-165">In Global Catalog</span></span>      | <span data-ttu-id="a9791-166">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-166">False</span></span>                             |
| <span data-ttu-id="a9791-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-171">Search-Flags</span></span>           | <span data-ttu-id="a9791-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9791-172">0x00000000</span></span>                        |
| <span data-ttu-id="a9791-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-173">System-Flags</span></span>           | <span data-ttu-id="a9791-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-174">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-175">Classes used in</span></span>        | [<span data-ttu-id="a9791-176">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9791-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9791-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9791-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-178">Entry</span></span> | <span data-ttu-id="a9791-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-182">System-Only</span></span>            | <span data-ttu-id="a9791-183">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-183">False</span></span>                             |
| <span data-ttu-id="a9791-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-185">True</span></span>                              |
| <span data-ttu-id="a9791-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-186">Is Indexed</span></span>             | <span data-ttu-id="a9791-187">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-187">False</span></span>                             |
| <span data-ttu-id="a9791-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-188">In Global Catalog</span></span>      | <span data-ttu-id="a9791-189">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-189">False</span></span>                             |
| <span data-ttu-id="a9791-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-194">Search-Flags</span></span>           | <span data-ttu-id="a9791-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9791-195">0x00000000</span></span>                        |
| <span data-ttu-id="a9791-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-196">System-Flags</span></span>           | <span data-ttu-id="a9791-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-197">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-198">Classes used in</span></span>        | [<span data-ttu-id="a9791-199">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9791-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9791-200">Windows Server 2008</span></span>



| <span data-ttu-id="a9791-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-201">Entry</span></span> | <span data-ttu-id="a9791-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-205">System-Only</span></span>            | <span data-ttu-id="a9791-206">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-206">False</span></span>                             |
| <span data-ttu-id="a9791-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-208">True</span></span>                              |
| <span data-ttu-id="a9791-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-209">Is Indexed</span></span>             | <span data-ttu-id="a9791-210">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-210">False</span></span>                             |
| <span data-ttu-id="a9791-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-211">In Global Catalog</span></span>      | <span data-ttu-id="a9791-212">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-212">False</span></span>                             |
| <span data-ttu-id="a9791-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-217">Search-Flags</span></span>           | <span data-ttu-id="a9791-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-218">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-219">System-Flags</span></span>           | <span data-ttu-id="a9791-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-220">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-221">Classes used in</span></span>        | [<span data-ttu-id="a9791-222">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9791-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9791-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9791-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-224">Entry</span></span> | <span data-ttu-id="a9791-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-228">System-Only</span></span>            | <span data-ttu-id="a9791-229">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-229">False</span></span>                             |
| <span data-ttu-id="a9791-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-231">True</span></span>                              |
| <span data-ttu-id="a9791-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-232">Is Indexed</span></span>             | <span data-ttu-id="a9791-233">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-233">False</span></span>                             |
| <span data-ttu-id="a9791-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-234">In Global Catalog</span></span>      | <span data-ttu-id="a9791-235">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-235">False</span></span>                             |
| <span data-ttu-id="a9791-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-240">Search-Flags</span></span>           | <span data-ttu-id="a9791-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-241">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-242">System-Flags</span></span>           | <span data-ttu-id="a9791-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-243">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-244">Classes used in</span></span>        | [<span data-ttu-id="a9791-245">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9791-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9791-246">Windows Server 2012</span></span>



| <span data-ttu-id="a9791-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="a9791-247">Entry</span></span> | <span data-ttu-id="a9791-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9791-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9791-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a9791-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9791-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9791-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9791-251">System-Only</span></span>            | <span data-ttu-id="a9791-252">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-252">False</span></span>                             |
| <span data-ttu-id="a9791-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a9791-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a9791-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="a9791-254">True</span></span>                              |
| <span data-ttu-id="a9791-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a9791-255">Is Indexed</span></span>             | <span data-ttu-id="a9791-256">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-256">False</span></span>                             |
| <span data-ttu-id="a9791-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a9791-257">In Global Catalog</span></span>      | <span data-ttu-id="a9791-258">Faux</span><span class="sxs-lookup"><span data-stu-id="a9791-258">False</span></span>                             |
| <span data-ttu-id="a9791-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a9791-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9791-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a9791-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9791-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9791-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9791-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9791-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9791-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-263">Search-Flags</span></span>           | <span data-ttu-id="a9791-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-264">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9791-265">System-Flags</span></span>           | <span data-ttu-id="a9791-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9791-266">0x00000010</span></span>                        |
| <span data-ttu-id="a9791-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a9791-267">Classes used in</span></span>        | [<span data-ttu-id="a9791-268">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a9791-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="a9791-269">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9791-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9791-270">Fonctions d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="a9791-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

