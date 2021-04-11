---
title: Attribut MS-SQL-NamedPipe
description: Connexion de canal nommé.
ms.assetid: d18c911d-06ed-4d08-b584-7b2748620770
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-SQL-NamedPipe
- Schéma AD de l’attribut mS-SQL-NamedPipe
topic_type:
- apiref
api_name:
- MS-SQL-NamedPipe
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e231be0561ae8c0e885911cb92954d6ff0d20d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385335"
---
# <a name="ms-sql-namedpipe-attribute"></a><span data-ttu-id="e849b-105">Attribut MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="e849b-105">MS-SQL-NamedPipe attribute</span></span>

<span data-ttu-id="e849b-106">Connexion de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="e849b-106">The named pipe connection.</span></span>



| <span data-ttu-id="e849b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-107">Entry</span></span> | <span data-ttu-id="e849b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e849b-109">CN</span><span class="sxs-lookup"><span data-stu-id="e849b-109">CN</span></span>                | <span data-ttu-id="e849b-110">MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="e849b-110">MS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="e849b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e849b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e849b-112">mS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="e849b-112">mS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="e849b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e849b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e849b-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e849b-114">Update Privilege</span></span>  | <span data-ttu-id="e849b-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e849b-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="e849b-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e849b-116">Update Frequency</span></span>  | <span data-ttu-id="e849b-117">Au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e849b-117">At system startup.</span></span>                          |
| <span data-ttu-id="e849b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-118">Attribute-Id</span></span>      | <span data-ttu-id="e849b-119">1.2.840.113556.1.4.1374</span><span class="sxs-lookup"><span data-stu-id="e849b-119">1.2.840.113556.1.4.1374</span></span>                     |
| <span data-ttu-id="e849b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e849b-120">System-Id-Guid</span></span>    | <span data-ttu-id="e849b-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e849b-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="e849b-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e849b-122">Syntax</span></span>            | [<span data-ttu-id="e849b-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e849b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e849b-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e849b-124">Implementations</span></span>

-   [<span data-ttu-id="e849b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e849b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e849b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e849b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e849b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e849b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e849b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e849b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e849b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e849b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e849b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e849b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e849b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e849b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e849b-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-132">Entry</span></span> | <span data-ttu-id="e849b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-136">System-Only</span></span>            | <span data-ttu-id="e849b-137">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-137">False</span></span>                                                     |
| <span data-ttu-id="e849b-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-139">True</span></span>                                                      |
| <span data-ttu-id="e849b-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-140">Is Indexed</span></span>             | <span data-ttu-id="e849b-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-141">False</span></span>                                                     |
| <span data-ttu-id="e849b-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-142">In Global Catalog</span></span>      | <span data-ttu-id="e849b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-143">False</span></span>                                                     |
| <span data-ttu-id="e849b-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-148">Search-Flags</span></span>           | <span data-ttu-id="e849b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-149">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-150">System-Flags</span></span>           | <span data-ttu-id="e849b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-151">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-152">Classes used in</span></span>        | [<span data-ttu-id="e849b-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e849b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e849b-154">Windows Server 2003</span></span>



| <span data-ttu-id="e849b-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-155">Entry</span></span> | <span data-ttu-id="e849b-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-159">System-Only</span></span>            | <span data-ttu-id="e849b-160">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-160">False</span></span>                                                     |
| <span data-ttu-id="e849b-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-162">True</span></span>                                                      |
| <span data-ttu-id="e849b-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-163">Is Indexed</span></span>             | <span data-ttu-id="e849b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-164">False</span></span>                                                     |
| <span data-ttu-id="e849b-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-165">In Global Catalog</span></span>      | <span data-ttu-id="e849b-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-166">False</span></span>                                                     |
| <span data-ttu-id="e849b-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-171">Search-Flags</span></span>           | <span data-ttu-id="e849b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-172">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-173">System-Flags</span></span>           | <span data-ttu-id="e849b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-174">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-175">Classes used in</span></span>        | [<span data-ttu-id="e849b-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e849b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e849b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e849b-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-178">Entry</span></span> | <span data-ttu-id="e849b-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-182">System-Only</span></span>            | <span data-ttu-id="e849b-183">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-183">False</span></span>                                                     |
| <span data-ttu-id="e849b-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-185">True</span></span>                                                      |
| <span data-ttu-id="e849b-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-186">Is Indexed</span></span>             | <span data-ttu-id="e849b-187">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-187">False</span></span>                                                     |
| <span data-ttu-id="e849b-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-188">In Global Catalog</span></span>      | <span data-ttu-id="e849b-189">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-189">False</span></span>                                                     |
| <span data-ttu-id="e849b-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-194">Search-Flags</span></span>           | <span data-ttu-id="e849b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-195">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-196">System-Flags</span></span>           | <span data-ttu-id="e849b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-197">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-198">Classes used in</span></span>        | [<span data-ttu-id="e849b-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e849b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e849b-200">Windows Server 2008</span></span>



| <span data-ttu-id="e849b-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-201">Entry</span></span> | <span data-ttu-id="e849b-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-205">System-Only</span></span>            | <span data-ttu-id="e849b-206">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-206">False</span></span>                                                     |
| <span data-ttu-id="e849b-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-208">True</span></span>                                                      |
| <span data-ttu-id="e849b-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-209">Is Indexed</span></span>             | <span data-ttu-id="e849b-210">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-210">False</span></span>                                                     |
| <span data-ttu-id="e849b-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-211">In Global Catalog</span></span>      | <span data-ttu-id="e849b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-212">False</span></span>                                                     |
| <span data-ttu-id="e849b-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-217">Search-Flags</span></span>           | <span data-ttu-id="e849b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-218">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-219">System-Flags</span></span>           | <span data-ttu-id="e849b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-220">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-221">Classes used in</span></span>        | [<span data-ttu-id="e849b-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e849b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e849b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e849b-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-224">Entry</span></span> | <span data-ttu-id="e849b-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-228">System-Only</span></span>            | <span data-ttu-id="e849b-229">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-229">False</span></span>                                                     |
| <span data-ttu-id="e849b-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-231">True</span></span>                                                      |
| <span data-ttu-id="e849b-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-232">Is Indexed</span></span>             | <span data-ttu-id="e849b-233">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-233">False</span></span>                                                     |
| <span data-ttu-id="e849b-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-234">In Global Catalog</span></span>      | <span data-ttu-id="e849b-235">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-235">False</span></span>                                                     |
| <span data-ttu-id="e849b-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-240">Search-Flags</span></span>           | <span data-ttu-id="e849b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-241">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-242">System-Flags</span></span>           | <span data-ttu-id="e849b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-243">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-244">Classes used in</span></span>        | [<span data-ttu-id="e849b-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e849b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e849b-246">Windows Server 2012</span></span>



| <span data-ttu-id="e849b-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="e849b-247">Entry</span></span> | <span data-ttu-id="e849b-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="e849b-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e849b-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e849b-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e849b-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e849b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e849b-251">System-Only</span></span>            | <span data-ttu-id="e849b-252">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-252">False</span></span>                                                     |
| <span data-ttu-id="e849b-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e849b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e849b-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="e849b-254">True</span></span>                                                      |
| <span data-ttu-id="e849b-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e849b-255">Is Indexed</span></span>             | <span data-ttu-id="e849b-256">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-256">False</span></span>                                                     |
| <span data-ttu-id="e849b-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e849b-257">In Global Catalog</span></span>      | <span data-ttu-id="e849b-258">Faux</span><span class="sxs-lookup"><span data-stu-id="e849b-258">False</span></span>                                                     |
| <span data-ttu-id="e849b-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e849b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e849b-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e849b-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e849b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e849b-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e849b-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e849b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-263">Search-Flags</span></span>           | <span data-ttu-id="e849b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e849b-264">0x00000000</span></span>                                                |
| <span data-ttu-id="e849b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e849b-265">System-Flags</span></span>           | <span data-ttu-id="e849b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e849b-266">0x00000010</span></span>                                                |
| <span data-ttu-id="e849b-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e849b-267">Classes used in</span></span>        | [<span data-ttu-id="e849b-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e849b-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





