---
title: MS-SQL-attribut cluster
description: True si le serveur est en cluster.
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut en cluster MS-SQL
- Schéma AD d’attribut en cluster mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515100"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="09e2b-105">MS-SQL-attribut cluster</span><span class="sxs-lookup"><span data-stu-id="09e2b-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="09e2b-106">True si le serveur est en cluster.</span><span class="sxs-lookup"><span data-stu-id="09e2b-106">True if the server is clustered.</span></span>



| <span data-ttu-id="09e2b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-107">Entry</span></span> | <span data-ttu-id="09e2b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="09e2b-109">CN</span><span class="sxs-lookup"><span data-stu-id="09e2b-109">CN</span></span>                | <span data-ttu-id="09e2b-110">MS-SQL-Clustered</span><span class="sxs-lookup"><span data-stu-id="09e2b-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="09e2b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="09e2b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="09e2b-112">mS-SQL-Clustered</span><span class="sxs-lookup"><span data-stu-id="09e2b-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="09e2b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="09e2b-113">Size</span></span>              | <span data-ttu-id="09e2b-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="09e2b-114">4 bytes</span></span>                              |
| <span data-ttu-id="09e2b-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="09e2b-115">Update Privilege</span></span>  | <span data-ttu-id="09e2b-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="09e2b-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="09e2b-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="09e2b-117">Update Frequency</span></span>  | <span data-ttu-id="09e2b-118">Au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="09e2b-118">At system startup.</span></span>                   |
| <span data-ttu-id="09e2b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-119">Attribute-Id</span></span>      | <span data-ttu-id="09e2b-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="09e2b-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="09e2b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09e2b-121">System-Id-Guid</span></span>    | <span data-ttu-id="09e2b-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="09e2b-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="09e2b-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09e2b-123">Syntax</span></span>            | [<span data-ttu-id="09e2b-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="09e2b-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="09e2b-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="09e2b-125">Implementations</span></span>

-   [<span data-ttu-id="09e2b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09e2b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09e2b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09e2b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09e2b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09e2b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09e2b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09e2b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09e2b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09e2b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09e2b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09e2b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09e2b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09e2b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="09e2b-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-133">Entry</span></span> | <span data-ttu-id="09e2b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-137">System-Only</span></span>            | <span data-ttu-id="09e2b-138">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-138">False</span></span>                                                     |
| <span data-ttu-id="09e2b-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-140">True</span></span>                                                      |
| <span data-ttu-id="09e2b-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-141">Is Indexed</span></span>             | <span data-ttu-id="09e2b-142">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-142">False</span></span>                                                     |
| <span data-ttu-id="09e2b-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-143">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-144">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-144">False</span></span>                                                     |
| <span data-ttu-id="09e2b-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-149">Search-Flags</span></span>           | <span data-ttu-id="09e2b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-150">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-151">System-Flags</span></span>           | <span data-ttu-id="09e2b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-152">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-153">Classes used in</span></span>        | [<span data-ttu-id="09e2b-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09e2b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09e2b-155">Windows Server 2003</span></span>



| <span data-ttu-id="09e2b-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-156">Entry</span></span> | <span data-ttu-id="09e2b-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-160">System-Only</span></span>            | <span data-ttu-id="09e2b-161">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-161">False</span></span>                                                     |
| <span data-ttu-id="09e2b-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-163">True</span></span>                                                      |
| <span data-ttu-id="09e2b-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-164">Is Indexed</span></span>             | <span data-ttu-id="09e2b-165">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-165">False</span></span>                                                     |
| <span data-ttu-id="09e2b-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-166">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-167">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-167">False</span></span>                                                     |
| <span data-ttu-id="09e2b-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-172">Search-Flags</span></span>           | <span data-ttu-id="09e2b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-173">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-174">System-Flags</span></span>           | <span data-ttu-id="09e2b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-175">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-176">Classes used in</span></span>        | [<span data-ttu-id="09e2b-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09e2b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09e2b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09e2b-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-179">Entry</span></span> | <span data-ttu-id="09e2b-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-183">System-Only</span></span>            | <span data-ttu-id="09e2b-184">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-184">False</span></span>                                                     |
| <span data-ttu-id="09e2b-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-186">True</span></span>                                                      |
| <span data-ttu-id="09e2b-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-187">Is Indexed</span></span>             | <span data-ttu-id="09e2b-188">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-188">False</span></span>                                                     |
| <span data-ttu-id="09e2b-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-189">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-190">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-190">False</span></span>                                                     |
| <span data-ttu-id="09e2b-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-195">Search-Flags</span></span>           | <span data-ttu-id="09e2b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-196">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-197">System-Flags</span></span>           | <span data-ttu-id="09e2b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-198">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-199">Classes used in</span></span>        | [<span data-ttu-id="09e2b-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09e2b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e2b-201">Windows Server 2008</span></span>



| <span data-ttu-id="09e2b-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-202">Entry</span></span> | <span data-ttu-id="09e2b-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-206">System-Only</span></span>            | <span data-ttu-id="09e2b-207">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-207">False</span></span>                                                     |
| <span data-ttu-id="09e2b-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-209">True</span></span>                                                      |
| <span data-ttu-id="09e2b-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-210">Is Indexed</span></span>             | <span data-ttu-id="09e2b-211">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-211">False</span></span>                                                     |
| <span data-ttu-id="09e2b-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-212">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-213">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-213">False</span></span>                                                     |
| <span data-ttu-id="09e2b-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-218">Search-Flags</span></span>           | <span data-ttu-id="09e2b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-219">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-220">System-Flags</span></span>           | <span data-ttu-id="09e2b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-221">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-222">Classes used in</span></span>        | [<span data-ttu-id="09e2b-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09e2b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09e2b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09e2b-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-225">Entry</span></span> | <span data-ttu-id="09e2b-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-229">System-Only</span></span>            | <span data-ttu-id="09e2b-230">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-230">False</span></span>                                                     |
| <span data-ttu-id="09e2b-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-232">True</span></span>                                                      |
| <span data-ttu-id="09e2b-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-233">Is Indexed</span></span>             | <span data-ttu-id="09e2b-234">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-234">False</span></span>                                                     |
| <span data-ttu-id="09e2b-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-235">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-236">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-236">False</span></span>                                                     |
| <span data-ttu-id="09e2b-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-241">Search-Flags</span></span>           | <span data-ttu-id="09e2b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-242">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-243">System-Flags</span></span>           | <span data-ttu-id="09e2b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-244">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-245">Classes used in</span></span>        | [<span data-ttu-id="09e2b-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09e2b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09e2b-247">Windows Server 2012</span></span>



| <span data-ttu-id="09e2b-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="09e2b-248">Entry</span></span> | <span data-ttu-id="09e2b-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e2b-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09e2b-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09e2b-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e2b-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="09e2b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e2b-252">System-Only</span></span>            | <span data-ttu-id="09e2b-253">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-253">False</span></span>                                                     |
| <span data-ttu-id="09e2b-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09e2b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="09e2b-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="09e2b-255">True</span></span>                                                      |
| <span data-ttu-id="09e2b-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09e2b-256">Is Indexed</span></span>             | <span data-ttu-id="09e2b-257">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-257">False</span></span>                                                     |
| <span data-ttu-id="09e2b-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09e2b-258">In Global Catalog</span></span>      | <span data-ttu-id="09e2b-259">Faux</span><span class="sxs-lookup"><span data-stu-id="09e2b-259">False</span></span>                                                     |
| <span data-ttu-id="09e2b-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09e2b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e2b-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09e2b-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="09e2b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e2b-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e2b-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="09e2b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-264">Search-Flags</span></span>           | <span data-ttu-id="09e2b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09e2b-265">0x00000000</span></span>                                                |
| <span data-ttu-id="09e2b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e2b-266">System-Flags</span></span>           | <span data-ttu-id="09e2b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09e2b-267">0x00000010</span></span>                                                |
| <span data-ttu-id="09e2b-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09e2b-268">Classes used in</span></span>        | [<span data-ttu-id="09e2b-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="09e2b-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





