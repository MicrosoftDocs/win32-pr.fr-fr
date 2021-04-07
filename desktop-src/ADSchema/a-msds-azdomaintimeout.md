---
title: ms-DS-AZ-domaine-Timeout (attribut)
description: Durée, en millisecondes, après qu’un domaine est détecté comme inaccessible et avant que le contrôleur de domaine soit de nouveau essayé.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-AZ-Domain-Timeout
- Schéma Active Directory de l’attribut msDS-AzDomainTimeout
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845177"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="c8565-105">ms-DS-AZ-domaine-Timeout (attribut)</span><span class="sxs-lookup"><span data-stu-id="c8565-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="c8565-106">Durée, en millisecondes, après qu’un domaine est détecté comme inaccessible et avant que le contrôleur de domaine soit de nouveau essayé.</span><span class="sxs-lookup"><span data-stu-id="c8565-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="c8565-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-107">Entry</span></span> | <span data-ttu-id="c8565-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c8565-109">CN</span><span class="sxs-lookup"><span data-stu-id="c8565-109">CN</span></span>                | <span data-ttu-id="c8565-110">ms-DS-AZ-domaine-Timeout</span><span class="sxs-lookup"><span data-stu-id="c8565-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="c8565-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c8565-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c8565-112">msDS-AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="c8565-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="c8565-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c8565-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c8565-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c8565-114">Update Privilege</span></span>  | <span data-ttu-id="c8565-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="c8565-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="c8565-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c8565-116">Update Frequency</span></span>  | <span data-ttu-id="c8565-117">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c8565-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="c8565-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-118">Attribute-Id</span></span>      | <span data-ttu-id="c8565-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="c8565-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="c8565-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8565-120">System-Id-Guid</span></span>    | <span data-ttu-id="c8565-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="c8565-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="c8565-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8565-122">Syntax</span></span>            | [<span data-ttu-id="c8565-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c8565-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="c8565-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c8565-124">Implementations</span></span>

-   [<span data-ttu-id="c8565-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8565-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8565-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8565-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8565-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8565-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8565-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8565-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8565-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8565-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c8565-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8565-130">Windows Server 2003</span></span>



| <span data-ttu-id="c8565-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-131">Entry</span></span> | <span data-ttu-id="c8565-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c8565-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c8565-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8565-135">System-Only</span></span>            | <span data-ttu-id="c8565-136">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-136">False</span></span>                                                              |
| <span data-ttu-id="c8565-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c8565-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c8565-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="c8565-138">True</span></span>                                                               |
| <span data-ttu-id="c8565-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c8565-139">Is Indexed</span></span>             | <span data-ttu-id="c8565-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-140">False</span></span>                                                              |
| <span data-ttu-id="c8565-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c8565-141">In Global Catalog</span></span>      | <span data-ttu-id="c8565-142">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-142">False</span></span>                                                              |
| <span data-ttu-id="c8565-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c8565-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8565-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c8565-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c8565-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8565-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8565-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-147">Search-Flags</span></span>           | <span data-ttu-id="c8565-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8565-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="c8565-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-149">System-Flags</span></span>           | <span data-ttu-id="c8565-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8565-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="c8565-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c8565-151">Classes used in</span></span>        | [<span data-ttu-id="c8565-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="c8565-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8565-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8565-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8565-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-154">Entry</span></span> | <span data-ttu-id="c8565-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c8565-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c8565-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8565-158">System-Only</span></span>            | <span data-ttu-id="c8565-159">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-159">False</span></span>                                                              |
| <span data-ttu-id="c8565-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c8565-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c8565-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="c8565-161">True</span></span>                                                               |
| <span data-ttu-id="c8565-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c8565-162">Is Indexed</span></span>             | <span data-ttu-id="c8565-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-163">False</span></span>                                                              |
| <span data-ttu-id="c8565-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c8565-164">In Global Catalog</span></span>      | <span data-ttu-id="c8565-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-165">False</span></span>                                                              |
| <span data-ttu-id="c8565-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c8565-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8565-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c8565-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c8565-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8565-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8565-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-170">Search-Flags</span></span>           | <span data-ttu-id="c8565-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8565-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="c8565-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-172">System-Flags</span></span>           | <span data-ttu-id="c8565-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8565-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="c8565-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c8565-174">Classes used in</span></span>        | [<span data-ttu-id="c8565-175">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="c8565-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8565-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8565-176">Windows Server 2008</span></span>



| <span data-ttu-id="c8565-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-177">Entry</span></span> | <span data-ttu-id="c8565-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c8565-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c8565-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8565-181">System-Only</span></span>            | <span data-ttu-id="c8565-182">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-182">False</span></span>                                                              |
| <span data-ttu-id="c8565-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c8565-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c8565-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="c8565-184">True</span></span>                                                               |
| <span data-ttu-id="c8565-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c8565-185">Is Indexed</span></span>             | <span data-ttu-id="c8565-186">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-186">False</span></span>                                                              |
| <span data-ttu-id="c8565-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c8565-187">In Global Catalog</span></span>      | <span data-ttu-id="c8565-188">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-188">False</span></span>                                                              |
| <span data-ttu-id="c8565-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c8565-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8565-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c8565-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c8565-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8565-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8565-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-193">Search-Flags</span></span>           | <span data-ttu-id="c8565-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8565-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="c8565-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-195">System-Flags</span></span>           | <span data-ttu-id="c8565-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8565-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="c8565-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c8565-197">Classes used in</span></span>        | [<span data-ttu-id="c8565-198">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="c8565-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8565-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8565-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8565-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-200">Entry</span></span> | <span data-ttu-id="c8565-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c8565-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c8565-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8565-204">System-Only</span></span>            | <span data-ttu-id="c8565-205">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-205">False</span></span>                                                              |
| <span data-ttu-id="c8565-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c8565-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c8565-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="c8565-207">True</span></span>                                                               |
| <span data-ttu-id="c8565-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c8565-208">Is Indexed</span></span>             | <span data-ttu-id="c8565-209">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-209">False</span></span>                                                              |
| <span data-ttu-id="c8565-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c8565-210">In Global Catalog</span></span>      | <span data-ttu-id="c8565-211">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-211">False</span></span>                                                              |
| <span data-ttu-id="c8565-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c8565-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8565-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c8565-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c8565-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8565-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8565-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-216">Search-Flags</span></span>           | <span data-ttu-id="c8565-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8565-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="c8565-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-218">System-Flags</span></span>           | <span data-ttu-id="c8565-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8565-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="c8565-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c8565-220">Classes used in</span></span>        | [<span data-ttu-id="c8565-221">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="c8565-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8565-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8565-222">Windows Server 2012</span></span>



| <span data-ttu-id="c8565-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="c8565-223">Entry</span></span> | <span data-ttu-id="c8565-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8565-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c8565-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c8565-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8565-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c8565-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8565-227">System-Only</span></span>            | <span data-ttu-id="c8565-228">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-228">False</span></span>                                                              |
| <span data-ttu-id="c8565-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c8565-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c8565-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="c8565-230">True</span></span>                                                               |
| <span data-ttu-id="c8565-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c8565-231">Is Indexed</span></span>             | <span data-ttu-id="c8565-232">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-232">False</span></span>                                                              |
| <span data-ttu-id="c8565-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c8565-233">In Global Catalog</span></span>      | <span data-ttu-id="c8565-234">Faux</span><span class="sxs-lookup"><span data-stu-id="c8565-234">False</span></span>                                                              |
| <span data-ttu-id="c8565-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c8565-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8565-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c8565-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c8565-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8565-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8565-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c8565-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-239">Search-Flags</span></span>           | <span data-ttu-id="c8565-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8565-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="c8565-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8565-241">System-Flags</span></span>           | <span data-ttu-id="c8565-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8565-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="c8565-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c8565-243">Classes used in</span></span>        | [<span data-ttu-id="c8565-244">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="c8565-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





