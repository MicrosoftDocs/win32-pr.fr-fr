---
title: Attribut de quota MS-DS-machine-Account
description: Nombre de comptes d’ordinateur qu’un utilisateur est autorisé à créer dans un domaine.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de quota MS-DS-machine-Account
- Schéma AD de l’attribut ms-DS-MachineAccountQuota
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107872"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="7bc16-105">Attribut de quota MS-DS-machine-Account</span><span class="sxs-lookup"><span data-stu-id="7bc16-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="7bc16-106">Nombre de comptes d’ordinateur qu’un utilisateur est autorisé à créer dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="7bc16-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="7bc16-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-107">Entry</span></span> | <span data-ttu-id="7bc16-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="7bc16-109">CN</span><span class="sxs-lookup"><span data-stu-id="7bc16-109">CN</span></span>                | <span data-ttu-id="7bc16-110">MS-DS-machine-Account-quota</span><span class="sxs-lookup"><span data-stu-id="7bc16-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="7bc16-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7bc16-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7bc16-112">ms-DS-MachineAccountQuota</span><span class="sxs-lookup"><span data-stu-id="7bc16-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="7bc16-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7bc16-113">Size</span></span>              | <span data-ttu-id="7bc16-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="7bc16-114">4 bytes</span></span>                                          |
| <span data-ttu-id="7bc16-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7bc16-115">Update Privilege</span></span>  | <span data-ttu-id="7bc16-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="7bc16-116">Domain administrator</span></span>                             |
| <span data-ttu-id="7bc16-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7bc16-117">Update Frequency</span></span>  | <span data-ttu-id="7bc16-118">Chaque fois que le quota d’un domaine doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="7bc16-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="7bc16-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-119">Attribute-Id</span></span>      | <span data-ttu-id="7bc16-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="7bc16-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="7bc16-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7bc16-121">System-Id-Guid</span></span>    | <span data-ttu-id="7bc16-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7bc16-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="7bc16-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bc16-123">Syntax</span></span>            | [<span data-ttu-id="7bc16-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="7bc16-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="7bc16-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7bc16-125">Implementations</span></span>

-   [<span data-ttu-id="7bc16-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7bc16-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7bc16-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7bc16-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7bc16-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7bc16-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7bc16-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bc16-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bc16-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bc16-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bc16-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bc16-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7bc16-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bc16-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7bc16-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-133">Entry</span></span> | <span data-ttu-id="7bc16-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-137">System-Only</span></span>            | <span data-ttu-id="7bc16-138">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-138">False</span></span>                                        |
| <span data-ttu-id="7bc16-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-140">True</span></span>                                         |
| <span data-ttu-id="7bc16-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-141">Is Indexed</span></span>             | <span data-ttu-id="7bc16-142">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-142">False</span></span>                                        |
| <span data-ttu-id="7bc16-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-143">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-144">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-144">False</span></span>                                        |
| <span data-ttu-id="7bc16-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-149">Search-Flags</span></span>           | <span data-ttu-id="7bc16-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-150">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-151">System-Flags</span></span>           | <span data-ttu-id="7bc16-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-152">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-153">Classes used in</span></span>        | [<span data-ttu-id="7bc16-154">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7bc16-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bc16-155">Windows Server 2003</span></span>



| <span data-ttu-id="7bc16-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-156">Entry</span></span> | <span data-ttu-id="7bc16-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-160">System-Only</span></span>            | <span data-ttu-id="7bc16-161">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-161">False</span></span>                                        |
| <span data-ttu-id="7bc16-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-163">True</span></span>                                         |
| <span data-ttu-id="7bc16-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-164">Is Indexed</span></span>             | <span data-ttu-id="7bc16-165">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-165">False</span></span>                                        |
| <span data-ttu-id="7bc16-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-166">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-167">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-167">False</span></span>                                        |
| <span data-ttu-id="7bc16-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-172">Search-Flags</span></span>           | <span data-ttu-id="7bc16-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-173">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-174">System-Flags</span></span>           | <span data-ttu-id="7bc16-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-175">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-176">Classes used in</span></span>        | [<span data-ttu-id="7bc16-177">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7bc16-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7bc16-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7bc16-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-179">Entry</span></span> | <span data-ttu-id="7bc16-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-183">System-Only</span></span>            | <span data-ttu-id="7bc16-184">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-184">False</span></span>                                        |
| <span data-ttu-id="7bc16-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-186">True</span></span>                                         |
| <span data-ttu-id="7bc16-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-187">Is Indexed</span></span>             | <span data-ttu-id="7bc16-188">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-188">False</span></span>                                        |
| <span data-ttu-id="7bc16-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-189">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-190">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-190">False</span></span>                                        |
| <span data-ttu-id="7bc16-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-195">Search-Flags</span></span>           | <span data-ttu-id="7bc16-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-196">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-197">System-Flags</span></span>           | <span data-ttu-id="7bc16-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-198">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-199">Classes used in</span></span>        | [<span data-ttu-id="7bc16-200">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7bc16-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bc16-201">Windows Server 2008</span></span>



| <span data-ttu-id="7bc16-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-202">Entry</span></span> | <span data-ttu-id="7bc16-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-206">System-Only</span></span>            | <span data-ttu-id="7bc16-207">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-207">False</span></span>                                        |
| <span data-ttu-id="7bc16-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-209">True</span></span>                                         |
| <span data-ttu-id="7bc16-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-210">Is Indexed</span></span>             | <span data-ttu-id="7bc16-211">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-211">False</span></span>                                        |
| <span data-ttu-id="7bc16-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-212">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-213">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-213">False</span></span>                                        |
| <span data-ttu-id="7bc16-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-218">Search-Flags</span></span>           | <span data-ttu-id="7bc16-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-219">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-220">System-Flags</span></span>           | <span data-ttu-id="7bc16-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-221">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-222">Classes used in</span></span>        | [<span data-ttu-id="7bc16-223">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bc16-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bc16-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bc16-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-225">Entry</span></span> | <span data-ttu-id="7bc16-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-229">System-Only</span></span>            | <span data-ttu-id="7bc16-230">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-230">False</span></span>                                        |
| <span data-ttu-id="7bc16-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-232">True</span></span>                                         |
| <span data-ttu-id="7bc16-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-233">Is Indexed</span></span>             | <span data-ttu-id="7bc16-234">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-234">False</span></span>                                        |
| <span data-ttu-id="7bc16-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-235">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-236">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-236">False</span></span>                                        |
| <span data-ttu-id="7bc16-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-241">Search-Flags</span></span>           | <span data-ttu-id="7bc16-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-242">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-243">System-Flags</span></span>           | <span data-ttu-id="7bc16-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-244">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-245">Classes used in</span></span>        | [<span data-ttu-id="7bc16-246">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bc16-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bc16-247">Windows Server 2012</span></span>



| <span data-ttu-id="7bc16-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="7bc16-248">Entry</span></span> | <span data-ttu-id="7bc16-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc16-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bc16-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7bc16-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc16-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bc16-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc16-252">System-Only</span></span>            | <span data-ttu-id="7bc16-253">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-253">False</span></span>                                        |
| <span data-ttu-id="7bc16-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7bc16-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc16-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="7bc16-255">True</span></span>                                         |
| <span data-ttu-id="7bc16-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7bc16-256">Is Indexed</span></span>             | <span data-ttu-id="7bc16-257">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-257">False</span></span>                                        |
| <span data-ttu-id="7bc16-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7bc16-258">In Global Catalog</span></span>      | <span data-ttu-id="7bc16-259">Faux</span><span class="sxs-lookup"><span data-stu-id="7bc16-259">False</span></span>                                        |
| <span data-ttu-id="7bc16-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7bc16-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc16-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7bc16-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bc16-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc16-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc16-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bc16-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-264">Search-Flags</span></span>           | <span data-ttu-id="7bc16-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc16-265">0x00000000</span></span>                                   |
| <span data-ttu-id="7bc16-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc16-266">System-Flags</span></span>           | <span data-ttu-id="7bc16-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc16-267">0x00000010</span></span>                                   |
| <span data-ttu-id="7bc16-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7bc16-268">Classes used in</span></span>        | [<span data-ttu-id="7bc16-269">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="7bc16-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





