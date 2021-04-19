---
title: Attribut Max-Renew-Age
description: Cet attribut détermine le délai, en jours, pendant lequel le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être renouvelé à des fins d’authentification Kerberos. Le paramètre par défaut est de 7 jours dans le domaine par défaut stratégie de groupe objet (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Max-Renew-Age
- Schéma AD de l’attribut maxRenewAge
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514273"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="339ed-106">Attribut Max-Renew-Age</span><span class="sxs-lookup"><span data-stu-id="339ed-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="339ed-107">Cet attribut détermine le délai, en jours, pendant lequel le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être renouvelé à des fins d’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="339ed-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="339ed-108">Le paramètre par défaut est de 7 jours dans le domaine par défaut stratégie de groupe objet (GPO).</span><span class="sxs-lookup"><span data-stu-id="339ed-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="339ed-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-109">Entry</span></span> | <span data-ttu-id="339ed-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="339ed-111">CN</span><span class="sxs-lookup"><span data-stu-id="339ed-111">CN</span></span>                | <span data-ttu-id="339ed-112">Max-Renew-Age</span><span class="sxs-lookup"><span data-stu-id="339ed-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="339ed-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="339ed-113">Ldap-Display-Name</span></span> | <span data-ttu-id="339ed-114">maxRenewAge</span><span class="sxs-lookup"><span data-stu-id="339ed-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="339ed-115">Taille</span><span class="sxs-lookup"><span data-stu-id="339ed-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="339ed-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="339ed-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="339ed-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="339ed-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="339ed-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-118">Attribute-Id</span></span>      | <span data-ttu-id="339ed-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="339ed-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="339ed-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="339ed-120">System-Id-Guid</span></span>    | <span data-ttu-id="339ed-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="339ed-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="339ed-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="339ed-122">Syntax</span></span>            | [<span data-ttu-id="339ed-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="339ed-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="339ed-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="339ed-124">Implementations</span></span>

-   [<span data-ttu-id="339ed-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="339ed-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="339ed-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="339ed-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="339ed-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="339ed-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="339ed-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="339ed-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="339ed-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="339ed-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="339ed-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="339ed-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="339ed-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="339ed-131">Windows 2000 Server</span></span>



| <span data-ttu-id="339ed-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-132">Entry</span></span> | <span data-ttu-id="339ed-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-136">System-Only</span></span>            | <span data-ttu-id="339ed-137">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-137">False</span></span>                                              |
| <span data-ttu-id="339ed-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-138">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-139">True</span></span>                                               |
| <span data-ttu-id="339ed-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-140">Is Indexed</span></span>             | <span data-ttu-id="339ed-141">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-141">False</span></span>                                              |
| <span data-ttu-id="339ed-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-142">In Global Catalog</span></span>      | <span data-ttu-id="339ed-143">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-143">False</span></span>                                              |
| <span data-ttu-id="339ed-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-148">Search-Flags</span></span>           | <span data-ttu-id="339ed-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-149">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-150">System-Flags</span></span>           | <span data-ttu-id="339ed-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-151">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-152">Classes used in</span></span>        | [<span data-ttu-id="339ed-153">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="339ed-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="339ed-154">Windows Server 2003</span></span>



| <span data-ttu-id="339ed-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-155">Entry</span></span> | <span data-ttu-id="339ed-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-159">System-Only</span></span>            | <span data-ttu-id="339ed-160">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-160">False</span></span>                                              |
| <span data-ttu-id="339ed-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-161">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-162">True</span></span>                                               |
| <span data-ttu-id="339ed-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-163">Is Indexed</span></span>             | <span data-ttu-id="339ed-164">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-164">False</span></span>                                              |
| <span data-ttu-id="339ed-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-165">In Global Catalog</span></span>      | <span data-ttu-id="339ed-166">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-166">False</span></span>                                              |
| <span data-ttu-id="339ed-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-171">Search-Flags</span></span>           | <span data-ttu-id="339ed-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-172">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-173">System-Flags</span></span>           | <span data-ttu-id="339ed-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-174">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-175">Classes used in</span></span>        | [<span data-ttu-id="339ed-176">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="339ed-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="339ed-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="339ed-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-178">Entry</span></span> | <span data-ttu-id="339ed-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-182">System-Only</span></span>            | <span data-ttu-id="339ed-183">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-183">False</span></span>                                              |
| <span data-ttu-id="339ed-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-184">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-185">True</span></span>                                               |
| <span data-ttu-id="339ed-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-186">Is Indexed</span></span>             | <span data-ttu-id="339ed-187">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-187">False</span></span>                                              |
| <span data-ttu-id="339ed-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-188">In Global Catalog</span></span>      | <span data-ttu-id="339ed-189">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-189">False</span></span>                                              |
| <span data-ttu-id="339ed-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-194">Search-Flags</span></span>           | <span data-ttu-id="339ed-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-195">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-196">System-Flags</span></span>           | <span data-ttu-id="339ed-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-197">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-198">Classes used in</span></span>        | [<span data-ttu-id="339ed-199">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="339ed-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="339ed-200">Windows Server 2008</span></span>



| <span data-ttu-id="339ed-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-201">Entry</span></span> | <span data-ttu-id="339ed-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-205">System-Only</span></span>            | <span data-ttu-id="339ed-206">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-206">False</span></span>                                              |
| <span data-ttu-id="339ed-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-207">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-208">True</span></span>                                               |
| <span data-ttu-id="339ed-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-209">Is Indexed</span></span>             | <span data-ttu-id="339ed-210">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-210">False</span></span>                                              |
| <span data-ttu-id="339ed-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-211">In Global Catalog</span></span>      | <span data-ttu-id="339ed-212">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-212">False</span></span>                                              |
| <span data-ttu-id="339ed-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-217">Search-Flags</span></span>           | <span data-ttu-id="339ed-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-218">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-219">System-Flags</span></span>           | <span data-ttu-id="339ed-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-220">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-221">Classes used in</span></span>        | [<span data-ttu-id="339ed-222">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="339ed-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="339ed-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="339ed-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-224">Entry</span></span> | <span data-ttu-id="339ed-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-228">System-Only</span></span>            | <span data-ttu-id="339ed-229">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-229">False</span></span>                                              |
| <span data-ttu-id="339ed-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-230">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-231">True</span></span>                                               |
| <span data-ttu-id="339ed-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-232">Is Indexed</span></span>             | <span data-ttu-id="339ed-233">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-233">False</span></span>                                              |
| <span data-ttu-id="339ed-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-234">In Global Catalog</span></span>      | <span data-ttu-id="339ed-235">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-235">False</span></span>                                              |
| <span data-ttu-id="339ed-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-240">Search-Flags</span></span>           | <span data-ttu-id="339ed-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-241">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-242">System-Flags</span></span>           | <span data-ttu-id="339ed-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-243">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-244">Classes used in</span></span>        | [<span data-ttu-id="339ed-245">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="339ed-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="339ed-246">Windows Server 2012</span></span>



| <span data-ttu-id="339ed-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="339ed-247">Entry</span></span> | <span data-ttu-id="339ed-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="339ed-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="339ed-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="339ed-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="339ed-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="339ed-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="339ed-251">System-Only</span></span>            | <span data-ttu-id="339ed-252">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-252">False</span></span>                                              |
| <span data-ttu-id="339ed-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="339ed-253">Is-Single-Valued</span></span>       | <span data-ttu-id="339ed-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="339ed-254">True</span></span>                                               |
| <span data-ttu-id="339ed-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="339ed-255">Is Indexed</span></span>             | <span data-ttu-id="339ed-256">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-256">False</span></span>                                              |
| <span data-ttu-id="339ed-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="339ed-257">In Global Catalog</span></span>      | <span data-ttu-id="339ed-258">Faux</span><span class="sxs-lookup"><span data-stu-id="339ed-258">False</span></span>                                              |
| <span data-ttu-id="339ed-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="339ed-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="339ed-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="339ed-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="339ed-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="339ed-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="339ed-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="339ed-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-263">Search-Flags</span></span>           | <span data-ttu-id="339ed-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="339ed-264">0x00000000</span></span>                                         |
| <span data-ttu-id="339ed-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="339ed-265">System-Flags</span></span>           | <span data-ttu-id="339ed-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="339ed-266">0x00000010</span></span>                                         |
| <span data-ttu-id="339ed-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="339ed-267">Classes used in</span></span>        | [<span data-ttu-id="339ed-268">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="339ed-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





