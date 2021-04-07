---
title: MS-SQL-attribut de base de données
description: Nom de la base de données SQL Server impliquée dans la réplication.
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-Database
- Schéma AD de l’attribut mS-SQL-Database
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844702"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="f1498-105">MS-SQL-attribut de base de données</span><span class="sxs-lookup"><span data-stu-id="f1498-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="f1498-106">Nom de la base de données SQL Server impliquée dans la réplication.</span><span class="sxs-lookup"><span data-stu-id="f1498-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="f1498-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-107">Entry</span></span> | <span data-ttu-id="f1498-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f1498-109">CN</span><span class="sxs-lookup"><span data-stu-id="f1498-109">CN</span></span>                | <span data-ttu-id="f1498-110">Base de données MS-SQL</span><span class="sxs-lookup"><span data-stu-id="f1498-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="f1498-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1498-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f1498-112">Base de données mS-SQL</span><span class="sxs-lookup"><span data-stu-id="f1498-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="f1498-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f1498-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f1498-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f1498-114">Update Privilege</span></span>  | <span data-ttu-id="f1498-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="f1498-115">Domain administrator</span></span>                        |
| <span data-ttu-id="f1498-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f1498-116">Update Frequency</span></span>  | <span data-ttu-id="f1498-117">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="f1498-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="f1498-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-118">Attribute-Id</span></span>      | <span data-ttu-id="f1498-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="f1498-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="f1498-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1498-120">System-Id-Guid</span></span>    | <span data-ttu-id="f1498-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f1498-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="f1498-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1498-122">Syntax</span></span>            | [<span data-ttu-id="f1498-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f1498-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f1498-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f1498-124">Implementations</span></span>

-   [<span data-ttu-id="f1498-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1498-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1498-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1498-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1498-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1498-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1498-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1498-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1498-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1498-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1498-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1498-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1498-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1498-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f1498-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-132">Entry</span></span> | <span data-ttu-id="f1498-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-136">System-Only</span></span>            | <span data-ttu-id="f1498-137">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-137">False</span></span>                                                               |
| <span data-ttu-id="f1498-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-139">True</span></span>                                                                |
| <span data-ttu-id="f1498-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-140">Is Indexed</span></span>             | <span data-ttu-id="f1498-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-141">True</span></span>                                                                |
| <span data-ttu-id="f1498-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-142">In Global Catalog</span></span>      | <span data-ttu-id="f1498-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-143">True</span></span>                                                                |
| <span data-ttu-id="f1498-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-148">Search-Flags</span></span>           | <span data-ttu-id="f1498-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-150">System-Flags</span></span>           | <span data-ttu-id="f1498-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-152">Classes used in</span></span>        | [<span data-ttu-id="f1498-153">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1498-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1498-154">Windows Server 2003</span></span>



| <span data-ttu-id="f1498-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-155">Entry</span></span> | <span data-ttu-id="f1498-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-159">System-Only</span></span>            | <span data-ttu-id="f1498-160">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-160">False</span></span>                                                               |
| <span data-ttu-id="f1498-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-162">True</span></span>                                                                |
| <span data-ttu-id="f1498-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-163">Is Indexed</span></span>             | <span data-ttu-id="f1498-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-164">True</span></span>                                                                |
| <span data-ttu-id="f1498-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-165">In Global Catalog</span></span>      | <span data-ttu-id="f1498-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-166">True</span></span>                                                                |
| <span data-ttu-id="f1498-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-171">Search-Flags</span></span>           | <span data-ttu-id="f1498-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-173">System-Flags</span></span>           | <span data-ttu-id="f1498-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-175">Classes used in</span></span>        | [<span data-ttu-id="f1498-176">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1498-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1498-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1498-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-178">Entry</span></span> | <span data-ttu-id="f1498-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-182">System-Only</span></span>            | <span data-ttu-id="f1498-183">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-183">False</span></span>                                                               |
| <span data-ttu-id="f1498-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-185">True</span></span>                                                                |
| <span data-ttu-id="f1498-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-186">Is Indexed</span></span>             | <span data-ttu-id="f1498-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-187">True</span></span>                                                                |
| <span data-ttu-id="f1498-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-188">In Global Catalog</span></span>      | <span data-ttu-id="f1498-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-189">True</span></span>                                                                |
| <span data-ttu-id="f1498-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-194">Search-Flags</span></span>           | <span data-ttu-id="f1498-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-196">System-Flags</span></span>           | <span data-ttu-id="f1498-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-198">Classes used in</span></span>        | [<span data-ttu-id="f1498-199">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1498-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1498-200">Windows Server 2008</span></span>



| <span data-ttu-id="f1498-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-201">Entry</span></span> | <span data-ttu-id="f1498-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-205">System-Only</span></span>            | <span data-ttu-id="f1498-206">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-206">False</span></span>                                                               |
| <span data-ttu-id="f1498-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-208">True</span></span>                                                                |
| <span data-ttu-id="f1498-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-209">Is Indexed</span></span>             | <span data-ttu-id="f1498-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-210">True</span></span>                                                                |
| <span data-ttu-id="f1498-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-211">In Global Catalog</span></span>      | <span data-ttu-id="f1498-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-212">True</span></span>                                                                |
| <span data-ttu-id="f1498-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-217">Search-Flags</span></span>           | <span data-ttu-id="f1498-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-219">System-Flags</span></span>           | <span data-ttu-id="f1498-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-221">Classes used in</span></span>        | [<span data-ttu-id="f1498-222">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1498-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1498-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1498-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-224">Entry</span></span> | <span data-ttu-id="f1498-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-228">System-Only</span></span>            | <span data-ttu-id="f1498-229">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-229">False</span></span>                                                               |
| <span data-ttu-id="f1498-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-231">True</span></span>                                                                |
| <span data-ttu-id="f1498-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-232">Is Indexed</span></span>             | <span data-ttu-id="f1498-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-233">True</span></span>                                                                |
| <span data-ttu-id="f1498-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-234">In Global Catalog</span></span>      | <span data-ttu-id="f1498-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-235">True</span></span>                                                                |
| <span data-ttu-id="f1498-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-240">Search-Flags</span></span>           | <span data-ttu-id="f1498-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-242">System-Flags</span></span>           | <span data-ttu-id="f1498-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-244">Classes used in</span></span>        | [<span data-ttu-id="f1498-245">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1498-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1498-246">Windows Server 2012</span></span>



| <span data-ttu-id="f1498-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1498-247">Entry</span></span> | <span data-ttu-id="f1498-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1498-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1498-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1498-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1498-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f1498-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1498-251">System-Only</span></span>            | <span data-ttu-id="f1498-252">Faux</span><span class="sxs-lookup"><span data-stu-id="f1498-252">False</span></span>                                                               |
| <span data-ttu-id="f1498-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1498-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f1498-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-254">True</span></span>                                                                |
| <span data-ttu-id="f1498-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1498-255">Is Indexed</span></span>             | <span data-ttu-id="f1498-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-256">True</span></span>                                                                |
| <span data-ttu-id="f1498-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1498-257">In Global Catalog</span></span>      | <span data-ttu-id="f1498-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1498-258">True</span></span>                                                                |
| <span data-ttu-id="f1498-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1498-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1498-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1498-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f1498-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1498-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1498-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f1498-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-263">Search-Flags</span></span>           | <span data-ttu-id="f1498-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f1498-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="f1498-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1498-265">System-Flags</span></span>           | <span data-ttu-id="f1498-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1498-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="f1498-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1498-267">Classes used in</span></span>        | [<span data-ttu-id="f1498-268">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="f1498-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





