---
title: MS-SQL-attribut multiprotocole
description: Point de connexion RPC.
ms.assetid: 70cb9f80-7140-4c26-a1a4-f78a60de430f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut multiprotocole MS-SQL
- Schéma AD d’attribut multiprotocole mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-MultiProtocol
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cdfb8e42d8e3d533090b7b0bf49dcefc5492a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515694"
---
# <a name="ms-sql-multiprotocol-attribute"></a><span data-ttu-id="e1bf2-105">MS-SQL-attribut multiprotocole</span><span class="sxs-lookup"><span data-stu-id="e1bf2-105">MS-SQL-MultiProtocol attribute</span></span>

<span data-ttu-id="e1bf2-106">Point de connexion RPC.</span><span class="sxs-lookup"><span data-stu-id="e1bf2-106">The RPC connection point.</span></span>



| <span data-ttu-id="e1bf2-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-107">Entry</span></span> | <span data-ttu-id="e1bf2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e1bf2-109">CN</span><span class="sxs-lookup"><span data-stu-id="e1bf2-109">CN</span></span>                | <span data-ttu-id="e1bf2-110">MS-SQL-multiprotocole</span><span class="sxs-lookup"><span data-stu-id="e1bf2-110">MS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="e1bf2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e1bf2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e1bf2-112">mS-SQL-multiprotocole</span><span class="sxs-lookup"><span data-stu-id="e1bf2-112">mS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="e1bf2-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e1bf2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e1bf2-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e1bf2-114">Update Privilege</span></span>  | <span data-ttu-id="e1bf2-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e1bf2-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="e1bf2-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e1bf2-116">Update Frequency</span></span>  | <span data-ttu-id="e1bf2-117">Au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e1bf2-117">At system startup.</span></span>                          |
| <span data-ttu-id="e1bf2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-118">Attribute-Id</span></span>      | <span data-ttu-id="e1bf2-119">1.2.840.113556.1.4.1375</span><span class="sxs-lookup"><span data-stu-id="e1bf2-119">1.2.840.113556.1.4.1375</span></span>                     |
| <span data-ttu-id="e1bf2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e1bf2-120">System-Id-Guid</span></span>    | <span data-ttu-id="e1bf2-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e1bf2-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="e1bf2-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1bf2-122">Syntax</span></span>            | [<span data-ttu-id="e1bf2-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e1bf2-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e1bf2-124">Implementations</span></span>

-   [<span data-ttu-id="e1bf2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e1bf2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e1bf2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e1bf2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e1bf2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e1bf2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e1bf2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1bf2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e1bf2-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-132">Entry</span></span> | <span data-ttu-id="e1bf2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-136">System-Only</span></span>            | <span data-ttu-id="e1bf2-137">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-137">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-139">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-140">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-141">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-142">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-143">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-148">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-149">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-150">System-Flags</span></span>           | <span data-ttu-id="e1bf2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-151">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-152">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e1bf2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1bf2-154">Windows Server 2003</span></span>



| <span data-ttu-id="e1bf2-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-155">Entry</span></span> | <span data-ttu-id="e1bf2-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-159">System-Only</span></span>            | <span data-ttu-id="e1bf2-160">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-160">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-162">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-163">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-164">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-165">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-166">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-171">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-172">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-173">System-Flags</span></span>           | <span data-ttu-id="e1bf2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-174">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-175">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e1bf2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e1bf2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e1bf2-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-178">Entry</span></span> | <span data-ttu-id="e1bf2-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-182">System-Only</span></span>            | <span data-ttu-id="e1bf2-183">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-183">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-185">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-186">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-187">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-187">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-188">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-189">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-189">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-194">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-195">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-196">System-Flags</span></span>           | <span data-ttu-id="e1bf2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-197">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-198">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e1bf2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1bf2-200">Windows Server 2008</span></span>



| <span data-ttu-id="e1bf2-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-201">Entry</span></span> | <span data-ttu-id="e1bf2-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-205">System-Only</span></span>            | <span data-ttu-id="e1bf2-206">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-206">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-208">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-209">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-210">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-210">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-211">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-212">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-212">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-217">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-218">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-219">System-Flags</span></span>           | <span data-ttu-id="e1bf2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-220">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-221">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e1bf2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1bf2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e1bf2-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-224">Entry</span></span> | <span data-ttu-id="e1bf2-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-228">System-Only</span></span>            | <span data-ttu-id="e1bf2-229">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-229">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-231">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-232">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-233">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-233">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-234">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-235">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-235">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-240">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-241">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-242">System-Flags</span></span>           | <span data-ttu-id="e1bf2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-243">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-244">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e1bf2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1bf2-246">Windows Server 2012</span></span>



| <span data-ttu-id="e1bf2-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1bf2-247">Entry</span></span> | <span data-ttu-id="e1bf2-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf2-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e1bf2-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1bf2-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1bf2-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e1bf2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1bf2-251">System-Only</span></span>            | <span data-ttu-id="e1bf2-252">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-252">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1bf2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e1bf2-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1bf2-254">True</span></span>                                                      |
| <span data-ttu-id="e1bf2-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1bf2-255">Is Indexed</span></span>             | <span data-ttu-id="e1bf2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-256">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1bf2-257">In Global Catalog</span></span>      | <span data-ttu-id="e1bf2-258">Faux</span><span class="sxs-lookup"><span data-stu-id="e1bf2-258">False</span></span>                                                     |
| <span data-ttu-id="e1bf2-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1bf2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1bf2-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1bf2-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e1bf2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1bf2-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1bf2-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e1bf2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-263">Search-Flags</span></span>           | <span data-ttu-id="e1bf2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1bf2-264">0x00000000</span></span>                                                |
| <span data-ttu-id="e1bf2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1bf2-265">System-Flags</span></span>           | <span data-ttu-id="e1bf2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1bf2-266">0x00000010</span></span>                                                |
| <span data-ttu-id="e1bf2-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1bf2-267">Classes used in</span></span>        | [<span data-ttu-id="e1bf2-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e1bf2-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





