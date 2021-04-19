---
title: Attribut Account-Expires
description: Date d’expiration du compte.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Account-Expires
- Schéma AD de l’attribut AccountExpires dans
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514062"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="148b0-105">Attribut Account-Expires</span><span class="sxs-lookup"><span data-stu-id="148b0-105">Account-Expires attribute</span></span>

<span data-ttu-id="148b0-106">Date d’expiration du compte.</span><span class="sxs-lookup"><span data-stu-id="148b0-106">The date when the account expires.</span></span> <span data-ttu-id="148b0-107">Cette valeur représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="148b0-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="148b0-108">La valeur 0 ou 0x7FFFFFFFFFFFFFFF (9223372036854775807) indique que le compte n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="148b0-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="148b0-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-109">Entry</span></span> | <span data-ttu-id="148b0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="148b0-111">CN</span><span class="sxs-lookup"><span data-stu-id="148b0-111">CN</span></span>                | <span data-ttu-id="148b0-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="148b0-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="148b0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="148b0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="148b0-114">AccountExpires dans</span><span class="sxs-lookup"><span data-stu-id="148b0-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="148b0-115">Taille</span><span class="sxs-lookup"><span data-stu-id="148b0-115">Size</span></span>              | <span data-ttu-id="148b0-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="148b0-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="148b0-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="148b0-117">Update Privilege</span></span>  | <span data-ttu-id="148b0-118">L’administrateur de domaine définit cet attribut.</span><span class="sxs-lookup"><span data-stu-id="148b0-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="148b0-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="148b0-119">Update Frequency</span></span>  | <span data-ttu-id="148b0-120">Chaque fois que la date d’expiration précédente arrive à expiration et doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="148b0-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="148b0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-121">Attribute-Id</span></span>      | <span data-ttu-id="148b0-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="148b0-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="148b0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="148b0-123">System-Id-Guid</span></span>    | <span data-ttu-id="148b0-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="148b0-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="148b0-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="148b0-125">Syntax</span></span>            | [<span data-ttu-id="148b0-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="148b0-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="148b0-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="148b0-127">Implementations</span></span>

-   [<span data-ttu-id="148b0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="148b0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="148b0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="148b0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="148b0-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="148b0-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="148b0-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="148b0-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="148b0-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="148b0-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="148b0-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="148b0-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="148b0-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="148b0-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="148b0-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="148b0-135">Windows 2000 Server</span></span>



| <span data-ttu-id="148b0-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-136">Entry</span></span> | <span data-ttu-id="148b0-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-140">System-Only</span></span>            | <span data-ttu-id="148b0-141">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-141">False</span></span>                             |
| <span data-ttu-id="148b0-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-142">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-143">True</span></span>                              |
| <span data-ttu-id="148b0-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-144">Is Indexed</span></span>             | <span data-ttu-id="148b0-145">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-145">False</span></span>                             |
| <span data-ttu-id="148b0-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-146">In Global Catalog</span></span>      | <span data-ttu-id="148b0-147">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-147">False</span></span>                             |
| <span data-ttu-id="148b0-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-152">Search-Flags</span></span>           | <span data-ttu-id="148b0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-153">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-154">System-Flags</span></span>           | <span data-ttu-id="148b0-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-155">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-156">Classes used in</span></span>        | [<span data-ttu-id="148b0-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="148b0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="148b0-158">Windows Server 2003</span></span>



| <span data-ttu-id="148b0-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-159">Entry</span></span> | <span data-ttu-id="148b0-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-163">System-Only</span></span>            | <span data-ttu-id="148b0-164">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-164">False</span></span>                             |
| <span data-ttu-id="148b0-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-166">True</span></span>                              |
| <span data-ttu-id="148b0-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-167">Is Indexed</span></span>             | <span data-ttu-id="148b0-168">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-168">False</span></span>                             |
| <span data-ttu-id="148b0-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-169">In Global Catalog</span></span>      | <span data-ttu-id="148b0-170">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-170">False</span></span>                             |
| <span data-ttu-id="148b0-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-175">Search-Flags</span></span>           | <span data-ttu-id="148b0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-176">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-177">System-Flags</span></span>           | <span data-ttu-id="148b0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-178">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-179">Classes used in</span></span>        | [<span data-ttu-id="148b0-180">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="148b0-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="148b0-181">ADAM</span></span>



| <span data-ttu-id="148b0-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-182">Entry</span></span> | <span data-ttu-id="148b0-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="148b0-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="148b0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="148b0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-186">System-Only</span></span>            | <span data-ttu-id="148b0-187">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-187">False</span></span>                                                             |
| <span data-ttu-id="148b0-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-189">True</span></span>                                                              |
| <span data-ttu-id="148b0-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-190">Is Indexed</span></span>             | <span data-ttu-id="148b0-191">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-191">False</span></span>                                                             |
| <span data-ttu-id="148b0-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-192">In Global Catalog</span></span>      | <span data-ttu-id="148b0-193">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-193">False</span></span>                                                             |
| <span data-ttu-id="148b0-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="148b0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="148b0-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="148b0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-198">Search-Flags</span></span>           | <span data-ttu-id="148b0-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="148b0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-200">System-Flags</span></span>           | <span data-ttu-id="148b0-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="148b0-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-202">Classes used in</span></span>        | [<span data-ttu-id="148b0-203">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="148b0-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="148b0-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="148b0-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="148b0-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-205">Entry</span></span> | <span data-ttu-id="148b0-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-209">System-Only</span></span>            | <span data-ttu-id="148b0-210">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-210">False</span></span>                             |
| <span data-ttu-id="148b0-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-212">True</span></span>                              |
| <span data-ttu-id="148b0-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-213">Is Indexed</span></span>             | <span data-ttu-id="148b0-214">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-214">False</span></span>                             |
| <span data-ttu-id="148b0-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-215">In Global Catalog</span></span>      | <span data-ttu-id="148b0-216">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-216">False</span></span>                             |
| <span data-ttu-id="148b0-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-221">Search-Flags</span></span>           | <span data-ttu-id="148b0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-222">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-223">System-Flags</span></span>           | <span data-ttu-id="148b0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-224">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-225">Classes used in</span></span>        | [<span data-ttu-id="148b0-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="148b0-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="148b0-227">Windows Server 2008</span></span>



| <span data-ttu-id="148b0-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-228">Entry</span></span> | <span data-ttu-id="148b0-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-232">System-Only</span></span>            | <span data-ttu-id="148b0-233">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-233">False</span></span>                             |
| <span data-ttu-id="148b0-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-234">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-235">True</span></span>                              |
| <span data-ttu-id="148b0-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-236">Is Indexed</span></span>             | <span data-ttu-id="148b0-237">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-237">False</span></span>                             |
| <span data-ttu-id="148b0-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-238">In Global Catalog</span></span>      | <span data-ttu-id="148b0-239">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-239">False</span></span>                             |
| <span data-ttu-id="148b0-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-244">Search-Flags</span></span>           | <span data-ttu-id="148b0-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-245">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-246">System-Flags</span></span>           | <span data-ttu-id="148b0-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-247">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-248">Classes used in</span></span>        | [<span data-ttu-id="148b0-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="148b0-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="148b0-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="148b0-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-251">Entry</span></span> | <span data-ttu-id="148b0-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-255">System-Only</span></span>            | <span data-ttu-id="148b0-256">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-256">False</span></span>                             |
| <span data-ttu-id="148b0-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-257">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-258">True</span></span>                              |
| <span data-ttu-id="148b0-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-259">Is Indexed</span></span>             | <span data-ttu-id="148b0-260">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-260">False</span></span>                             |
| <span data-ttu-id="148b0-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-261">In Global Catalog</span></span>      | <span data-ttu-id="148b0-262">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-262">False</span></span>                             |
| <span data-ttu-id="148b0-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-267">Search-Flags</span></span>           | <span data-ttu-id="148b0-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-268">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-269">System-Flags</span></span>           | <span data-ttu-id="148b0-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-270">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-271">Classes used in</span></span>        | [<span data-ttu-id="148b0-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="148b0-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="148b0-273">Windows Server 2012</span></span>



| <span data-ttu-id="148b0-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="148b0-274">Entry</span></span> | <span data-ttu-id="148b0-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="148b0-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="148b0-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="148b0-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="148b0-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="148b0-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="148b0-278">System-Only</span></span>            | <span data-ttu-id="148b0-279">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-279">False</span></span>                             |
| <span data-ttu-id="148b0-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="148b0-280">Is-Single-Valued</span></span>       | <span data-ttu-id="148b0-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="148b0-281">True</span></span>                              |
| <span data-ttu-id="148b0-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="148b0-282">Is Indexed</span></span>             | <span data-ttu-id="148b0-283">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-283">False</span></span>                             |
| <span data-ttu-id="148b0-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="148b0-284">In Global Catalog</span></span>      | <span data-ttu-id="148b0-285">Faux</span><span class="sxs-lookup"><span data-stu-id="148b0-285">False</span></span>                             |
| <span data-ttu-id="148b0-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="148b0-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="148b0-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="148b0-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="148b0-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="148b0-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="148b0-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="148b0-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="148b0-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-290">Search-Flags</span></span>           | <span data-ttu-id="148b0-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-291">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="148b0-292">System-Flags</span></span>           | <span data-ttu-id="148b0-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="148b0-293">0x00000010</span></span>                        |
| <span data-ttu-id="148b0-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="148b0-294">Classes used in</span></span>        | [<span data-ttu-id="148b0-295">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="148b0-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="148b0-296">Notes</span><span class="sxs-lookup"><span data-stu-id="148b0-296">Remarks</span></span>

<span data-ttu-id="148b0-297">La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="148b0-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

