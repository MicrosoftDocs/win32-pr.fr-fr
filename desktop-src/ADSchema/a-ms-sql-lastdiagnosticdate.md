---
title: Attribut MS-SQL-LastDiagnosticDate
description: Date de la dernière exécution de DBCC CHECKDB.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-LastDiagnosticDate
- Schéma AD de l’attribut mS-SQL-LastDiagnosticDate
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744317"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="c9c01-105">Attribut MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c9c01-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="c9c01-106">Date de la dernière exécution de DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="c9c01-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="c9c01-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-107">Entry</span></span> | <span data-ttu-id="c9c01-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9c01-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9c01-109">CN</span></span>                | <span data-ttu-id="c9c01-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c9c01-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="c9c01-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9c01-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9c01-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c9c01-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="c9c01-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c9c01-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9c01-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c9c01-114">Update Privilege</span></span>  | <span data-ttu-id="c9c01-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="c9c01-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="c9c01-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c9c01-116">Update Frequency</span></span>  | <span data-ttu-id="c9c01-117">Lors de l’exécution de DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="c9c01-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="c9c01-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-118">Attribute-Id</span></span>      | <span data-ttu-id="c9c01-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="c9c01-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="c9c01-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9c01-120">System-Id-Guid</span></span>    | <span data-ttu-id="c9c01-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c9c01-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="c9c01-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9c01-122">Syntax</span></span>            | [<span data-ttu-id="c9c01-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c9c01-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9c01-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c9c01-124">Implementations</span></span>

-   [<span data-ttu-id="c9c01-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9c01-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9c01-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9c01-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9c01-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9c01-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9c01-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9c01-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9c01-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9c01-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9c01-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9c01-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9c01-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9c01-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c9c01-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-132">Entry</span></span> | <span data-ttu-id="c9c01-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-136">System-Only</span></span>            | <span data-ttu-id="c9c01-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-137">False</span></span>                                                         |
| <span data-ttu-id="c9c01-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-139">True</span></span>                                                          |
| <span data-ttu-id="c9c01-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-140">Is Indexed</span></span>             | <span data-ttu-id="c9c01-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-141">False</span></span>                                                         |
| <span data-ttu-id="c9c01-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-142">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-143">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-143">False</span></span>                                                         |
| <span data-ttu-id="c9c01-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-148">Search-Flags</span></span>           | <span data-ttu-id="c9c01-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-150">System-Flags</span></span>           | <span data-ttu-id="c9c01-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-152">Classes used in</span></span>        | [<span data-ttu-id="c9c01-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9c01-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9c01-154">Windows Server 2003</span></span>



| <span data-ttu-id="c9c01-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-155">Entry</span></span> | <span data-ttu-id="c9c01-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-159">System-Only</span></span>            | <span data-ttu-id="c9c01-160">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-160">False</span></span>                                                         |
| <span data-ttu-id="c9c01-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-162">True</span></span>                                                          |
| <span data-ttu-id="c9c01-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-163">Is Indexed</span></span>             | <span data-ttu-id="c9c01-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-164">False</span></span>                                                         |
| <span data-ttu-id="c9c01-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-165">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-166">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-166">False</span></span>                                                         |
| <span data-ttu-id="c9c01-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-171">Search-Flags</span></span>           | <span data-ttu-id="c9c01-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-173">System-Flags</span></span>           | <span data-ttu-id="c9c01-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-175">Classes used in</span></span>        | [<span data-ttu-id="c9c01-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9c01-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9c01-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9c01-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-178">Entry</span></span> | <span data-ttu-id="c9c01-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-182">System-Only</span></span>            | <span data-ttu-id="c9c01-183">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-183">False</span></span>                                                         |
| <span data-ttu-id="c9c01-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-185">True</span></span>                                                          |
| <span data-ttu-id="c9c01-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-186">Is Indexed</span></span>             | <span data-ttu-id="c9c01-187">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-187">False</span></span>                                                         |
| <span data-ttu-id="c9c01-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-188">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-189">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-189">False</span></span>                                                         |
| <span data-ttu-id="c9c01-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-194">Search-Flags</span></span>           | <span data-ttu-id="c9c01-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-196">System-Flags</span></span>           | <span data-ttu-id="c9c01-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-198">Classes used in</span></span>        | [<span data-ttu-id="c9c01-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9c01-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9c01-200">Windows Server 2008</span></span>



| <span data-ttu-id="c9c01-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-201">Entry</span></span> | <span data-ttu-id="c9c01-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-205">System-Only</span></span>            | <span data-ttu-id="c9c01-206">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-206">False</span></span>                                                         |
| <span data-ttu-id="c9c01-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-208">True</span></span>                                                          |
| <span data-ttu-id="c9c01-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-209">Is Indexed</span></span>             | <span data-ttu-id="c9c01-210">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-210">False</span></span>                                                         |
| <span data-ttu-id="c9c01-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-211">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-212">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-212">False</span></span>                                                         |
| <span data-ttu-id="c9c01-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-217">Search-Flags</span></span>           | <span data-ttu-id="c9c01-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-219">System-Flags</span></span>           | <span data-ttu-id="c9c01-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-221">Classes used in</span></span>        | [<span data-ttu-id="c9c01-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9c01-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9c01-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9c01-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-224">Entry</span></span> | <span data-ttu-id="c9c01-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-228">System-Only</span></span>            | <span data-ttu-id="c9c01-229">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-229">False</span></span>                                                         |
| <span data-ttu-id="c9c01-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-231">True</span></span>                                                          |
| <span data-ttu-id="c9c01-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-232">Is Indexed</span></span>             | <span data-ttu-id="c9c01-233">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-233">False</span></span>                                                         |
| <span data-ttu-id="c9c01-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-234">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-235">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-235">False</span></span>                                                         |
| <span data-ttu-id="c9c01-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-240">Search-Flags</span></span>           | <span data-ttu-id="c9c01-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-242">System-Flags</span></span>           | <span data-ttu-id="c9c01-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-244">Classes used in</span></span>        | [<span data-ttu-id="c9c01-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9c01-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9c01-246">Windows Server 2012</span></span>



| <span data-ttu-id="c9c01-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9c01-247">Entry</span></span> | <span data-ttu-id="c9c01-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c01-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9c01-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9c01-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9c01-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c9c01-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9c01-251">System-Only</span></span>            | <span data-ttu-id="c9c01-252">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-252">False</span></span>                                                         |
| <span data-ttu-id="c9c01-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9c01-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c9c01-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9c01-254">True</span></span>                                                          |
| <span data-ttu-id="c9c01-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9c01-255">Is Indexed</span></span>             | <span data-ttu-id="c9c01-256">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-256">False</span></span>                                                         |
| <span data-ttu-id="c9c01-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9c01-257">In Global Catalog</span></span>      | <span data-ttu-id="c9c01-258">Faux</span><span class="sxs-lookup"><span data-stu-id="c9c01-258">False</span></span>                                                         |
| <span data-ttu-id="c9c01-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9c01-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9c01-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9c01-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c9c01-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9c01-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9c01-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c9c01-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-263">Search-Flags</span></span>           | <span data-ttu-id="c9c01-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9c01-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="c9c01-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9c01-265">System-Flags</span></span>           | <span data-ttu-id="c9c01-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9c01-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="c9c01-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9c01-267">Classes used in</span></span>        | [<span data-ttu-id="c9c01-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c9c01-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





