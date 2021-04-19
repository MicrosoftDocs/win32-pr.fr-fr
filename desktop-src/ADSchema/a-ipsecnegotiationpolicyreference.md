---
title: IPSec-négociation-stratégie-attribut de référence
description: L’attribut IPSec-Negotiation-Policy-Reference est destiné à un usage interne uniquement.
ms.assetid: d30d8817-0661-430a-939d-f91072585807
ms.tgt_platform: multiple
keywords:
- IPSec-négociation-stratégie-schéma AD (attribut de référence)
- Schéma AD de l’attribut ipsecNegotiationPolicyReference
topic_type:
- apiref
api_name:
- Ipsec-Negotiation-Policy-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b0fa5ca8d564b02e27aa5c9dfbcb7f3a90d78e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106512002"
---
# <a name="ipsec-negotiation-policy-reference-attribute"></a><span data-ttu-id="5fc3f-105">IPSec-négociation-stratégie-attribut de référence</span><span class="sxs-lookup"><span data-stu-id="5fc3f-105">Ipsec-Negotiation-Policy-Reference attribute</span></span>

<span data-ttu-id="5fc3f-106">L’attribut **IPSec-Negotiation-Policy-Reference** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="5fc3f-106">The **Ipsec-Negotiation-Policy-Reference** attribute is for internal use only.</span></span>



| <span data-ttu-id="5fc3f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-107">Entry</span></span> | <span data-ttu-id="5fc3f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5fc3f-109">CN</span><span class="sxs-lookup"><span data-stu-id="5fc3f-109">CN</span></span>                | <span data-ttu-id="5fc3f-110">Informations de référence sur la stratégie IPSec-Negotiation</span><span class="sxs-lookup"><span data-stu-id="5fc3f-110">Ipsec-Negotiation-Policy-Reference</span></span>      |
| <span data-ttu-id="5fc3f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5fc3f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5fc3f-112">ipsecNegotiationPolicyReference</span><span class="sxs-lookup"><span data-stu-id="5fc3f-112">ipsecNegotiationPolicyReference</span></span>         |
| <span data-ttu-id="5fc3f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="5fc3f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5fc3f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="5fc3f-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="5fc3f-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="5fc3f-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5fc3f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-116">Attribute-Id</span></span>      | <span data-ttu-id="5fc3f-117">1.2.840.113556.1.4.628</span><span class="sxs-lookup"><span data-stu-id="5fc3f-117">1.2.840.113556.1.4.628</span></span>                  |
| <span data-ttu-id="5fc3f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5fc3f-118">System-Id-Guid</span></span>    | <span data-ttu-id="5fc3f-119">b40ff822-427a-11d1-a9c2-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5fc3f-119">b40ff822-427a-11d1-a9c2-0000f80367c1</span></span>    |
| <span data-ttu-id="5fc3f-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fc3f-120">Syntax</span></span>            | [<span data-ttu-id="5fc3f-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5fc3f-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="5fc3f-122">Implementations</span></span>

-   [<span data-ttu-id="5fc3f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5fc3f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5fc3f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5fc3f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5fc3f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5fc3f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5fc3f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5fc3f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5fc3f-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-130">Entry</span></span> | <span data-ttu-id="5fc3f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-132">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-133">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-134">System-Only</span></span>            | <span data-ttu-id="5fc3f-135">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-135">False</span></span>                                      |
| <span data-ttu-id="5fc3f-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-137">True</span></span>                                       |
| <span data-ttu-id="5fc3f-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-138">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-139">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-139">False</span></span>                                      |
| <span data-ttu-id="5fc3f-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-140">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-141">False</span></span>                                      |
| <span data-ttu-id="5fc3f-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-143">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-144">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-145">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-146">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-147">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-148">System-Flags</span></span>           | <span data-ttu-id="5fc3f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-149">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-150">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-151">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-151">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5fc3f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fc3f-152">Windows Server 2003</span></span>



| <span data-ttu-id="5fc3f-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-153">Entry</span></span> | <span data-ttu-id="5fc3f-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-154">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-155">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-156">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-157">System-Only</span></span>            | <span data-ttu-id="5fc3f-158">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-158">False</span></span>                                      |
| <span data-ttu-id="5fc3f-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-160">True</span></span>                                       |
| <span data-ttu-id="5fc3f-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-161">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-162">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-162">False</span></span>                                      |
| <span data-ttu-id="5fc3f-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-163">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-164">False</span></span>                                      |
| <span data-ttu-id="5fc3f-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-166">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-167">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-168">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-169">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-170">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-171">System-Flags</span></span>           | <span data-ttu-id="5fc3f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-172">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-173">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-174">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-174">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5fc3f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5fc3f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5fc3f-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-176">Entry</span></span> | <span data-ttu-id="5fc3f-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-177">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-178">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-179">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-180">System-Only</span></span>            | <span data-ttu-id="5fc3f-181">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-181">False</span></span>                                      |
| <span data-ttu-id="5fc3f-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-183">True</span></span>                                       |
| <span data-ttu-id="5fc3f-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-184">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-185">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-185">False</span></span>                                      |
| <span data-ttu-id="5fc3f-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-186">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-187">False</span></span>                                      |
| <span data-ttu-id="5fc3f-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-189">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-190">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-191">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-192">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-193">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-194">System-Flags</span></span>           | <span data-ttu-id="5fc3f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-195">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-196">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-197">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-197">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5fc3f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fc3f-198">Windows Server 2008</span></span>



| <span data-ttu-id="5fc3f-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-199">Entry</span></span> | <span data-ttu-id="5fc3f-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-200">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-201">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-202">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-203">System-Only</span></span>            | <span data-ttu-id="5fc3f-204">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-204">False</span></span>                                      |
| <span data-ttu-id="5fc3f-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-206">True</span></span>                                       |
| <span data-ttu-id="5fc3f-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-207">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-208">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-208">False</span></span>                                      |
| <span data-ttu-id="5fc3f-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-209">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-210">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-210">False</span></span>                                      |
| <span data-ttu-id="5fc3f-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-212">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-213">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-214">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-215">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-216">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-217">System-Flags</span></span>           | <span data-ttu-id="5fc3f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-218">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-219">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-220">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-220">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5fc3f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5fc3f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5fc3f-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-222">Entry</span></span> | <span data-ttu-id="5fc3f-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-223">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-224">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-225">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-226">System-Only</span></span>            | <span data-ttu-id="5fc3f-227">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-227">False</span></span>                                      |
| <span data-ttu-id="5fc3f-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-229">True</span></span>                                       |
| <span data-ttu-id="5fc3f-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-230">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-231">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-231">False</span></span>                                      |
| <span data-ttu-id="5fc3f-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-232">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-233">False</span></span>                                      |
| <span data-ttu-id="5fc3f-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-235">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-236">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-237">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-238">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-239">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-240">System-Flags</span></span>           | <span data-ttu-id="5fc3f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-241">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-242">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-243">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-243">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5fc3f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fc3f-244">Windows Server 2012</span></span>



| <span data-ttu-id="5fc3f-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-245">Entry</span></span> | <span data-ttu-id="5fc3f-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-246">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5fc3f-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5fc3f-247">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc3f-248">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5fc3f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc3f-249">System-Only</span></span>            | <span data-ttu-id="5fc3f-250">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-250">False</span></span>                                      |
| <span data-ttu-id="5fc3f-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5fc3f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc3f-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="5fc3f-252">True</span></span>                                       |
| <span data-ttu-id="5fc3f-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5fc3f-253">Is Indexed</span></span>             | <span data-ttu-id="5fc3f-254">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-254">False</span></span>                                      |
| <span data-ttu-id="5fc3f-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5fc3f-255">In Global Catalog</span></span>      | <span data-ttu-id="5fc3f-256">Faux</span><span class="sxs-lookup"><span data-stu-id="5fc3f-256">False</span></span>                                      |
| <span data-ttu-id="5fc3f-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5fc3f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc3f-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5fc3f-258">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5fc3f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc3f-259">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc3f-260">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5fc3f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-261">Search-Flags</span></span>           | <span data-ttu-id="5fc3f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc3f-262">0x00000000</span></span>                                 |
| <span data-ttu-id="5fc3f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc3f-263">System-Flags</span></span>           | <span data-ttu-id="5fc3f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc3f-264">0x00000010</span></span>                                 |
| <span data-ttu-id="5fc3f-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5fc3f-265">Classes used in</span></span>        | [<span data-ttu-id="5fc3f-266">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-266">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



 

 





