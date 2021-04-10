---
title: attribut ms-DS-AZ-Operation-ID
description: ID spécifique à l’application qui rend l’opération unique à l’application.
ms.assetid: 0d0fc8ce-7044-481a-8df2-489e33264412
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-AZ-Operation-ID
- Schéma Active Directory de l’attribut msDS-AzOperationID
topic_type:
- apiref
api_name:
- ms-DS-Az-Operation-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58cc05338fa3960185a795422c62256a63e6f1ca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104200613"
---
# <a name="ms-ds-az-operation-id-attribute"></a><span data-ttu-id="97b4b-105">attribut ms-DS-AZ-Operation-ID</span><span class="sxs-lookup"><span data-stu-id="97b4b-105">ms-DS-Az-Operation-ID attribute</span></span>

<span data-ttu-id="97b4b-106">ID spécifique à l’application qui rend l’opération unique à l’application.</span><span class="sxs-lookup"><span data-stu-id="97b4b-106">An application specific ID that makes the operation unique to the application.</span></span>



| <span data-ttu-id="97b4b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-107">Entry</span></span> | <span data-ttu-id="97b4b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="97b4b-109">CN</span><span class="sxs-lookup"><span data-stu-id="97b4b-109">CN</span></span>                | <span data-ttu-id="97b4b-110">ms-DS-AZ-Operation-ID</span><span class="sxs-lookup"><span data-stu-id="97b4b-110">ms-DS-Az-Operation-ID</span></span>                   |
| <span data-ttu-id="97b4b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="97b4b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="97b4b-112">msDS-AzOperationID</span><span class="sxs-lookup"><span data-stu-id="97b4b-112">msDS-AzOperationID</span></span>                      |
| <span data-ttu-id="97b4b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="97b4b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="97b4b-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="97b4b-114">Update Privilege</span></span>  | <span data-ttu-id="97b4b-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="97b4b-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="97b4b-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="97b4b-116">Update Frequency</span></span>  | <span data-ttu-id="97b4b-117">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="97b4b-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="97b4b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-118">Attribute-Id</span></span>      | <span data-ttu-id="97b4b-119">1.2.840.113556.1.4.1800</span><span class="sxs-lookup"><span data-stu-id="97b4b-119">1.2.840.113556.1.4.1800</span></span>                 |
| <span data-ttu-id="97b4b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="97b4b-120">System-Id-Guid</span></span>    | <span data-ttu-id="97b4b-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span><span class="sxs-lookup"><span data-stu-id="97b4b-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span></span>    |
| <span data-ttu-id="97b4b-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97b4b-122">Syntax</span></span>            | [<span data-ttu-id="97b4b-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="97b4b-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="97b4b-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="97b4b-124">Implementations</span></span>

-   [<span data-ttu-id="97b4b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97b4b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97b4b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97b4b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97b4b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97b4b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97b4b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97b4b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97b4b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97b4b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="97b4b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97b4b-130">Windows Server 2003</span></span>



| <span data-ttu-id="97b4b-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-131">Entry</span></span> | <span data-ttu-id="97b4b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-132">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="97b4b-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="97b4b-133">Link-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="97b4b-135">System-Only</span></span>            | <span data-ttu-id="97b4b-136">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-136">False</span></span>        |
| <span data-ttu-id="97b4b-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="97b4b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="97b4b-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="97b4b-138">True</span></span>         |
| <span data-ttu-id="97b4b-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="97b4b-139">Is Indexed</span></span>             | <span data-ttu-id="97b4b-140">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-140">False</span></span>        |
| <span data-ttu-id="97b4b-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="97b4b-141">In Global Catalog</span></span>      | <span data-ttu-id="97b4b-142">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-142">False</span></span>        |
| <span data-ttu-id="97b4b-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="97b4b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="97b4b-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="97b4b-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="97b4b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97b4b-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="97b4b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97b4b-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="97b4b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-147">Search-Flags</span></span>           | <span data-ttu-id="97b4b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b4b-148">0x00000000</span></span>   |
| <span data-ttu-id="97b4b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-149">System-Flags</span></span>           | <span data-ttu-id="97b4b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97b4b-150">0x00000010</span></span>   |
| <span data-ttu-id="97b4b-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="97b4b-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97b4b-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97b4b-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97b4b-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-153">Entry</span></span> | <span data-ttu-id="97b4b-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="97b4b-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="97b4b-155">Link-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-156">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="97b4b-157">System-Only</span></span>            | <span data-ttu-id="97b4b-158">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-158">False</span></span>        |
| <span data-ttu-id="97b4b-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="97b4b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="97b4b-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="97b4b-160">True</span></span>         |
| <span data-ttu-id="97b4b-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="97b4b-161">Is Indexed</span></span>             | <span data-ttu-id="97b4b-162">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-162">False</span></span>        |
| <span data-ttu-id="97b4b-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="97b4b-163">In Global Catalog</span></span>      | <span data-ttu-id="97b4b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-164">False</span></span>        |
| <span data-ttu-id="97b4b-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="97b4b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="97b4b-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="97b4b-166">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="97b4b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97b4b-167">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="97b4b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97b4b-168">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="97b4b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-169">Search-Flags</span></span>           | <span data-ttu-id="97b4b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b4b-170">0x00000000</span></span>   |
| <span data-ttu-id="97b4b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-171">System-Flags</span></span>           | <span data-ttu-id="97b4b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97b4b-172">0x00000010</span></span>   |
| <span data-ttu-id="97b4b-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="97b4b-173">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="97b4b-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97b4b-174">Windows Server 2008</span></span>



| <span data-ttu-id="97b4b-175">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-175">Entry</span></span> | <span data-ttu-id="97b4b-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-176">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="97b4b-177">ID de lien</span><span class="sxs-lookup"><span data-stu-id="97b4b-177">Link-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-178">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="97b4b-179">System-Only</span></span>            | <span data-ttu-id="97b4b-180">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-180">False</span></span>        |
| <span data-ttu-id="97b4b-181">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="97b4b-181">Is-Single-Valued</span></span>       | <span data-ttu-id="97b4b-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="97b4b-182">True</span></span>         |
| <span data-ttu-id="97b4b-183">Est indexé</span><span class="sxs-lookup"><span data-stu-id="97b4b-183">Is Indexed</span></span>             | <span data-ttu-id="97b4b-184">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-184">False</span></span>        |
| <span data-ttu-id="97b4b-185">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="97b4b-185">In Global Catalog</span></span>      | <span data-ttu-id="97b4b-186">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-186">False</span></span>        |
| <span data-ttu-id="97b4b-187">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="97b4b-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="97b4b-188">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="97b4b-188">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="97b4b-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97b4b-189">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="97b4b-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97b4b-190">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="97b4b-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-191">Search-Flags</span></span>           | <span data-ttu-id="97b4b-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b4b-192">0x00000000</span></span>   |
| <span data-ttu-id="97b4b-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-193">System-Flags</span></span>           | <span data-ttu-id="97b4b-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97b4b-194">0x00000010</span></span>   |
| <span data-ttu-id="97b4b-195">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="97b4b-195">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97b4b-196">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97b4b-196">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97b4b-197">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-197">Entry</span></span> | <span data-ttu-id="97b4b-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-198">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="97b4b-199">ID de lien</span><span class="sxs-lookup"><span data-stu-id="97b4b-199">Link-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-200">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="97b4b-201">System-Only</span></span>            | <span data-ttu-id="97b4b-202">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-202">False</span></span>        |
| <span data-ttu-id="97b4b-203">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="97b4b-203">Is-Single-Valued</span></span>       | <span data-ttu-id="97b4b-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="97b4b-204">True</span></span>         |
| <span data-ttu-id="97b4b-205">Est indexé</span><span class="sxs-lookup"><span data-stu-id="97b4b-205">Is Indexed</span></span>             | <span data-ttu-id="97b4b-206">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-206">False</span></span>        |
| <span data-ttu-id="97b4b-207">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="97b4b-207">In Global Catalog</span></span>      | <span data-ttu-id="97b4b-208">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-208">False</span></span>        |
| <span data-ttu-id="97b4b-209">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="97b4b-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="97b4b-210">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="97b4b-210">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="97b4b-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97b4b-211">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="97b4b-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97b4b-212">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="97b4b-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-213">Search-Flags</span></span>           | <span data-ttu-id="97b4b-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b4b-214">0x00000000</span></span>   |
| <span data-ttu-id="97b4b-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-215">System-Flags</span></span>           | <span data-ttu-id="97b4b-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97b4b-216">0x00000010</span></span>   |
| <span data-ttu-id="97b4b-217">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="97b4b-217">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="97b4b-218">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97b4b-218">Windows Server 2012</span></span>



| <span data-ttu-id="97b4b-219">Entrée</span><span class="sxs-lookup"><span data-stu-id="97b4b-219">Entry</span></span> | <span data-ttu-id="97b4b-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b4b-220">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="97b4b-221">ID de lien</span><span class="sxs-lookup"><span data-stu-id="97b4b-221">Link-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97b4b-222">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="97b4b-223">System-Only</span><span class="sxs-lookup"><span data-stu-id="97b4b-223">System-Only</span></span>            | <span data-ttu-id="97b4b-224">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-224">False</span></span>        |
| <span data-ttu-id="97b4b-225">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="97b4b-225">Is-Single-Valued</span></span>       | <span data-ttu-id="97b4b-226">Vrai</span><span class="sxs-lookup"><span data-stu-id="97b4b-226">True</span></span>         |
| <span data-ttu-id="97b4b-227">Est indexé</span><span class="sxs-lookup"><span data-stu-id="97b4b-227">Is Indexed</span></span>             | <span data-ttu-id="97b4b-228">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-228">False</span></span>        |
| <span data-ttu-id="97b4b-229">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="97b4b-229">In Global Catalog</span></span>      | <span data-ttu-id="97b4b-230">Faux</span><span class="sxs-lookup"><span data-stu-id="97b4b-230">False</span></span>        |
| <span data-ttu-id="97b4b-231">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="97b4b-231">NT-Security-Descriptor</span></span> | <span data-ttu-id="97b4b-232">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="97b4b-232">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="97b4b-233">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97b4b-233">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="97b4b-234">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97b4b-234">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="97b4b-235">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-235">Search-Flags</span></span>           | <span data-ttu-id="97b4b-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b4b-236">0x00000000</span></span>   |
| <span data-ttu-id="97b4b-237">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97b4b-237">System-Flags</span></span>           | <span data-ttu-id="97b4b-238">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97b4b-238">0x00000010</span></span>   |
| <span data-ttu-id="97b4b-239">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="97b4b-239">Classes used in</span></span>        | \-           |



 

 




