---
title: MS-SQL-attribut version
description: Version de l’instance actuelle de SQL Server.
ms.assetid: 0003892c-906d-429b-bc98-bbc441b2d58b
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-version
- Schéma AD de l’attribut mS-SQL-version
topic_type:
- apiref
api_name:
- MS-SQL-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a436a30311f5696d8ed63334b0cf796eb2767
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845542"
---
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="6ffd3-105">MS-SQL-attribut version</span><span class="sxs-lookup"><span data-stu-id="6ffd3-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="6ffd3-106">Version de l’instance actuelle de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ffd3-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="6ffd3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-107">Entry</span></span> | <span data-ttu-id="6ffd3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6ffd3-109">CN</span><span class="sxs-lookup"><span data-stu-id="6ffd3-109">CN</span></span>                | <span data-ttu-id="6ffd3-110">MS-SQL-version</span><span class="sxs-lookup"><span data-stu-id="6ffd3-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="6ffd3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6ffd3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6ffd3-112">mS-SQL-version</span><span class="sxs-lookup"><span data-stu-id="6ffd3-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="6ffd3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="6ffd3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6ffd3-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6ffd3-114">Update Privilege</span></span>  | <span data-ttu-id="6ffd3-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="6ffd3-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="6ffd3-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6ffd3-116">Update Frequency</span></span>  | <span data-ttu-id="6ffd3-117">Dans le programme d’installation du système.</span><span class="sxs-lookup"><span data-stu-id="6ffd3-117">At system setup.</span></span>                            |
| <span data-ttu-id="6ffd3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-118">Attribute-Id</span></span>      | <span data-ttu-id="6ffd3-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="6ffd3-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="6ffd3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6ffd3-120">System-Id-Guid</span></span>    | <span data-ttu-id="6ffd3-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="6ffd3-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="6ffd3-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ffd3-122">Syntax</span></span>            | [<span data-ttu-id="6ffd3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6ffd3-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6ffd3-124">Implementations</span></span>

-   [<span data-ttu-id="6ffd3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6ffd3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ffd3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ffd3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ffd3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ffd3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6ffd3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ffd3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6ffd3-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-132">Entry</span></span> | <span data-ttu-id="6ffd3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-136">System-Only</span></span>            | <span data-ttu-id="6ffd3-137">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-140">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-142">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-148">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-150">System-Flags</span></span>           | <span data-ttu-id="6ffd3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-152">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-153">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-154">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6ffd3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ffd3-155">Windows Server 2003</span></span>



| <span data-ttu-id="6ffd3-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-156">Entry</span></span> | <span data-ttu-id="6ffd3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-160">System-Only</span></span>            | <span data-ttu-id="6ffd3-161">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-164">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-166">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-172">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-174">System-Flags</span></span>           | <span data-ttu-id="6ffd3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-176">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-177">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-178">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ffd3-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ffd3-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ffd3-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-180">Entry</span></span> | <span data-ttu-id="6ffd3-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-184">System-Only</span></span>            | <span data-ttu-id="6ffd3-185">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-188">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-190">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-196">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-198">System-Flags</span></span>           | <span data-ttu-id="6ffd3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-200">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-201">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-202">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ffd3-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ffd3-203">Windows Server 2008</span></span>



| <span data-ttu-id="6ffd3-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-204">Entry</span></span> | <span data-ttu-id="6ffd3-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-208">System-Only</span></span>            | <span data-ttu-id="6ffd3-209">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-212">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-214">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-220">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-222">System-Flags</span></span>           | <span data-ttu-id="6ffd3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-224">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-225">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-226">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ffd3-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ffd3-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ffd3-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-228">Entry</span></span> | <span data-ttu-id="6ffd3-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-232">System-Only</span></span>            | <span data-ttu-id="6ffd3-233">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-236">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-238">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-244">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-246">System-Flags</span></span>           | <span data-ttu-id="6ffd3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-248">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-249">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-250">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ffd3-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ffd3-251">Windows Server 2012</span></span>



| <span data-ttu-id="6ffd3-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="6ffd3-252">Entry</span></span> | <span data-ttu-id="6ffd3-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffd3-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd3-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6ffd3-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ffd3-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ffd3-256">System-Only</span></span>            | <span data-ttu-id="6ffd3-257">Faux</span><span class="sxs-lookup"><span data-stu-id="6ffd3-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="6ffd3-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6ffd3-258">Is-Single-Valued</span></span>       | <span data-ttu-id="6ffd3-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6ffd3-260">Is Indexed</span></span>             | <span data-ttu-id="6ffd3-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6ffd3-262">In Global Catalog</span></span>      | <span data-ttu-id="6ffd3-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="6ffd3-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="6ffd3-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6ffd3-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ffd3-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6ffd3-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6ffd3-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ffd3-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ffd3-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6ffd3-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-268">Search-Flags</span></span>           | <span data-ttu-id="6ffd3-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ffd3-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ffd3-270">System-Flags</span></span>           | <span data-ttu-id="6ffd3-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ffd3-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6ffd3-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6ffd3-272">Classes used in</span></span>        | [<span data-ttu-id="6ffd3-273">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="6ffd3-274">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="6ffd3-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





