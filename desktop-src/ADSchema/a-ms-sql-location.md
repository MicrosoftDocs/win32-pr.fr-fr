---
title: MS-SQL-attribut d’emplacement
description: Chaîne définie par l’utilisateur. La valeur par défaut est l’emplacement.
ms.assetid: e0d8a83f-a979-49a8-a92d-842c18c8f9fd
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut d’emplacement MS-SQL
- Schéma Active Directory de l’attribut d’emplacement mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ffa71a40e7deff12385e0e45eb16d8dcc998269
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509146"
---
# <a name="ms-sql-location-attribute"></a><span data-ttu-id="593d8-106">MS-SQL-attribut d’emplacement</span><span class="sxs-lookup"><span data-stu-id="593d8-106">MS-SQL-Location attribute</span></span>

<span data-ttu-id="593d8-107">Chaîne définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="593d8-107">A user defined string.</span></span> <span data-ttu-id="593d8-108">La valeur par défaut est l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="593d8-108">Default is set to Location.</span></span>



| <span data-ttu-id="593d8-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-109">Entry</span></span> | <span data-ttu-id="593d8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="593d8-111">CN</span><span class="sxs-lookup"><span data-stu-id="593d8-111">CN</span></span>                | <span data-ttu-id="593d8-112">Emplacement MS-SQL-</span><span class="sxs-lookup"><span data-stu-id="593d8-112">MS-SQL-Location</span></span>                             |
| <span data-ttu-id="593d8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="593d8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="593d8-114">Emplacement mS-SQL-</span><span class="sxs-lookup"><span data-stu-id="593d8-114">mS-SQL-Location</span></span>                             |
| <span data-ttu-id="593d8-115">Taille</span><span class="sxs-lookup"><span data-stu-id="593d8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="593d8-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="593d8-116">Update Privilege</span></span>  | <span data-ttu-id="593d8-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="593d8-117">Domain administrator</span></span>                        |
| <span data-ttu-id="593d8-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="593d8-118">Update Frequency</span></span>  | <span data-ttu-id="593d8-119">Dans le programme d’installation du système.</span><span class="sxs-lookup"><span data-stu-id="593d8-119">At system setup.</span></span>                            |
| <span data-ttu-id="593d8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-120">Attribute-Id</span></span>      | <span data-ttu-id="593d8-121">1.2.840.113556.1.4.1366</span><span class="sxs-lookup"><span data-stu-id="593d8-121">1.2.840.113556.1.4.1366</span></span>                     |
| <span data-ttu-id="593d8-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="593d8-122">System-Id-Guid</span></span>    | <span data-ttu-id="593d8-123">561c9644-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="593d8-123">561c9644-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="593d8-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="593d8-124">Syntax</span></span>            | [<span data-ttu-id="593d8-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="593d8-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="593d8-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="593d8-126">Implementations</span></span>

-   [<span data-ttu-id="593d8-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="593d8-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="593d8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="593d8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="593d8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="593d8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="593d8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="593d8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="593d8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="593d8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="593d8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="593d8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="593d8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="593d8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="593d8-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-134">Entry</span></span> | <span data-ttu-id="593d8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-138">System-Only</span></span>            | <span data-ttu-id="593d8-139">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-139">False</span></span>                                                     |
| <span data-ttu-id="593d8-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-141">True</span></span>                                                      |
| <span data-ttu-id="593d8-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-142">Is Indexed</span></span>             | <span data-ttu-id="593d8-143">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-143">False</span></span>                                                     |
| <span data-ttu-id="593d8-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-144">In Global Catalog</span></span>      | <span data-ttu-id="593d8-145">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-145">False</span></span>                                                     |
| <span data-ttu-id="593d8-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-150">Search-Flags</span></span>           | <span data-ttu-id="593d8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-151">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-152">System-Flags</span></span>           | <span data-ttu-id="593d8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-153">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-154">Classes used in</span></span>        | [<span data-ttu-id="593d8-155">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="593d8-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="593d8-156">Windows Server 2003</span></span>



| <span data-ttu-id="593d8-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-157">Entry</span></span> | <span data-ttu-id="593d8-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-161">System-Only</span></span>            | <span data-ttu-id="593d8-162">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-162">False</span></span>                                                     |
| <span data-ttu-id="593d8-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-163">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-164">True</span></span>                                                      |
| <span data-ttu-id="593d8-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-165">Is Indexed</span></span>             | <span data-ttu-id="593d8-166">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-166">False</span></span>                                                     |
| <span data-ttu-id="593d8-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-167">In Global Catalog</span></span>      | <span data-ttu-id="593d8-168">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-168">False</span></span>                                                     |
| <span data-ttu-id="593d8-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-173">Search-Flags</span></span>           | <span data-ttu-id="593d8-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-174">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-175">System-Flags</span></span>           | <span data-ttu-id="593d8-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-176">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-177">Classes used in</span></span>        | [<span data-ttu-id="593d8-178">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-178">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="593d8-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="593d8-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="593d8-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-180">Entry</span></span> | <span data-ttu-id="593d8-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-184">System-Only</span></span>            | <span data-ttu-id="593d8-185">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-185">False</span></span>                                                     |
| <span data-ttu-id="593d8-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-187">True</span></span>                                                      |
| <span data-ttu-id="593d8-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-188">Is Indexed</span></span>             | <span data-ttu-id="593d8-189">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-189">False</span></span>                                                     |
| <span data-ttu-id="593d8-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-190">In Global Catalog</span></span>      | <span data-ttu-id="593d8-191">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-191">False</span></span>                                                     |
| <span data-ttu-id="593d8-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-196">Search-Flags</span></span>           | <span data-ttu-id="593d8-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-197">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-198">System-Flags</span></span>           | <span data-ttu-id="593d8-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-199">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-200">Classes used in</span></span>        | [<span data-ttu-id="593d8-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="593d8-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="593d8-202">Windows Server 2008</span></span>



| <span data-ttu-id="593d8-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-203">Entry</span></span> | <span data-ttu-id="593d8-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-207">System-Only</span></span>            | <span data-ttu-id="593d8-208">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-208">False</span></span>                                                     |
| <span data-ttu-id="593d8-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-209">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-210">True</span></span>                                                      |
| <span data-ttu-id="593d8-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-211">Is Indexed</span></span>             | <span data-ttu-id="593d8-212">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-212">False</span></span>                                                     |
| <span data-ttu-id="593d8-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-213">In Global Catalog</span></span>      | <span data-ttu-id="593d8-214">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-214">False</span></span>                                                     |
| <span data-ttu-id="593d8-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-219">Search-Flags</span></span>           | <span data-ttu-id="593d8-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-220">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-221">System-Flags</span></span>           | <span data-ttu-id="593d8-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-222">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-223">Classes used in</span></span>        | [<span data-ttu-id="593d8-224">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-224">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="593d8-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="593d8-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="593d8-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-226">Entry</span></span> | <span data-ttu-id="593d8-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-230">System-Only</span></span>            | <span data-ttu-id="593d8-231">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-231">False</span></span>                                                     |
| <span data-ttu-id="593d8-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-232">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-233">True</span></span>                                                      |
| <span data-ttu-id="593d8-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-234">Is Indexed</span></span>             | <span data-ttu-id="593d8-235">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-235">False</span></span>                                                     |
| <span data-ttu-id="593d8-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-236">In Global Catalog</span></span>      | <span data-ttu-id="593d8-237">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-237">False</span></span>                                                     |
| <span data-ttu-id="593d8-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-242">Search-Flags</span></span>           | <span data-ttu-id="593d8-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-243">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-244">System-Flags</span></span>           | <span data-ttu-id="593d8-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-245">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-246">Classes used in</span></span>        | [<span data-ttu-id="593d8-247">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-247">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="593d8-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="593d8-248">Windows Server 2012</span></span>



| <span data-ttu-id="593d8-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="593d8-249">Entry</span></span> | <span data-ttu-id="593d8-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d8-250">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="593d8-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="593d8-251">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="593d8-252">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="593d8-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="593d8-253">System-Only</span></span>            | <span data-ttu-id="593d8-254">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-254">False</span></span>                                                     |
| <span data-ttu-id="593d8-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="593d8-255">Is-Single-Valued</span></span>       | <span data-ttu-id="593d8-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="593d8-256">True</span></span>                                                      |
| <span data-ttu-id="593d8-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="593d8-257">Is Indexed</span></span>             | <span data-ttu-id="593d8-258">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-258">False</span></span>                                                     |
| <span data-ttu-id="593d8-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="593d8-259">In Global Catalog</span></span>      | <span data-ttu-id="593d8-260">Faux</span><span class="sxs-lookup"><span data-stu-id="593d8-260">False</span></span>                                                     |
| <span data-ttu-id="593d8-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="593d8-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="593d8-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="593d8-262">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="593d8-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="593d8-263">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="593d8-264">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="593d8-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-265">Search-Flags</span></span>           | <span data-ttu-id="593d8-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593d8-266">0x00000000</span></span>                                                |
| <span data-ttu-id="593d8-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="593d8-267">System-Flags</span></span>           | <span data-ttu-id="593d8-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="593d8-268">0x00000010</span></span>                                                |
| <span data-ttu-id="593d8-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="593d8-269">Classes used in</span></span>        | [<span data-ttu-id="593d8-270">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="593d8-270">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





