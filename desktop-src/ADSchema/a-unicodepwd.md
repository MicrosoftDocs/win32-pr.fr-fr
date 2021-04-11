---
title: Attribut Unicode-Pwd
description: Mot de passe de l’utilisateur dans le format à sens unique Windows NT (OWF). Windows 2000 utilise Windows NT OWF. Cette propriété est utilisée uniquement par le système d’exploitation. Notez que vous ne pouvez pas dériver le mot de passe en clair à partir de la forme OWF du mot de passe.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Unicode-Pwd
- attribut unicodePwd schéma AD
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107930"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="f6290-108">Attribut Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="f6290-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="f6290-109">Mot de passe de l’utilisateur dans le format à sens unique Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="f6290-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="f6290-110">Windows 2000 utilise Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="f6290-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="f6290-111">Cette propriété est utilisée uniquement par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f6290-111">This property is used only by the operating system.</span></span> <span data-ttu-id="f6290-112">Notez que vous ne pouvez pas dériver le mot de passe en clair à partir de la forme OWF du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f6290-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="f6290-113">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-113">Entry</span></span> | <span data-ttu-id="f6290-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f6290-115">CN</span><span class="sxs-lookup"><span data-stu-id="f6290-115">CN</span></span>                | <span data-ttu-id="f6290-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="f6290-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="f6290-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f6290-117">Ldap-Display-Name</span></span> | <span data-ttu-id="f6290-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="f6290-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="f6290-119">Taille</span><span class="sxs-lookup"><span data-stu-id="f6290-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="f6290-120">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f6290-120">Update Privilege</span></span>  | <span data-ttu-id="f6290-121">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="f6290-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="f6290-122">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f6290-122">Update Frequency</span></span>  | <span data-ttu-id="f6290-123">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le mot de passe doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="f6290-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="f6290-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-124">Attribute-Id</span></span>      | <span data-ttu-id="f6290-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="f6290-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="f6290-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f6290-126">System-Id-Guid</span></span>    | <span data-ttu-id="f6290-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f6290-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="f6290-128">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6290-128">Syntax</span></span>            | [<span data-ttu-id="f6290-129">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f6290-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="f6290-130">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f6290-130">Implementations</span></span>

-   [<span data-ttu-id="f6290-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f6290-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f6290-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6290-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6290-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f6290-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f6290-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6290-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6290-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6290-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6290-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6290-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6290-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6290-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f6290-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6290-138">Windows 2000 Server</span></span>



| <span data-ttu-id="f6290-139">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-139">Entry</span></span> | <span data-ttu-id="f6290-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-141">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-143">System-Only</span></span>            | <span data-ttu-id="f6290-144">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-144">False</span></span>                             |
| <span data-ttu-id="f6290-145">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-145">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-146">True</span></span>                              |
| <span data-ttu-id="f6290-147">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-147">Is Indexed</span></span>             | <span data-ttu-id="f6290-148">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-148">False</span></span>                             |
| <span data-ttu-id="f6290-149">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-149">In Global Catalog</span></span>      | <span data-ttu-id="f6290-150">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-150">False</span></span>                             |
| <span data-ttu-id="f6290-151">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-152">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-155">Search-Flags</span></span>           | <span data-ttu-id="f6290-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-156">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-157">System-Flags</span></span>           | <span data-ttu-id="f6290-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-158">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-159">Classes used in</span></span>        | [<span data-ttu-id="f6290-160">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f6290-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6290-161">Windows Server 2003</span></span>



| <span data-ttu-id="f6290-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-162">Entry</span></span> | <span data-ttu-id="f6290-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-166">System-Only</span></span>            | <span data-ttu-id="f6290-167">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-167">False</span></span>                             |
| <span data-ttu-id="f6290-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-168">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-169">True</span></span>                              |
| <span data-ttu-id="f6290-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-170">Is Indexed</span></span>             | <span data-ttu-id="f6290-171">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-171">False</span></span>                             |
| <span data-ttu-id="f6290-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-172">In Global Catalog</span></span>      | <span data-ttu-id="f6290-173">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-173">False</span></span>                             |
| <span data-ttu-id="f6290-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-178">Search-Flags</span></span>           | <span data-ttu-id="f6290-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-179">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-180">System-Flags</span></span>           | <span data-ttu-id="f6290-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-181">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-182">Classes used in</span></span>        | [<span data-ttu-id="f6290-183">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f6290-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="f6290-184">ADAM</span></span>



| <span data-ttu-id="f6290-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-185">Entry</span></span> | <span data-ttu-id="f6290-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f6290-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f6290-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f6290-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-189">System-Only</span></span>            | <span data-ttu-id="f6290-190">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-190">False</span></span>                                                             |
| <span data-ttu-id="f6290-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-192">True</span></span>                                                              |
| <span data-ttu-id="f6290-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-193">Is Indexed</span></span>             | <span data-ttu-id="f6290-194">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-194">False</span></span>                                                             |
| <span data-ttu-id="f6290-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-195">In Global Catalog</span></span>      | <span data-ttu-id="f6290-196">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-196">False</span></span>                                                             |
| <span data-ttu-id="f6290-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f6290-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f6290-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f6290-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-201">Search-Flags</span></span>           | <span data-ttu-id="f6290-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="f6290-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-203">System-Flags</span></span>           | <span data-ttu-id="f6290-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="f6290-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-205">Classes used in</span></span>        | [<span data-ttu-id="f6290-206">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="f6290-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6290-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6290-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6290-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-208">Entry</span></span> | <span data-ttu-id="f6290-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-212">System-Only</span></span>            | <span data-ttu-id="f6290-213">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-213">False</span></span>                             |
| <span data-ttu-id="f6290-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-215">True</span></span>                              |
| <span data-ttu-id="f6290-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-216">Is Indexed</span></span>             | <span data-ttu-id="f6290-217">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-217">False</span></span>                             |
| <span data-ttu-id="f6290-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-218">In Global Catalog</span></span>      | <span data-ttu-id="f6290-219">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-219">False</span></span>                             |
| <span data-ttu-id="f6290-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-224">Search-Flags</span></span>           | <span data-ttu-id="f6290-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-225">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-226">System-Flags</span></span>           | <span data-ttu-id="f6290-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-227">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-228">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-228">Classes used in</span></span>        | [<span data-ttu-id="f6290-229">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6290-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6290-230">Windows Server 2008</span></span>



| <span data-ttu-id="f6290-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-231">Entry</span></span> | <span data-ttu-id="f6290-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-235">System-Only</span></span>            | <span data-ttu-id="f6290-236">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-236">False</span></span>                             |
| <span data-ttu-id="f6290-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-237">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-238">True</span></span>                              |
| <span data-ttu-id="f6290-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-239">Is Indexed</span></span>             | <span data-ttu-id="f6290-240">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-240">False</span></span>                             |
| <span data-ttu-id="f6290-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-241">In Global Catalog</span></span>      | <span data-ttu-id="f6290-242">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-242">False</span></span>                             |
| <span data-ttu-id="f6290-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-247">Search-Flags</span></span>           | <span data-ttu-id="f6290-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-248">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-249">System-Flags</span></span>           | <span data-ttu-id="f6290-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-250">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-251">Classes used in</span></span>        | [<span data-ttu-id="f6290-252">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6290-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6290-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6290-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-254">Entry</span></span> | <span data-ttu-id="f6290-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-258">System-Only</span></span>            | <span data-ttu-id="f6290-259">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-259">False</span></span>                             |
| <span data-ttu-id="f6290-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-260">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-261">True</span></span>                              |
| <span data-ttu-id="f6290-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-262">Is Indexed</span></span>             | <span data-ttu-id="f6290-263">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-263">False</span></span>                             |
| <span data-ttu-id="f6290-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-264">In Global Catalog</span></span>      | <span data-ttu-id="f6290-265">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-265">False</span></span>                             |
| <span data-ttu-id="f6290-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-270">Search-Flags</span></span>           | <span data-ttu-id="f6290-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-271">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-272">System-Flags</span></span>           | <span data-ttu-id="f6290-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-273">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-274">Classes used in</span></span>        | [<span data-ttu-id="f6290-275">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6290-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6290-276">Windows Server 2012</span></span>



| <span data-ttu-id="f6290-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6290-277">Entry</span></span> | <span data-ttu-id="f6290-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6290-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f6290-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6290-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6290-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f6290-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6290-281">System-Only</span></span>            | <span data-ttu-id="f6290-282">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-282">False</span></span>                             |
| <span data-ttu-id="f6290-283">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6290-283">Is-Single-Valued</span></span>       | <span data-ttu-id="f6290-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6290-284">True</span></span>                              |
| <span data-ttu-id="f6290-285">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6290-285">Is Indexed</span></span>             | <span data-ttu-id="f6290-286">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-286">False</span></span>                             |
| <span data-ttu-id="f6290-287">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6290-287">In Global Catalog</span></span>      | <span data-ttu-id="f6290-288">Faux</span><span class="sxs-lookup"><span data-stu-id="f6290-288">False</span></span>                             |
| <span data-ttu-id="f6290-289">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6290-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6290-290">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6290-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f6290-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6290-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f6290-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6290-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f6290-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-293">Search-Flags</span></span>           | <span data-ttu-id="f6290-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6290-294">0x00000000</span></span>                        |
| <span data-ttu-id="f6290-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6290-295">System-Flags</span></span>           | <span data-ttu-id="f6290-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6290-296">0x00000010</span></span>                        |
| <span data-ttu-id="f6290-297">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6290-297">Classes used in</span></span>        | [<span data-ttu-id="f6290-298">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f6290-298">**User**</span></span>](c-user.md)<br/> |



 

 





