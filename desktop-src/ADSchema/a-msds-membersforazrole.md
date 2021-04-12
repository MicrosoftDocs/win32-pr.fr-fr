---
title: ms-DS-Members-for-AZ-Role, attribut
description: Liste des groupes d’applications membres ou des utilisateurs liés à AZ-Role.
ms.assetid: c1234443-fd25-4ed8-a8ee-9853810ebe7d
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-Members-for-AZ-Role Attribute
- Schéma Active Directory de l’attribut msDS-MembersForAzRole
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b19203e5c44d0389e64531867444d1bb2865196
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480373"
---
# <a name="ms-ds-members-for-az-role-attribute"></a><span data-ttu-id="3e270-105">ms-DS-Members-for-AZ-Role, attribut</span><span class="sxs-lookup"><span data-stu-id="3e270-105">ms-DS-Members-For-Az-Role attribute</span></span>

<span data-ttu-id="3e270-106">Liste des groupes d’applications membres ou des utilisateurs liés à AZ-Role.</span><span class="sxs-lookup"><span data-stu-id="3e270-106">List of member application groups or users linked to Az-Role.</span></span>



| <span data-ttu-id="3e270-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-107">Entry</span></span> | <span data-ttu-id="3e270-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3e270-109">CN</span><span class="sxs-lookup"><span data-stu-id="3e270-109">CN</span></span>                | <span data-ttu-id="3e270-110">ms-DS-Members-for-AZ-Role</span><span class="sxs-lookup"><span data-stu-id="3e270-110">ms-DS-Members-For-Az-Role</span></span>               |
| <span data-ttu-id="3e270-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e270-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3e270-112">msDS-MembersForAzRole</span><span class="sxs-lookup"><span data-stu-id="3e270-112">msDS-MembersForAzRole</span></span>                   |
| <span data-ttu-id="3e270-113">Taille</span><span class="sxs-lookup"><span data-stu-id="3e270-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="3e270-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3e270-114">Update Privilege</span></span>  | <span data-ttu-id="3e270-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="3e270-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="3e270-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3e270-116">Update Frequency</span></span>  | <span data-ttu-id="3e270-117">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3e270-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="3e270-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-118">Attribute-Id</span></span>      | <span data-ttu-id="3e270-119">1.2.840.113556.1.4.1806</span><span class="sxs-lookup"><span data-stu-id="3e270-119">1.2.840.113556.1.4.1806</span></span>                 |
| <span data-ttu-id="3e270-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e270-120">System-Id-Guid</span></span>    | <span data-ttu-id="3e270-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span><span class="sxs-lookup"><span data-stu-id="3e270-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span></span>    |
| <span data-ttu-id="3e270-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e270-122">Syntax</span></span>            | [<span data-ttu-id="3e270-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3e270-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3e270-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3e270-124">Implementations</span></span>

-   [<span data-ttu-id="3e270-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e270-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e270-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e270-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e270-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e270-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e270-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e270-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e270-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e270-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3e270-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e270-130">Windows Server 2003</span></span>



| <span data-ttu-id="3e270-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-131">Entry</span></span> | <span data-ttu-id="3e270-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-132">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="3e270-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e270-133">Link-Id</span></span>                | <span data-ttu-id="3e270-134">2016</span><span class="sxs-lookup"><span data-stu-id="3e270-134">2016</span></span>                                              |
| <span data-ttu-id="3e270-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="3e270-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e270-136">System-Only</span></span>            | <span data-ttu-id="3e270-137">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-137">False</span></span>                                             |
| <span data-ttu-id="3e270-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e270-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3e270-139">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-139">False</span></span>                                             |
| <span data-ttu-id="3e270-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e270-140">Is Indexed</span></span>             | <span data-ttu-id="3e270-141">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-141">False</span></span>                                             |
| <span data-ttu-id="3e270-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e270-142">In Global Catalog</span></span>      | <span data-ttu-id="3e270-143">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-143">False</span></span>                                             |
| <span data-ttu-id="3e270-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e270-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e270-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e270-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="3e270-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e270-146">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="3e270-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e270-147">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="3e270-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-148">Search-Flags</span></span>           | <span data-ttu-id="3e270-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e270-149">0x00000000</span></span>                                        |
| <span data-ttu-id="3e270-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-150">System-Flags</span></span>           | <span data-ttu-id="3e270-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e270-151">0x00000010</span></span>                                        |
| <span data-ttu-id="3e270-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e270-152">Classes used in</span></span>        | [<span data-ttu-id="3e270-153">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="3e270-153">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e270-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e270-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e270-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-155">Entry</span></span> | <span data-ttu-id="3e270-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-156">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="3e270-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e270-157">Link-Id</span></span>                | <span data-ttu-id="3e270-158">2016</span><span class="sxs-lookup"><span data-stu-id="3e270-158">2016</span></span>                                              |
| <span data-ttu-id="3e270-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-159">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="3e270-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e270-160">System-Only</span></span>            | <span data-ttu-id="3e270-161">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-161">False</span></span>                                             |
| <span data-ttu-id="3e270-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e270-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3e270-163">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-163">False</span></span>                                             |
| <span data-ttu-id="3e270-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e270-164">Is Indexed</span></span>             | <span data-ttu-id="3e270-165">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-165">False</span></span>                                             |
| <span data-ttu-id="3e270-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e270-166">In Global Catalog</span></span>      | <span data-ttu-id="3e270-167">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-167">False</span></span>                                             |
| <span data-ttu-id="3e270-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e270-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e270-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e270-169">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="3e270-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e270-170">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="3e270-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e270-171">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="3e270-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-172">Search-Flags</span></span>           | <span data-ttu-id="3e270-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e270-173">0x00000000</span></span>                                        |
| <span data-ttu-id="3e270-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-174">System-Flags</span></span>           | <span data-ttu-id="3e270-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e270-175">0x00000010</span></span>                                        |
| <span data-ttu-id="3e270-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e270-176">Classes used in</span></span>        | [<span data-ttu-id="3e270-177">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="3e270-177">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e270-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e270-178">Windows Server 2008</span></span>



| <span data-ttu-id="3e270-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-179">Entry</span></span> | <span data-ttu-id="3e270-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-180">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="3e270-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e270-181">Link-Id</span></span>                | <span data-ttu-id="3e270-182">2016</span><span class="sxs-lookup"><span data-stu-id="3e270-182">2016</span></span>                                              |
| <span data-ttu-id="3e270-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-183">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="3e270-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e270-184">System-Only</span></span>            | <span data-ttu-id="3e270-185">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-185">False</span></span>                                             |
| <span data-ttu-id="3e270-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e270-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3e270-187">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-187">False</span></span>                                             |
| <span data-ttu-id="3e270-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e270-188">Is Indexed</span></span>             | <span data-ttu-id="3e270-189">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-189">False</span></span>                                             |
| <span data-ttu-id="3e270-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e270-190">In Global Catalog</span></span>      | <span data-ttu-id="3e270-191">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-191">False</span></span>                                             |
| <span data-ttu-id="3e270-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e270-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e270-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e270-193">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="3e270-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e270-194">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="3e270-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e270-195">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="3e270-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-196">Search-Flags</span></span>           | <span data-ttu-id="3e270-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e270-197">0x00000000</span></span>                                        |
| <span data-ttu-id="3e270-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-198">System-Flags</span></span>           | <span data-ttu-id="3e270-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e270-199">0x00000010</span></span>                                        |
| <span data-ttu-id="3e270-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e270-200">Classes used in</span></span>        | [<span data-ttu-id="3e270-201">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="3e270-201">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e270-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e270-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e270-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-203">Entry</span></span> | <span data-ttu-id="3e270-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-204">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="3e270-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e270-205">Link-Id</span></span>                | <span data-ttu-id="3e270-206">2016</span><span class="sxs-lookup"><span data-stu-id="3e270-206">2016</span></span>                                              |
| <span data-ttu-id="3e270-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-207">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="3e270-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e270-208">System-Only</span></span>            | <span data-ttu-id="3e270-209">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-209">False</span></span>                                             |
| <span data-ttu-id="3e270-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e270-210">Is-Single-Valued</span></span>       | <span data-ttu-id="3e270-211">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-211">False</span></span>                                             |
| <span data-ttu-id="3e270-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e270-212">Is Indexed</span></span>             | <span data-ttu-id="3e270-213">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-213">False</span></span>                                             |
| <span data-ttu-id="3e270-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e270-214">In Global Catalog</span></span>      | <span data-ttu-id="3e270-215">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-215">False</span></span>                                             |
| <span data-ttu-id="3e270-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e270-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e270-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e270-217">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="3e270-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e270-218">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="3e270-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e270-219">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="3e270-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-220">Search-Flags</span></span>           | <span data-ttu-id="3e270-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e270-221">0x00000000</span></span>                                        |
| <span data-ttu-id="3e270-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-222">System-Flags</span></span>           | <span data-ttu-id="3e270-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e270-223">0x00000010</span></span>                                        |
| <span data-ttu-id="3e270-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e270-224">Classes used in</span></span>        | [<span data-ttu-id="3e270-225">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="3e270-225">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e270-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e270-226">Windows Server 2012</span></span>



| <span data-ttu-id="3e270-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e270-227">Entry</span></span> | <span data-ttu-id="3e270-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e270-228">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="3e270-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e270-229">Link-Id</span></span>                | <span data-ttu-id="3e270-230">2016</span><span class="sxs-lookup"><span data-stu-id="3e270-230">2016</span></span>                                              |
| <span data-ttu-id="3e270-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e270-231">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="3e270-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e270-232">System-Only</span></span>            | <span data-ttu-id="3e270-233">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-233">False</span></span>                                             |
| <span data-ttu-id="3e270-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e270-234">Is-Single-Valued</span></span>       | <span data-ttu-id="3e270-235">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-235">False</span></span>                                             |
| <span data-ttu-id="3e270-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e270-236">Is Indexed</span></span>             | <span data-ttu-id="3e270-237">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-237">False</span></span>                                             |
| <span data-ttu-id="3e270-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e270-238">In Global Catalog</span></span>      | <span data-ttu-id="3e270-239">Faux</span><span class="sxs-lookup"><span data-stu-id="3e270-239">False</span></span>                                             |
| <span data-ttu-id="3e270-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e270-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e270-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e270-241">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="3e270-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e270-242">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="3e270-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e270-243">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="3e270-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-244">Search-Flags</span></span>           | <span data-ttu-id="3e270-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e270-245">0x00000000</span></span>                                        |
| <span data-ttu-id="3e270-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e270-246">System-Flags</span></span>           | <span data-ttu-id="3e270-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e270-247">0x00000010</span></span>                                        |
| <span data-ttu-id="3e270-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e270-248">Classes used in</span></span>        | [<span data-ttu-id="3e270-249">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="3e270-249">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



 

 





