---
title: Attribut MS-SQL-LastBackupDate
description: Date de la dernière sauvegarde de la base de données.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-LastBackupDate
- Schéma AD de l’attribut mS-SQL-LastBackupDate
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949908"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="2215e-105">Attribut MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="2215e-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="2215e-106">Date de la dernière sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2215e-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="2215e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-107">Entry</span></span> | <span data-ttu-id="2215e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2215e-109">CN</span><span class="sxs-lookup"><span data-stu-id="2215e-109">CN</span></span>                | <span data-ttu-id="2215e-110">MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="2215e-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="2215e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2215e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2215e-112">mS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="2215e-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="2215e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="2215e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2215e-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2215e-114">Update Privilege</span></span>  | <span data-ttu-id="2215e-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="2215e-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="2215e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2215e-116">Update Frequency</span></span>  | <span data-ttu-id="2215e-117">Lors de la sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2215e-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="2215e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-118">Attribute-Id</span></span>      | <span data-ttu-id="2215e-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="2215e-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="2215e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2215e-120">System-Id-Guid</span></span>    | <span data-ttu-id="2215e-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2215e-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="2215e-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2215e-122">Syntax</span></span>            | [<span data-ttu-id="2215e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2215e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2215e-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2215e-124">Implementations</span></span>

-   [<span data-ttu-id="2215e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2215e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2215e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2215e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2215e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2215e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2215e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2215e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2215e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2215e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2215e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2215e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2215e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2215e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2215e-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-132">Entry</span></span> | <span data-ttu-id="2215e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-136">System-Only</span></span>            | <span data-ttu-id="2215e-137">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-140">Is Indexed</span></span>             | <span data-ttu-id="2215e-141">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-142">In Global Catalog</span></span>      | <span data-ttu-id="2215e-143">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-148">Search-Flags</span></span>           | <span data-ttu-id="2215e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-150">System-Flags</span></span>           | <span data-ttu-id="2215e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-152">Classes used in</span></span>        | [<span data-ttu-id="2215e-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-154">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2215e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2215e-155">Windows Server 2003</span></span>



| <span data-ttu-id="2215e-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-156">Entry</span></span> | <span data-ttu-id="2215e-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-160">System-Only</span></span>            | <span data-ttu-id="2215e-161">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-164">Is Indexed</span></span>             | <span data-ttu-id="2215e-165">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-166">In Global Catalog</span></span>      | <span data-ttu-id="2215e-167">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-172">Search-Flags</span></span>           | <span data-ttu-id="2215e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-174">System-Flags</span></span>           | <span data-ttu-id="2215e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-176">Classes used in</span></span>        | [<span data-ttu-id="2215e-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-178">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2215e-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2215e-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2215e-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-180">Entry</span></span> | <span data-ttu-id="2215e-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-184">System-Only</span></span>            | <span data-ttu-id="2215e-185">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-188">Is Indexed</span></span>             | <span data-ttu-id="2215e-189">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-190">In Global Catalog</span></span>      | <span data-ttu-id="2215e-191">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-196">Search-Flags</span></span>           | <span data-ttu-id="2215e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-198">System-Flags</span></span>           | <span data-ttu-id="2215e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-200">Classes used in</span></span>        | [<span data-ttu-id="2215e-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-202">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2215e-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2215e-203">Windows Server 2008</span></span>



| <span data-ttu-id="2215e-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-204">Entry</span></span> | <span data-ttu-id="2215e-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-208">System-Only</span></span>            | <span data-ttu-id="2215e-209">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-212">Is Indexed</span></span>             | <span data-ttu-id="2215e-213">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-214">In Global Catalog</span></span>      | <span data-ttu-id="2215e-215">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-220">Search-Flags</span></span>           | <span data-ttu-id="2215e-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-222">System-Flags</span></span>           | <span data-ttu-id="2215e-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-224">Classes used in</span></span>        | [<span data-ttu-id="2215e-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-226">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2215e-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2215e-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2215e-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-228">Entry</span></span> | <span data-ttu-id="2215e-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-232">System-Only</span></span>            | <span data-ttu-id="2215e-233">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-236">Is Indexed</span></span>             | <span data-ttu-id="2215e-237">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-238">In Global Catalog</span></span>      | <span data-ttu-id="2215e-239">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-244">Search-Flags</span></span>           | <span data-ttu-id="2215e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-246">System-Flags</span></span>           | <span data-ttu-id="2215e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-248">Classes used in</span></span>        | [<span data-ttu-id="2215e-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-250">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2215e-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2215e-251">Windows Server 2012</span></span>



| <span data-ttu-id="2215e-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="2215e-252">Entry</span></span> | <span data-ttu-id="2215e-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="2215e-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2215e-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2215e-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2215e-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2215e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="2215e-256">System-Only</span></span>            | <span data-ttu-id="2215e-257">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2215e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="2215e-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="2215e-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="2215e-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2215e-260">Is Indexed</span></span>             | <span data-ttu-id="2215e-261">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2215e-262">In Global Catalog</span></span>      | <span data-ttu-id="2215e-263">Faux</span><span class="sxs-lookup"><span data-stu-id="2215e-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="2215e-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2215e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="2215e-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2215e-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2215e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2215e-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2215e-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2215e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-268">Search-Flags</span></span>           | <span data-ttu-id="2215e-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2215e-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2215e-270">System-Flags</span></span>           | <span data-ttu-id="2215e-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2215e-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2215e-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2215e-272">Classes used in</span></span>        | [<span data-ttu-id="2215e-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="2215e-274">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="2215e-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





