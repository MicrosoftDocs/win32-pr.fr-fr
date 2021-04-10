---
title: Attribut Last-Logon-timestamp
description: Il s’agit de l’heure de la dernière connexion de l’utilisateur au domaine.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Last-Logon-timestamp
- Schéma AD de l’attribut lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107239"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="25488-105">Attribut Last-Logon-timestamp</span><span class="sxs-lookup"><span data-stu-id="25488-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="25488-106">Il s’agit de l’heure de la dernière connexion de l’utilisateur au domaine.</span><span class="sxs-lookup"><span data-stu-id="25488-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="25488-107">Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="25488-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="25488-108">Chaque fois qu’un utilisateur ouvre une session, la valeur de cet attribut est lue à partir du DC.</span><span class="sxs-lookup"><span data-stu-id="25488-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="25488-109">Si la valeur est plus ancienne \[ `current_time - msDS-LogonTimeSyncInterval` \] , la valeur est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="25488-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="25488-110">La mise à jour initiale après l’augmentation du niveau fonctionnel du domaine est calculée comme suit : 14 jours moins un pourcentage aléatoire de 5 jours.</span><span class="sxs-lookup"><span data-stu-id="25488-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="25488-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-111">Entry</span></span> | <span data-ttu-id="25488-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25488-113">CN</span><span class="sxs-lookup"><span data-stu-id="25488-113">CN</span></span>                | <span data-ttu-id="25488-114">Last-Logon-timestamp</span><span class="sxs-lookup"><span data-stu-id="25488-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="25488-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="25488-115">Ldap-Display-Name</span></span> | <span data-ttu-id="25488-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="25488-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="25488-117">Taille</span><span class="sxs-lookup"><span data-stu-id="25488-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="25488-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="25488-118">Update Privilege</span></span>  | <span data-ttu-id="25488-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="25488-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="25488-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="25488-120">Update Frequency</span></span>  | <span data-ttu-id="25488-121">Lorsque l’utilisateur ouvre une session et si cette valeur est antérieure à l’heure actuelle moins la valeur de msDS-LogonTimeSyncInterval.</span><span class="sxs-lookup"><span data-stu-id="25488-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="25488-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="25488-122">Attribute-Id</span></span>      | <span data-ttu-id="25488-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="25488-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="25488-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="25488-124">System-Id-Guid</span></span>    | <span data-ttu-id="25488-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="25488-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="25488-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25488-126">Syntax</span></span>            | [<span data-ttu-id="25488-127">**Défini**</span><span class="sxs-lookup"><span data-stu-id="25488-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="25488-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="25488-128">Implementations</span></span>

-   [<span data-ttu-id="25488-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="25488-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="25488-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="25488-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="25488-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="25488-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="25488-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="25488-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="25488-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="25488-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="25488-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="25488-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="25488-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25488-135">Windows Server 2003</span></span>



| <span data-ttu-id="25488-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-136">Entry</span></span> | <span data-ttu-id="25488-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="25488-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-140">System-Only</span></span>            | <span data-ttu-id="25488-141">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-141">False</span></span>                             |
| <span data-ttu-id="25488-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-142">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-143">True</span></span>                              |
| <span data-ttu-id="25488-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-144">Is Indexed</span></span>             | <span data-ttu-id="25488-145">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-145">False</span></span>                             |
| <span data-ttu-id="25488-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-146">In Global Catalog</span></span>      | <span data-ttu-id="25488-147">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-147">False</span></span>                             |
| <span data-ttu-id="25488-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="25488-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="25488-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="25488-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-152">Search-Flags</span></span>           | <span data-ttu-id="25488-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25488-153">0x00000000</span></span>                        |
| <span data-ttu-id="25488-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-154">System-Flags</span></span>           | <span data-ttu-id="25488-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-155">0x00000010</span></span>                        |
| <span data-ttu-id="25488-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-156">Classes used in</span></span>        | [<span data-ttu-id="25488-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="25488-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="25488-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="25488-158">ADAM</span></span>



| <span data-ttu-id="25488-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-159">Entry</span></span> | <span data-ttu-id="25488-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="25488-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="25488-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="25488-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-163">System-Only</span></span>            | <span data-ttu-id="25488-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-164">True</span></span>                                                              |
| <span data-ttu-id="25488-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-165">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-166">True</span></span>                                                              |
| <span data-ttu-id="25488-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-167">Is Indexed</span></span>             | <span data-ttu-id="25488-168">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-168">False</span></span>                                                             |
| <span data-ttu-id="25488-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-169">In Global Catalog</span></span>      | <span data-ttu-id="25488-170">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-170">False</span></span>                                                             |
| <span data-ttu-id="25488-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="25488-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="25488-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="25488-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-175">Search-Flags</span></span>           | <span data-ttu-id="25488-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25488-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="25488-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-177">System-Flags</span></span>           | <span data-ttu-id="25488-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="25488-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-179">Classes used in</span></span>        | [<span data-ttu-id="25488-180">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="25488-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="25488-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="25488-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="25488-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-182">Entry</span></span> | <span data-ttu-id="25488-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="25488-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-186">System-Only</span></span>            | <span data-ttu-id="25488-187">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-187">False</span></span>                             |
| <span data-ttu-id="25488-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-188">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-189">True</span></span>                              |
| <span data-ttu-id="25488-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-190">Is Indexed</span></span>             | <span data-ttu-id="25488-191">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-191">False</span></span>                             |
| <span data-ttu-id="25488-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-192">In Global Catalog</span></span>      | <span data-ttu-id="25488-193">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-193">False</span></span>                             |
| <span data-ttu-id="25488-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="25488-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="25488-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="25488-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-198">Search-Flags</span></span>           | <span data-ttu-id="25488-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25488-199">0x00000000</span></span>                        |
| <span data-ttu-id="25488-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-200">System-Flags</span></span>           | <span data-ttu-id="25488-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-201">0x00000010</span></span>                        |
| <span data-ttu-id="25488-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-202">Classes used in</span></span>        | [<span data-ttu-id="25488-203">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="25488-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="25488-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25488-204">Windows Server 2008</span></span>



| <span data-ttu-id="25488-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-205">Entry</span></span> | <span data-ttu-id="25488-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="25488-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-209">System-Only</span></span>            | <span data-ttu-id="25488-210">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-210">False</span></span>                             |
| <span data-ttu-id="25488-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-211">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-212">True</span></span>                              |
| <span data-ttu-id="25488-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-213">Is Indexed</span></span>             | <span data-ttu-id="25488-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-214">True</span></span>                              |
| <span data-ttu-id="25488-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-215">In Global Catalog</span></span>      | <span data-ttu-id="25488-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-216">True</span></span>                              |
| <span data-ttu-id="25488-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="25488-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="25488-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="25488-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-221">Search-Flags</span></span>           | <span data-ttu-id="25488-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="25488-222">0x00000001</span></span>                        |
| <span data-ttu-id="25488-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-223">System-Flags</span></span>           | <span data-ttu-id="25488-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-224">0x00000010</span></span>                        |
| <span data-ttu-id="25488-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-225">Classes used in</span></span>        | [<span data-ttu-id="25488-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="25488-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="25488-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="25488-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="25488-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-228">Entry</span></span> | <span data-ttu-id="25488-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="25488-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-232">System-Only</span></span>            | <span data-ttu-id="25488-233">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-233">False</span></span>                             |
| <span data-ttu-id="25488-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-234">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-235">True</span></span>                              |
| <span data-ttu-id="25488-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-236">Is Indexed</span></span>             | <span data-ttu-id="25488-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-237">True</span></span>                              |
| <span data-ttu-id="25488-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-238">In Global Catalog</span></span>      | <span data-ttu-id="25488-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-239">True</span></span>                              |
| <span data-ttu-id="25488-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="25488-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="25488-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="25488-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-244">Search-Flags</span></span>           | <span data-ttu-id="25488-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="25488-245">0x00000001</span></span>                        |
| <span data-ttu-id="25488-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-246">System-Flags</span></span>           | <span data-ttu-id="25488-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-247">0x00000010</span></span>                        |
| <span data-ttu-id="25488-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-248">Classes used in</span></span>        | [<span data-ttu-id="25488-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="25488-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="25488-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25488-250">Windows Server 2012</span></span>



| <span data-ttu-id="25488-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="25488-251">Entry</span></span> | <span data-ttu-id="25488-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="25488-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="25488-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25488-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25488-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="25488-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="25488-255">System-Only</span></span>            | <span data-ttu-id="25488-256">Faux</span><span class="sxs-lookup"><span data-stu-id="25488-256">False</span></span>                             |
| <span data-ttu-id="25488-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25488-257">Is-Single-Valued</span></span>       | <span data-ttu-id="25488-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-258">True</span></span>                              |
| <span data-ttu-id="25488-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25488-259">Is Indexed</span></span>             | <span data-ttu-id="25488-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-260">True</span></span>                              |
| <span data-ttu-id="25488-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25488-261">In Global Catalog</span></span>      | <span data-ttu-id="25488-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="25488-262">True</span></span>                              |
| <span data-ttu-id="25488-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25488-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="25488-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25488-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="25488-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25488-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="25488-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25488-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="25488-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-267">Search-Flags</span></span>           | <span data-ttu-id="25488-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="25488-268">0x00000001</span></span>                        |
| <span data-ttu-id="25488-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25488-269">System-Flags</span></span>           | <span data-ttu-id="25488-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25488-270">0x00000010</span></span>                        |
| <span data-ttu-id="25488-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25488-271">Classes used in</span></span>        | [<span data-ttu-id="25488-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="25488-272">**User**</span></span>](c-user.md)<br/> |



 

 





