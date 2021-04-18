---
title: Attribut MS-SQL-AllowImmediateUpdatingSubscription
description: True si la publication autorise les abonnements de mise à jour de la transaction synchronisée.
ms.assetid: 7efa4b8f-77ad-4f68-9852-7dac9f922d95
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-AllowImmediateUpdatingSubscription
- Schéma AD de l’attribut mS-SQL-AllowImmediateUpdatingSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowImmediateUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed7970aa4b4f26a7221ea9a0c3d4e279ddc5db1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519514"
---
# <a name="ms-sql-allowimmediateupdatingsubscription-attribute"></a><span data-ttu-id="a533d-105">Attribut MS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a533d-105">MS-SQL-AllowImmediateUpdatingSubscription attribute</span></span>

<span data-ttu-id="a533d-106">True si la publication autorise les abonnements de mise à jour de la transaction synchronisée.</span><span class="sxs-lookup"><span data-stu-id="a533d-106">True if the publication allows synchronized transaction updating subscriptions.</span></span>



| <span data-ttu-id="a533d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-107">Entry</span></span> | <span data-ttu-id="a533d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="a533d-109">CN</span><span class="sxs-lookup"><span data-stu-id="a533d-109">CN</span></span>                | <span data-ttu-id="a533d-110">MS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a533d-110">MS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="a533d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a533d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a533d-112">mS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a533d-112">mS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="a533d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="a533d-113">Size</span></span>              | <span data-ttu-id="a533d-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="a533d-114">4 bytes</span></span>                                   |
| <span data-ttu-id="a533d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a533d-115">Update Privilege</span></span>  | <span data-ttu-id="a533d-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="a533d-116">This value is set by the system.</span></span>          |
| <span data-ttu-id="a533d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a533d-117">Update Frequency</span></span>  | <span data-ttu-id="a533d-118">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="a533d-118">When replication is setup.</span></span>                |
| <span data-ttu-id="a533d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-119">Attribute-Id</span></span>      | <span data-ttu-id="a533d-120">1.2.840.113556.1.4.1404</span><span class="sxs-lookup"><span data-stu-id="a533d-120">1.2.840.113556.1.4.1404</span></span>                   |
| <span data-ttu-id="a533d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a533d-121">System-Id-Guid</span></span>    | <span data-ttu-id="a533d-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a533d-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span></span>      |
| <span data-ttu-id="a533d-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a533d-123">Syntax</span></span>            | [<span data-ttu-id="a533d-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a533d-124">**Boolean**</span></span>](s-boolean.md)              |



## <a name="implementations"></a><span data-ttu-id="a533d-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a533d-125">Implementations</span></span>

-   [<span data-ttu-id="a533d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a533d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a533d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a533d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a533d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a533d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a533d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a533d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a533d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a533d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a533d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a533d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a533d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a533d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a533d-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-133">Entry</span></span> | <span data-ttu-id="a533d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-137">System-Only</span></span>            | <span data-ttu-id="a533d-138">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-138">False</span></span>                                                               |
| <span data-ttu-id="a533d-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-140">True</span></span>                                                                |
| <span data-ttu-id="a533d-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-141">Is Indexed</span></span>             | <span data-ttu-id="a533d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-142">False</span></span>                                                               |
| <span data-ttu-id="a533d-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-143">In Global Catalog</span></span>      | <span data-ttu-id="a533d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-144">False</span></span>                                                               |
| <span data-ttu-id="a533d-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-149">Search-Flags</span></span>           | <span data-ttu-id="a533d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-151">System-Flags</span></span>           | <span data-ttu-id="a533d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-153">Classes used in</span></span>        | [<span data-ttu-id="a533d-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a533d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a533d-155">Windows Server 2003</span></span>



| <span data-ttu-id="a533d-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-156">Entry</span></span> | <span data-ttu-id="a533d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-160">System-Only</span></span>            | <span data-ttu-id="a533d-161">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-161">False</span></span>                                                               |
| <span data-ttu-id="a533d-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-163">True</span></span>                                                                |
| <span data-ttu-id="a533d-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-164">Is Indexed</span></span>             | <span data-ttu-id="a533d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-165">False</span></span>                                                               |
| <span data-ttu-id="a533d-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-166">In Global Catalog</span></span>      | <span data-ttu-id="a533d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-167">False</span></span>                                                               |
| <span data-ttu-id="a533d-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-172">Search-Flags</span></span>           | <span data-ttu-id="a533d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-174">System-Flags</span></span>           | <span data-ttu-id="a533d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-176">Classes used in</span></span>        | [<span data-ttu-id="a533d-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a533d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a533d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a533d-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-179">Entry</span></span> | <span data-ttu-id="a533d-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-183">System-Only</span></span>            | <span data-ttu-id="a533d-184">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-184">False</span></span>                                                               |
| <span data-ttu-id="a533d-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-186">True</span></span>                                                                |
| <span data-ttu-id="a533d-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-187">Is Indexed</span></span>             | <span data-ttu-id="a533d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-188">False</span></span>                                                               |
| <span data-ttu-id="a533d-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-189">In Global Catalog</span></span>      | <span data-ttu-id="a533d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-190">False</span></span>                                                               |
| <span data-ttu-id="a533d-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-195">Search-Flags</span></span>           | <span data-ttu-id="a533d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-197">System-Flags</span></span>           | <span data-ttu-id="a533d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-199">Classes used in</span></span>        | [<span data-ttu-id="a533d-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a533d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a533d-201">Windows Server 2008</span></span>



| <span data-ttu-id="a533d-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-202">Entry</span></span> | <span data-ttu-id="a533d-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-206">System-Only</span></span>            | <span data-ttu-id="a533d-207">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-207">False</span></span>                                                               |
| <span data-ttu-id="a533d-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-209">True</span></span>                                                                |
| <span data-ttu-id="a533d-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-210">Is Indexed</span></span>             | <span data-ttu-id="a533d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-211">False</span></span>                                                               |
| <span data-ttu-id="a533d-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-212">In Global Catalog</span></span>      | <span data-ttu-id="a533d-213">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-213">False</span></span>                                                               |
| <span data-ttu-id="a533d-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-218">Search-Flags</span></span>           | <span data-ttu-id="a533d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-220">System-Flags</span></span>           | <span data-ttu-id="a533d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-222">Classes used in</span></span>        | [<span data-ttu-id="a533d-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a533d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a533d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a533d-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-225">Entry</span></span> | <span data-ttu-id="a533d-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-229">System-Only</span></span>            | <span data-ttu-id="a533d-230">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-230">False</span></span>                                                               |
| <span data-ttu-id="a533d-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-232">True</span></span>                                                                |
| <span data-ttu-id="a533d-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-233">Is Indexed</span></span>             | <span data-ttu-id="a533d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-234">False</span></span>                                                               |
| <span data-ttu-id="a533d-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-235">In Global Catalog</span></span>      | <span data-ttu-id="a533d-236">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-236">False</span></span>                                                               |
| <span data-ttu-id="a533d-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-241">Search-Flags</span></span>           | <span data-ttu-id="a533d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-243">System-Flags</span></span>           | <span data-ttu-id="a533d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-245">Classes used in</span></span>        | [<span data-ttu-id="a533d-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a533d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a533d-247">Windows Server 2012</span></span>



| <span data-ttu-id="a533d-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="a533d-248">Entry</span></span> | <span data-ttu-id="a533d-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="a533d-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a533d-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a533d-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a533d-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a533d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a533d-252">System-Only</span></span>            | <span data-ttu-id="a533d-253">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-253">False</span></span>                                                               |
| <span data-ttu-id="a533d-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a533d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a533d-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="a533d-255">True</span></span>                                                                |
| <span data-ttu-id="a533d-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a533d-256">Is Indexed</span></span>             | <span data-ttu-id="a533d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-257">False</span></span>                                                               |
| <span data-ttu-id="a533d-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a533d-258">In Global Catalog</span></span>      | <span data-ttu-id="a533d-259">Faux</span><span class="sxs-lookup"><span data-stu-id="a533d-259">False</span></span>                                                               |
| <span data-ttu-id="a533d-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a533d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a533d-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a533d-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a533d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a533d-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a533d-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a533d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-264">Search-Flags</span></span>           | <span data-ttu-id="a533d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a533d-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="a533d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a533d-266">System-Flags</span></span>           | <span data-ttu-id="a533d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a533d-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="a533d-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a533d-268">Classes used in</span></span>        | [<span data-ttu-id="a533d-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a533d-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





