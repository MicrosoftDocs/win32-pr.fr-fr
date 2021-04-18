---
title: attribut ms-DS-allowed-to-Delegate-to
description: Il s’agit d’un attribut sur les objets du compte de service (compte d’ordinateur ou d’utilisateur).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour l’attribut ms-DS-allowed-to-Delegate-to
- Schéma Active Directory de l’attribut msDS-AllowedToDelegateTo
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106519159"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="860d5-105">attribut ms-DS-allowed-to-Delegate-to</span><span class="sxs-lookup"><span data-stu-id="860d5-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="860d5-106">Il s’agit d’un attribut sur les objets du compte de service (compte d’ordinateur ou d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="860d5-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="860d5-107">Elle contient une liste de noms de principaux du service (SPN).</span><span class="sxs-lookup"><span data-stu-id="860d5-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="860d5-108">Cet attribut est utilisé pour configurer un service afin qu’il puisse obtenir des tickets de service qui peuvent être utilisés pour la délégation avec restriction.</span><span class="sxs-lookup"><span data-stu-id="860d5-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="860d5-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-109">Entry</span></span> | <span data-ttu-id="860d5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="860d5-111">CN</span><span class="sxs-lookup"><span data-stu-id="860d5-111">CN</span></span>                | <span data-ttu-id="860d5-112">ms-DS-autorisé-à-déléguer-à</span><span class="sxs-lookup"><span data-stu-id="860d5-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="860d5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="860d5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="860d5-114">msDS-AllowedToDelegateTo</span><span class="sxs-lookup"><span data-stu-id="860d5-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="860d5-115">Taille</span><span class="sxs-lookup"><span data-stu-id="860d5-115">Size</span></span>              | <span data-ttu-id="860d5-116">0 à 64 Ko</span><span class="sxs-lookup"><span data-stu-id="860d5-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="860d5-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="860d5-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="860d5-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="860d5-118">Update Frequency</span></span>  | <span data-ttu-id="860d5-119">Rarement</span><span class="sxs-lookup"><span data-stu-id="860d5-119">Infrequently</span></span>                                |
| <span data-ttu-id="860d5-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-120">Attribute-Id</span></span>      | <span data-ttu-id="860d5-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="860d5-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="860d5-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="860d5-122">System-Id-Guid</span></span>    | <span data-ttu-id="860d5-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="860d5-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="860d5-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="860d5-124">Syntax</span></span>            | [<span data-ttu-id="860d5-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="860d5-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="860d5-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="860d5-126">Implementations</span></span>

-   [<span data-ttu-id="860d5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="860d5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="860d5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="860d5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="860d5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="860d5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="860d5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="860d5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="860d5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="860d5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="860d5-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="860d5-132">Windows Server 2003</span></span>



| <span data-ttu-id="860d5-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-133">Entry</span></span> | <span data-ttu-id="860d5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="860d5-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="860d5-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="860d5-137">System-Only</span></span>            | <span data-ttu-id="860d5-138">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-138">False</span></span>                                                              |
| <span data-ttu-id="860d5-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="860d5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="860d5-140">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-140">False</span></span>                                                              |
| <span data-ttu-id="860d5-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="860d5-141">Is Indexed</span></span>             | <span data-ttu-id="860d5-142">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-142">False</span></span>                                                              |
| <span data-ttu-id="860d5-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="860d5-143">In Global Catalog</span></span>      | <span data-ttu-id="860d5-144">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-144">False</span></span>                                                              |
| <span data-ttu-id="860d5-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="860d5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="860d5-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="860d5-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="860d5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="860d5-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="860d5-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-149">Search-Flags</span></span>           | <span data-ttu-id="860d5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="860d5-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="860d5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-151">System-Flags</span></span>           | <span data-ttu-id="860d5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="860d5-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="860d5-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="860d5-153">Classes used in</span></span>        | [<span data-ttu-id="860d5-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="860d5-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="860d5-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="860d5-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="860d5-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-156">Entry</span></span> | <span data-ttu-id="860d5-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="860d5-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="860d5-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="860d5-160">System-Only</span></span>            | <span data-ttu-id="860d5-161">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-161">False</span></span>                                                              |
| <span data-ttu-id="860d5-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="860d5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="860d5-163">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-163">False</span></span>                                                              |
| <span data-ttu-id="860d5-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="860d5-164">Is Indexed</span></span>             | <span data-ttu-id="860d5-165">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-165">False</span></span>                                                              |
| <span data-ttu-id="860d5-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="860d5-166">In Global Catalog</span></span>      | <span data-ttu-id="860d5-167">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-167">False</span></span>                                                              |
| <span data-ttu-id="860d5-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="860d5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="860d5-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="860d5-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="860d5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="860d5-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="860d5-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-172">Search-Flags</span></span>           | <span data-ttu-id="860d5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="860d5-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="860d5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-174">System-Flags</span></span>           | <span data-ttu-id="860d5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="860d5-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="860d5-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="860d5-176">Classes used in</span></span>        | [<span data-ttu-id="860d5-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="860d5-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="860d5-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="860d5-178">Windows Server 2008</span></span>



| <span data-ttu-id="860d5-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-179">Entry</span></span> | <span data-ttu-id="860d5-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="860d5-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="860d5-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="860d5-183">System-Only</span></span>            | <span data-ttu-id="860d5-184">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-184">False</span></span>                                                              |
| <span data-ttu-id="860d5-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="860d5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="860d5-186">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-186">False</span></span>                                                              |
| <span data-ttu-id="860d5-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="860d5-187">Is Indexed</span></span>             | <span data-ttu-id="860d5-188">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-188">False</span></span>                                                              |
| <span data-ttu-id="860d5-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="860d5-189">In Global Catalog</span></span>      | <span data-ttu-id="860d5-190">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-190">False</span></span>                                                              |
| <span data-ttu-id="860d5-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="860d5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="860d5-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="860d5-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="860d5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="860d5-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="860d5-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-195">Search-Flags</span></span>           | <span data-ttu-id="860d5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="860d5-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="860d5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-197">System-Flags</span></span>           | <span data-ttu-id="860d5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="860d5-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="860d5-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="860d5-199">Classes used in</span></span>        | [<span data-ttu-id="860d5-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="860d5-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="860d5-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="860d5-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="860d5-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-202">Entry</span></span> | <span data-ttu-id="860d5-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="860d5-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="860d5-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="860d5-206">System-Only</span></span>            | <span data-ttu-id="860d5-207">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-207">False</span></span>                                                              |
| <span data-ttu-id="860d5-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="860d5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="860d5-209">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-209">False</span></span>                                                              |
| <span data-ttu-id="860d5-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="860d5-210">Is Indexed</span></span>             | <span data-ttu-id="860d5-211">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-211">False</span></span>                                                              |
| <span data-ttu-id="860d5-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="860d5-212">In Global Catalog</span></span>      | <span data-ttu-id="860d5-213">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-213">False</span></span>                                                              |
| <span data-ttu-id="860d5-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="860d5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="860d5-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="860d5-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="860d5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="860d5-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="860d5-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-218">Search-Flags</span></span>           | <span data-ttu-id="860d5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="860d5-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="860d5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-220">System-Flags</span></span>           | <span data-ttu-id="860d5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="860d5-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="860d5-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="860d5-222">Classes used in</span></span>        | [<span data-ttu-id="860d5-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="860d5-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="860d5-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="860d5-224">Windows Server 2012</span></span>



| <span data-ttu-id="860d5-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="860d5-225">Entry</span></span> | <span data-ttu-id="860d5-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="860d5-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="860d5-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="860d5-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="860d5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="860d5-229">System-Only</span></span>            | <span data-ttu-id="860d5-230">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-230">False</span></span>                                                              |
| <span data-ttu-id="860d5-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="860d5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="860d5-232">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-232">False</span></span>                                                              |
| <span data-ttu-id="860d5-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="860d5-233">Is Indexed</span></span>             | <span data-ttu-id="860d5-234">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-234">False</span></span>                                                              |
| <span data-ttu-id="860d5-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="860d5-235">In Global Catalog</span></span>      | <span data-ttu-id="860d5-236">Faux</span><span class="sxs-lookup"><span data-stu-id="860d5-236">False</span></span>                                                              |
| <span data-ttu-id="860d5-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="860d5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="860d5-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="860d5-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="860d5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="860d5-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="860d5-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="860d5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-241">Search-Flags</span></span>           | <span data-ttu-id="860d5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="860d5-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="860d5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="860d5-243">System-Flags</span></span>           | <span data-ttu-id="860d5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="860d5-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="860d5-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="860d5-245">Classes used in</span></span>        | [<span data-ttu-id="860d5-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="860d5-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





