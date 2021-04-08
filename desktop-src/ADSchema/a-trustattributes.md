---
title: Attribut Trust-Attributes
description: Cet attribut stocke les attributs d’approbation pour un domaine approuvé.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Trust-Attributes
- Schéma AD de l’attribut trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744884"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="cd0eb-105">Attribut Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="cd0eb-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="cd0eb-106">Cet attribut stocke les attributs d’approbation pour un domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="cd0eb-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="cd0eb-107">Les valeurs d’attribut possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="cd0eb-108">\_Attribut de \_ confiance \_ : désactivation de la transitivité non transitive.</span><span class="sxs-lookup"><span data-stu-id="cd0eb-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="cd0eb-109">\_ \_ \_ L’approbation parente de l’arborescence d’attributs d’approbation est définie sur le parent de l’arborescence d’organisation.</span><span class="sxs-lookup"><span data-stu-id="cd0eb-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="cd0eb-110">\_ \_ Approbation racine de l’arborescence des attributs de confiance \_ définie sur une autre racine d’arborescence dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="cd0eb-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="cd0eb-111">Le \_ \_ \_ lien de confiance de niveau supérieur d’attribut uniquement valide uniquement pour le client de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="cd0eb-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="cd0eb-112">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-112">Entry</span></span> | <span data-ttu-id="cd0eb-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cd0eb-114">CN</span><span class="sxs-lookup"><span data-stu-id="cd0eb-114">CN</span></span>                | <span data-ttu-id="cd0eb-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="cd0eb-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="cd0eb-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cd0eb-116">Ldap-Display-Name</span></span> | <span data-ttu-id="cd0eb-117">trustAttributes</span><span class="sxs-lookup"><span data-stu-id="cd0eb-117">trustAttributes</span></span>                      |
| <span data-ttu-id="cd0eb-118">Taille</span><span class="sxs-lookup"><span data-stu-id="cd0eb-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="cd0eb-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cd0eb-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cd0eb-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cd0eb-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cd0eb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-121">Attribute-Id</span></span>      | <span data-ttu-id="cd0eb-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="cd0eb-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="cd0eb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd0eb-123">System-Id-Guid</span></span>    | <span data-ttu-id="cd0eb-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="cd0eb-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="cd0eb-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd0eb-125">Syntax</span></span>            | [<span data-ttu-id="cd0eb-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cd0eb-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cd0eb-127">Implementations</span></span>

-   [<span data-ttu-id="cd0eb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cd0eb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd0eb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd0eb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd0eb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd0eb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cd0eb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd0eb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="cd0eb-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-135">Entry</span></span> | <span data-ttu-id="cd0eb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-139">System-Only</span></span>            | <span data-ttu-id="cd0eb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-140">False</span></span>                                                |
| <span data-ttu-id="cd0eb-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-142">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-143">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-144">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-144">False</span></span>                                                |
| <span data-ttu-id="cd0eb-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-145">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-146">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-146">False</span></span>                                                |
| <span data-ttu-id="cd0eb-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-151">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-152">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-153">System-Flags</span></span>           | <span data-ttu-id="cd0eb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-154">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-155">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-156">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cd0eb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd0eb-157">Windows Server 2003</span></span>



| <span data-ttu-id="cd0eb-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-158">Entry</span></span> | <span data-ttu-id="cd0eb-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-162">System-Only</span></span>            | <span data-ttu-id="cd0eb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-163">False</span></span>                                                |
| <span data-ttu-id="cd0eb-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-165">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-166">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-167">False</span></span>                                                |
| <span data-ttu-id="cd0eb-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-168">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-169">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-174">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-175">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-176">System-Flags</span></span>           | <span data-ttu-id="cd0eb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-177">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-178">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-179">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd0eb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd0eb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd0eb-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-181">Entry</span></span> | <span data-ttu-id="cd0eb-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-185">System-Only</span></span>            | <span data-ttu-id="cd0eb-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-186">False</span></span>                                                |
| <span data-ttu-id="cd0eb-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-188">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-189">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-190">False</span></span>                                                |
| <span data-ttu-id="cd0eb-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-191">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-192">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-197">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-198">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-199">System-Flags</span></span>           | <span data-ttu-id="cd0eb-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-200">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-201">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-202">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd0eb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd0eb-203">Windows Server 2008</span></span>



| <span data-ttu-id="cd0eb-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-204">Entry</span></span> | <span data-ttu-id="cd0eb-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-208">System-Only</span></span>            | <span data-ttu-id="cd0eb-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-209">False</span></span>                                                |
| <span data-ttu-id="cd0eb-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-211">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-212">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-213">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-213">False</span></span>                                                |
| <span data-ttu-id="cd0eb-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-214">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-215">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-220">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-221">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-222">System-Flags</span></span>           | <span data-ttu-id="cd0eb-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-223">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-224">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-225">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd0eb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd0eb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd0eb-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-227">Entry</span></span> | <span data-ttu-id="cd0eb-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-231">System-Only</span></span>            | <span data-ttu-id="cd0eb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-232">False</span></span>                                                |
| <span data-ttu-id="cd0eb-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-234">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-235">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-236">False</span></span>                                                |
| <span data-ttu-id="cd0eb-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-237">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-238">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-243">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-244">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-245">System-Flags</span></span>           | <span data-ttu-id="cd0eb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-246">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-247">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-248">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd0eb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd0eb-249">Windows Server 2012</span></span>



| <span data-ttu-id="cd0eb-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd0eb-250">Entry</span></span> | <span data-ttu-id="cd0eb-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0eb-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cd0eb-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd0eb-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0eb-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cd0eb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0eb-254">System-Only</span></span>            | <span data-ttu-id="cd0eb-255">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-255">False</span></span>                                                |
| <span data-ttu-id="cd0eb-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd0eb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0eb-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-257">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd0eb-258">Is Indexed</span></span>             | <span data-ttu-id="cd0eb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="cd0eb-259">False</span></span>                                                |
| <span data-ttu-id="cd0eb-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd0eb-260">In Global Catalog</span></span>      | <span data-ttu-id="cd0eb-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd0eb-261">True</span></span>                                                 |
| <span data-ttu-id="cd0eb-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd0eb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0eb-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd0eb-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cd0eb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0eb-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0eb-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cd0eb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-266">Search-Flags</span></span>           | <span data-ttu-id="cd0eb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd0eb-267">0x00000000</span></span>                                           |
| <span data-ttu-id="cd0eb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0eb-268">System-Flags</span></span>           | <span data-ttu-id="cd0eb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0eb-269">0x00000010</span></span>                                           |
| <span data-ttu-id="cd0eb-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd0eb-270">Classes used in</span></span>        | [<span data-ttu-id="cd0eb-271">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="cd0eb-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





