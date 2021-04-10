---
title: ACS-attribut Server-List
description: Contient les noms DNS des serveurs Windows NT qui sont autorisés à exécuter les services ACS.
ms.assetid: 1a26ba49-e9c9-4881-a7ce-7c91bf32875e
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ACS-Server-List
- Schéma AD de l’attribut aCSServerList
topic_type:
- apiref
api_name:
- ACS-Server-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74968d0c5b11502e2ba867bccfff246fb50cae80
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845642"
---
# <a name="acs-server-list-attribute"></a><span data-ttu-id="a2ab4-105">ACS-attribut Server-List</span><span class="sxs-lookup"><span data-stu-id="a2ab4-105">ACS-Server-List attribute</span></span>

<span data-ttu-id="a2ab4-106">Contient les noms DNS des serveurs Windows NT qui sont autorisés à exécuter les services ACS.</span><span class="sxs-lookup"><span data-stu-id="a2ab4-106">Contains the DNS names of Windows NT servers that are allowed to run ACS.</span></span>



| <span data-ttu-id="a2ab4-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-107">Entry</span></span> | <span data-ttu-id="a2ab4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a2ab4-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2ab4-109">CN</span></span>                | <span data-ttu-id="a2ab4-110">ACS-Server-List</span><span class="sxs-lookup"><span data-stu-id="a2ab4-110">ACS-Server-List</span></span>                             |
| <span data-ttu-id="a2ab4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a2ab4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2ab4-112">aCSServerList</span><span class="sxs-lookup"><span data-stu-id="a2ab4-112">aCSServerList</span></span>                               |
| <span data-ttu-id="a2ab4-113">Taille</span><span class="sxs-lookup"><span data-stu-id="a2ab4-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a2ab4-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a2ab4-114">Update Privilege</span></span>  | <span data-ttu-id="a2ab4-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="a2ab4-115">Domain administrator</span></span>                        |
| <span data-ttu-id="a2ab4-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a2ab4-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a2ab4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-117">Attribute-Id</span></span>      | <span data-ttu-id="a2ab4-118">1.2.840.113556.1.4.1312</span><span class="sxs-lookup"><span data-stu-id="a2ab4-118">1.2.840.113556.1.4.1312</span></span>                     |
| <span data-ttu-id="a2ab4-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2ab4-119">System-Id-Guid</span></span>    | <span data-ttu-id="a2ab4-120">7cbd59a5-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="a2ab4-120">7cbd59a5-3b90-11d2-90cc-00c04fd91ab1</span></span>        |
| <span data-ttu-id="a2ab4-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2ab4-121">Syntax</span></span>            | [<span data-ttu-id="a2ab4-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a2ab4-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a2ab4-123">Implementations</span></span>

-   [<span data-ttu-id="a2ab4-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2ab4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2ab4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2ab4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2ab4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2ab4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2ab4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2ab4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a2ab4-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-131">Entry</span></span> | <span data-ttu-id="a2ab4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-135">System-Only</span></span>            | <span data-ttu-id="a2ab4-136">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-136">False</span></span>                                        |
| <span data-ttu-id="a2ab4-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-138">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-138">False</span></span>                                        |
| <span data-ttu-id="a2ab4-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-139">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-140">False</span></span>                                        |
| <span data-ttu-id="a2ab4-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-141">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-142">False</span></span>                                        |
| <span data-ttu-id="a2ab4-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-147">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-148">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-149">System-Flags</span></span>           | <span data-ttu-id="a2ab4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-150">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-151">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-152">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2ab4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2ab4-153">Windows Server 2003</span></span>



| <span data-ttu-id="a2ab4-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-154">Entry</span></span> | <span data-ttu-id="a2ab4-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-158">System-Only</span></span>            | <span data-ttu-id="a2ab4-159">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-159">False</span></span>                                        |
| <span data-ttu-id="a2ab4-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-161">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-161">False</span></span>                                        |
| <span data-ttu-id="a2ab4-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-162">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-163">False</span></span>                                        |
| <span data-ttu-id="a2ab4-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-164">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-165">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-165">False</span></span>                                        |
| <span data-ttu-id="a2ab4-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-170">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-171">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-172">System-Flags</span></span>           | <span data-ttu-id="a2ab4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-173">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-174">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-175">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2ab4-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2ab4-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2ab4-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-177">Entry</span></span> | <span data-ttu-id="a2ab4-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-181">System-Only</span></span>            | <span data-ttu-id="a2ab4-182">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-182">False</span></span>                                        |
| <span data-ttu-id="a2ab4-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-184">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-184">False</span></span>                                        |
| <span data-ttu-id="a2ab4-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-185">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-186">False</span></span>                                        |
| <span data-ttu-id="a2ab4-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-187">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-188">False</span></span>                                        |
| <span data-ttu-id="a2ab4-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-193">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-194">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-195">System-Flags</span></span>           | <span data-ttu-id="a2ab4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-196">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-197">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-198">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2ab4-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2ab4-199">Windows Server 2008</span></span>



| <span data-ttu-id="a2ab4-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-200">Entry</span></span> | <span data-ttu-id="a2ab4-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-204">System-Only</span></span>            | <span data-ttu-id="a2ab4-205">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-205">False</span></span>                                        |
| <span data-ttu-id="a2ab4-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-207">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-207">False</span></span>                                        |
| <span data-ttu-id="a2ab4-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-208">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-209">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-209">False</span></span>                                        |
| <span data-ttu-id="a2ab4-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-210">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-211">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-211">False</span></span>                                        |
| <span data-ttu-id="a2ab4-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-216">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-217">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-218">System-Flags</span></span>           | <span data-ttu-id="a2ab4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-219">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-220">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-221">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2ab4-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2ab4-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2ab4-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-223">Entry</span></span> | <span data-ttu-id="a2ab4-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-227">System-Only</span></span>            | <span data-ttu-id="a2ab4-228">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-228">False</span></span>                                        |
| <span data-ttu-id="a2ab4-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-230">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-230">False</span></span>                                        |
| <span data-ttu-id="a2ab4-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-231">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-232">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-232">False</span></span>                                        |
| <span data-ttu-id="a2ab4-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-233">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-234">False</span></span>                                        |
| <span data-ttu-id="a2ab4-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-239">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-240">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-241">System-Flags</span></span>           | <span data-ttu-id="a2ab4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-242">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-243">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-244">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2ab4-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2ab4-245">Windows Server 2012</span></span>



| <span data-ttu-id="a2ab4-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2ab4-246">Entry</span></span> | <span data-ttu-id="a2ab4-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ab4-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2ab4-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2ab4-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ab4-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2ab4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ab4-250">System-Only</span></span>            | <span data-ttu-id="a2ab4-251">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-251">False</span></span>                                        |
| <span data-ttu-id="a2ab4-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2ab4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ab4-253">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-253">False</span></span>                                        |
| <span data-ttu-id="a2ab4-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2ab4-254">Is Indexed</span></span>             | <span data-ttu-id="a2ab4-255">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-255">False</span></span>                                        |
| <span data-ttu-id="a2ab4-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2ab4-256">In Global Catalog</span></span>      | <span data-ttu-id="a2ab4-257">Faux</span><span class="sxs-lookup"><span data-stu-id="a2ab4-257">False</span></span>                                        |
| <span data-ttu-id="a2ab4-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2ab4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ab4-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2ab4-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2ab4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ab4-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ab4-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2ab4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-262">Search-Flags</span></span>           | <span data-ttu-id="a2ab4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ab4-263">0x00000000</span></span>                                   |
| <span data-ttu-id="a2ab4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ab4-264">System-Flags</span></span>           | <span data-ttu-id="a2ab4-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ab4-265">0x00000010</span></span>                                   |
| <span data-ttu-id="a2ab4-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2ab4-266">Classes used in</span></span>        | [<span data-ttu-id="a2ab4-267">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a2ab4-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





