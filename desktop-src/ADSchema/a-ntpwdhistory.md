---
title: Attribut NT-pwd-History
description: Historique du mot de passe de l’utilisateur dans le format à sens unique Windows NT (OWF). Windows 2000 utilise Windows NT OWF.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut NT-pwd-History
- Schéma AD de l’attribut ntPwdHistory
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520065"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="88d4d-106">Attribut NT-pwd-History</span><span class="sxs-lookup"><span data-stu-id="88d4d-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="88d4d-107">Historique du mot de passe de l’utilisateur dans le format à sens unique Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="88d4d-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="88d4d-108">Windows 2000 utilise Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="88d4d-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="88d4d-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-109">Entry</span></span> | <span data-ttu-id="88d4d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="88d4d-111">CN</span><span class="sxs-lookup"><span data-stu-id="88d4d-111">CN</span></span>                | <span data-ttu-id="88d4d-112">NT-pwd-historique</span><span class="sxs-lookup"><span data-stu-id="88d4d-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="88d4d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88d4d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="88d4d-114">ntPwdHistory</span><span class="sxs-lookup"><span data-stu-id="88d4d-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="88d4d-115">Taille</span><span class="sxs-lookup"><span data-stu-id="88d4d-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="88d4d-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="88d4d-116">Update Privilege</span></span>  | <span data-ttu-id="88d4d-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="88d4d-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="88d4d-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="88d4d-118">Update Frequency</span></span>  | <span data-ttu-id="88d4d-119">Chaque fois que l’utilisateur modifie les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="88d4d-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="88d4d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-120">Attribute-Id</span></span>      | <span data-ttu-id="88d4d-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="88d4d-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="88d4d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88d4d-122">System-Id-Guid</span></span>    | <span data-ttu-id="88d4d-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="88d4d-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="88d4d-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88d4d-124">Syntax</span></span>            | [<span data-ttu-id="88d4d-125">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="88d4d-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="88d4d-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="88d4d-126">Implementations</span></span>

-   [<span data-ttu-id="88d4d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="88d4d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="88d4d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88d4d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88d4d-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="88d4d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="88d4d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88d4d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88d4d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88d4d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88d4d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88d4d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88d4d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88d4d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="88d4d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88d4d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="88d4d-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-135">Entry</span></span> | <span data-ttu-id="88d4d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-139">System-Only</span></span>            | <span data-ttu-id="88d4d-140">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-140">False</span></span>                             |
| <span data-ttu-id="88d4d-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-142">False</span></span>                             |
| <span data-ttu-id="88d4d-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-143">Is Indexed</span></span>             | <span data-ttu-id="88d4d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-144">False</span></span>                             |
| <span data-ttu-id="88d4d-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-145">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-146">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-146">False</span></span>                             |
| <span data-ttu-id="88d4d-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-151">Search-Flags</span></span>           | <span data-ttu-id="88d4d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-152">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-153">System-Flags</span></span>           | <span data-ttu-id="88d4d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-154">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-155">Classes used in</span></span>        | [<span data-ttu-id="88d4d-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="88d4d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88d4d-157">Windows Server 2003</span></span>



| <span data-ttu-id="88d4d-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-158">Entry</span></span> | <span data-ttu-id="88d4d-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-162">System-Only</span></span>            | <span data-ttu-id="88d4d-163">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-163">False</span></span>                             |
| <span data-ttu-id="88d4d-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-165">False</span></span>                             |
| <span data-ttu-id="88d4d-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-166">Is Indexed</span></span>             | <span data-ttu-id="88d4d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-167">False</span></span>                             |
| <span data-ttu-id="88d4d-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-168">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-169">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-169">False</span></span>                             |
| <span data-ttu-id="88d4d-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-174">Search-Flags</span></span>           | <span data-ttu-id="88d4d-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-175">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-176">System-Flags</span></span>           | <span data-ttu-id="88d4d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-177">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-178">Classes used in</span></span>        | [<span data-ttu-id="88d4d-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="88d4d-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="88d4d-180">ADAM</span></span>



| <span data-ttu-id="88d4d-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-181">Entry</span></span> | <span data-ttu-id="88d4d-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="88d4d-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="88d4d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="88d4d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-185">System-Only</span></span>            | <span data-ttu-id="88d4d-186">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-186">False</span></span>                                                             |
| <span data-ttu-id="88d4d-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-188">False</span></span>                                                             |
| <span data-ttu-id="88d4d-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-189">Is Indexed</span></span>             | <span data-ttu-id="88d4d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-190">False</span></span>                                                             |
| <span data-ttu-id="88d4d-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-191">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-192">False</span></span>                                                             |
| <span data-ttu-id="88d4d-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="88d4d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="88d4d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="88d4d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-197">Search-Flags</span></span>           | <span data-ttu-id="88d4d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="88d4d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-199">System-Flags</span></span>           | <span data-ttu-id="88d4d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="88d4d-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-201">Classes used in</span></span>        | [<span data-ttu-id="88d4d-202">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="88d4d-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88d4d-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88d4d-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88d4d-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-204">Entry</span></span> | <span data-ttu-id="88d4d-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-208">System-Only</span></span>            | <span data-ttu-id="88d4d-209">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-209">False</span></span>                             |
| <span data-ttu-id="88d4d-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-210">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-211">False</span></span>                             |
| <span data-ttu-id="88d4d-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-212">Is Indexed</span></span>             | <span data-ttu-id="88d4d-213">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-213">False</span></span>                             |
| <span data-ttu-id="88d4d-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-214">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-215">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-215">False</span></span>                             |
| <span data-ttu-id="88d4d-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-220">Search-Flags</span></span>           | <span data-ttu-id="88d4d-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-221">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-222">System-Flags</span></span>           | <span data-ttu-id="88d4d-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-223">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-224">Classes used in</span></span>        | [<span data-ttu-id="88d4d-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88d4d-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88d4d-226">Windows Server 2008</span></span>



| <span data-ttu-id="88d4d-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-227">Entry</span></span> | <span data-ttu-id="88d4d-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-231">System-Only</span></span>            | <span data-ttu-id="88d4d-232">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-232">False</span></span>                             |
| <span data-ttu-id="88d4d-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-234">False</span></span>                             |
| <span data-ttu-id="88d4d-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-235">Is Indexed</span></span>             | <span data-ttu-id="88d4d-236">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-236">False</span></span>                             |
| <span data-ttu-id="88d4d-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-237">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-238">False</span></span>                             |
| <span data-ttu-id="88d4d-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-243">Search-Flags</span></span>           | <span data-ttu-id="88d4d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-244">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-245">System-Flags</span></span>           | <span data-ttu-id="88d4d-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-246">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-247">Classes used in</span></span>        | [<span data-ttu-id="88d4d-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88d4d-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88d4d-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88d4d-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-250">Entry</span></span> | <span data-ttu-id="88d4d-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-254">System-Only</span></span>            | <span data-ttu-id="88d4d-255">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-255">False</span></span>                             |
| <span data-ttu-id="88d4d-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-256">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-257">False</span></span>                             |
| <span data-ttu-id="88d4d-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-258">Is Indexed</span></span>             | <span data-ttu-id="88d4d-259">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-259">False</span></span>                             |
| <span data-ttu-id="88d4d-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-260">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-261">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-261">False</span></span>                             |
| <span data-ttu-id="88d4d-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-266">Search-Flags</span></span>           | <span data-ttu-id="88d4d-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-267">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-268">System-Flags</span></span>           | <span data-ttu-id="88d4d-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-269">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-270">Classes used in</span></span>        | [<span data-ttu-id="88d4d-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88d4d-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88d4d-272">Windows Server 2012</span></span>



| <span data-ttu-id="88d4d-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="88d4d-273">Entry</span></span> | <span data-ttu-id="88d4d-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d4d-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="88d4d-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88d4d-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88d4d-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="88d4d-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="88d4d-277">System-Only</span></span>            | <span data-ttu-id="88d4d-278">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-278">False</span></span>                             |
| <span data-ttu-id="88d4d-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88d4d-279">Is-Single-Valued</span></span>       | <span data-ttu-id="88d4d-280">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-280">False</span></span>                             |
| <span data-ttu-id="88d4d-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88d4d-281">Is Indexed</span></span>             | <span data-ttu-id="88d4d-282">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-282">False</span></span>                             |
| <span data-ttu-id="88d4d-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88d4d-283">In Global Catalog</span></span>      | <span data-ttu-id="88d4d-284">Faux</span><span class="sxs-lookup"><span data-stu-id="88d4d-284">False</span></span>                             |
| <span data-ttu-id="88d4d-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88d4d-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="88d4d-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88d4d-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="88d4d-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88d4d-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="88d4d-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88d4d-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="88d4d-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-289">Search-Flags</span></span>           | <span data-ttu-id="88d4d-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88d4d-290">0x00000000</span></span>                        |
| <span data-ttu-id="88d4d-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88d4d-291">System-Flags</span></span>           | <span data-ttu-id="88d4d-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88d4d-292">0x00000010</span></span>                        |
| <span data-ttu-id="88d4d-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88d4d-293">Classes used in</span></span>        | [<span data-ttu-id="88d4d-294">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="88d4d-294">**User**</span></span>](c-user.md)<br/> |



 

 





