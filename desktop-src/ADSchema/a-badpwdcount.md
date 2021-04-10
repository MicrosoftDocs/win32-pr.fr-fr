---
title: Attribut Bad-pwd-Count
description: Nombre de fois où l’utilisateur a tenté de se connecter au compte à l’aide d’un mot de passe incorrect.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Bad-pwd-Count
- Schéma AD de l’attribut badPwdCount
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107284"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="27d30-105">Attribut Bad-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="27d30-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="27d30-106">Nombre de fois où l’utilisateur a tenté de se connecter au compte à l’aide d’un mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="27d30-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="27d30-107">La valeur 0 indique que la valeur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="27d30-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="27d30-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-108">Entry</span></span> | <span data-ttu-id="27d30-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="27d30-110">CN</span><span class="sxs-lookup"><span data-stu-id="27d30-110">CN</span></span>                | <span data-ttu-id="27d30-111">Nombre de mot de passe incorrect</span><span class="sxs-lookup"><span data-stu-id="27d30-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="27d30-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27d30-112">Ldap-Display-Name</span></span> | <span data-ttu-id="27d30-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="27d30-113">badPwdCount</span></span>                               |
| <span data-ttu-id="27d30-114">Taille</span><span class="sxs-lookup"><span data-stu-id="27d30-114">Size</span></span>              | <span data-ttu-id="27d30-115">4 octets</span><span class="sxs-lookup"><span data-stu-id="27d30-115">4 bytes</span></span>                                   |
| <span data-ttu-id="27d30-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="27d30-116">Update Privilege</span></span>  | <span data-ttu-id="27d30-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="27d30-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="27d30-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="27d30-118">Update Frequency</span></span>  | <span data-ttu-id="27d30-119">Chaque fois que l’utilisateur entre un mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="27d30-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="27d30-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-120">Attribute-Id</span></span>      | <span data-ttu-id="27d30-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="27d30-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="27d30-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27d30-122">System-Id-Guid</span></span>    | <span data-ttu-id="27d30-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="27d30-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="27d30-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27d30-124">Syntax</span></span>            | [<span data-ttu-id="27d30-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="27d30-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="27d30-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="27d30-126">Implementations</span></span>

-   [<span data-ttu-id="27d30-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27d30-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27d30-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27d30-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27d30-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="27d30-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="27d30-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27d30-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27d30-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27d30-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27d30-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27d30-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27d30-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27d30-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27d30-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27d30-134">Windows 2000 Server</span></span>



| <span data-ttu-id="27d30-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-135">Entry</span></span> | <span data-ttu-id="27d30-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-139">System-Only</span></span>            | <span data-ttu-id="27d30-140">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-140">False</span></span>                             |
| <span data-ttu-id="27d30-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-141">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-142">True</span></span>                              |
| <span data-ttu-id="27d30-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-143">Is Indexed</span></span>             | <span data-ttu-id="27d30-144">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-144">False</span></span>                             |
| <span data-ttu-id="27d30-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-145">In Global Catalog</span></span>      | <span data-ttu-id="27d30-146">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-146">False</span></span>                             |
| <span data-ttu-id="27d30-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-151">Search-Flags</span></span>           | <span data-ttu-id="27d30-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-152">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-153">System-Flags</span></span>           | <span data-ttu-id="27d30-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-154">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-155">Classes used in</span></span>        | [<span data-ttu-id="27d30-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27d30-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27d30-157">Windows Server 2003</span></span>



| <span data-ttu-id="27d30-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-158">Entry</span></span> | <span data-ttu-id="27d30-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-162">System-Only</span></span>            | <span data-ttu-id="27d30-163">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-163">False</span></span>                             |
| <span data-ttu-id="27d30-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-164">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-165">True</span></span>                              |
| <span data-ttu-id="27d30-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-166">Is Indexed</span></span>             | <span data-ttu-id="27d30-167">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-167">False</span></span>                             |
| <span data-ttu-id="27d30-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-168">In Global Catalog</span></span>      | <span data-ttu-id="27d30-169">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-169">False</span></span>                             |
| <span data-ttu-id="27d30-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-174">Search-Flags</span></span>           | <span data-ttu-id="27d30-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-175">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-176">System-Flags</span></span>           | <span data-ttu-id="27d30-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-177">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-178">Classes used in</span></span>        | [<span data-ttu-id="27d30-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="27d30-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="27d30-180">ADAM</span></span>



| <span data-ttu-id="27d30-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-181">Entry</span></span> | <span data-ttu-id="27d30-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="27d30-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="27d30-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="27d30-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-185">System-Only</span></span>            | <span data-ttu-id="27d30-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-186">True</span></span>                                                              |
| <span data-ttu-id="27d30-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-187">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-188">True</span></span>                                                              |
| <span data-ttu-id="27d30-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-189">Is Indexed</span></span>             | <span data-ttu-id="27d30-190">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-190">False</span></span>                                                             |
| <span data-ttu-id="27d30-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-191">In Global Catalog</span></span>      | <span data-ttu-id="27d30-192">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-192">False</span></span>                                                             |
| <span data-ttu-id="27d30-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="27d30-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="27d30-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="27d30-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-197">Search-Flags</span></span>           | <span data-ttu-id="27d30-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="27d30-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-199">System-Flags</span></span>           | <span data-ttu-id="27d30-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="27d30-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-201">Classes used in</span></span>        | [<span data-ttu-id="27d30-202">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="27d30-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27d30-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27d30-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27d30-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-204">Entry</span></span> | <span data-ttu-id="27d30-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-208">System-Only</span></span>            | <span data-ttu-id="27d30-209">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-209">False</span></span>                             |
| <span data-ttu-id="27d30-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-210">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-211">True</span></span>                              |
| <span data-ttu-id="27d30-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-212">Is Indexed</span></span>             | <span data-ttu-id="27d30-213">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-213">False</span></span>                             |
| <span data-ttu-id="27d30-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-214">In Global Catalog</span></span>      | <span data-ttu-id="27d30-215">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-215">False</span></span>                             |
| <span data-ttu-id="27d30-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-220">Search-Flags</span></span>           | <span data-ttu-id="27d30-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-221">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-222">System-Flags</span></span>           | <span data-ttu-id="27d30-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-223">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-224">Classes used in</span></span>        | [<span data-ttu-id="27d30-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27d30-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27d30-226">Windows Server 2008</span></span>



| <span data-ttu-id="27d30-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-227">Entry</span></span> | <span data-ttu-id="27d30-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-231">System-Only</span></span>            | <span data-ttu-id="27d30-232">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-232">False</span></span>                             |
| <span data-ttu-id="27d30-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-233">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-234">True</span></span>                              |
| <span data-ttu-id="27d30-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-235">Is Indexed</span></span>             | <span data-ttu-id="27d30-236">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-236">False</span></span>                             |
| <span data-ttu-id="27d30-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-237">In Global Catalog</span></span>      | <span data-ttu-id="27d30-238">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-238">False</span></span>                             |
| <span data-ttu-id="27d30-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-243">Search-Flags</span></span>           | <span data-ttu-id="27d30-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-244">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-245">System-Flags</span></span>           | <span data-ttu-id="27d30-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-246">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-247">Classes used in</span></span>        | [<span data-ttu-id="27d30-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27d30-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27d30-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27d30-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-250">Entry</span></span> | <span data-ttu-id="27d30-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-254">System-Only</span></span>            | <span data-ttu-id="27d30-255">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-255">False</span></span>                             |
| <span data-ttu-id="27d30-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-256">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-257">True</span></span>                              |
| <span data-ttu-id="27d30-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-258">Is Indexed</span></span>             | <span data-ttu-id="27d30-259">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-259">False</span></span>                             |
| <span data-ttu-id="27d30-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-260">In Global Catalog</span></span>      | <span data-ttu-id="27d30-261">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-261">False</span></span>                             |
| <span data-ttu-id="27d30-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-266">Search-Flags</span></span>           | <span data-ttu-id="27d30-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-267">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-268">System-Flags</span></span>           | <span data-ttu-id="27d30-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-269">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-270">Classes used in</span></span>        | [<span data-ttu-id="27d30-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27d30-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27d30-272">Windows Server 2012</span></span>



| <span data-ttu-id="27d30-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="27d30-273">Entry</span></span> | <span data-ttu-id="27d30-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="27d30-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27d30-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="27d30-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d30-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27d30-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d30-277">System-Only</span></span>            | <span data-ttu-id="27d30-278">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-278">False</span></span>                             |
| <span data-ttu-id="27d30-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="27d30-279">Is-Single-Valued</span></span>       | <span data-ttu-id="27d30-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="27d30-280">True</span></span>                              |
| <span data-ttu-id="27d30-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="27d30-281">Is Indexed</span></span>             | <span data-ttu-id="27d30-282">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-282">False</span></span>                             |
| <span data-ttu-id="27d30-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="27d30-283">In Global Catalog</span></span>      | <span data-ttu-id="27d30-284">Faux</span><span class="sxs-lookup"><span data-stu-id="27d30-284">False</span></span>                             |
| <span data-ttu-id="27d30-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="27d30-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d30-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="27d30-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27d30-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d30-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27d30-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d30-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27d30-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-289">Search-Flags</span></span>           | <span data-ttu-id="27d30-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d30-290">0x00000000</span></span>                        |
| <span data-ttu-id="27d30-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d30-291">System-Flags</span></span>           | <span data-ttu-id="27d30-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="27d30-292">0x00000011</span></span>                        |
| <span data-ttu-id="27d30-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="27d30-293">Classes used in</span></span>        | [<span data-ttu-id="27d30-294">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="27d30-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="27d30-295">Notes</span><span class="sxs-lookup"><span data-stu-id="27d30-295">Remarks</span></span>

<span data-ttu-id="27d30-296">Cet attribut n’est pas répliqué et est conservé séparément sur chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="27d30-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="27d30-297">Cet attribut est réinitialisé sur un contrôleur de domaine spécifique lorsque l’utilisateur parvient à se connecter à ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="27d30-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





