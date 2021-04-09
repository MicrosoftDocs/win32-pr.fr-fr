---
title: Attribut MS-SQL-ThirdParty
description: Cet attribut indique si les données de publication proviennent d’une source de données autre que SQL Server. S’il provient d’une autre source, il est défini sur TRUE.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-ThirdParty
- Schéma AD de l’attribut mS-SQL-ThirdParty
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744300"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="b71a6-106">Attribut MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="b71a6-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="b71a6-107">Cet attribut indique si les données de publication proviennent d’une source de données autre que SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b71a6-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="b71a6-108">S’il provient d’une autre source, il est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b71a6-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="b71a6-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-109">Entry</span></span> | <span data-ttu-id="b71a6-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b71a6-111">CN</span><span class="sxs-lookup"><span data-stu-id="b71a6-111">CN</span></span>                | <span data-ttu-id="b71a6-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="b71a6-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="b71a6-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b71a6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b71a6-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="b71a6-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="b71a6-115">Taille</span><span class="sxs-lookup"><span data-stu-id="b71a6-115">Size</span></span>              | <span data-ttu-id="b71a6-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="b71a6-116">4 bytes</span></span>                              |
| <span data-ttu-id="b71a6-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b71a6-117">Update Privilege</span></span>  | <span data-ttu-id="b71a6-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="b71a6-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="b71a6-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b71a6-119">Update Frequency</span></span>  | <span data-ttu-id="b71a6-120">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="b71a6-120">When replication is setup.</span></span>           |
| <span data-ttu-id="b71a6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-121">Attribute-Id</span></span>      | <span data-ttu-id="b71a6-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="b71a6-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="b71a6-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b71a6-123">System-Id-Guid</span></span>    | <span data-ttu-id="b71a6-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b71a6-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="b71a6-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b71a6-125">Syntax</span></span>            | [<span data-ttu-id="b71a6-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b71a6-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b71a6-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b71a6-127">Implementations</span></span>

-   [<span data-ttu-id="b71a6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b71a6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b71a6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b71a6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b71a6-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b71a6-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b71a6-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b71a6-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b71a6-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b71a6-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b71a6-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b71a6-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b71a6-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b71a6-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b71a6-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-135">Entry</span></span> | <span data-ttu-id="b71a6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-139">System-Only</span></span>            | <span data-ttu-id="b71a6-140">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-140">False</span></span>                                                               |
| <span data-ttu-id="b71a6-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-142">True</span></span>                                                                |
| <span data-ttu-id="b71a6-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-143">Is Indexed</span></span>             | <span data-ttu-id="b71a6-144">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-144">False</span></span>                                                               |
| <span data-ttu-id="b71a6-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-145">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-146">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-146">False</span></span>                                                               |
| <span data-ttu-id="b71a6-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-151">Search-Flags</span></span>           | <span data-ttu-id="b71a6-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-153">System-Flags</span></span>           | <span data-ttu-id="b71a6-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-155">Classes used in</span></span>        | [<span data-ttu-id="b71a6-156">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b71a6-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b71a6-157">Windows Server 2003</span></span>



| <span data-ttu-id="b71a6-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-158">Entry</span></span> | <span data-ttu-id="b71a6-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-162">System-Only</span></span>            | <span data-ttu-id="b71a6-163">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-163">False</span></span>                                                               |
| <span data-ttu-id="b71a6-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-165">True</span></span>                                                                |
| <span data-ttu-id="b71a6-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-166">Is Indexed</span></span>             | <span data-ttu-id="b71a6-167">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-167">False</span></span>                                                               |
| <span data-ttu-id="b71a6-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-168">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-169">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-169">False</span></span>                                                               |
| <span data-ttu-id="b71a6-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-174">Search-Flags</span></span>           | <span data-ttu-id="b71a6-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-176">System-Flags</span></span>           | <span data-ttu-id="b71a6-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-178">Classes used in</span></span>        | [<span data-ttu-id="b71a6-179">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b71a6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b71a6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b71a6-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-181">Entry</span></span> | <span data-ttu-id="b71a6-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-185">System-Only</span></span>            | <span data-ttu-id="b71a6-186">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-186">False</span></span>                                                               |
| <span data-ttu-id="b71a6-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-188">True</span></span>                                                                |
| <span data-ttu-id="b71a6-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-189">Is Indexed</span></span>             | <span data-ttu-id="b71a6-190">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-190">False</span></span>                                                               |
| <span data-ttu-id="b71a6-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-191">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-192">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-192">False</span></span>                                                               |
| <span data-ttu-id="b71a6-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-197">Search-Flags</span></span>           | <span data-ttu-id="b71a6-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-199">System-Flags</span></span>           | <span data-ttu-id="b71a6-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-201">Classes used in</span></span>        | [<span data-ttu-id="b71a6-202">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b71a6-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b71a6-203">Windows Server 2008</span></span>



| <span data-ttu-id="b71a6-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-204">Entry</span></span> | <span data-ttu-id="b71a6-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-208">System-Only</span></span>            | <span data-ttu-id="b71a6-209">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-209">False</span></span>                                                               |
| <span data-ttu-id="b71a6-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-211">True</span></span>                                                                |
| <span data-ttu-id="b71a6-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-212">Is Indexed</span></span>             | <span data-ttu-id="b71a6-213">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-213">False</span></span>                                                               |
| <span data-ttu-id="b71a6-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-214">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-215">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-215">False</span></span>                                                               |
| <span data-ttu-id="b71a6-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-220">Search-Flags</span></span>           | <span data-ttu-id="b71a6-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-222">System-Flags</span></span>           | <span data-ttu-id="b71a6-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-224">Classes used in</span></span>        | [<span data-ttu-id="b71a6-225">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b71a6-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b71a6-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b71a6-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-227">Entry</span></span> | <span data-ttu-id="b71a6-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-231">System-Only</span></span>            | <span data-ttu-id="b71a6-232">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-232">False</span></span>                                                               |
| <span data-ttu-id="b71a6-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-234">True</span></span>                                                                |
| <span data-ttu-id="b71a6-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-235">Is Indexed</span></span>             | <span data-ttu-id="b71a6-236">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-236">False</span></span>                                                               |
| <span data-ttu-id="b71a6-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-237">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-238">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-238">False</span></span>                                                               |
| <span data-ttu-id="b71a6-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-243">Search-Flags</span></span>           | <span data-ttu-id="b71a6-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-245">System-Flags</span></span>           | <span data-ttu-id="b71a6-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-247">Classes used in</span></span>        | [<span data-ttu-id="b71a6-248">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b71a6-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b71a6-249">Windows Server 2012</span></span>



| <span data-ttu-id="b71a6-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="b71a6-250">Entry</span></span> | <span data-ttu-id="b71a6-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71a6-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b71a6-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b71a6-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b71a6-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b71a6-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="b71a6-254">System-Only</span></span>            | <span data-ttu-id="b71a6-255">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-255">False</span></span>                                                               |
| <span data-ttu-id="b71a6-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b71a6-256">Is-Single-Valued</span></span>       | <span data-ttu-id="b71a6-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="b71a6-257">True</span></span>                                                                |
| <span data-ttu-id="b71a6-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b71a6-258">Is Indexed</span></span>             | <span data-ttu-id="b71a6-259">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-259">False</span></span>                                                               |
| <span data-ttu-id="b71a6-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b71a6-260">In Global Catalog</span></span>      | <span data-ttu-id="b71a6-261">Faux</span><span class="sxs-lookup"><span data-stu-id="b71a6-261">False</span></span>                                                               |
| <span data-ttu-id="b71a6-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b71a6-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="b71a6-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b71a6-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b71a6-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b71a6-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b71a6-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b71a6-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-266">Search-Flags</span></span>           | <span data-ttu-id="b71a6-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b71a6-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="b71a6-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b71a6-268">System-Flags</span></span>           | <span data-ttu-id="b71a6-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b71a6-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="b71a6-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b71a6-270">Classes used in</span></span>        | [<span data-ttu-id="b71a6-271">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="b71a6-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





