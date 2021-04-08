---
title: Attribut Code-Page
description: Spécifie la page de codes pour la langue choisie par l’utilisateur. Cette valeur n’est pas utilisée par Windows 2000.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Code-Page
- Schéma Active Directory d’attribut codePage
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744404"
---
# <a name="code-page-attribute"></a><span data-ttu-id="7f004-106">Attribut Code-Page</span><span class="sxs-lookup"><span data-stu-id="7f004-106">Code-Page attribute</span></span>

<span data-ttu-id="7f004-107">Spécifie la page de codes pour la langue choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f004-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="7f004-108">Cette valeur n’est pas utilisée par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f004-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="7f004-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-109">Entry</span></span> | <span data-ttu-id="7f004-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7f004-111">CN</span><span class="sxs-lookup"><span data-stu-id="7f004-111">CN</span></span>                | <span data-ttu-id="7f004-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="7f004-112">Code-Page</span></span>                                             |
| <span data-ttu-id="7f004-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7f004-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7f004-114">Courante</span><span class="sxs-lookup"><span data-stu-id="7f004-114">codePage</span></span>                                              |
| <span data-ttu-id="7f004-115">Taille</span><span class="sxs-lookup"><span data-stu-id="7f004-115">Size</span></span>              | <span data-ttu-id="7f004-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="7f004-116">4 bytes</span></span>                                               |
| <span data-ttu-id="7f004-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7f004-117">Update Privilege</span></span>  | <span data-ttu-id="7f004-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="7f004-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="7f004-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7f004-119">Update Frequency</span></span>  | <span data-ttu-id="7f004-120">Lorsque l’utilisateur souhaite modifier la langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f004-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="7f004-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-121">Attribute-Id</span></span>      | <span data-ttu-id="7f004-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="7f004-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="7f004-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7f004-123">System-Id-Guid</span></span>    | <span data-ttu-id="7f004-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7f004-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="7f004-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f004-125">Syntax</span></span>            | [<span data-ttu-id="7f004-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="7f004-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="7f004-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7f004-127">Implementations</span></span>

-   [<span data-ttu-id="7f004-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f004-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f004-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f004-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f004-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f004-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f004-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f004-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f004-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f004-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f004-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f004-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f004-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f004-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7f004-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-135">Entry</span></span> | <span data-ttu-id="7f004-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-139">System-Only</span></span>            | <span data-ttu-id="7f004-140">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-140">False</span></span>                             |
| <span data-ttu-id="7f004-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-142">True</span></span>                              |
| <span data-ttu-id="7f004-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-143">Is Indexed</span></span>             | <span data-ttu-id="7f004-144">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-144">False</span></span>                             |
| <span data-ttu-id="7f004-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-145">In Global Catalog</span></span>      | <span data-ttu-id="7f004-146">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-146">False</span></span>                             |
| <span data-ttu-id="7f004-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f004-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f004-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-151">Search-Flags</span></span>           | <span data-ttu-id="7f004-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-152">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-153">System-Flags</span></span>           | <span data-ttu-id="7f004-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-154">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-155">Classes used in</span></span>        | [<span data-ttu-id="7f004-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f004-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f004-157">Windows Server 2003</span></span>



| <span data-ttu-id="7f004-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-158">Entry</span></span> | <span data-ttu-id="7f004-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-162">System-Only</span></span>            | <span data-ttu-id="7f004-163">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-163">False</span></span>                             |
| <span data-ttu-id="7f004-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-165">True</span></span>                              |
| <span data-ttu-id="7f004-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-166">Is Indexed</span></span>             | <span data-ttu-id="7f004-167">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-167">False</span></span>                             |
| <span data-ttu-id="7f004-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-168">In Global Catalog</span></span>      | <span data-ttu-id="7f004-169">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-169">False</span></span>                             |
| <span data-ttu-id="7f004-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-172">Range-Lower</span></span>            | <span data-ttu-id="7f004-173">0</span><span class="sxs-lookup"><span data-stu-id="7f004-173">0</span></span>                                 |
| <span data-ttu-id="7f004-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-174">Range-Upper</span></span>            | <span data-ttu-id="7f004-175">65535</span><span class="sxs-lookup"><span data-stu-id="7f004-175">65535</span></span>                             |
| <span data-ttu-id="7f004-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-176">Search-Flags</span></span>           | <span data-ttu-id="7f004-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-177">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-178">System-Flags</span></span>           | <span data-ttu-id="7f004-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-179">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-180">Classes used in</span></span>        | [<span data-ttu-id="7f004-181">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f004-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f004-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f004-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-183">Entry</span></span> | <span data-ttu-id="7f004-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-187">System-Only</span></span>            | <span data-ttu-id="7f004-188">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-188">False</span></span>                             |
| <span data-ttu-id="7f004-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-190">True</span></span>                              |
| <span data-ttu-id="7f004-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-191">Is Indexed</span></span>             | <span data-ttu-id="7f004-192">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-192">False</span></span>                             |
| <span data-ttu-id="7f004-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-193">In Global Catalog</span></span>      | <span data-ttu-id="7f004-194">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-194">False</span></span>                             |
| <span data-ttu-id="7f004-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-197">Range-Lower</span></span>            | <span data-ttu-id="7f004-198">0</span><span class="sxs-lookup"><span data-stu-id="7f004-198">0</span></span>                                 |
| <span data-ttu-id="7f004-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-199">Range-Upper</span></span>            | <span data-ttu-id="7f004-200">65535</span><span class="sxs-lookup"><span data-stu-id="7f004-200">65535</span></span>                             |
| <span data-ttu-id="7f004-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-201">Search-Flags</span></span>           | <span data-ttu-id="7f004-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-202">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-203">System-Flags</span></span>           | <span data-ttu-id="7f004-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-204">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-205">Classes used in</span></span>        | [<span data-ttu-id="7f004-206">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f004-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f004-207">Windows Server 2008</span></span>



| <span data-ttu-id="7f004-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-208">Entry</span></span> | <span data-ttu-id="7f004-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-212">System-Only</span></span>            | <span data-ttu-id="7f004-213">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-213">False</span></span>                             |
| <span data-ttu-id="7f004-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-214">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-215">True</span></span>                              |
| <span data-ttu-id="7f004-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-216">Is Indexed</span></span>             | <span data-ttu-id="7f004-217">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-217">False</span></span>                             |
| <span data-ttu-id="7f004-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-218">In Global Catalog</span></span>      | <span data-ttu-id="7f004-219">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-219">False</span></span>                             |
| <span data-ttu-id="7f004-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-222">Range-Lower</span></span>            | <span data-ttu-id="7f004-223">0</span><span class="sxs-lookup"><span data-stu-id="7f004-223">0</span></span>                                 |
| <span data-ttu-id="7f004-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-224">Range-Upper</span></span>            | <span data-ttu-id="7f004-225">65535</span><span class="sxs-lookup"><span data-stu-id="7f004-225">65535</span></span>                             |
| <span data-ttu-id="7f004-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-226">Search-Flags</span></span>           | <span data-ttu-id="7f004-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-227">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-228">System-Flags</span></span>           | <span data-ttu-id="7f004-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-229">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-230">Classes used in</span></span>        | [<span data-ttu-id="7f004-231">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f004-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f004-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f004-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-233">Entry</span></span> | <span data-ttu-id="7f004-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-237">System-Only</span></span>            | <span data-ttu-id="7f004-238">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-238">False</span></span>                             |
| <span data-ttu-id="7f004-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-239">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-240">True</span></span>                              |
| <span data-ttu-id="7f004-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-241">Is Indexed</span></span>             | <span data-ttu-id="7f004-242">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-242">False</span></span>                             |
| <span data-ttu-id="7f004-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-243">In Global Catalog</span></span>      | <span data-ttu-id="7f004-244">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-244">False</span></span>                             |
| <span data-ttu-id="7f004-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-247">Range-Lower</span></span>            | <span data-ttu-id="7f004-248">0</span><span class="sxs-lookup"><span data-stu-id="7f004-248">0</span></span>                                 |
| <span data-ttu-id="7f004-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-249">Range-Upper</span></span>            | <span data-ttu-id="7f004-250">65535</span><span class="sxs-lookup"><span data-stu-id="7f004-250">65535</span></span>                             |
| <span data-ttu-id="7f004-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-251">Search-Flags</span></span>           | <span data-ttu-id="7f004-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-252">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-253">System-Flags</span></span>           | <span data-ttu-id="7f004-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-254">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-255">Classes used in</span></span>        | [<span data-ttu-id="7f004-256">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f004-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f004-257">Windows Server 2012</span></span>



| <span data-ttu-id="7f004-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f004-258">Entry</span></span> | <span data-ttu-id="7f004-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f004-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f004-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f004-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f004-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f004-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f004-262">System-Only</span></span>            | <span data-ttu-id="7f004-263">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-263">False</span></span>                             |
| <span data-ttu-id="7f004-264">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f004-264">Is-Single-Valued</span></span>       | <span data-ttu-id="7f004-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f004-265">True</span></span>                              |
| <span data-ttu-id="7f004-266">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f004-266">Is Indexed</span></span>             | <span data-ttu-id="7f004-267">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-267">False</span></span>                             |
| <span data-ttu-id="7f004-268">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f004-268">In Global Catalog</span></span>      | <span data-ttu-id="7f004-269">Faux</span><span class="sxs-lookup"><span data-stu-id="7f004-269">False</span></span>                             |
| <span data-ttu-id="7f004-270">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f004-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f004-271">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f004-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f004-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f004-272">Range-Lower</span></span>            | <span data-ttu-id="7f004-273">0</span><span class="sxs-lookup"><span data-stu-id="7f004-273">0</span></span>                                 |
| <span data-ttu-id="7f004-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f004-274">Range-Upper</span></span>            | <span data-ttu-id="7f004-275">65535</span><span class="sxs-lookup"><span data-stu-id="7f004-275">65535</span></span>                             |
| <span data-ttu-id="7f004-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-276">Search-Flags</span></span>           | <span data-ttu-id="7f004-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-277">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f004-278">System-Flags</span></span>           | <span data-ttu-id="7f004-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f004-279">0x00000010</span></span>                        |
| <span data-ttu-id="7f004-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f004-280">Classes used in</span></span>        | [<span data-ttu-id="7f004-281">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7f004-281">**User**</span></span>](c-user.md)<br/> |



 

 





