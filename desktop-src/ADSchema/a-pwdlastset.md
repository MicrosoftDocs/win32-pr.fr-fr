---
title: Pwd-Last-Set (attribut)
description: Date et heure de la dernière modification du mot de passe de ce compte.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-schéma Active Directory de l’attribut Last-Set
- Schéma AD de l’attribut pwdLastSet
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106512004"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="8dcc2-105">Pwd-Last-Set (attribut)</span><span class="sxs-lookup"><span data-stu-id="8dcc2-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="8dcc2-106">Date et heure de la dernière modification du mot de passe de ce compte.</span><span class="sxs-lookup"><span data-stu-id="8dcc2-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="8dcc2-107">Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de nanosecondes de 100 depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="8dcc2-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="8dcc2-108">Si cette valeur est définie sur 0 et que l’attribut [**User-Account-Control**](a-useraccountcontrol.md) ne contient pas l’indicateur de mot de passe uf ne pas faire **\_ \_ expirer \_** , l’utilisateur doit définir le mot de passe à la prochaine ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="8dcc2-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="8dcc2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-109">Entry</span></span> | <span data-ttu-id="8dcc2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8dcc2-111">CN</span><span class="sxs-lookup"><span data-stu-id="8dcc2-111">CN</span></span>                | <span data-ttu-id="8dcc2-112">Pwd-dernier jeu</span><span class="sxs-lookup"><span data-stu-id="8dcc2-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="8dcc2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8dcc2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8dcc2-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="8dcc2-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="8dcc2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="8dcc2-115">Size</span></span>              | <span data-ttu-id="8dcc2-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="8dcc2-116">8 bytes</span></span>                              |
| <span data-ttu-id="8dcc2-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8dcc2-117">Update Privilege</span></span>  | <span data-ttu-id="8dcc2-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="8dcc2-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="8dcc2-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8dcc2-119">Update Frequency</span></span>  | <span data-ttu-id="8dcc2-120">Chaque fois que le mot de passe est modifié.</span><span class="sxs-lookup"><span data-stu-id="8dcc2-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="8dcc2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-121">Attribute-Id</span></span>      | <span data-ttu-id="8dcc2-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="8dcc2-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="8dcc2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8dcc2-123">System-Id-Guid</span></span>    | <span data-ttu-id="8dcc2-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8dcc2-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8dcc2-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dcc2-125">Syntax</span></span>            | [<span data-ttu-id="8dcc2-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8dcc2-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8dcc2-127">Implementations</span></span>

-   [<span data-ttu-id="8dcc2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8dcc2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8dcc2-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8dcc2-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8dcc2-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8dcc2-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8dcc2-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8dcc2-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8dcc2-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8dcc2-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-136">Entry</span></span> | <span data-ttu-id="8dcc2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-140">System-Only</span></span>            | <span data-ttu-id="8dcc2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-141">False</span></span>                             |
| <span data-ttu-id="8dcc2-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-143">True</span></span>                              |
| <span data-ttu-id="8dcc2-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-144">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-145">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-145">False</span></span>                             |
| <span data-ttu-id="8dcc2-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-146">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-147">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-147">False</span></span>                             |
| <span data-ttu-id="8dcc2-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-152">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-153">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-154">System-Flags</span></span>           | <span data-ttu-id="8dcc2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-155">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-156">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8dcc2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8dcc2-158">Windows Server 2003</span></span>



| <span data-ttu-id="8dcc2-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-159">Entry</span></span> | <span data-ttu-id="8dcc2-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-163">System-Only</span></span>            | <span data-ttu-id="8dcc2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-164">False</span></span>                             |
| <span data-ttu-id="8dcc2-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-166">True</span></span>                              |
| <span data-ttu-id="8dcc2-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-167">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-168">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-168">False</span></span>                             |
| <span data-ttu-id="8dcc2-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-169">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-170">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-170">False</span></span>                             |
| <span data-ttu-id="8dcc2-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-175">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-176">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-177">System-Flags</span></span>           | <span data-ttu-id="8dcc2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-178">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-179">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-180">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8dcc2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="8dcc2-181">ADAM</span></span>



| <span data-ttu-id="8dcc2-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-182">Entry</span></span> | <span data-ttu-id="8dcc2-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8dcc2-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8dcc2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8dcc2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-186">System-Only</span></span>            | <span data-ttu-id="8dcc2-187">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-187">False</span></span>                                                             |
| <span data-ttu-id="8dcc2-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-189">True</span></span>                                                              |
| <span data-ttu-id="8dcc2-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-190">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-191">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-191">False</span></span>                                                             |
| <span data-ttu-id="8dcc2-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-192">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-193">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-193">False</span></span>                                                             |
| <span data-ttu-id="8dcc2-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8dcc2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8dcc2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8dcc2-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-198">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="8dcc2-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-200">System-Flags</span></span>           | <span data-ttu-id="8dcc2-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="8dcc2-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-202">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-203">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8dcc2-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc2-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8dcc2-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-205">Entry</span></span> | <span data-ttu-id="8dcc2-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-209">System-Only</span></span>            | <span data-ttu-id="8dcc2-210">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-210">False</span></span>                             |
| <span data-ttu-id="8dcc2-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-212">True</span></span>                              |
| <span data-ttu-id="8dcc2-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-213">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-214">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-214">False</span></span>                             |
| <span data-ttu-id="8dcc2-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-215">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-216">False</span></span>                             |
| <span data-ttu-id="8dcc2-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-221">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-222">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-223">System-Flags</span></span>           | <span data-ttu-id="8dcc2-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-224">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-225">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8dcc2-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dcc2-227">Windows Server 2008</span></span>



| <span data-ttu-id="8dcc2-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-228">Entry</span></span> | <span data-ttu-id="8dcc2-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-232">System-Only</span></span>            | <span data-ttu-id="8dcc2-233">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-233">False</span></span>                             |
| <span data-ttu-id="8dcc2-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-234">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-235">True</span></span>                              |
| <span data-ttu-id="8dcc2-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-236">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-237">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-237">False</span></span>                             |
| <span data-ttu-id="8dcc2-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-238">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-239">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-239">False</span></span>                             |
| <span data-ttu-id="8dcc2-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-244">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-245">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-246">System-Flags</span></span>           | <span data-ttu-id="8dcc2-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-247">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-248">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8dcc2-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc2-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8dcc2-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-251">Entry</span></span> | <span data-ttu-id="8dcc2-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-255">System-Only</span></span>            | <span data-ttu-id="8dcc2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-256">False</span></span>                             |
| <span data-ttu-id="8dcc2-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-257">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-258">True</span></span>                              |
| <span data-ttu-id="8dcc2-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-259">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-260">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-260">False</span></span>                             |
| <span data-ttu-id="8dcc2-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-261">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-262">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-262">False</span></span>                             |
| <span data-ttu-id="8dcc2-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-267">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-268">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-269">System-Flags</span></span>           | <span data-ttu-id="8dcc2-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-270">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-271">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8dcc2-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dcc2-273">Windows Server 2012</span></span>



| <span data-ttu-id="8dcc2-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="8dcc2-274">Entry</span></span> | <span data-ttu-id="8dcc2-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcc2-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8dcc2-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8dcc2-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dcc2-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8dcc2-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dcc2-278">System-Only</span></span>            | <span data-ttu-id="8dcc2-279">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-279">False</span></span>                             |
| <span data-ttu-id="8dcc2-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8dcc2-280">Is-Single-Valued</span></span>       | <span data-ttu-id="8dcc2-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="8dcc2-281">True</span></span>                              |
| <span data-ttu-id="8dcc2-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8dcc2-282">Is Indexed</span></span>             | <span data-ttu-id="8dcc2-283">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-283">False</span></span>                             |
| <span data-ttu-id="8dcc2-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8dcc2-284">In Global Catalog</span></span>      | <span data-ttu-id="8dcc2-285">Faux</span><span class="sxs-lookup"><span data-stu-id="8dcc2-285">False</span></span>                             |
| <span data-ttu-id="8dcc2-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8dcc2-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dcc2-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8dcc2-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8dcc2-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dcc2-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dcc2-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8dcc2-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-290">Search-Flags</span></span>           | <span data-ttu-id="8dcc2-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dcc2-291">0x00000000</span></span>                        |
| <span data-ttu-id="8dcc2-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dcc2-292">System-Flags</span></span>           | <span data-ttu-id="8dcc2-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dcc2-293">0x00000010</span></span>                        |
| <span data-ttu-id="8dcc2-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8dcc2-294">Classes used in</span></span>        | [<span data-ttu-id="8dcc2-295">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8dcc2-296">Notes</span><span class="sxs-lookup"><span data-stu-id="8dcc2-296">Remarks</span></span>

<span data-ttu-id="8dcc2-297">La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="8dcc2-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="8dcc2-298">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dcc2-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcc2-299">**Contrôle de compte d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8dcc2-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

