---
title: Attribut d’heure de mot de passe incorrect
description: Date et heure de la dernière tentative d’ouverture de session sur ce compte avec un mot de passe non valide.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de mot de passe incorrect
- Schéma AD de l’attribut badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480469"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="40d96-105">Attribut d’heure de mot de passe incorrect</span><span class="sxs-lookup"><span data-stu-id="40d96-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="40d96-106">Date et heure de la dernière tentative d’ouverture de session sur ce compte avec un mot de passe non valide.</span><span class="sxs-lookup"><span data-stu-id="40d96-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="40d96-107">Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="40d96-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="40d96-108">La valeur zéro signifie que la dernière fois qu’un mot de passe incorrect a été utilisé est inconnu.</span><span class="sxs-lookup"><span data-stu-id="40d96-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="40d96-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-109">Entry</span></span> | <span data-ttu-id="40d96-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="40d96-111">CN</span><span class="sxs-lookup"><span data-stu-id="40d96-111">CN</span></span>                | <span data-ttu-id="40d96-112">Mot de passe incorrect</span><span class="sxs-lookup"><span data-stu-id="40d96-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="40d96-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="40d96-113">Ldap-Display-Name</span></span> | <span data-ttu-id="40d96-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="40d96-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="40d96-115">Taille</span><span class="sxs-lookup"><span data-stu-id="40d96-115">Size</span></span>              | <span data-ttu-id="40d96-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="40d96-116">8 bytes</span></span>                                   |
| <span data-ttu-id="40d96-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="40d96-117">Update Privilege</span></span>  | <span data-ttu-id="40d96-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="40d96-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="40d96-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="40d96-119">Update Frequency</span></span>  | <span data-ttu-id="40d96-120">Chaque fois que l’utilisateur entre un mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="40d96-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="40d96-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-121">Attribute-Id</span></span>      | <span data-ttu-id="40d96-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="40d96-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="40d96-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="40d96-123">System-Id-Guid</span></span>    | <span data-ttu-id="40d96-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="40d96-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="40d96-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40d96-125">Syntax</span></span>            | [<span data-ttu-id="40d96-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="40d96-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="40d96-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="40d96-127">Implementations</span></span>

-   [<span data-ttu-id="40d96-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="40d96-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="40d96-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="40d96-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="40d96-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="40d96-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="40d96-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="40d96-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="40d96-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="40d96-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="40d96-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="40d96-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="40d96-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="40d96-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="40d96-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40d96-135">Windows 2000 Server</span></span>



| <span data-ttu-id="40d96-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-136">Entry</span></span> | <span data-ttu-id="40d96-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-140">System-Only</span></span>            | <span data-ttu-id="40d96-141">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-141">False</span></span>                             |
| <span data-ttu-id="40d96-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-142">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-143">True</span></span>                              |
| <span data-ttu-id="40d96-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-144">Is Indexed</span></span>             | <span data-ttu-id="40d96-145">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-145">False</span></span>                             |
| <span data-ttu-id="40d96-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-146">In Global Catalog</span></span>      | <span data-ttu-id="40d96-147">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-147">False</span></span>                             |
| <span data-ttu-id="40d96-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-152">Search-Flags</span></span>           | <span data-ttu-id="40d96-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-153">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-154">System-Flags</span></span>           | <span data-ttu-id="40d96-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-155">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-156">Classes used in</span></span>        | [<span data-ttu-id="40d96-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="40d96-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40d96-158">Windows Server 2003</span></span>



| <span data-ttu-id="40d96-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-159">Entry</span></span> | <span data-ttu-id="40d96-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-163">System-Only</span></span>            | <span data-ttu-id="40d96-164">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-164">False</span></span>                             |
| <span data-ttu-id="40d96-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-165">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-166">True</span></span>                              |
| <span data-ttu-id="40d96-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-167">Is Indexed</span></span>             | <span data-ttu-id="40d96-168">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-168">False</span></span>                             |
| <span data-ttu-id="40d96-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-169">In Global Catalog</span></span>      | <span data-ttu-id="40d96-170">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-170">False</span></span>                             |
| <span data-ttu-id="40d96-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-175">Search-Flags</span></span>           | <span data-ttu-id="40d96-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-176">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-177">System-Flags</span></span>           | <span data-ttu-id="40d96-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-178">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-179">Classes used in</span></span>        | [<span data-ttu-id="40d96-180">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="40d96-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="40d96-181">ADAM</span></span>



| <span data-ttu-id="40d96-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-182">Entry</span></span> | <span data-ttu-id="40d96-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="40d96-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="40d96-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="40d96-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-186">System-Only</span></span>            | <span data-ttu-id="40d96-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-187">True</span></span>                                                              |
| <span data-ttu-id="40d96-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-188">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-189">True</span></span>                                                              |
| <span data-ttu-id="40d96-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-190">Is Indexed</span></span>             | <span data-ttu-id="40d96-191">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-191">False</span></span>                                                             |
| <span data-ttu-id="40d96-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-192">In Global Catalog</span></span>      | <span data-ttu-id="40d96-193">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-193">False</span></span>                                                             |
| <span data-ttu-id="40d96-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="40d96-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="40d96-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="40d96-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-198">Search-Flags</span></span>           | <span data-ttu-id="40d96-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="40d96-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-200">System-Flags</span></span>           | <span data-ttu-id="40d96-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="40d96-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-202">Classes used in</span></span>        | [<span data-ttu-id="40d96-203">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="40d96-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="40d96-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="40d96-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="40d96-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-205">Entry</span></span> | <span data-ttu-id="40d96-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-209">System-Only</span></span>            | <span data-ttu-id="40d96-210">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-210">False</span></span>                             |
| <span data-ttu-id="40d96-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-211">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-212">True</span></span>                              |
| <span data-ttu-id="40d96-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-213">Is Indexed</span></span>             | <span data-ttu-id="40d96-214">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-214">False</span></span>                             |
| <span data-ttu-id="40d96-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-215">In Global Catalog</span></span>      | <span data-ttu-id="40d96-216">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-216">False</span></span>                             |
| <span data-ttu-id="40d96-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-221">Search-Flags</span></span>           | <span data-ttu-id="40d96-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-222">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-223">System-Flags</span></span>           | <span data-ttu-id="40d96-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-224">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-225">Classes used in</span></span>        | [<span data-ttu-id="40d96-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="40d96-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40d96-227">Windows Server 2008</span></span>



| <span data-ttu-id="40d96-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-228">Entry</span></span> | <span data-ttu-id="40d96-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-232">System-Only</span></span>            | <span data-ttu-id="40d96-233">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-233">False</span></span>                             |
| <span data-ttu-id="40d96-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-234">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-235">True</span></span>                              |
| <span data-ttu-id="40d96-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-236">Is Indexed</span></span>             | <span data-ttu-id="40d96-237">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-237">False</span></span>                             |
| <span data-ttu-id="40d96-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-238">In Global Catalog</span></span>      | <span data-ttu-id="40d96-239">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-239">False</span></span>                             |
| <span data-ttu-id="40d96-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-244">Search-Flags</span></span>           | <span data-ttu-id="40d96-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-245">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-246">System-Flags</span></span>           | <span data-ttu-id="40d96-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-247">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-248">Classes used in</span></span>        | [<span data-ttu-id="40d96-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="40d96-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40d96-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="40d96-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-251">Entry</span></span> | <span data-ttu-id="40d96-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-255">System-Only</span></span>            | <span data-ttu-id="40d96-256">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-256">False</span></span>                             |
| <span data-ttu-id="40d96-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-257">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-258">True</span></span>                              |
| <span data-ttu-id="40d96-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-259">Is Indexed</span></span>             | <span data-ttu-id="40d96-260">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-260">False</span></span>                             |
| <span data-ttu-id="40d96-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-261">In Global Catalog</span></span>      | <span data-ttu-id="40d96-262">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-262">False</span></span>                             |
| <span data-ttu-id="40d96-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-267">Search-Flags</span></span>           | <span data-ttu-id="40d96-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-268">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-269">System-Flags</span></span>           | <span data-ttu-id="40d96-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-270">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-271">Classes used in</span></span>        | [<span data-ttu-id="40d96-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="40d96-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40d96-273">Windows Server 2012</span></span>



| <span data-ttu-id="40d96-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="40d96-274">Entry</span></span> | <span data-ttu-id="40d96-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d96-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40d96-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="40d96-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40d96-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40d96-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="40d96-278">System-Only</span></span>            | <span data-ttu-id="40d96-279">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-279">False</span></span>                             |
| <span data-ttu-id="40d96-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="40d96-280">Is-Single-Valued</span></span>       | <span data-ttu-id="40d96-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="40d96-281">True</span></span>                              |
| <span data-ttu-id="40d96-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="40d96-282">Is Indexed</span></span>             | <span data-ttu-id="40d96-283">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-283">False</span></span>                             |
| <span data-ttu-id="40d96-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="40d96-284">In Global Catalog</span></span>      | <span data-ttu-id="40d96-285">Faux</span><span class="sxs-lookup"><span data-stu-id="40d96-285">False</span></span>                             |
| <span data-ttu-id="40d96-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="40d96-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="40d96-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="40d96-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40d96-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40d96-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40d96-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40d96-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40d96-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-290">Search-Flags</span></span>           | <span data-ttu-id="40d96-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d96-291">0x00000000</span></span>                        |
| <span data-ttu-id="40d96-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40d96-292">System-Flags</span></span>           | <span data-ttu-id="40d96-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="40d96-293">0x00000011</span></span>                        |
| <span data-ttu-id="40d96-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="40d96-294">Classes used in</span></span>        | [<span data-ttu-id="40d96-295">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40d96-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="40d96-296">Notes</span><span class="sxs-lookup"><span data-stu-id="40d96-296">Remarks</span></span>

<span data-ttu-id="40d96-297">La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="40d96-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="40d96-298">Cet attribut n’est pas répliqué et est conservé séparément sur chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="40d96-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="40d96-299">Pour obtenir une valeur précise pour le dernier mot de passe incorrect de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé.</span><span class="sxs-lookup"><span data-stu-id="40d96-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="40d96-300">La valeur la plus élevée obtenue représente l’heure réelle du mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="40d96-300">The largest value that is obtained represents the true bad password time.</span></span>

 

