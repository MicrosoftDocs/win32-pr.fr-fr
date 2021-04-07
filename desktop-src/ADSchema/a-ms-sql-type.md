---
title: MS-SQL-attribut de type
description: Type de réplication utilisé par ce serveur SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de type MS-SQL
- Schéma AD d’attribut de type mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845545"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="11c38-105">MS-SQL-attribut de type</span><span class="sxs-lookup"><span data-stu-id="11c38-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="11c38-106">Type de réplication utilisé par ce serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11c38-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="11c38-107">Les valeurs suivantes sont les valeurs possibles pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="11c38-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="11c38-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-108">Value</span></span>        | <span data-ttu-id="11c38-109">Description</span><span class="sxs-lookup"><span data-stu-id="11c38-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="11c38-110">0</span><span class="sxs-lookup"><span data-stu-id="11c38-110">0</span></span><br/> | <span data-ttu-id="11c38-111">Réplication transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="11c38-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="11c38-112">1</span><span class="sxs-lookup"><span data-stu-id="11c38-112">1</span></span><br/> | <span data-ttu-id="11c38-113">Réplication d'instantané.</span><span class="sxs-lookup"><span data-stu-id="11c38-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="11c38-114">2</span><span class="sxs-lookup"><span data-stu-id="11c38-114">2</span></span><br/> | <span data-ttu-id="11c38-115">Réplication de fusion.</span><span class="sxs-lookup"><span data-stu-id="11c38-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="11c38-116">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-116">Entry</span></span> | <span data-ttu-id="11c38-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="11c38-118">CN</span><span class="sxs-lookup"><span data-stu-id="11c38-118">CN</span></span>                | <span data-ttu-id="11c38-119">Type MS-SQL</span><span class="sxs-lookup"><span data-stu-id="11c38-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="11c38-120">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="11c38-120">Ldap-Display-Name</span></span> | <span data-ttu-id="11c38-121">Type mS-SQL</span><span class="sxs-lookup"><span data-stu-id="11c38-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="11c38-122">Taille</span><span class="sxs-lookup"><span data-stu-id="11c38-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="11c38-123">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="11c38-123">Update Privilege</span></span>  | <span data-ttu-id="11c38-124">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="11c38-124">Domain administrator</span></span>                        |
| <span data-ttu-id="11c38-125">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="11c38-125">Update Frequency</span></span>  | <span data-ttu-id="11c38-126">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="11c38-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="11c38-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-127">Attribute-Id</span></span>      | <span data-ttu-id="11c38-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="11c38-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="11c38-129">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="11c38-129">System-Id-Guid</span></span>    | <span data-ttu-id="11c38-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="11c38-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="11c38-131">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11c38-131">Syntax</span></span>            | [<span data-ttu-id="11c38-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="11c38-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="11c38-133">Implémentations</span><span class="sxs-lookup"><span data-stu-id="11c38-133">Implementations</span></span>

-   [<span data-ttu-id="11c38-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="11c38-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="11c38-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="11c38-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="11c38-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="11c38-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="11c38-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="11c38-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="11c38-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="11c38-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="11c38-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="11c38-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="11c38-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11c38-140">Windows 2000 Server</span></span>



| <span data-ttu-id="11c38-141">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-141">Entry</span></span> | <span data-ttu-id="11c38-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-143">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-145">System-Only</span></span>            | <span data-ttu-id="11c38-146">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-147">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-147">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-149">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-149">Is Indexed</span></span>             | <span data-ttu-id="11c38-150">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-151">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-151">In Global Catalog</span></span>      | <span data-ttu-id="11c38-152">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-153">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-154">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-157">Search-Flags</span></span>           | <span data-ttu-id="11c38-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-159">System-Flags</span></span>           | <span data-ttu-id="11c38-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-161">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-161">Classes used in</span></span>        | [<span data-ttu-id="11c38-162">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-163">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="11c38-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11c38-164">Windows Server 2003</span></span>



| <span data-ttu-id="11c38-165">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-165">Entry</span></span> | <span data-ttu-id="11c38-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-167">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-169">System-Only</span></span>            | <span data-ttu-id="11c38-170">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-171">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-171">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-173">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-173">Is Indexed</span></span>             | <span data-ttu-id="11c38-174">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-175">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-175">In Global Catalog</span></span>      | <span data-ttu-id="11c38-176">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-177">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-178">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-181">Search-Flags</span></span>           | <span data-ttu-id="11c38-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-183">System-Flags</span></span>           | <span data-ttu-id="11c38-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-185">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-185">Classes used in</span></span>        | [<span data-ttu-id="11c38-186">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-187">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="11c38-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="11c38-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="11c38-189">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-189">Entry</span></span> | <span data-ttu-id="11c38-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-191">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-193">System-Only</span></span>            | <span data-ttu-id="11c38-194">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-195">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-197">Is Indexed</span></span>             | <span data-ttu-id="11c38-198">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-199">In Global Catalog</span></span>      | <span data-ttu-id="11c38-200">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-205">Search-Flags</span></span>           | <span data-ttu-id="11c38-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-207">System-Flags</span></span>           | <span data-ttu-id="11c38-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-209">Classes used in</span></span>        | [<span data-ttu-id="11c38-210">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-211">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="11c38-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11c38-212">Windows Server 2008</span></span>



| <span data-ttu-id="11c38-213">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-213">Entry</span></span> | <span data-ttu-id="11c38-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-215">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-217">System-Only</span></span>            | <span data-ttu-id="11c38-218">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-219">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-221">Is Indexed</span></span>             | <span data-ttu-id="11c38-222">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-223">In Global Catalog</span></span>      | <span data-ttu-id="11c38-224">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-229">Search-Flags</span></span>           | <span data-ttu-id="11c38-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-231">System-Flags</span></span>           | <span data-ttu-id="11c38-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-233">Classes used in</span></span>        | [<span data-ttu-id="11c38-234">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-235">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="11c38-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11c38-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="11c38-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-237">Entry</span></span> | <span data-ttu-id="11c38-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-241">System-Only</span></span>            | <span data-ttu-id="11c38-242">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-243">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-245">Is Indexed</span></span>             | <span data-ttu-id="11c38-246">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-247">In Global Catalog</span></span>      | <span data-ttu-id="11c38-248">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-253">Search-Flags</span></span>           | <span data-ttu-id="11c38-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-255">System-Flags</span></span>           | <span data-ttu-id="11c38-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-257">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-257">Classes used in</span></span>        | [<span data-ttu-id="11c38-258">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-259">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="11c38-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11c38-260">Windows Server 2012</span></span>



| <span data-ttu-id="11c38-261">Entrée</span><span class="sxs-lookup"><span data-stu-id="11c38-261">Entry</span></span> | <span data-ttu-id="11c38-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c38-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c38-263">ID de lien</span><span class="sxs-lookup"><span data-stu-id="11c38-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c38-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="11c38-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c38-265">System-Only</span></span>            | <span data-ttu-id="11c38-266">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-267">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="11c38-267">Is-Single-Valued</span></span>       | <span data-ttu-id="11c38-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="11c38-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="11c38-269">Est indexé</span><span class="sxs-lookup"><span data-stu-id="11c38-269">Is Indexed</span></span>             | <span data-ttu-id="11c38-270">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-271">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="11c38-271">In Global Catalog</span></span>      | <span data-ttu-id="11c38-272">Faux</span><span class="sxs-lookup"><span data-stu-id="11c38-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="11c38-273">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="11c38-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c38-274">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="11c38-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="11c38-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c38-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c38-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="11c38-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-277">Search-Flags</span></span>           | <span data-ttu-id="11c38-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c38-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c38-279">System-Flags</span></span>           | <span data-ttu-id="11c38-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c38-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="11c38-281">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="11c38-281">Classes used in</span></span>        | [<span data-ttu-id="11c38-282">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="11c38-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="11c38-283">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="11c38-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





