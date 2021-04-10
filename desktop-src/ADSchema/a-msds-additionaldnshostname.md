---
title: ms-DS-addition-DNS-Host-Name (attribut)
description: L’attribut est utilisé pour stocker le nom d’hôte DNS supplémentaire d’un objet ordinateur. Cet attribut est utilisé au moment où un contrôleur de périphérique est renommé.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Additional-DNS-Host-Name
- Schéma Active Directory de l’attribut msDS-AdditionalDnsHostName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943183"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="00723-106">ms-DS-addition-DNS-Host-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="00723-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="00723-107">L’attribut est utilisé pour stocker le nom d’hôte DNS supplémentaire d’un objet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00723-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="00723-108">Cet attribut est utilisé au moment où un ordinateur est renommé, ou les noms sont gérés avec « NETDOM ComputerName ».</span><span class="sxs-lookup"><span data-stu-id="00723-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="00723-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-109">Entry</span></span> | <span data-ttu-id="00723-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="00723-111">CN</span><span class="sxs-lookup"><span data-stu-id="00723-111">CN</span></span>                | <span data-ttu-id="00723-112">ms-DS-supplémentaire-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="00723-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="00723-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="00723-113">Ldap-Display-Name</span></span> | <span data-ttu-id="00723-114">msDS-AdditionalDnsHostName</span><span class="sxs-lookup"><span data-stu-id="00723-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="00723-115">Taille</span><span class="sxs-lookup"><span data-stu-id="00723-115">Size</span></span>              | <span data-ttu-id="00723-116">Chaque valeur peut être de 2048 caractères.</span><span class="sxs-lookup"><span data-stu-id="00723-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="00723-117">Le nombre de valeurs correspond à la limite de la base de données d’environ 1200 valeurs.</span><span class="sxs-lookup"><span data-stu-id="00723-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="00723-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="00723-118">Update Privilege</span></span>  | <span data-ttu-id="00723-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="00723-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="00723-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="00723-120">Update Frequency</span></span>  | <span data-ttu-id="00723-121">Lorsqu’un ordinateur est renommé.</span><span class="sxs-lookup"><span data-stu-id="00723-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="00723-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00723-122">Attribute-Id</span></span>      | <span data-ttu-id="00723-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="00723-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="00723-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00723-124">System-Id-Guid</span></span>    | <span data-ttu-id="00723-125">80863791-dbe9-4EB8-837e-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="00723-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="00723-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00723-126">Syntax</span></span>            | [<span data-ttu-id="00723-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="00723-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="00723-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="00723-128">Implementations</span></span>

-   [<span data-ttu-id="00723-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00723-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00723-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00723-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00723-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00723-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00723-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00723-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00723-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00723-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="00723-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00723-134">Windows Server 2003</span></span>



| <span data-ttu-id="00723-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-135">Entry</span></span> | <span data-ttu-id="00723-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="00723-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00723-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00723-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="00723-139">System-Only</span></span>            | <span data-ttu-id="00723-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="00723-140">True</span></span>                                      |
| <span data-ttu-id="00723-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00723-141">Is-Single-Valued</span></span>       | <span data-ttu-id="00723-142">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-142">False</span></span>                                     |
| <span data-ttu-id="00723-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00723-143">Is Indexed</span></span>             | <span data-ttu-id="00723-144">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-144">False</span></span>                                     |
| <span data-ttu-id="00723-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00723-145">In Global Catalog</span></span>      | <span data-ttu-id="00723-146">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-146">False</span></span>                                     |
| <span data-ttu-id="00723-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00723-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="00723-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00723-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="00723-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00723-149">Range-Lower</span></span>            | <span data-ttu-id="00723-150">0</span><span class="sxs-lookup"><span data-stu-id="00723-150">0</span></span>                                         |
| <span data-ttu-id="00723-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00723-151">Range-Upper</span></span>            | <span data-ttu-id="00723-152">2 048</span><span class="sxs-lookup"><span data-stu-id="00723-152">2048</span></span>                                      |
| <span data-ttu-id="00723-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-153">Search-Flags</span></span>           | <span data-ttu-id="00723-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00723-154">0x00000000</span></span>                                |
| <span data-ttu-id="00723-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-155">System-Flags</span></span>           | <span data-ttu-id="00723-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00723-156">0x00000010</span></span>                                |
| <span data-ttu-id="00723-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00723-157">Classes used in</span></span>        | [<span data-ttu-id="00723-158">**Computer**</span><span class="sxs-lookup"><span data-stu-id="00723-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00723-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00723-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00723-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-160">Entry</span></span> | <span data-ttu-id="00723-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="00723-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00723-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00723-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="00723-164">System-Only</span></span>            | <span data-ttu-id="00723-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="00723-165">True</span></span>                                      |
| <span data-ttu-id="00723-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00723-166">Is-Single-Valued</span></span>       | <span data-ttu-id="00723-167">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-167">False</span></span>                                     |
| <span data-ttu-id="00723-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00723-168">Is Indexed</span></span>             | <span data-ttu-id="00723-169">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-169">False</span></span>                                     |
| <span data-ttu-id="00723-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00723-170">In Global Catalog</span></span>      | <span data-ttu-id="00723-171">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-171">False</span></span>                                     |
| <span data-ttu-id="00723-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00723-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="00723-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00723-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="00723-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00723-174">Range-Lower</span></span>            | <span data-ttu-id="00723-175">0</span><span class="sxs-lookup"><span data-stu-id="00723-175">0</span></span>                                         |
| <span data-ttu-id="00723-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00723-176">Range-Upper</span></span>            | <span data-ttu-id="00723-177">2 048</span><span class="sxs-lookup"><span data-stu-id="00723-177">2048</span></span>                                      |
| <span data-ttu-id="00723-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-178">Search-Flags</span></span>           | <span data-ttu-id="00723-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00723-179">0x00000000</span></span>                                |
| <span data-ttu-id="00723-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-180">System-Flags</span></span>           | <span data-ttu-id="00723-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00723-181">0x00000010</span></span>                                |
| <span data-ttu-id="00723-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00723-182">Classes used in</span></span>        | [<span data-ttu-id="00723-183">**Computer**</span><span class="sxs-lookup"><span data-stu-id="00723-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00723-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00723-184">Windows Server 2008</span></span>



| <span data-ttu-id="00723-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-185">Entry</span></span> | <span data-ttu-id="00723-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="00723-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00723-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00723-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="00723-189">System-Only</span></span>            | <span data-ttu-id="00723-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="00723-190">True</span></span>                                      |
| <span data-ttu-id="00723-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00723-191">Is-Single-Valued</span></span>       | <span data-ttu-id="00723-192">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-192">False</span></span>                                     |
| <span data-ttu-id="00723-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00723-193">Is Indexed</span></span>             | <span data-ttu-id="00723-194">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-194">False</span></span>                                     |
| <span data-ttu-id="00723-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00723-195">In Global Catalog</span></span>      | <span data-ttu-id="00723-196">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-196">False</span></span>                                     |
| <span data-ttu-id="00723-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00723-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="00723-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00723-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="00723-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00723-199">Range-Lower</span></span>            | <span data-ttu-id="00723-200">0</span><span class="sxs-lookup"><span data-stu-id="00723-200">0</span></span>                                         |
| <span data-ttu-id="00723-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00723-201">Range-Upper</span></span>            | <span data-ttu-id="00723-202">2 048</span><span class="sxs-lookup"><span data-stu-id="00723-202">2048</span></span>                                      |
| <span data-ttu-id="00723-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-203">Search-Flags</span></span>           | <span data-ttu-id="00723-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00723-204">0x00000000</span></span>                                |
| <span data-ttu-id="00723-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-205">System-Flags</span></span>           | <span data-ttu-id="00723-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00723-206">0x00000010</span></span>                                |
| <span data-ttu-id="00723-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00723-207">Classes used in</span></span>        | [<span data-ttu-id="00723-208">**Computer**</span><span class="sxs-lookup"><span data-stu-id="00723-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00723-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00723-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00723-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-210">Entry</span></span> | <span data-ttu-id="00723-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="00723-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00723-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00723-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="00723-214">System-Only</span></span>            | <span data-ttu-id="00723-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="00723-215">True</span></span>                                      |
| <span data-ttu-id="00723-216">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00723-216">Is-Single-Valued</span></span>       | <span data-ttu-id="00723-217">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-217">False</span></span>                                     |
| <span data-ttu-id="00723-218">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00723-218">Is Indexed</span></span>             | <span data-ttu-id="00723-219">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-219">False</span></span>                                     |
| <span data-ttu-id="00723-220">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00723-220">In Global Catalog</span></span>      | <span data-ttu-id="00723-221">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-221">False</span></span>                                     |
| <span data-ttu-id="00723-222">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00723-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="00723-223">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00723-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="00723-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00723-224">Range-Lower</span></span>            | <span data-ttu-id="00723-225">0</span><span class="sxs-lookup"><span data-stu-id="00723-225">0</span></span>                                         |
| <span data-ttu-id="00723-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00723-226">Range-Upper</span></span>            | <span data-ttu-id="00723-227">2 048</span><span class="sxs-lookup"><span data-stu-id="00723-227">2048</span></span>                                      |
| <span data-ttu-id="00723-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-228">Search-Flags</span></span>           | <span data-ttu-id="00723-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00723-229">0x00000000</span></span>                                |
| <span data-ttu-id="00723-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-230">System-Flags</span></span>           | <span data-ttu-id="00723-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00723-231">0x00000010</span></span>                                |
| <span data-ttu-id="00723-232">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00723-232">Classes used in</span></span>        | [<span data-ttu-id="00723-233">**Computer**</span><span class="sxs-lookup"><span data-stu-id="00723-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00723-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00723-234">Windows Server 2012</span></span>



| <span data-ttu-id="00723-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="00723-235">Entry</span></span> | <span data-ttu-id="00723-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="00723-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="00723-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00723-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00723-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="00723-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="00723-239">System-Only</span></span>            | <span data-ttu-id="00723-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="00723-240">True</span></span>                                      |
| <span data-ttu-id="00723-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00723-241">Is-Single-Valued</span></span>       | <span data-ttu-id="00723-242">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-242">False</span></span>                                     |
| <span data-ttu-id="00723-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00723-243">Is Indexed</span></span>             | <span data-ttu-id="00723-244">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-244">False</span></span>                                     |
| <span data-ttu-id="00723-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00723-245">In Global Catalog</span></span>      | <span data-ttu-id="00723-246">Faux</span><span class="sxs-lookup"><span data-stu-id="00723-246">False</span></span>                                     |
| <span data-ttu-id="00723-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00723-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="00723-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00723-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="00723-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00723-249">Range-Lower</span></span>            | <span data-ttu-id="00723-250">0</span><span class="sxs-lookup"><span data-stu-id="00723-250">0</span></span>                                         |
| <span data-ttu-id="00723-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00723-251">Range-Upper</span></span>            | <span data-ttu-id="00723-252">2 048</span><span class="sxs-lookup"><span data-stu-id="00723-252">2048</span></span>                                      |
| <span data-ttu-id="00723-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-253">Search-Flags</span></span>           | <span data-ttu-id="00723-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00723-254">0x00000000</span></span>                                |
| <span data-ttu-id="00723-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00723-255">System-Flags</span></span>           | <span data-ttu-id="00723-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00723-256">0x00000010</span></span>                                |
| <span data-ttu-id="00723-257">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00723-257">Classes used in</span></span>        | [<span data-ttu-id="00723-258">**Computer**</span><span class="sxs-lookup"><span data-stu-id="00723-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





