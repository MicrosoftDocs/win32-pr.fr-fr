---
title: attribut ms-DS-allowed-suffixes DNS
description: Liste des suffixes autorisés pour l’attribut dNSHostName dans les objets ordinateur.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-allowed-DNS-suffixes
- Schéma AD de l’attribut msDS-AllowedDNSSuffixes
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744748"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="7ff95-105">attribut ms-DS-allowed-suffixes DNS</span><span class="sxs-lookup"><span data-stu-id="7ff95-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="7ff95-106">Liste des suffixes autorisés pour l’attribut dNSHostName dans les objets ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ff95-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="7ff95-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-107">Entry</span></span> | <span data-ttu-id="7ff95-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7ff95-109">CN</span><span class="sxs-lookup"><span data-stu-id="7ff95-109">CN</span></span>                | <span data-ttu-id="7ff95-110">ms-DS-autorisé-DNS-suffixes</span><span class="sxs-lookup"><span data-stu-id="7ff95-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="7ff95-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7ff95-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7ff95-112">msDS-AllowedDNSSuffixes</span><span class="sxs-lookup"><span data-stu-id="7ff95-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="7ff95-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7ff95-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7ff95-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7ff95-114">Update Privilege</span></span>  | <span data-ttu-id="7ff95-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="7ff95-115">Domain administrator</span></span>                        |
| <span data-ttu-id="7ff95-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7ff95-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7ff95-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-117">Attribute-Id</span></span>      | <span data-ttu-id="7ff95-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="7ff95-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="7ff95-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7ff95-119">System-Id-Guid</span></span>    | <span data-ttu-id="7ff95-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="7ff95-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="7ff95-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ff95-121">Syntax</span></span>            | [<span data-ttu-id="7ff95-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7ff95-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7ff95-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7ff95-123">Implementations</span></span>

-   [<span data-ttu-id="7ff95-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ff95-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ff95-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7ff95-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7ff95-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ff95-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ff95-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ff95-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ff95-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ff95-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ff95-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ff95-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7ff95-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ff95-130">Windows Server 2003</span></span>



| <span data-ttu-id="7ff95-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-131">Entry</span></span> | <span data-ttu-id="7ff95-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-135">System-Only</span></span>            | <span data-ttu-id="7ff95-136">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-136">False</span></span>                                        |
| <span data-ttu-id="7ff95-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-138">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-138">False</span></span>                                        |
| <span data-ttu-id="7ff95-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-139">Is Indexed</span></span>             | <span data-ttu-id="7ff95-140">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-140">False</span></span>                                        |
| <span data-ttu-id="7ff95-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-141">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-142">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-142">False</span></span>                                        |
| <span data-ttu-id="7ff95-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-145">Range-Lower</span></span>            | <span data-ttu-id="7ff95-146">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-146">0</span></span>                                            |
| <span data-ttu-id="7ff95-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-147">Range-Upper</span></span>            | <span data-ttu-id="7ff95-148">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-148">2048</span></span>                                         |
| <span data-ttu-id="7ff95-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-149">Search-Flags</span></span>           | <span data-ttu-id="7ff95-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-150">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-151">System-Flags</span></span>           | <span data-ttu-id="7ff95-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-152">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-153">Classes used in</span></span>        | [<span data-ttu-id="7ff95-154">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7ff95-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="7ff95-155">ADAM</span></span>



| <span data-ttu-id="7ff95-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-156">Entry</span></span> | <span data-ttu-id="7ff95-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-160">System-Only</span></span>            | <span data-ttu-id="7ff95-161">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-161">False</span></span>                                        |
| <span data-ttu-id="7ff95-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-163">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-163">False</span></span>                                        |
| <span data-ttu-id="7ff95-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-164">Is Indexed</span></span>             | <span data-ttu-id="7ff95-165">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-165">False</span></span>                                        |
| <span data-ttu-id="7ff95-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-166">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-167">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-167">False</span></span>                                        |
| <span data-ttu-id="7ff95-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-170">Range-Lower</span></span>            | <span data-ttu-id="7ff95-171">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-171">0</span></span>                                            |
| <span data-ttu-id="7ff95-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-172">Range-Upper</span></span>            | <span data-ttu-id="7ff95-173">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-173">2048</span></span>                                         |
| <span data-ttu-id="7ff95-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-174">Search-Flags</span></span>           | <span data-ttu-id="7ff95-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-175">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-176">System-Flags</span></span>           | <span data-ttu-id="7ff95-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-177">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-178">Classes used in</span></span>        | [<span data-ttu-id="7ff95-179">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ff95-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ff95-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ff95-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-181">Entry</span></span> | <span data-ttu-id="7ff95-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-185">System-Only</span></span>            | <span data-ttu-id="7ff95-186">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-186">False</span></span>                                        |
| <span data-ttu-id="7ff95-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-188">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-188">False</span></span>                                        |
| <span data-ttu-id="7ff95-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-189">Is Indexed</span></span>             | <span data-ttu-id="7ff95-190">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-190">False</span></span>                                        |
| <span data-ttu-id="7ff95-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-191">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-192">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-192">False</span></span>                                        |
| <span data-ttu-id="7ff95-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-195">Range-Lower</span></span>            | <span data-ttu-id="7ff95-196">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-196">0</span></span>                                            |
| <span data-ttu-id="7ff95-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-197">Range-Upper</span></span>            | <span data-ttu-id="7ff95-198">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-198">2048</span></span>                                         |
| <span data-ttu-id="7ff95-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-199">Search-Flags</span></span>           | <span data-ttu-id="7ff95-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-200">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-201">System-Flags</span></span>           | <span data-ttu-id="7ff95-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-202">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-203">Classes used in</span></span>        | [<span data-ttu-id="7ff95-204">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ff95-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ff95-205">Windows Server 2008</span></span>



| <span data-ttu-id="7ff95-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-206">Entry</span></span> | <span data-ttu-id="7ff95-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-210">System-Only</span></span>            | <span data-ttu-id="7ff95-211">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-211">False</span></span>                                        |
| <span data-ttu-id="7ff95-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-213">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-213">False</span></span>                                        |
| <span data-ttu-id="7ff95-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-214">Is Indexed</span></span>             | <span data-ttu-id="7ff95-215">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-215">False</span></span>                                        |
| <span data-ttu-id="7ff95-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-216">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-217">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-217">False</span></span>                                        |
| <span data-ttu-id="7ff95-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-220">Range-Lower</span></span>            | <span data-ttu-id="7ff95-221">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-221">0</span></span>                                            |
| <span data-ttu-id="7ff95-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-222">Range-Upper</span></span>            | <span data-ttu-id="7ff95-223">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-223">2048</span></span>                                         |
| <span data-ttu-id="7ff95-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-224">Search-Flags</span></span>           | <span data-ttu-id="7ff95-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-225">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-226">System-Flags</span></span>           | <span data-ttu-id="7ff95-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-227">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-228">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-228">Classes used in</span></span>        | [<span data-ttu-id="7ff95-229">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ff95-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ff95-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ff95-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-231">Entry</span></span> | <span data-ttu-id="7ff95-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-235">System-Only</span></span>            | <span data-ttu-id="7ff95-236">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-236">False</span></span>                                        |
| <span data-ttu-id="7ff95-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-237">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-238">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-238">False</span></span>                                        |
| <span data-ttu-id="7ff95-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-239">Is Indexed</span></span>             | <span data-ttu-id="7ff95-240">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-240">False</span></span>                                        |
| <span data-ttu-id="7ff95-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-241">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-242">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-242">False</span></span>                                        |
| <span data-ttu-id="7ff95-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-245">Range-Lower</span></span>            | <span data-ttu-id="7ff95-246">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-246">0</span></span>                                            |
| <span data-ttu-id="7ff95-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-247">Range-Upper</span></span>            | <span data-ttu-id="7ff95-248">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-248">2048</span></span>                                         |
| <span data-ttu-id="7ff95-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-249">Search-Flags</span></span>           | <span data-ttu-id="7ff95-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-250">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-251">System-Flags</span></span>           | <span data-ttu-id="7ff95-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-252">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-253">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-253">Classes used in</span></span>        | [<span data-ttu-id="7ff95-254">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ff95-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ff95-255">Windows Server 2012</span></span>



| <span data-ttu-id="7ff95-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff95-256">Entry</span></span> | <span data-ttu-id="7ff95-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff95-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7ff95-258">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff95-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff95-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7ff95-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff95-260">System-Only</span></span>            | <span data-ttu-id="7ff95-261">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-261">False</span></span>                                        |
| <span data-ttu-id="7ff95-262">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff95-262">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff95-263">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-263">False</span></span>                                        |
| <span data-ttu-id="7ff95-264">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff95-264">Is Indexed</span></span>             | <span data-ttu-id="7ff95-265">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-265">False</span></span>                                        |
| <span data-ttu-id="7ff95-266">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff95-266">In Global Catalog</span></span>      | <span data-ttu-id="7ff95-267">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff95-267">False</span></span>                                        |
| <span data-ttu-id="7ff95-268">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff95-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff95-269">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff95-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7ff95-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff95-270">Range-Lower</span></span>            | <span data-ttu-id="7ff95-271">0</span><span class="sxs-lookup"><span data-stu-id="7ff95-271">0</span></span>                                            |
| <span data-ttu-id="7ff95-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff95-272">Range-Upper</span></span>            | <span data-ttu-id="7ff95-273">2 048</span><span class="sxs-lookup"><span data-stu-id="7ff95-273">2048</span></span>                                         |
| <span data-ttu-id="7ff95-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-274">Search-Flags</span></span>           | <span data-ttu-id="7ff95-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff95-275">0x00000000</span></span>                                   |
| <span data-ttu-id="7ff95-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff95-276">System-Flags</span></span>           | <span data-ttu-id="7ff95-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff95-277">0x00000010</span></span>                                   |
| <span data-ttu-id="7ff95-278">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff95-278">Classes used in</span></span>        | [<span data-ttu-id="7ff95-279">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="7ff95-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





