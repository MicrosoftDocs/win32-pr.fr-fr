---
title: attribut ms-DS-non-members
description: Cet attribut remplit la même fonction que l’attribut de membre de non-sécurité, mais avec les règles de portée appliquées.
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-non-members
- Schéma Active Directory de l’attribut msDS-non-members
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845153"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="74e2a-105">attribut ms-DS-non-members</span><span class="sxs-lookup"><span data-stu-id="74e2a-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="74e2a-106">Cet attribut remplit la même fonction que l’attribut de membre de non-sécurité, mais avec les règles de portée appliquées.</span><span class="sxs-lookup"><span data-stu-id="74e2a-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="74e2a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-107">Entry</span></span> | <span data-ttu-id="74e2a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="74e2a-109">CN</span><span class="sxs-lookup"><span data-stu-id="74e2a-109">CN</span></span>                | <span data-ttu-id="74e2a-110">ms-DS-non-membres</span><span class="sxs-lookup"><span data-stu-id="74e2a-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="74e2a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="74e2a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="74e2a-112">msDS-non-membres</span><span class="sxs-lookup"><span data-stu-id="74e2a-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="74e2a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="74e2a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="74e2a-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="74e2a-114">Update Privilege</span></span>  | <span data-ttu-id="74e2a-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="74e2a-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="74e2a-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="74e2a-116">Update Frequency</span></span>  | <span data-ttu-id="74e2a-117">Lors de l’initialisation et de la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="74e2a-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="74e2a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-118">Attribute-Id</span></span>      | <span data-ttu-id="74e2a-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="74e2a-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="74e2a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="74e2a-120">System-Id-Guid</span></span>    | <span data-ttu-id="74e2a-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="74e2a-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="74e2a-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74e2a-122">Syntax</span></span>            | [<span data-ttu-id="74e2a-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="74e2a-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="74e2a-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="74e2a-124">Implementations</span></span>

-   [<span data-ttu-id="74e2a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74e2a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74e2a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74e2a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74e2a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74e2a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74e2a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74e2a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74e2a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74e2a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="74e2a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74e2a-130">Windows Server 2003</span></span>



| <span data-ttu-id="74e2a-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-131">Entry</span></span> | <span data-ttu-id="74e2a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="74e2a-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="74e2a-133">Link-Id</span></span>                | <span data-ttu-id="74e2a-134">2014</span><span class="sxs-lookup"><span data-stu-id="74e2a-134">2014</span></span>                                |
| <span data-ttu-id="74e2a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="74e2a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74e2a-136">System-Only</span></span>            | <span data-ttu-id="74e2a-137">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-137">False</span></span>                               |
| <span data-ttu-id="74e2a-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="74e2a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74e2a-139">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-139">False</span></span>                               |
| <span data-ttu-id="74e2a-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="74e2a-140">Is Indexed</span></span>             | <span data-ttu-id="74e2a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-141">False</span></span>                               |
| <span data-ttu-id="74e2a-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="74e2a-142">In Global Catalog</span></span>      | <span data-ttu-id="74e2a-143">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-143">False</span></span>                               |
| <span data-ttu-id="74e2a-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="74e2a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74e2a-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="74e2a-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="74e2a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74e2a-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74e2a-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-148">Search-Flags</span></span>           | <span data-ttu-id="74e2a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74e2a-149">0x00000000</span></span>                          |
| <span data-ttu-id="74e2a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-150">System-Flags</span></span>           | <span data-ttu-id="74e2a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74e2a-151">0x00000010</span></span>                          |
| <span data-ttu-id="74e2a-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="74e2a-152">Classes used in</span></span>        | [<span data-ttu-id="74e2a-153">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="74e2a-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74e2a-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74e2a-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74e2a-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-155">Entry</span></span> | <span data-ttu-id="74e2a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="74e2a-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="74e2a-157">Link-Id</span></span>                | <span data-ttu-id="74e2a-158">2014</span><span class="sxs-lookup"><span data-stu-id="74e2a-158">2014</span></span>                                |
| <span data-ttu-id="74e2a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="74e2a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="74e2a-160">System-Only</span></span>            | <span data-ttu-id="74e2a-161">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-161">False</span></span>                               |
| <span data-ttu-id="74e2a-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="74e2a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="74e2a-163">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-163">False</span></span>                               |
| <span data-ttu-id="74e2a-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="74e2a-164">Is Indexed</span></span>             | <span data-ttu-id="74e2a-165">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-165">False</span></span>                               |
| <span data-ttu-id="74e2a-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="74e2a-166">In Global Catalog</span></span>      | <span data-ttu-id="74e2a-167">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-167">False</span></span>                               |
| <span data-ttu-id="74e2a-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="74e2a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="74e2a-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="74e2a-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="74e2a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74e2a-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74e2a-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-172">Search-Flags</span></span>           | <span data-ttu-id="74e2a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74e2a-173">0x00000000</span></span>                          |
| <span data-ttu-id="74e2a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-174">System-Flags</span></span>           | <span data-ttu-id="74e2a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74e2a-175">0x00000010</span></span>                          |
| <span data-ttu-id="74e2a-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="74e2a-176">Classes used in</span></span>        | [<span data-ttu-id="74e2a-177">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="74e2a-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74e2a-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74e2a-178">Windows Server 2008</span></span>



| <span data-ttu-id="74e2a-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-179">Entry</span></span> | <span data-ttu-id="74e2a-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="74e2a-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="74e2a-181">Link-Id</span></span>                | <span data-ttu-id="74e2a-182">2014</span><span class="sxs-lookup"><span data-stu-id="74e2a-182">2014</span></span>                                |
| <span data-ttu-id="74e2a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="74e2a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="74e2a-184">System-Only</span></span>            | <span data-ttu-id="74e2a-185">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-185">False</span></span>                               |
| <span data-ttu-id="74e2a-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="74e2a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="74e2a-187">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-187">False</span></span>                               |
| <span data-ttu-id="74e2a-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="74e2a-188">Is Indexed</span></span>             | <span data-ttu-id="74e2a-189">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-189">False</span></span>                               |
| <span data-ttu-id="74e2a-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="74e2a-190">In Global Catalog</span></span>      | <span data-ttu-id="74e2a-191">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-191">False</span></span>                               |
| <span data-ttu-id="74e2a-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="74e2a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="74e2a-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="74e2a-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="74e2a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74e2a-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74e2a-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-196">Search-Flags</span></span>           | <span data-ttu-id="74e2a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74e2a-197">0x00000000</span></span>                          |
| <span data-ttu-id="74e2a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-198">System-Flags</span></span>           | <span data-ttu-id="74e2a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74e2a-199">0x00000010</span></span>                          |
| <span data-ttu-id="74e2a-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="74e2a-200">Classes used in</span></span>        | [<span data-ttu-id="74e2a-201">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="74e2a-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74e2a-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74e2a-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74e2a-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-203">Entry</span></span> | <span data-ttu-id="74e2a-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="74e2a-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="74e2a-205">Link-Id</span></span>                | <span data-ttu-id="74e2a-206">2014</span><span class="sxs-lookup"><span data-stu-id="74e2a-206">2014</span></span>                                |
| <span data-ttu-id="74e2a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="74e2a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="74e2a-208">System-Only</span></span>            | <span data-ttu-id="74e2a-209">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-209">False</span></span>                               |
| <span data-ttu-id="74e2a-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="74e2a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="74e2a-211">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-211">False</span></span>                               |
| <span data-ttu-id="74e2a-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="74e2a-212">Is Indexed</span></span>             | <span data-ttu-id="74e2a-213">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-213">False</span></span>                               |
| <span data-ttu-id="74e2a-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="74e2a-214">In Global Catalog</span></span>      | <span data-ttu-id="74e2a-215">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-215">False</span></span>                               |
| <span data-ttu-id="74e2a-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="74e2a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="74e2a-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="74e2a-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="74e2a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74e2a-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74e2a-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-220">Search-Flags</span></span>           | <span data-ttu-id="74e2a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74e2a-221">0x00000000</span></span>                          |
| <span data-ttu-id="74e2a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-222">System-Flags</span></span>           | <span data-ttu-id="74e2a-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74e2a-223">0x00000010</span></span>                          |
| <span data-ttu-id="74e2a-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="74e2a-224">Classes used in</span></span>        | [<span data-ttu-id="74e2a-225">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="74e2a-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74e2a-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74e2a-226">Windows Server 2012</span></span>



| <span data-ttu-id="74e2a-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="74e2a-227">Entry</span></span> | <span data-ttu-id="74e2a-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e2a-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="74e2a-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="74e2a-229">Link-Id</span></span>                | <span data-ttu-id="74e2a-230">2014</span><span class="sxs-lookup"><span data-stu-id="74e2a-230">2014</span></span>                                |
| <span data-ttu-id="74e2a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74e2a-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="74e2a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="74e2a-232">System-Only</span></span>            | <span data-ttu-id="74e2a-233">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-233">False</span></span>                               |
| <span data-ttu-id="74e2a-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="74e2a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="74e2a-235">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-235">False</span></span>                               |
| <span data-ttu-id="74e2a-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="74e2a-236">Is Indexed</span></span>             | <span data-ttu-id="74e2a-237">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-237">False</span></span>                               |
| <span data-ttu-id="74e2a-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="74e2a-238">In Global Catalog</span></span>      | <span data-ttu-id="74e2a-239">Faux</span><span class="sxs-lookup"><span data-stu-id="74e2a-239">False</span></span>                               |
| <span data-ttu-id="74e2a-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="74e2a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="74e2a-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="74e2a-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="74e2a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74e2a-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74e2a-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="74e2a-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-244">Search-Flags</span></span>           | <span data-ttu-id="74e2a-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74e2a-245">0x00000000</span></span>                          |
| <span data-ttu-id="74e2a-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74e2a-246">System-Flags</span></span>           | <span data-ttu-id="74e2a-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74e2a-247">0x00000010</span></span>                          |
| <span data-ttu-id="74e2a-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="74e2a-248">Classes used in</span></span>        | [<span data-ttu-id="74e2a-249">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="74e2a-249">**Group**</span></span>](c-group.md)<br/> |



 

 





