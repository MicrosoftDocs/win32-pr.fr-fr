---
title: Attribut Max-ticket-Age
description: Cet attribut détermine la durée maximale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé dans le cadre de l’authentification Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Max-ticket-Age
- Schéma AD de l’attribut maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744348"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="7f9bd-105">Attribut Max-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="7f9bd-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="7f9bd-106">Cet attribut détermine la durée maximale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé dans le cadre de l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7f9bd-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="7f9bd-107">Lorsque le ticket TGT d’un utilisateur expire, un nouveau doit être demandé ou le ticket existant doit être renouvelé.</span><span class="sxs-lookup"><span data-stu-id="7f9bd-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="7f9bd-108">Par défaut, ce paramètre est défini sur 10 heures dans l’objet de stratégie de groupe de domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f9bd-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="7f9bd-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-109">Entry</span></span> | <span data-ttu-id="7f9bd-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7f9bd-111">CN</span><span class="sxs-lookup"><span data-stu-id="7f9bd-111">CN</span></span>                | <span data-ttu-id="7f9bd-112">Max-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="7f9bd-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="7f9bd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7f9bd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7f9bd-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="7f9bd-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="7f9bd-115">Taille</span><span class="sxs-lookup"><span data-stu-id="7f9bd-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="7f9bd-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7f9bd-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7f9bd-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7f9bd-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7f9bd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-118">Attribute-Id</span></span>      | <span data-ttu-id="7f9bd-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="7f9bd-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="7f9bd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7f9bd-120">System-Id-Guid</span></span>    | <span data-ttu-id="7f9bd-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7f9bd-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7f9bd-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f9bd-122">Syntax</span></span>            | [<span data-ttu-id="7f9bd-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7f9bd-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7f9bd-124">Implementations</span></span>

-   [<span data-ttu-id="7f9bd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f9bd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f9bd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f9bd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f9bd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f9bd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f9bd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f9bd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7f9bd-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-132">Entry</span></span> | <span data-ttu-id="7f9bd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-136">System-Only</span></span>            | <span data-ttu-id="7f9bd-137">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-137">False</span></span>                                              |
| <span data-ttu-id="7f9bd-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-139">True</span></span>                                               |
| <span data-ttu-id="7f9bd-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-140">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-141">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-141">False</span></span>                                              |
| <span data-ttu-id="7f9bd-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-142">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-143">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-143">False</span></span>                                              |
| <span data-ttu-id="7f9bd-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-148">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-149">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-150">System-Flags</span></span>           | <span data-ttu-id="7f9bd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-151">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-152">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-153">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f9bd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f9bd-154">Windows Server 2003</span></span>



| <span data-ttu-id="7f9bd-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-155">Entry</span></span> | <span data-ttu-id="7f9bd-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-159">System-Only</span></span>            | <span data-ttu-id="7f9bd-160">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-160">False</span></span>                                              |
| <span data-ttu-id="7f9bd-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-162">True</span></span>                                               |
| <span data-ttu-id="7f9bd-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-163">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-164">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-164">False</span></span>                                              |
| <span data-ttu-id="7f9bd-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-165">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-166">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-166">False</span></span>                                              |
| <span data-ttu-id="7f9bd-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-171">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-172">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-173">System-Flags</span></span>           | <span data-ttu-id="7f9bd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-174">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-175">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-176">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f9bd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f9bd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f9bd-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-178">Entry</span></span> | <span data-ttu-id="7f9bd-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-182">System-Only</span></span>            | <span data-ttu-id="7f9bd-183">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-183">False</span></span>                                              |
| <span data-ttu-id="7f9bd-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-185">True</span></span>                                               |
| <span data-ttu-id="7f9bd-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-186">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-187">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-187">False</span></span>                                              |
| <span data-ttu-id="7f9bd-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-188">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-189">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-189">False</span></span>                                              |
| <span data-ttu-id="7f9bd-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-194">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-195">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-196">System-Flags</span></span>           | <span data-ttu-id="7f9bd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-197">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-198">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-199">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f9bd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f9bd-200">Windows Server 2008</span></span>



| <span data-ttu-id="7f9bd-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-201">Entry</span></span> | <span data-ttu-id="7f9bd-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-205">System-Only</span></span>            | <span data-ttu-id="7f9bd-206">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-206">False</span></span>                                              |
| <span data-ttu-id="7f9bd-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-208">True</span></span>                                               |
| <span data-ttu-id="7f9bd-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-209">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-210">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-210">False</span></span>                                              |
| <span data-ttu-id="7f9bd-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-211">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-212">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-212">False</span></span>                                              |
| <span data-ttu-id="7f9bd-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-217">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-218">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-219">System-Flags</span></span>           | <span data-ttu-id="7f9bd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-220">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-221">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-222">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f9bd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f9bd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f9bd-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-224">Entry</span></span> | <span data-ttu-id="7f9bd-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-228">System-Only</span></span>            | <span data-ttu-id="7f9bd-229">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-229">False</span></span>                                              |
| <span data-ttu-id="7f9bd-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-231">True</span></span>                                               |
| <span data-ttu-id="7f9bd-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-232">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-233">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-233">False</span></span>                                              |
| <span data-ttu-id="7f9bd-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-234">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-235">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-235">False</span></span>                                              |
| <span data-ttu-id="7f9bd-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-240">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-241">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-242">System-Flags</span></span>           | <span data-ttu-id="7f9bd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-243">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-244">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-245">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f9bd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f9bd-246">Windows Server 2012</span></span>



| <span data-ttu-id="7f9bd-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f9bd-247">Entry</span></span> | <span data-ttu-id="7f9bd-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f9bd-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="7f9bd-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7f9bd-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f9bd-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="7f9bd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f9bd-251">System-Only</span></span>            | <span data-ttu-id="7f9bd-252">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-252">False</span></span>                                              |
| <span data-ttu-id="7f9bd-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7f9bd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7f9bd-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="7f9bd-254">True</span></span>                                               |
| <span data-ttu-id="7f9bd-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7f9bd-255">Is Indexed</span></span>             | <span data-ttu-id="7f9bd-256">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-256">False</span></span>                                              |
| <span data-ttu-id="7f9bd-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7f9bd-257">In Global Catalog</span></span>      | <span data-ttu-id="7f9bd-258">Faux</span><span class="sxs-lookup"><span data-stu-id="7f9bd-258">False</span></span>                                              |
| <span data-ttu-id="7f9bd-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7f9bd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f9bd-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7f9bd-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="7f9bd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f9bd-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f9bd-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="7f9bd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-263">Search-Flags</span></span>           | <span data-ttu-id="7f9bd-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f9bd-264">0x00000000</span></span>                                         |
| <span data-ttu-id="7f9bd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f9bd-265">System-Flags</span></span>           | <span data-ttu-id="7f9bd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f9bd-266">0x00000010</span></span>                                         |
| <span data-ttu-id="7f9bd-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7f9bd-267">Classes used in</span></span>        | [<span data-ttu-id="7f9bd-268">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="7f9bd-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





