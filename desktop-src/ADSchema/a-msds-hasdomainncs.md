---
title: attribut ms-DS-has-domaine-NC
description: Informations de réplication du service d’annuaire qui détaillent les contextes d’attribution de noms de domaine présents sur un serveur particulier.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-has-domaine-NC
- Schéma Active Directory de l’attribut msDS-HasDomainNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480100"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="37c3f-105">attribut ms-DS-has-domaine-NC</span><span class="sxs-lookup"><span data-stu-id="37c3f-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="37c3f-106">Informations de réplication du service d’annuaire qui détaillent les contextes d’attribution de noms de domaine présents sur un serveur particulier.</span><span class="sxs-lookup"><span data-stu-id="37c3f-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="37c3f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-107">Entry</span></span> | <span data-ttu-id="37c3f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="37c3f-109">CN</span><span class="sxs-lookup"><span data-stu-id="37c3f-109">CN</span></span>                | <span data-ttu-id="37c3f-110">ms-DS-a-Domain-NC</span><span class="sxs-lookup"><span data-stu-id="37c3f-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="37c3f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="37c3f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="37c3f-112">msDS-HasDomainNCs</span><span class="sxs-lookup"><span data-stu-id="37c3f-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="37c3f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="37c3f-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="37c3f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="37c3f-114">Update Privilege</span></span>  | <span data-ttu-id="37c3f-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="37c3f-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="37c3f-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="37c3f-116">Update Frequency</span></span>  | <span data-ttu-id="37c3f-117">Il est défini par DCPromo et n’est jamais modifié par la suite.</span><span class="sxs-lookup"><span data-stu-id="37c3f-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="37c3f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-118">Attribute-Id</span></span>      | <span data-ttu-id="37c3f-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="37c3f-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="37c3f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="37c3f-120">System-Id-Guid</span></span>    | <span data-ttu-id="37c3f-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="37c3f-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="37c3f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37c3f-122">Syntax</span></span>            | [<span data-ttu-id="37c3f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="37c3f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="37c3f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="37c3f-124">Implementations</span></span>

-   [<span data-ttu-id="37c3f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37c3f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37c3f-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="37c3f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="37c3f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37c3f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37c3f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37c3f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37c3f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37c3f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37c3f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37c3f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="37c3f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37c3f-131">Windows Server 2003</span></span>



| <span data-ttu-id="37c3f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-132">Entry</span></span> | <span data-ttu-id="37c3f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-134">Link-Id</span></span>                | <span data-ttu-id="37c3f-135">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-135">2026</span></span>                                     |
| <span data-ttu-id="37c3f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-137">System-Only</span></span>            | <span data-ttu-id="37c3f-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-138">True</span></span>                                     |
| <span data-ttu-id="37c3f-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-140">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-140">False</span></span>                                    |
| <span data-ttu-id="37c3f-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-141">Is Indexed</span></span>             | <span data-ttu-id="37c3f-142">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-142">False</span></span>                                    |
| <span data-ttu-id="37c3f-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-143">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-144">False</span></span>                                    |
| <span data-ttu-id="37c3f-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-147">Range-Lower</span></span>            | <span data-ttu-id="37c3f-148">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-148">4</span></span>                                        |
| <span data-ttu-id="37c3f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-149">Range-Upper</span></span>            | <span data-ttu-id="37c3f-150">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-150">4</span></span>                                        |
| <span data-ttu-id="37c3f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-151">Search-Flags</span></span>           | <span data-ttu-id="37c3f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-152">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-153">System-Flags</span></span>           | <span data-ttu-id="37c3f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-154">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-155">Classes used in</span></span>        | [<span data-ttu-id="37c3f-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="37c3f-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="37c3f-157">ADAM</span></span>



| <span data-ttu-id="37c3f-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-158">Entry</span></span> | <span data-ttu-id="37c3f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-160">Link-Id</span></span>                | <span data-ttu-id="37c3f-161">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-161">2026</span></span>                                     |
| <span data-ttu-id="37c3f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-163">System-Only</span></span>            | <span data-ttu-id="37c3f-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-164">True</span></span>                                     |
| <span data-ttu-id="37c3f-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-166">False</span></span>                                    |
| <span data-ttu-id="37c3f-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-167">Is Indexed</span></span>             | <span data-ttu-id="37c3f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-168">False</span></span>                                    |
| <span data-ttu-id="37c3f-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-169">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-170">False</span></span>                                    |
| <span data-ttu-id="37c3f-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-173">Range-Lower</span></span>            | <span data-ttu-id="37c3f-174">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-174">4</span></span>                                        |
| <span data-ttu-id="37c3f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-175">Range-Upper</span></span>            | <span data-ttu-id="37c3f-176">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-176">4</span></span>                                        |
| <span data-ttu-id="37c3f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-177">Search-Flags</span></span>           | <span data-ttu-id="37c3f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-178">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-179">System-Flags</span></span>           | <span data-ttu-id="37c3f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-180">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-181">Classes used in</span></span>        | [<span data-ttu-id="37c3f-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37c3f-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37c3f-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37c3f-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-184">Entry</span></span> | <span data-ttu-id="37c3f-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-186">Link-Id</span></span>                | <span data-ttu-id="37c3f-187">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-187">2026</span></span>                                     |
| <span data-ttu-id="37c3f-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-189">System-Only</span></span>            | <span data-ttu-id="37c3f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-190">True</span></span>                                     |
| <span data-ttu-id="37c3f-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-192">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-192">False</span></span>                                    |
| <span data-ttu-id="37c3f-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-193">Is Indexed</span></span>             | <span data-ttu-id="37c3f-194">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-194">False</span></span>                                    |
| <span data-ttu-id="37c3f-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-195">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-196">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-196">False</span></span>                                    |
| <span data-ttu-id="37c3f-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-199">Range-Lower</span></span>            | <span data-ttu-id="37c3f-200">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-200">4</span></span>                                        |
| <span data-ttu-id="37c3f-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-201">Range-Upper</span></span>            | <span data-ttu-id="37c3f-202">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-202">4</span></span>                                        |
| <span data-ttu-id="37c3f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-203">Search-Flags</span></span>           | <span data-ttu-id="37c3f-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-204">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-205">System-Flags</span></span>           | <span data-ttu-id="37c3f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-206">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-207">Classes used in</span></span>        | [<span data-ttu-id="37c3f-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37c3f-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37c3f-209">Windows Server 2008</span></span>



| <span data-ttu-id="37c3f-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-210">Entry</span></span> | <span data-ttu-id="37c3f-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-212">Link-Id</span></span>                | <span data-ttu-id="37c3f-213">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-213">2026</span></span>                                     |
| <span data-ttu-id="37c3f-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-215">System-Only</span></span>            | <span data-ttu-id="37c3f-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-216">True</span></span>                                     |
| <span data-ttu-id="37c3f-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-217">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-218">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-218">False</span></span>                                    |
| <span data-ttu-id="37c3f-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-219">Is Indexed</span></span>             | <span data-ttu-id="37c3f-220">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-220">False</span></span>                                    |
| <span data-ttu-id="37c3f-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-221">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-222">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-222">False</span></span>                                    |
| <span data-ttu-id="37c3f-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-225">Range-Lower</span></span>            | <span data-ttu-id="37c3f-226">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-226">4</span></span>                                        |
| <span data-ttu-id="37c3f-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-227">Range-Upper</span></span>            | <span data-ttu-id="37c3f-228">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-228">4</span></span>                                        |
| <span data-ttu-id="37c3f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-229">Search-Flags</span></span>           | <span data-ttu-id="37c3f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-230">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-231">System-Flags</span></span>           | <span data-ttu-id="37c3f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-232">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-233">Classes used in</span></span>        | [<span data-ttu-id="37c3f-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37c3f-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37c3f-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37c3f-236">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-236">Entry</span></span> | <span data-ttu-id="37c3f-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-238">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-238">Link-Id</span></span>                | <span data-ttu-id="37c3f-239">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-239">2026</span></span>                                     |
| <span data-ttu-id="37c3f-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-241">System-Only</span></span>            | <span data-ttu-id="37c3f-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-242">True</span></span>                                     |
| <span data-ttu-id="37c3f-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-243">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-244">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-244">False</span></span>                                    |
| <span data-ttu-id="37c3f-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-245">Is Indexed</span></span>             | <span data-ttu-id="37c3f-246">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-246">False</span></span>                                    |
| <span data-ttu-id="37c3f-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-247">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-248">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-248">False</span></span>                                    |
| <span data-ttu-id="37c3f-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-251">Range-Lower</span></span>            | <span data-ttu-id="37c3f-252">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-252">4</span></span>                                        |
| <span data-ttu-id="37c3f-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-253">Range-Upper</span></span>            | <span data-ttu-id="37c3f-254">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-254">4</span></span>                                        |
| <span data-ttu-id="37c3f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-255">Search-Flags</span></span>           | <span data-ttu-id="37c3f-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-256">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-257">System-Flags</span></span>           | <span data-ttu-id="37c3f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-258">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-259">Classes used in</span></span>        | [<span data-ttu-id="37c3f-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37c3f-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37c3f-261">Windows Server 2012</span></span>



| <span data-ttu-id="37c3f-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="37c3f-262">Entry</span></span> | <span data-ttu-id="37c3f-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3f-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="37c3f-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="37c3f-264">Link-Id</span></span>                | <span data-ttu-id="37c3f-265">2026</span><span class="sxs-lookup"><span data-stu-id="37c3f-265">2026</span></span>                                     |
| <span data-ttu-id="37c3f-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3f-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="37c3f-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3f-267">System-Only</span></span>            | <span data-ttu-id="37c3f-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="37c3f-268">True</span></span>                                     |
| <span data-ttu-id="37c3f-269">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="37c3f-269">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3f-270">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-270">False</span></span>                                    |
| <span data-ttu-id="37c3f-271">Est indexé</span><span class="sxs-lookup"><span data-stu-id="37c3f-271">Is Indexed</span></span>             | <span data-ttu-id="37c3f-272">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-272">False</span></span>                                    |
| <span data-ttu-id="37c3f-273">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="37c3f-273">In Global Catalog</span></span>      | <span data-ttu-id="37c3f-274">Faux</span><span class="sxs-lookup"><span data-stu-id="37c3f-274">False</span></span>                                    |
| <span data-ttu-id="37c3f-275">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="37c3f-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3f-276">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="37c3f-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="37c3f-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3f-277">Range-Lower</span></span>            | <span data-ttu-id="37c3f-278">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-278">4</span></span>                                        |
| <span data-ttu-id="37c3f-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3f-279">Range-Upper</span></span>            | <span data-ttu-id="37c3f-280">4</span><span class="sxs-lookup"><span data-stu-id="37c3f-280">4</span></span>                                        |
| <span data-ttu-id="37c3f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-281">Search-Flags</span></span>           | <span data-ttu-id="37c3f-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3f-282">0x00000000</span></span>                               |
| <span data-ttu-id="37c3f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3f-283">System-Flags</span></span>           | <span data-ttu-id="37c3f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3f-284">0x00000010</span></span>                               |
| <span data-ttu-id="37c3f-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="37c3f-285">Classes used in</span></span>        | [<span data-ttu-id="37c3f-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="37c3f-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





