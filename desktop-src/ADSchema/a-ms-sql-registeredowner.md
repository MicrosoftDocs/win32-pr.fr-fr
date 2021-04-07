---
title: Attribut MS-SQL-RegisteredOwner
description: Propriétaire inscrit pour l’instance actuelle de SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-RegisteredOwner
- Schéma AD de l’attribut mS-SQL-RegisteredOwner
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745204"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="39509-105">Attribut MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="39509-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="39509-106">Propriétaire inscrit pour l’instance actuelle de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39509-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="39509-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-107">Entry</span></span> | <span data-ttu-id="39509-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="39509-109">CN</span><span class="sxs-lookup"><span data-stu-id="39509-109">CN</span></span>                | <span data-ttu-id="39509-110">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="39509-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="39509-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39509-111">Ldap-Display-Name</span></span> | <span data-ttu-id="39509-112">mS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="39509-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="39509-113">Taille</span><span class="sxs-lookup"><span data-stu-id="39509-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="39509-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="39509-114">Update Privilege</span></span>  | <span data-ttu-id="39509-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="39509-115">Domain administrator</span></span>                        |
| <span data-ttu-id="39509-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="39509-116">Update Frequency</span></span>  | <span data-ttu-id="39509-117">Dans le programme d’installation du système.</span><span class="sxs-lookup"><span data-stu-id="39509-117">At system setup.</span></span>                            |
| <span data-ttu-id="39509-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39509-118">Attribute-Id</span></span>      | <span data-ttu-id="39509-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="39509-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="39509-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39509-120">System-Id-Guid</span></span>    | <span data-ttu-id="39509-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="39509-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="39509-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39509-122">Syntax</span></span>            | [<span data-ttu-id="39509-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="39509-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="39509-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="39509-124">Implementations</span></span>

-   [<span data-ttu-id="39509-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39509-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39509-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39509-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39509-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39509-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39509-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39509-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39509-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39509-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39509-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39509-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39509-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39509-131">Windows 2000 Server</span></span>



| <span data-ttu-id="39509-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-132">Entry</span></span> | <span data-ttu-id="39509-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-136">System-Only</span></span>            | <span data-ttu-id="39509-137">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-138">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-140">Is Indexed</span></span>             | <span data-ttu-id="39509-141">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-142">In Global Catalog</span></span>      | <span data-ttu-id="39509-143">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-148">Search-Flags</span></span>           | <span data-ttu-id="39509-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-150">System-Flags</span></span>           | <span data-ttu-id="39509-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-152">Classes used in</span></span>        | [<span data-ttu-id="39509-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-154">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39509-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39509-155">Windows Server 2003</span></span>



| <span data-ttu-id="39509-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-156">Entry</span></span> | <span data-ttu-id="39509-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-160">System-Only</span></span>            | <span data-ttu-id="39509-161">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-162">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-164">Is Indexed</span></span>             | <span data-ttu-id="39509-165">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-166">In Global Catalog</span></span>      | <span data-ttu-id="39509-167">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-172">Search-Flags</span></span>           | <span data-ttu-id="39509-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-174">System-Flags</span></span>           | <span data-ttu-id="39509-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-176">Classes used in</span></span>        | [<span data-ttu-id="39509-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-178">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39509-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39509-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39509-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-180">Entry</span></span> | <span data-ttu-id="39509-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-184">System-Only</span></span>            | <span data-ttu-id="39509-185">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-186">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-188">Is Indexed</span></span>             | <span data-ttu-id="39509-189">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-190">In Global Catalog</span></span>      | <span data-ttu-id="39509-191">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-196">Search-Flags</span></span>           | <span data-ttu-id="39509-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-198">System-Flags</span></span>           | <span data-ttu-id="39509-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-200">Classes used in</span></span>        | [<span data-ttu-id="39509-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-202">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39509-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39509-203">Windows Server 2008</span></span>



| <span data-ttu-id="39509-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-204">Entry</span></span> | <span data-ttu-id="39509-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-208">System-Only</span></span>            | <span data-ttu-id="39509-209">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-210">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-212">Is Indexed</span></span>             | <span data-ttu-id="39509-213">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-214">In Global Catalog</span></span>      | <span data-ttu-id="39509-215">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-220">Search-Flags</span></span>           | <span data-ttu-id="39509-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-222">System-Flags</span></span>           | <span data-ttu-id="39509-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-224">Classes used in</span></span>        | [<span data-ttu-id="39509-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-226">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39509-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39509-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39509-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-228">Entry</span></span> | <span data-ttu-id="39509-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-232">System-Only</span></span>            | <span data-ttu-id="39509-233">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-234">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-236">Is Indexed</span></span>             | <span data-ttu-id="39509-237">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-238">In Global Catalog</span></span>      | <span data-ttu-id="39509-239">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-244">Search-Flags</span></span>           | <span data-ttu-id="39509-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-246">System-Flags</span></span>           | <span data-ttu-id="39509-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-248">Classes used in</span></span>        | [<span data-ttu-id="39509-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-250">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39509-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39509-251">Windows Server 2012</span></span>



| <span data-ttu-id="39509-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="39509-252">Entry</span></span> | <span data-ttu-id="39509-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="39509-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39509-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="39509-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39509-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="39509-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="39509-256">System-Only</span></span>            | <span data-ttu-id="39509-257">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="39509-258">Is-Single-Valued</span></span>       | <span data-ttu-id="39509-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="39509-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="39509-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="39509-260">Is Indexed</span></span>             | <span data-ttu-id="39509-261">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="39509-262">In Global Catalog</span></span>      | <span data-ttu-id="39509-263">Faux</span><span class="sxs-lookup"><span data-stu-id="39509-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="39509-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="39509-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="39509-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="39509-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="39509-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39509-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39509-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="39509-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-268">Search-Flags</span></span>           | <span data-ttu-id="39509-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39509-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="39509-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39509-270">System-Flags</span></span>           | <span data-ttu-id="39509-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39509-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="39509-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="39509-272">Classes used in</span></span>        | [<span data-ttu-id="39509-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="39509-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="39509-274">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="39509-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





