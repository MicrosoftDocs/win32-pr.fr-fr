---
title: Attribut min-ticket-Age
description: Cet attribut détermine la période minimale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé pour l’authentification Kerberos avant qu’une demande puisse être renouvelée pour renouveler le ticket.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut min-ticket-Age
- Schéma AD de l’attribut minTicketAge
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107200"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="ab7a2-105">Attribut min-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="ab7a2-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="ab7a2-106">Cet attribut détermine la période minimale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé pour l’authentification Kerberos avant qu’une demande puisse être renouvelée pour renouveler le ticket.</span><span class="sxs-lookup"><span data-stu-id="ab7a2-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="ab7a2-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-107">Entry</span></span> | <span data-ttu-id="ab7a2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ab7a2-109">CN</span><span class="sxs-lookup"><span data-stu-id="ab7a2-109">CN</span></span>                | <span data-ttu-id="ab7a2-110">Min-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="ab7a2-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="ab7a2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ab7a2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ab7a2-112">minTicketAge</span><span class="sxs-lookup"><span data-stu-id="ab7a2-112">minTicketAge</span></span>                         |
| <span data-ttu-id="ab7a2-113">Taille</span><span class="sxs-lookup"><span data-stu-id="ab7a2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ab7a2-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ab7a2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ab7a2-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ab7a2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ab7a2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-116">Attribute-Id</span></span>      | <span data-ttu-id="ab7a2-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="ab7a2-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="ab7a2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ab7a2-118">System-Id-Guid</span></span>    | <span data-ttu-id="ab7a2-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ab7a2-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ab7a2-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab7a2-120">Syntax</span></span>            | [<span data-ttu-id="ab7a2-121">**Défini**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ab7a2-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ab7a2-122">Implementations</span></span>

-   [<span data-ttu-id="ab7a2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ab7a2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab7a2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab7a2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab7a2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab7a2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ab7a2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab7a2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ab7a2-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-130">Entry</span></span> | <span data-ttu-id="ab7a2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-134">System-Only</span></span>            | <span data-ttu-id="ab7a2-135">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-135">False</span></span>                                              |
| <span data-ttu-id="ab7a2-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-137">True</span></span>                                               |
| <span data-ttu-id="ab7a2-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-138">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-139">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-139">False</span></span>                                              |
| <span data-ttu-id="ab7a2-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-140">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-141">False</span></span>                                              |
| <span data-ttu-id="ab7a2-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-146">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-147">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-148">System-Flags</span></span>           | <span data-ttu-id="ab7a2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-149">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-150">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-151">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ab7a2-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab7a2-152">Windows Server 2003</span></span>



| <span data-ttu-id="ab7a2-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-153">Entry</span></span> | <span data-ttu-id="ab7a2-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-157">System-Only</span></span>            | <span data-ttu-id="ab7a2-158">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-158">False</span></span>                                              |
| <span data-ttu-id="ab7a2-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-160">True</span></span>                                               |
| <span data-ttu-id="ab7a2-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-161">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-162">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-162">False</span></span>                                              |
| <span data-ttu-id="ab7a2-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-163">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-164">False</span></span>                                              |
| <span data-ttu-id="ab7a2-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-169">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-170">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-171">System-Flags</span></span>           | <span data-ttu-id="ab7a2-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-172">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-173">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-174">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab7a2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab7a2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab7a2-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-176">Entry</span></span> | <span data-ttu-id="ab7a2-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-180">System-Only</span></span>            | <span data-ttu-id="ab7a2-181">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-181">False</span></span>                                              |
| <span data-ttu-id="ab7a2-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-183">True</span></span>                                               |
| <span data-ttu-id="ab7a2-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-184">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-185">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-185">False</span></span>                                              |
| <span data-ttu-id="ab7a2-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-186">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-187">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-187">False</span></span>                                              |
| <span data-ttu-id="ab7a2-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-192">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-193">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-194">System-Flags</span></span>           | <span data-ttu-id="ab7a2-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-195">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-196">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-197">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab7a2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab7a2-198">Windows Server 2008</span></span>



| <span data-ttu-id="ab7a2-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-199">Entry</span></span> | <span data-ttu-id="ab7a2-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-203">System-Only</span></span>            | <span data-ttu-id="ab7a2-204">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-204">False</span></span>                                              |
| <span data-ttu-id="ab7a2-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-206">True</span></span>                                               |
| <span data-ttu-id="ab7a2-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-207">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-208">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-208">False</span></span>                                              |
| <span data-ttu-id="ab7a2-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-209">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-210">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-210">False</span></span>                                              |
| <span data-ttu-id="ab7a2-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-215">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-216">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-217">System-Flags</span></span>           | <span data-ttu-id="ab7a2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-218">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-219">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-220">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab7a2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab7a2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab7a2-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-222">Entry</span></span> | <span data-ttu-id="ab7a2-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-226">System-Only</span></span>            | <span data-ttu-id="ab7a2-227">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-227">False</span></span>                                              |
| <span data-ttu-id="ab7a2-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-229">True</span></span>                                               |
| <span data-ttu-id="ab7a2-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-230">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-231">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-231">False</span></span>                                              |
| <span data-ttu-id="ab7a2-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-232">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-233">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-233">False</span></span>                                              |
| <span data-ttu-id="ab7a2-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-238">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-239">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-240">System-Flags</span></span>           | <span data-ttu-id="ab7a2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-241">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-242">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-243">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab7a2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab7a2-244">Windows Server 2012</span></span>



| <span data-ttu-id="ab7a2-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="ab7a2-245">Entry</span></span> | <span data-ttu-id="ab7a2-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7a2-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ab7a2-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ab7a2-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab7a2-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ab7a2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab7a2-249">System-Only</span></span>            | <span data-ttu-id="ab7a2-250">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-250">False</span></span>                                              |
| <span data-ttu-id="ab7a2-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ab7a2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="ab7a2-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="ab7a2-252">True</span></span>                                               |
| <span data-ttu-id="ab7a2-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ab7a2-253">Is Indexed</span></span>             | <span data-ttu-id="ab7a2-254">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-254">False</span></span>                                              |
| <span data-ttu-id="ab7a2-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ab7a2-255">In Global Catalog</span></span>      | <span data-ttu-id="ab7a2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="ab7a2-256">False</span></span>                                              |
| <span data-ttu-id="ab7a2-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ab7a2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab7a2-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ab7a2-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ab7a2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab7a2-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab7a2-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ab7a2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-261">Search-Flags</span></span>           | <span data-ttu-id="ab7a2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab7a2-262">0x00000000</span></span>                                         |
| <span data-ttu-id="ab7a2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab7a2-263">System-Flags</span></span>           | <span data-ttu-id="ab7a2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab7a2-264">0x00000010</span></span>                                         |
| <span data-ttu-id="ab7a2-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ab7a2-265">Classes used in</span></span>        | [<span data-ttu-id="ab7a2-266">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="ab7a2-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





