---
title: Attribut NC-Name
description: Nom unique du contexte d’appellation de l’objet.
ms.assetid: c60294b6-b803-49b4-9c94-6c0b82a45a9c
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut NC-Name
- Schéma AD de l’attribut nCName
topic_type:
- apiref
api_name:
- NC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152083e53950be81f2942ac217691989d5eb07b7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106536089"
---
# <a name="nc-name-attribute"></a><span data-ttu-id="7cb2f-105">Attribut NC-Name</span><span class="sxs-lookup"><span data-stu-id="7cb2f-105">NC-Name attribute</span></span>

<span data-ttu-id="7cb2f-106">Nom unique du contexte d’appellation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7cb2f-106">The distinguished name of the Naming Context for the object.</span></span>



| <span data-ttu-id="7cb2f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-107">Entry</span></span> | <span data-ttu-id="7cb2f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7cb2f-109">CN</span><span class="sxs-lookup"><span data-stu-id="7cb2f-109">CN</span></span>                | <span data-ttu-id="7cb2f-110">NC-Name</span><span class="sxs-lookup"><span data-stu-id="7cb2f-110">NC-Name</span></span>                                 |
| <span data-ttu-id="7cb2f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7cb2f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7cb2f-112">nCName</span><span class="sxs-lookup"><span data-stu-id="7cb2f-112">nCName</span></span>                                  |
| <span data-ttu-id="7cb2f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7cb2f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7cb2f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7cb2f-114">Update Privilege</span></span>  | <span data-ttu-id="7cb2f-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="7cb2f-115">Domain administrator</span></span>                    |
| <span data-ttu-id="7cb2f-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7cb2f-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7cb2f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-117">Attribute-Id</span></span>      | <span data-ttu-id="7cb2f-118">1.2.840.113556.1.2.16</span><span class="sxs-lookup"><span data-stu-id="7cb2f-118">1.2.840.113556.1.2.16</span></span>                   |
| <span data-ttu-id="7cb2f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7cb2f-119">System-Id-Guid</span></span>    | <span data-ttu-id="7cb2f-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7cb2f-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="7cb2f-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb2f-121">Syntax</span></span>            | [<span data-ttu-id="7cb2f-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7cb2f-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7cb2f-123">Implementations</span></span>

-   [<span data-ttu-id="7cb2f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7cb2f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7cb2f-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7cb2f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7cb2f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7cb2f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7cb2f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7cb2f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7cb2f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7cb2f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-132">Entry</span></span> | <span data-ttu-id="7cb2f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-136">System-Only</span></span>            | <span data-ttu-id="7cb2f-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-137">True</span></span>                                       |
| <span data-ttu-id="7cb2f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-139">True</span></span>                                       |
| <span data-ttu-id="7cb2f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-140">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-141">False</span></span>                                      |
| <span data-ttu-id="7cb2f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-142">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-143">False</span></span>                                      |
| <span data-ttu-id="7cb2f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-148">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-149">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-150">System-Flags</span></span>           | <span data-ttu-id="7cb2f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-151">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-152">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-153">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7cb2f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7cb2f-154">Windows Server 2003</span></span>



| <span data-ttu-id="7cb2f-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-155">Entry</span></span> | <span data-ttu-id="7cb2f-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-159">System-Only</span></span>            | <span data-ttu-id="7cb2f-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-160">True</span></span>                                       |
| <span data-ttu-id="7cb2f-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-162">True</span></span>                                       |
| <span data-ttu-id="7cb2f-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-163">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-164">False</span></span>                                      |
| <span data-ttu-id="7cb2f-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-165">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-166">False</span></span>                                      |
| <span data-ttu-id="7cb2f-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-171">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-172">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-173">System-Flags</span></span>           | <span data-ttu-id="7cb2f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-174">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-175">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-176">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7cb2f-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="7cb2f-177">ADAM</span></span>



| <span data-ttu-id="7cb2f-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-178">Entry</span></span> | <span data-ttu-id="7cb2f-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-182">System-Only</span></span>            | <span data-ttu-id="7cb2f-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-183">True</span></span>                                       |
| <span data-ttu-id="7cb2f-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-185">True</span></span>                                       |
| <span data-ttu-id="7cb2f-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-186">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-187">False</span></span>                                      |
| <span data-ttu-id="7cb2f-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-188">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-189">False</span></span>                                      |
| <span data-ttu-id="7cb2f-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-194">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-195">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-196">System-Flags</span></span>           | <span data-ttu-id="7cb2f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-197">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-198">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-199">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7cb2f-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7cb2f-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7cb2f-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-201">Entry</span></span> | <span data-ttu-id="7cb2f-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-205">System-Only</span></span>            | <span data-ttu-id="7cb2f-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-206">True</span></span>                                       |
| <span data-ttu-id="7cb2f-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-208">True</span></span>                                       |
| <span data-ttu-id="7cb2f-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-209">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-210">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-210">False</span></span>                                      |
| <span data-ttu-id="7cb2f-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-211">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-212">False</span></span>                                      |
| <span data-ttu-id="7cb2f-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-217">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-218">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-219">System-Flags</span></span>           | <span data-ttu-id="7cb2f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-220">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-221">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-222">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7cb2f-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-223">Windows Server 2008</span></span>



| <span data-ttu-id="7cb2f-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-224">Entry</span></span> | <span data-ttu-id="7cb2f-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-228">System-Only</span></span>            | <span data-ttu-id="7cb2f-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-229">True</span></span>                                       |
| <span data-ttu-id="7cb2f-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-231">True</span></span>                                       |
| <span data-ttu-id="7cb2f-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-232">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-233">False</span></span>                                      |
| <span data-ttu-id="7cb2f-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-234">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-235">False</span></span>                                      |
| <span data-ttu-id="7cb2f-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-240">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-241">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-242">System-Flags</span></span>           | <span data-ttu-id="7cb2f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-243">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-244">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-245">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7cb2f-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cb2f-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7cb2f-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-247">Entry</span></span> | <span data-ttu-id="7cb2f-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-251">System-Only</span></span>            | <span data-ttu-id="7cb2f-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-252">True</span></span>                                       |
| <span data-ttu-id="7cb2f-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-254">True</span></span>                                       |
| <span data-ttu-id="7cb2f-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-255">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-256">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-256">False</span></span>                                      |
| <span data-ttu-id="7cb2f-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-257">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-258">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-258">False</span></span>                                      |
| <span data-ttu-id="7cb2f-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-263">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-264">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-265">System-Flags</span></span>           | <span data-ttu-id="7cb2f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-266">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-267">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-268">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7cb2f-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7cb2f-269">Windows Server 2012</span></span>



| <span data-ttu-id="7cb2f-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="7cb2f-270">Entry</span></span> | <span data-ttu-id="7cb2f-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb2f-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7cb2f-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7cb2f-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb2f-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7cb2f-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb2f-274">System-Only</span></span>            | <span data-ttu-id="7cb2f-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-275">True</span></span>                                       |
| <span data-ttu-id="7cb2f-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7cb2f-276">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb2f-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="7cb2f-277">True</span></span>                                       |
| <span data-ttu-id="7cb2f-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7cb2f-278">Is Indexed</span></span>             | <span data-ttu-id="7cb2f-279">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-279">False</span></span>                                      |
| <span data-ttu-id="7cb2f-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7cb2f-280">In Global Catalog</span></span>      | <span data-ttu-id="7cb2f-281">Faux</span><span class="sxs-lookup"><span data-stu-id="7cb2f-281">False</span></span>                                      |
| <span data-ttu-id="7cb2f-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7cb2f-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb2f-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7cb2f-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7cb2f-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb2f-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb2f-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7cb2f-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-286">Search-Flags</span></span>           | <span data-ttu-id="7cb2f-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7cb2f-287">0x00000008</span></span>                                 |
| <span data-ttu-id="7cb2f-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb2f-288">System-Flags</span></span>           | <span data-ttu-id="7cb2f-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb2f-289">0x00000010</span></span>                                 |
| <span data-ttu-id="7cb2f-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7cb2f-290">Classes used in</span></span>        | [<span data-ttu-id="7cb2f-291">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="7cb2f-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





