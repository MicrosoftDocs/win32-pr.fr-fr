---
title: Attribut MS-SQL-AllowAnonymousSubscription
description: True si la publication autorise les abonnés anonymes à s’y abonner.
ms.assetid: d4ac86ce-d3c5-493e-8212-e9250671a522
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-AllowAnonymousSubscription
- Schéma AD de l’attribut mS-SQL-AllowAnonymousSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowAnonymousSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23de7f731ffaca310a39d81d4af80a5b0a23a84
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108210"
---
# <a name="ms-sql-allowanonymoussubscription-attribute"></a><span data-ttu-id="7059c-105">Attribut MS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="7059c-105">MS-SQL-AllowAnonymousSubscription attribute</span></span>

<span data-ttu-id="7059c-106">True si la publication autorise les abonnés anonymes à s’y abonner.</span><span class="sxs-lookup"><span data-stu-id="7059c-106">True if the publication allows anonymous subscribers to subscribe to it.</span></span>



| <span data-ttu-id="7059c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-107">Entry</span></span> | <span data-ttu-id="7059c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7059c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7059c-109">CN</span></span>                | <span data-ttu-id="7059c-110">MS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="7059c-110">MS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="7059c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7059c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7059c-112">mS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="7059c-112">mS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="7059c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7059c-113">Size</span></span>              | <span data-ttu-id="7059c-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="7059c-114">4 bytes</span></span>                              |
| <span data-ttu-id="7059c-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7059c-115">Update Privilege</span></span>  | <span data-ttu-id="7059c-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="7059c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7059c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7059c-117">Update Frequency</span></span>  | <span data-ttu-id="7059c-118">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="7059c-118">When replication is setup.</span></span>           |
| <span data-ttu-id="7059c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-119">Attribute-Id</span></span>      | <span data-ttu-id="7059c-120">1.2.840.113556.1.4.1394</span><span class="sxs-lookup"><span data-stu-id="7059c-120">1.2.840.113556.1.4.1394</span></span>              |
| <span data-ttu-id="7059c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7059c-121">System-Id-Guid</span></span>    | <span data-ttu-id="7059c-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7059c-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="7059c-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7059c-123">Syntax</span></span>            | [<span data-ttu-id="7059c-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7059c-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7059c-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7059c-125">Implementations</span></span>

-   [<span data-ttu-id="7059c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7059c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7059c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7059c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7059c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7059c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7059c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7059c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7059c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7059c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7059c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7059c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7059c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7059c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7059c-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-133">Entry</span></span> | <span data-ttu-id="7059c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-137">System-Only</span></span>            | <span data-ttu-id="7059c-138">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-138">False</span></span>                                                               |
| <span data-ttu-id="7059c-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-140">True</span></span>                                                                |
| <span data-ttu-id="7059c-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-141">Is Indexed</span></span>             | <span data-ttu-id="7059c-142">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-142">False</span></span>                                                               |
| <span data-ttu-id="7059c-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-143">In Global Catalog</span></span>      | <span data-ttu-id="7059c-144">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-144">False</span></span>                                                               |
| <span data-ttu-id="7059c-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-149">Search-Flags</span></span>           | <span data-ttu-id="7059c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-151">System-Flags</span></span>           | <span data-ttu-id="7059c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-153">Classes used in</span></span>        | [<span data-ttu-id="7059c-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7059c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7059c-155">Windows Server 2003</span></span>



| <span data-ttu-id="7059c-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-156">Entry</span></span> | <span data-ttu-id="7059c-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-160">System-Only</span></span>            | <span data-ttu-id="7059c-161">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-161">False</span></span>                                                               |
| <span data-ttu-id="7059c-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-163">True</span></span>                                                                |
| <span data-ttu-id="7059c-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-164">Is Indexed</span></span>             | <span data-ttu-id="7059c-165">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-165">False</span></span>                                                               |
| <span data-ttu-id="7059c-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-166">In Global Catalog</span></span>      | <span data-ttu-id="7059c-167">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-167">False</span></span>                                                               |
| <span data-ttu-id="7059c-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-172">Search-Flags</span></span>           | <span data-ttu-id="7059c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-174">System-Flags</span></span>           | <span data-ttu-id="7059c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-176">Classes used in</span></span>        | [<span data-ttu-id="7059c-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7059c-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7059c-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7059c-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-179">Entry</span></span> | <span data-ttu-id="7059c-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-183">System-Only</span></span>            | <span data-ttu-id="7059c-184">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-184">False</span></span>                                                               |
| <span data-ttu-id="7059c-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-186">True</span></span>                                                                |
| <span data-ttu-id="7059c-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-187">Is Indexed</span></span>             | <span data-ttu-id="7059c-188">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-188">False</span></span>                                                               |
| <span data-ttu-id="7059c-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-189">In Global Catalog</span></span>      | <span data-ttu-id="7059c-190">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-190">False</span></span>                                                               |
| <span data-ttu-id="7059c-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-195">Search-Flags</span></span>           | <span data-ttu-id="7059c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-197">System-Flags</span></span>           | <span data-ttu-id="7059c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-199">Classes used in</span></span>        | [<span data-ttu-id="7059c-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7059c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7059c-201">Windows Server 2008</span></span>



| <span data-ttu-id="7059c-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-202">Entry</span></span> | <span data-ttu-id="7059c-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-206">System-Only</span></span>            | <span data-ttu-id="7059c-207">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-207">False</span></span>                                                               |
| <span data-ttu-id="7059c-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-209">True</span></span>                                                                |
| <span data-ttu-id="7059c-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-210">Is Indexed</span></span>             | <span data-ttu-id="7059c-211">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-211">False</span></span>                                                               |
| <span data-ttu-id="7059c-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-212">In Global Catalog</span></span>      | <span data-ttu-id="7059c-213">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-213">False</span></span>                                                               |
| <span data-ttu-id="7059c-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-218">Search-Flags</span></span>           | <span data-ttu-id="7059c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-220">System-Flags</span></span>           | <span data-ttu-id="7059c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-222">Classes used in</span></span>        | [<span data-ttu-id="7059c-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7059c-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7059c-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7059c-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-225">Entry</span></span> | <span data-ttu-id="7059c-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-229">System-Only</span></span>            | <span data-ttu-id="7059c-230">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-230">False</span></span>                                                               |
| <span data-ttu-id="7059c-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-232">True</span></span>                                                                |
| <span data-ttu-id="7059c-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-233">Is Indexed</span></span>             | <span data-ttu-id="7059c-234">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-234">False</span></span>                                                               |
| <span data-ttu-id="7059c-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-235">In Global Catalog</span></span>      | <span data-ttu-id="7059c-236">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-236">False</span></span>                                                               |
| <span data-ttu-id="7059c-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-241">Search-Flags</span></span>           | <span data-ttu-id="7059c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-243">System-Flags</span></span>           | <span data-ttu-id="7059c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-245">Classes used in</span></span>        | [<span data-ttu-id="7059c-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7059c-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7059c-247">Windows Server 2012</span></span>



| <span data-ttu-id="7059c-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="7059c-248">Entry</span></span> | <span data-ttu-id="7059c-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="7059c-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7059c-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7059c-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7059c-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7059c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7059c-252">System-Only</span></span>            | <span data-ttu-id="7059c-253">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-253">False</span></span>                                                               |
| <span data-ttu-id="7059c-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7059c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7059c-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="7059c-255">True</span></span>                                                                |
| <span data-ttu-id="7059c-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7059c-256">Is Indexed</span></span>             | <span data-ttu-id="7059c-257">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-257">False</span></span>                                                               |
| <span data-ttu-id="7059c-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7059c-258">In Global Catalog</span></span>      | <span data-ttu-id="7059c-259">Faux</span><span class="sxs-lookup"><span data-stu-id="7059c-259">False</span></span>                                                               |
| <span data-ttu-id="7059c-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7059c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7059c-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7059c-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7059c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7059c-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7059c-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7059c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-264">Search-Flags</span></span>           | <span data-ttu-id="7059c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7059c-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="7059c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7059c-266">System-Flags</span></span>           | <span data-ttu-id="7059c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7059c-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="7059c-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7059c-268">Classes used in</span></span>        | [<span data-ttu-id="7059c-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7059c-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





