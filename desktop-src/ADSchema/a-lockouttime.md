---
title: Attribut Lockout-Time
description: Date et heure (UTC) de verrouillage du compte.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Lockout-Time
- Schéma Active Directory de l’attribut lockoutTime
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514886"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="15f07-105">Attribut Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="15f07-105">Lockout-Time attribute</span></span>

<span data-ttu-id="15f07-106">Date et heure (UTC) de verrouillage du compte. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="15f07-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="15f07-107">La valeur zéro signifie que le compte n’est pas actuellement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="15f07-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="15f07-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-108">Entry</span></span> | <span data-ttu-id="15f07-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15f07-110">CN</span><span class="sxs-lookup"><span data-stu-id="15f07-110">CN</span></span>                | <span data-ttu-id="15f07-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="15f07-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="15f07-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="15f07-112">Ldap-Display-Name</span></span> | <span data-ttu-id="15f07-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="15f07-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="15f07-114">Taille</span><span class="sxs-lookup"><span data-stu-id="15f07-114">Size</span></span>              | <span data-ttu-id="15f07-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="15f07-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="15f07-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="15f07-116">Update Privilege</span></span>  | <span data-ttu-id="15f07-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="15f07-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="15f07-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="15f07-118">Update Frequency</span></span>  | <span data-ttu-id="15f07-119">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le temps de verrouillage doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="15f07-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="15f07-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-120">Attribute-Id</span></span>      | <span data-ttu-id="15f07-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="15f07-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="15f07-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="15f07-122">System-Id-Guid</span></span>    | <span data-ttu-id="15f07-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="15f07-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="15f07-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f07-124">Syntax</span></span>            | [<span data-ttu-id="15f07-125">**Défini**</span><span class="sxs-lookup"><span data-stu-id="15f07-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="15f07-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="15f07-126">Implementations</span></span>

-   [<span data-ttu-id="15f07-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="15f07-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="15f07-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15f07-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15f07-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="15f07-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="15f07-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15f07-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15f07-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15f07-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15f07-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15f07-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15f07-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15f07-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="15f07-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15f07-134">Windows 2000 Server</span></span>



| <span data-ttu-id="15f07-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-135">Entry</span></span> | <span data-ttu-id="15f07-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-139">System-Only</span></span>            | <span data-ttu-id="15f07-140">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-140">False</span></span>                             |
| <span data-ttu-id="15f07-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-141">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-142">True</span></span>                              |
| <span data-ttu-id="15f07-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-143">Is Indexed</span></span>             | <span data-ttu-id="15f07-144">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-144">False</span></span>                             |
| <span data-ttu-id="15f07-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-145">In Global Catalog</span></span>      | <span data-ttu-id="15f07-146">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-146">False</span></span>                             |
| <span data-ttu-id="15f07-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-151">Search-Flags</span></span>           | <span data-ttu-id="15f07-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-152">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-153">System-Flags</span></span>           | <span data-ttu-id="15f07-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-154">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-155">Classes used in</span></span>        | [<span data-ttu-id="15f07-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="15f07-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15f07-157">Windows Server 2003</span></span>



| <span data-ttu-id="15f07-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-158">Entry</span></span> | <span data-ttu-id="15f07-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-162">System-Only</span></span>            | <span data-ttu-id="15f07-163">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-163">False</span></span>                             |
| <span data-ttu-id="15f07-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-164">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-165">True</span></span>                              |
| <span data-ttu-id="15f07-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-166">Is Indexed</span></span>             | <span data-ttu-id="15f07-167">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-167">False</span></span>                             |
| <span data-ttu-id="15f07-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-168">In Global Catalog</span></span>      | <span data-ttu-id="15f07-169">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-169">False</span></span>                             |
| <span data-ttu-id="15f07-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-174">Search-Flags</span></span>           | <span data-ttu-id="15f07-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-175">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-176">System-Flags</span></span>           | <span data-ttu-id="15f07-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-177">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-178">Classes used in</span></span>        | [<span data-ttu-id="15f07-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="15f07-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="15f07-180">ADAM</span></span>



| <span data-ttu-id="15f07-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-181">Entry</span></span> | <span data-ttu-id="15f07-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="15f07-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="15f07-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="15f07-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-185">System-Only</span></span>            | <span data-ttu-id="15f07-186">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-186">False</span></span>                                                             |
| <span data-ttu-id="15f07-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-187">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-188">True</span></span>                                                              |
| <span data-ttu-id="15f07-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-189">Is Indexed</span></span>             | <span data-ttu-id="15f07-190">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-190">False</span></span>                                                             |
| <span data-ttu-id="15f07-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-191">In Global Catalog</span></span>      | <span data-ttu-id="15f07-192">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-192">False</span></span>                                                             |
| <span data-ttu-id="15f07-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="15f07-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="15f07-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="15f07-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-197">Search-Flags</span></span>           | <span data-ttu-id="15f07-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="15f07-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-199">System-Flags</span></span>           | <span data-ttu-id="15f07-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="15f07-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-201">Classes used in</span></span>        | [<span data-ttu-id="15f07-202">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="15f07-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15f07-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15f07-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15f07-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-204">Entry</span></span> | <span data-ttu-id="15f07-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-208">System-Only</span></span>            | <span data-ttu-id="15f07-209">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-209">False</span></span>                             |
| <span data-ttu-id="15f07-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-210">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-211">True</span></span>                              |
| <span data-ttu-id="15f07-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-212">Is Indexed</span></span>             | <span data-ttu-id="15f07-213">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-213">False</span></span>                             |
| <span data-ttu-id="15f07-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-214">In Global Catalog</span></span>      | <span data-ttu-id="15f07-215">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-215">False</span></span>                             |
| <span data-ttu-id="15f07-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-220">Search-Flags</span></span>           | <span data-ttu-id="15f07-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-221">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-222">System-Flags</span></span>           | <span data-ttu-id="15f07-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-223">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-224">Classes used in</span></span>        | [<span data-ttu-id="15f07-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15f07-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15f07-226">Windows Server 2008</span></span>



| <span data-ttu-id="15f07-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-227">Entry</span></span> | <span data-ttu-id="15f07-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-231">System-Only</span></span>            | <span data-ttu-id="15f07-232">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-232">False</span></span>                             |
| <span data-ttu-id="15f07-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-233">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-234">True</span></span>                              |
| <span data-ttu-id="15f07-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-235">Is Indexed</span></span>             | <span data-ttu-id="15f07-236">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-236">False</span></span>                             |
| <span data-ttu-id="15f07-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-237">In Global Catalog</span></span>      | <span data-ttu-id="15f07-238">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-238">False</span></span>                             |
| <span data-ttu-id="15f07-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-243">Search-Flags</span></span>           | <span data-ttu-id="15f07-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-244">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-245">System-Flags</span></span>           | <span data-ttu-id="15f07-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-246">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-247">Classes used in</span></span>        | [<span data-ttu-id="15f07-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15f07-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15f07-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15f07-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-250">Entry</span></span> | <span data-ttu-id="15f07-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-254">System-Only</span></span>            | <span data-ttu-id="15f07-255">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-255">False</span></span>                             |
| <span data-ttu-id="15f07-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-256">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-257">True</span></span>                              |
| <span data-ttu-id="15f07-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-258">Is Indexed</span></span>             | <span data-ttu-id="15f07-259">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-259">False</span></span>                             |
| <span data-ttu-id="15f07-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-260">In Global Catalog</span></span>      | <span data-ttu-id="15f07-261">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-261">False</span></span>                             |
| <span data-ttu-id="15f07-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-266">Search-Flags</span></span>           | <span data-ttu-id="15f07-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-267">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-268">System-Flags</span></span>           | <span data-ttu-id="15f07-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-269">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-270">Classes used in</span></span>        | [<span data-ttu-id="15f07-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15f07-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f07-272">Windows Server 2012</span></span>



| <span data-ttu-id="15f07-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="15f07-273">Entry</span></span> | <span data-ttu-id="15f07-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f07-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="15f07-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="15f07-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15f07-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="15f07-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="15f07-277">System-Only</span></span>            | <span data-ttu-id="15f07-278">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-278">False</span></span>                             |
| <span data-ttu-id="15f07-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="15f07-279">Is-Single-Valued</span></span>       | <span data-ttu-id="15f07-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="15f07-280">True</span></span>                              |
| <span data-ttu-id="15f07-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="15f07-281">Is Indexed</span></span>             | <span data-ttu-id="15f07-282">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-282">False</span></span>                             |
| <span data-ttu-id="15f07-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="15f07-283">In Global Catalog</span></span>      | <span data-ttu-id="15f07-284">Faux</span><span class="sxs-lookup"><span data-stu-id="15f07-284">False</span></span>                             |
| <span data-ttu-id="15f07-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="15f07-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="15f07-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="15f07-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="15f07-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15f07-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="15f07-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15f07-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="15f07-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-289">Search-Flags</span></span>           | <span data-ttu-id="15f07-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15f07-290">0x00000000</span></span>                        |
| <span data-ttu-id="15f07-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15f07-291">System-Flags</span></span>           | <span data-ttu-id="15f07-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15f07-292">0x00000010</span></span>                        |
| <span data-ttu-id="15f07-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="15f07-293">Classes used in</span></span>        | [<span data-ttu-id="15f07-294">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="15f07-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="15f07-295">Notes</span><span class="sxs-lookup"><span data-stu-id="15f07-295">Remarks</span></span>

<span data-ttu-id="15f07-296">La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="15f07-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="15f07-297">Cette valeur d’attribut est réinitialisée uniquement lorsque le compte est correctement connecté.</span><span class="sxs-lookup"><span data-stu-id="15f07-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="15f07-298">Cela signifie que cette valeur peut être différente de zéro, mais que le compte n’est pas verrouillé. Pour déterminer avec précision si le compte est verrouillé, vous devez ajouter la [**durée de verrouillage**](a-lockoutduration.md) à cette heure et comparer le résultat à l’heure actuelle, en tenant compte des fuseaux horaires et de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="15f07-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="15f07-299">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f07-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f07-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="15f07-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="15f07-301">**Verrouillage-durée**</span><span class="sxs-lookup"><span data-stu-id="15f07-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

