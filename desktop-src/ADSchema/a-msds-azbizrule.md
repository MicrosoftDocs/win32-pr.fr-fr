---
title: ms-DS-AZ-biz-Rule Attribute
description: Texte du script qui implémente la règle d’entreprise.
ms.assetid: 884513ae-9600-49b0-a371-6f77b84b54f9
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-AZ-biz-Rule Attribute
- Schéma Active Directory de l’attribut msDS-AzBizRule
topic_type:
- apiref
api_name:
- ms-DS-Az-Biz-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571ab48c9742ffb93015c433685c01cb3a9666d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108158"
---
# <a name="ms-ds-az-biz-rule-attribute"></a><span data-ttu-id="85a0a-105">ms-DS-AZ-biz-Rule Attribute</span><span class="sxs-lookup"><span data-stu-id="85a0a-105">ms-DS-Az-Biz-Rule attribute</span></span>

<span data-ttu-id="85a0a-106">Texte du script qui implémente la règle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="85a0a-106">Text of the script implementing the business rule.</span></span>



| <span data-ttu-id="85a0a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-107">Entry</span></span> | <span data-ttu-id="85a0a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="85a0a-109">CN</span><span class="sxs-lookup"><span data-stu-id="85a0a-109">CN</span></span>                | <span data-ttu-id="85a0a-110">ms-DS-AZ-biz-Rule</span><span class="sxs-lookup"><span data-stu-id="85a0a-110">ms-DS-Az-Biz-Rule</span></span>                           |
| <span data-ttu-id="85a0a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="85a0a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="85a0a-112">msDS-AzBizRule</span><span class="sxs-lookup"><span data-stu-id="85a0a-112">msDS-AzBizRule</span></span>                              |
| <span data-ttu-id="85a0a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="85a0a-113">Size</span></span>              | <span data-ttu-id="85a0a-114">128 caractères</span><span class="sxs-lookup"><span data-stu-id="85a0a-114">128 characters</span></span>                              |
| <span data-ttu-id="85a0a-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="85a0a-115">Update Privilege</span></span>  | <span data-ttu-id="85a0a-116">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="85a0a-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="85a0a-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="85a0a-117">Update Frequency</span></span>  | <span data-ttu-id="85a0a-118">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="85a0a-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="85a0a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-119">Attribute-Id</span></span>      | <span data-ttu-id="85a0a-120">1.2.840.113556.1.4.1801</span><span class="sxs-lookup"><span data-stu-id="85a0a-120">1.2.840.113556.1.4.1801</span></span>                     |
| <span data-ttu-id="85a0a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="85a0a-121">System-Id-Guid</span></span>    | <span data-ttu-id="85a0a-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span><span class="sxs-lookup"><span data-stu-id="85a0a-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span></span>        |
| <span data-ttu-id="85a0a-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85a0a-123">Syntax</span></span>            | [<span data-ttu-id="85a0a-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="85a0a-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="85a0a-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="85a0a-125">Implementations</span></span>

-   [<span data-ttu-id="85a0a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85a0a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85a0a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85a0a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85a0a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85a0a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85a0a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85a0a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85a0a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85a0a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="85a0a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85a0a-131">Windows Server 2003</span></span>



| <span data-ttu-id="85a0a-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-132">Entry</span></span> | <span data-ttu-id="85a0a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-133">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="85a0a-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="85a0a-134">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="85a0a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="85a0a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a0a-136">System-Only</span></span>            | <span data-ttu-id="85a0a-137">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-137">False</span></span>                                             |
| <span data-ttu-id="85a0a-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="85a0a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="85a0a-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="85a0a-139">True</span></span>                                              |
| <span data-ttu-id="85a0a-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="85a0a-140">Is Indexed</span></span>             | <span data-ttu-id="85a0a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-141">False</span></span>                                             |
| <span data-ttu-id="85a0a-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="85a0a-142">In Global Catalog</span></span>      | <span data-ttu-id="85a0a-143">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-143">False</span></span>                                             |
| <span data-ttu-id="85a0a-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="85a0a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a0a-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="85a0a-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="85a0a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a0a-146">Range-Lower</span></span>            | <span data-ttu-id="85a0a-147">0</span><span class="sxs-lookup"><span data-stu-id="85a0a-147">0</span></span>                                                 |
| <span data-ttu-id="85a0a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a0a-148">Range-Upper</span></span>            | <span data-ttu-id="85a0a-149">65536</span><span class="sxs-lookup"><span data-stu-id="85a0a-149">65536</span></span>                                             |
| <span data-ttu-id="85a0a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-150">Search-Flags</span></span>           | <span data-ttu-id="85a0a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a0a-151">0x00000000</span></span>                                        |
| <span data-ttu-id="85a0a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-152">System-Flags</span></span>           | <span data-ttu-id="85a0a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a0a-153">0x00000010</span></span>                                        |
| <span data-ttu-id="85a0a-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="85a0a-154">Classes used in</span></span>        | [<span data-ttu-id="85a0a-155">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="85a0a-155">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85a0a-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85a0a-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85a0a-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-157">Entry</span></span> | <span data-ttu-id="85a0a-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-158">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="85a0a-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="85a0a-159">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="85a0a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-160">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="85a0a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a0a-161">System-Only</span></span>            | <span data-ttu-id="85a0a-162">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-162">False</span></span>                                             |
| <span data-ttu-id="85a0a-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="85a0a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="85a0a-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="85a0a-164">True</span></span>                                              |
| <span data-ttu-id="85a0a-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="85a0a-165">Is Indexed</span></span>             | <span data-ttu-id="85a0a-166">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-166">False</span></span>                                             |
| <span data-ttu-id="85a0a-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="85a0a-167">In Global Catalog</span></span>      | <span data-ttu-id="85a0a-168">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-168">False</span></span>                                             |
| <span data-ttu-id="85a0a-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="85a0a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a0a-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="85a0a-170">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="85a0a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a0a-171">Range-Lower</span></span>            | <span data-ttu-id="85a0a-172">0</span><span class="sxs-lookup"><span data-stu-id="85a0a-172">0</span></span>                                                 |
| <span data-ttu-id="85a0a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a0a-173">Range-Upper</span></span>            | <span data-ttu-id="85a0a-174">65536</span><span class="sxs-lookup"><span data-stu-id="85a0a-174">65536</span></span>                                             |
| <span data-ttu-id="85a0a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-175">Search-Flags</span></span>           | <span data-ttu-id="85a0a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a0a-176">0x00000000</span></span>                                        |
| <span data-ttu-id="85a0a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-177">System-Flags</span></span>           | <span data-ttu-id="85a0a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a0a-178">0x00000010</span></span>                                        |
| <span data-ttu-id="85a0a-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="85a0a-179">Classes used in</span></span>        | [<span data-ttu-id="85a0a-180">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="85a0a-180">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85a0a-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85a0a-181">Windows Server 2008</span></span>



| <span data-ttu-id="85a0a-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-182">Entry</span></span> | <span data-ttu-id="85a0a-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85a0a-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="85a0a-184">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-185">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a0a-186">System-Only</span></span>            | <span data-ttu-id="85a0a-187">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-187">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="85a0a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="85a0a-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="85a0a-189">True</span></span>                                                                                  |
| <span data-ttu-id="85a0a-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="85a0a-190">Is Indexed</span></span>             | <span data-ttu-id="85a0a-191">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-191">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="85a0a-192">In Global Catalog</span></span>      | <span data-ttu-id="85a0a-193">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-193">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="85a0a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a0a-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="85a0a-195">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="85a0a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a0a-196">Range-Lower</span></span>            | <span data-ttu-id="85a0a-197">0</span><span class="sxs-lookup"><span data-stu-id="85a0a-197">0</span></span>                                                                                     |
| <span data-ttu-id="85a0a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a0a-198">Range-Upper</span></span>            | <span data-ttu-id="85a0a-199">65536</span><span class="sxs-lookup"><span data-stu-id="85a0a-199">65536</span></span>                                                                                 |
| <span data-ttu-id="85a0a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-200">Search-Flags</span></span>           | <span data-ttu-id="85a0a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a0a-201">0x00000000</span></span>                                                                            |
| <span data-ttu-id="85a0a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-202">System-Flags</span></span>           | <span data-ttu-id="85a0a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a0a-203">0x00000010</span></span>                                                                            |
| <span data-ttu-id="85a0a-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="85a0a-204">Classes used in</span></span>        | [<span data-ttu-id="85a0a-205">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="85a0a-205">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="85a0a-206">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="85a0a-206">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85a0a-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85a0a-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85a0a-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-208">Entry</span></span> | <span data-ttu-id="85a0a-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85a0a-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="85a0a-210">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-211">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a0a-212">System-Only</span></span>            | <span data-ttu-id="85a0a-213">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-213">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="85a0a-214">Is-Single-Valued</span></span>       | <span data-ttu-id="85a0a-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="85a0a-215">True</span></span>                                                                                  |
| <span data-ttu-id="85a0a-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="85a0a-216">Is Indexed</span></span>             | <span data-ttu-id="85a0a-217">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-217">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="85a0a-218">In Global Catalog</span></span>      | <span data-ttu-id="85a0a-219">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-219">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="85a0a-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a0a-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="85a0a-221">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="85a0a-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a0a-222">Range-Lower</span></span>            | <span data-ttu-id="85a0a-223">0</span><span class="sxs-lookup"><span data-stu-id="85a0a-223">0</span></span>                                                                                     |
| <span data-ttu-id="85a0a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a0a-224">Range-Upper</span></span>            | <span data-ttu-id="85a0a-225">65536</span><span class="sxs-lookup"><span data-stu-id="85a0a-225">65536</span></span>                                                                                 |
| <span data-ttu-id="85a0a-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-226">Search-Flags</span></span>           | <span data-ttu-id="85a0a-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a0a-227">0x00000000</span></span>                                                                            |
| <span data-ttu-id="85a0a-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-228">System-Flags</span></span>           | <span data-ttu-id="85a0a-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a0a-229">0x00000010</span></span>                                                                            |
| <span data-ttu-id="85a0a-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="85a0a-230">Classes used in</span></span>        | [<span data-ttu-id="85a0a-231">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="85a0a-231">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="85a0a-232">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="85a0a-232">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85a0a-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85a0a-233">Windows Server 2012</span></span>



| <span data-ttu-id="85a0a-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="85a0a-234">Entry</span></span> | <span data-ttu-id="85a0a-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a0a-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85a0a-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="85a0a-236">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a0a-237">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="85a0a-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a0a-238">System-Only</span></span>            | <span data-ttu-id="85a0a-239">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-239">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="85a0a-240">Is-Single-Valued</span></span>       | <span data-ttu-id="85a0a-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="85a0a-241">True</span></span>                                                                                  |
| <span data-ttu-id="85a0a-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="85a0a-242">Is Indexed</span></span>             | <span data-ttu-id="85a0a-243">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-243">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="85a0a-244">In Global Catalog</span></span>      | <span data-ttu-id="85a0a-245">Faux</span><span class="sxs-lookup"><span data-stu-id="85a0a-245">False</span></span>                                                                                 |
| <span data-ttu-id="85a0a-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="85a0a-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a0a-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="85a0a-247">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="85a0a-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a0a-248">Range-Lower</span></span>            | <span data-ttu-id="85a0a-249">0</span><span class="sxs-lookup"><span data-stu-id="85a0a-249">0</span></span>                                                                                     |
| <span data-ttu-id="85a0a-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a0a-250">Range-Upper</span></span>            | <span data-ttu-id="85a0a-251">65536</span><span class="sxs-lookup"><span data-stu-id="85a0a-251">65536</span></span>                                                                                 |
| <span data-ttu-id="85a0a-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-252">Search-Flags</span></span>           | <span data-ttu-id="85a0a-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a0a-253">0x00000000</span></span>                                                                            |
| <span data-ttu-id="85a0a-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a0a-254">System-Flags</span></span>           | <span data-ttu-id="85a0a-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a0a-255">0x00000010</span></span>                                                                            |
| <span data-ttu-id="85a0a-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="85a0a-256">Classes used in</span></span>        | [<span data-ttu-id="85a0a-257">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="85a0a-257">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="85a0a-258">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="85a0a-258">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



 

 





