---
title: ms-DS-supplémentaire-Sam-Account-Name (attribut)
description: Cet attribut est utilisé pour stocker les noms de compte SAM qui correspondent aux noms d’hôte DNS dans ms-DS-addition-DNS-Host-Name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-supplémentaire-Sam-Account-Name
- Schéma Active Directory de l’attribut msDS-AdditionalSamAccountName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515293"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="33120-105">ms-DS-supplémentaire-Sam-Account-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="33120-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="33120-106">Cet attribut est utilisé pour stocker les noms de compte SAM qui correspondent aux noms d’hôte DNS dans ms-DS-addition-DNS-Host-Name.</span><span class="sxs-lookup"><span data-stu-id="33120-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="33120-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-107">Entry</span></span> | <span data-ttu-id="33120-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="33120-109">CN</span><span class="sxs-lookup"><span data-stu-id="33120-109">CN</span></span>                | <span data-ttu-id="33120-110">ms-DS-supplémentaire-Sam-Account-Name</span><span class="sxs-lookup"><span data-stu-id="33120-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="33120-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="33120-111">Ldap-Display-Name</span></span> | <span data-ttu-id="33120-112">msDS-AdditionalSamAccountName</span><span class="sxs-lookup"><span data-stu-id="33120-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="33120-113">Taille</span><span class="sxs-lookup"><span data-stu-id="33120-113">Size</span></span>              | <span data-ttu-id="33120-114">Moins de 20 octets.</span><span class="sxs-lookup"><span data-stu-id="33120-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="33120-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="33120-115">Update Privilege</span></span>  | <span data-ttu-id="33120-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="33120-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="33120-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="33120-117">Update Frequency</span></span>  | <span data-ttu-id="33120-118">Lorsque le contrôleur de périphérique est renommé.</span><span class="sxs-lookup"><span data-stu-id="33120-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="33120-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33120-119">Attribute-Id</span></span>      | <span data-ttu-id="33120-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="33120-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="33120-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="33120-121">System-Id-Guid</span></span>    | <span data-ttu-id="33120-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="33120-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="33120-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33120-123">Syntax</span></span>            | [<span data-ttu-id="33120-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="33120-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="33120-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="33120-125">Implementations</span></span>

-   [<span data-ttu-id="33120-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33120-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33120-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33120-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33120-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33120-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33120-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33120-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33120-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33120-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="33120-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33120-131">Windows Server 2003</span></span>



| <span data-ttu-id="33120-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-132">Entry</span></span> | <span data-ttu-id="33120-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="33120-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="33120-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33120-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="33120-136">System-Only</span></span>            | <span data-ttu-id="33120-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-137">True</span></span>                                      |
| <span data-ttu-id="33120-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="33120-138">Is-Single-Valued</span></span>       | <span data-ttu-id="33120-139">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-139">False</span></span>                                     |
| <span data-ttu-id="33120-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="33120-140">Is Indexed</span></span>             | <span data-ttu-id="33120-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-141">True</span></span>                                      |
| <span data-ttu-id="33120-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="33120-142">In Global Catalog</span></span>      | <span data-ttu-id="33120-143">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-143">False</span></span>                                     |
| <span data-ttu-id="33120-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="33120-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="33120-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="33120-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="33120-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33120-146">Range-Lower</span></span>            | <span data-ttu-id="33120-147">0</span><span class="sxs-lookup"><span data-stu-id="33120-147">0</span></span>                                         |
| <span data-ttu-id="33120-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33120-148">Range-Upper</span></span>            | <span data-ttu-id="33120-149">256</span><span class="sxs-lookup"><span data-stu-id="33120-149">256</span></span>                                       |
| <span data-ttu-id="33120-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-150">Search-Flags</span></span>           | <span data-ttu-id="33120-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="33120-151">0x0000000D</span></span>                                |
| <span data-ttu-id="33120-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-152">System-Flags</span></span>           | <span data-ttu-id="33120-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33120-153">0x00000010</span></span>                                |
| <span data-ttu-id="33120-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="33120-154">Classes used in</span></span>        | [<span data-ttu-id="33120-155">**Computer**</span><span class="sxs-lookup"><span data-stu-id="33120-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33120-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33120-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33120-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-157">Entry</span></span> | <span data-ttu-id="33120-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="33120-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="33120-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33120-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="33120-161">System-Only</span></span>            | <span data-ttu-id="33120-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-162">True</span></span>                                      |
| <span data-ttu-id="33120-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="33120-163">Is-Single-Valued</span></span>       | <span data-ttu-id="33120-164">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-164">False</span></span>                                     |
| <span data-ttu-id="33120-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="33120-165">Is Indexed</span></span>             | <span data-ttu-id="33120-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-166">True</span></span>                                      |
| <span data-ttu-id="33120-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="33120-167">In Global Catalog</span></span>      | <span data-ttu-id="33120-168">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-168">False</span></span>                                     |
| <span data-ttu-id="33120-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="33120-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="33120-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="33120-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="33120-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33120-171">Range-Lower</span></span>            | <span data-ttu-id="33120-172">0</span><span class="sxs-lookup"><span data-stu-id="33120-172">0</span></span>                                         |
| <span data-ttu-id="33120-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33120-173">Range-Upper</span></span>            | <span data-ttu-id="33120-174">256</span><span class="sxs-lookup"><span data-stu-id="33120-174">256</span></span>                                       |
| <span data-ttu-id="33120-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-175">Search-Flags</span></span>           | <span data-ttu-id="33120-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="33120-176">0x0000000D</span></span>                                |
| <span data-ttu-id="33120-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-177">System-Flags</span></span>           | <span data-ttu-id="33120-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33120-178">0x00000010</span></span>                                |
| <span data-ttu-id="33120-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="33120-179">Classes used in</span></span>        | [<span data-ttu-id="33120-180">**Computer**</span><span class="sxs-lookup"><span data-stu-id="33120-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="33120-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33120-181">Windows Server 2008</span></span>



| <span data-ttu-id="33120-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-182">Entry</span></span> | <span data-ttu-id="33120-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="33120-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="33120-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33120-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="33120-186">System-Only</span></span>            | <span data-ttu-id="33120-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-187">True</span></span>                                      |
| <span data-ttu-id="33120-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="33120-188">Is-Single-Valued</span></span>       | <span data-ttu-id="33120-189">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-189">False</span></span>                                     |
| <span data-ttu-id="33120-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="33120-190">Is Indexed</span></span>             | <span data-ttu-id="33120-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-191">True</span></span>                                      |
| <span data-ttu-id="33120-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="33120-192">In Global Catalog</span></span>      | <span data-ttu-id="33120-193">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-193">False</span></span>                                     |
| <span data-ttu-id="33120-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="33120-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="33120-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="33120-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="33120-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33120-196">Range-Lower</span></span>            | <span data-ttu-id="33120-197">0</span><span class="sxs-lookup"><span data-stu-id="33120-197">0</span></span>                                         |
| <span data-ttu-id="33120-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33120-198">Range-Upper</span></span>            | <span data-ttu-id="33120-199">256</span><span class="sxs-lookup"><span data-stu-id="33120-199">256</span></span>                                       |
| <span data-ttu-id="33120-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-200">Search-Flags</span></span>           | <span data-ttu-id="33120-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="33120-201">0x0000000D</span></span>                                |
| <span data-ttu-id="33120-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-202">System-Flags</span></span>           | <span data-ttu-id="33120-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33120-203">0x00000010</span></span>                                |
| <span data-ttu-id="33120-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="33120-204">Classes used in</span></span>        | [<span data-ttu-id="33120-205">**Computer**</span><span class="sxs-lookup"><span data-stu-id="33120-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33120-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33120-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33120-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-207">Entry</span></span> | <span data-ttu-id="33120-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="33120-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="33120-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33120-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="33120-211">System-Only</span></span>            | <span data-ttu-id="33120-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-212">True</span></span>                                      |
| <span data-ttu-id="33120-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="33120-213">Is-Single-Valued</span></span>       | <span data-ttu-id="33120-214">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-214">False</span></span>                                     |
| <span data-ttu-id="33120-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="33120-215">Is Indexed</span></span>             | <span data-ttu-id="33120-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-216">True</span></span>                                      |
| <span data-ttu-id="33120-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="33120-217">In Global Catalog</span></span>      | <span data-ttu-id="33120-218">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-218">False</span></span>                                     |
| <span data-ttu-id="33120-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="33120-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="33120-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="33120-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="33120-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33120-221">Range-Lower</span></span>            | <span data-ttu-id="33120-222">0</span><span class="sxs-lookup"><span data-stu-id="33120-222">0</span></span>                                         |
| <span data-ttu-id="33120-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33120-223">Range-Upper</span></span>            | <span data-ttu-id="33120-224">256</span><span class="sxs-lookup"><span data-stu-id="33120-224">256</span></span>                                       |
| <span data-ttu-id="33120-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-225">Search-Flags</span></span>           | <span data-ttu-id="33120-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="33120-226">0x0000000D</span></span>                                |
| <span data-ttu-id="33120-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-227">System-Flags</span></span>           | <span data-ttu-id="33120-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33120-228">0x00000010</span></span>                                |
| <span data-ttu-id="33120-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="33120-229">Classes used in</span></span>        | [<span data-ttu-id="33120-230">**Computer**</span><span class="sxs-lookup"><span data-stu-id="33120-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="33120-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33120-231">Windows Server 2012</span></span>



| <span data-ttu-id="33120-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="33120-232">Entry</span></span> | <span data-ttu-id="33120-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="33120-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="33120-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="33120-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33120-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="33120-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="33120-236">System-Only</span></span>            | <span data-ttu-id="33120-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-237">True</span></span>                                      |
| <span data-ttu-id="33120-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="33120-238">Is-Single-Valued</span></span>       | <span data-ttu-id="33120-239">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-239">False</span></span>                                     |
| <span data-ttu-id="33120-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="33120-240">Is Indexed</span></span>             | <span data-ttu-id="33120-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="33120-241">True</span></span>                                      |
| <span data-ttu-id="33120-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="33120-242">In Global Catalog</span></span>      | <span data-ttu-id="33120-243">Faux</span><span class="sxs-lookup"><span data-stu-id="33120-243">False</span></span>                                     |
| <span data-ttu-id="33120-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="33120-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="33120-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="33120-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="33120-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33120-246">Range-Lower</span></span>            | <span data-ttu-id="33120-247">0</span><span class="sxs-lookup"><span data-stu-id="33120-247">0</span></span>                                         |
| <span data-ttu-id="33120-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33120-248">Range-Upper</span></span>            | <span data-ttu-id="33120-249">256</span><span class="sxs-lookup"><span data-stu-id="33120-249">256</span></span>                                       |
| <span data-ttu-id="33120-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-250">Search-Flags</span></span>           | <span data-ttu-id="33120-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="33120-251">0x0000000D</span></span>                                |
| <span data-ttu-id="33120-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33120-252">System-Flags</span></span>           | <span data-ttu-id="33120-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33120-253">0x00000010</span></span>                                |
| <span data-ttu-id="33120-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="33120-254">Classes used in</span></span>        | [<span data-ttu-id="33120-255">**Computer**</span><span class="sxs-lookup"><span data-stu-id="33120-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





