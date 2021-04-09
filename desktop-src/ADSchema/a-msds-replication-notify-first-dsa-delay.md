---
title: attribut ms-DS-Replication-Notify-First-DSA-Delay
description: Cet attribut contrôle le délai entre les modifications du DS et la notification du premier partenaire de réplication pour un contexte de nommage.
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Replication-notification-First-DSA-Delay
- Schéma AD de l’attribut msDS-Replication-Notify-First-DSA-Delay
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845133"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="c3b70-105">attribut ms-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="c3b70-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="c3b70-106">Cet attribut contrôle le délai entre les modifications du DS et la notification du premier partenaire de réplication pour un contexte de nommage.</span><span class="sxs-lookup"><span data-stu-id="c3b70-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="c3b70-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-107">Entry</span></span> | <span data-ttu-id="c3b70-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="c3b70-109">CN</span><span class="sxs-lookup"><span data-stu-id="c3b70-109">CN</span></span>                | <span data-ttu-id="c3b70-110">ms-DS-réplication-notification-premier-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="c3b70-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="c3b70-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c3b70-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c3b70-112">msDS-Replication-notification-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="c3b70-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="c3b70-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c3b70-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="c3b70-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c3b70-114">Update Privilege</span></span>  | <span data-ttu-id="c3b70-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="c3b70-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="c3b70-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c3b70-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="c3b70-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-117">Attribute-Id</span></span>      | <span data-ttu-id="c3b70-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="c3b70-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="c3b70-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3b70-119">System-Id-Guid</span></span>    | <span data-ttu-id="c3b70-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="c3b70-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="c3b70-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3b70-121">Syntax</span></span>            | [<span data-ttu-id="c3b70-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c3b70-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="c3b70-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c3b70-123">Implementations</span></span>

-   [<span data-ttu-id="c3b70-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3b70-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3b70-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c3b70-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c3b70-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3b70-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3b70-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3b70-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3b70-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3b70-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3b70-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3b70-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c3b70-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3b70-130">Windows Server 2003</span></span>



| <span data-ttu-id="c3b70-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-131">Entry</span></span> | <span data-ttu-id="c3b70-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-135">System-Only</span></span>            | <span data-ttu-id="c3b70-136">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-136">False</span></span>                                      |
| <span data-ttu-id="c3b70-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-138">True</span></span>                                       |
| <span data-ttu-id="c3b70-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-139">Is Indexed</span></span>             | <span data-ttu-id="c3b70-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-140">False</span></span>                                      |
| <span data-ttu-id="c3b70-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-141">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-142">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-142">False</span></span>                                      |
| <span data-ttu-id="c3b70-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-147">Search-Flags</span></span>           | <span data-ttu-id="c3b70-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-148">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-149">System-Flags</span></span>           | <span data-ttu-id="c3b70-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-150">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-151">Classes used in</span></span>        | [<span data-ttu-id="c3b70-152">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c3b70-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="c3b70-153">ADAM</span></span>



| <span data-ttu-id="c3b70-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-154">Entry</span></span> | <span data-ttu-id="c3b70-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-158">System-Only</span></span>            | <span data-ttu-id="c3b70-159">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-159">False</span></span>                                      |
| <span data-ttu-id="c3b70-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-161">True</span></span>                                       |
| <span data-ttu-id="c3b70-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-162">Is Indexed</span></span>             | <span data-ttu-id="c3b70-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-163">False</span></span>                                      |
| <span data-ttu-id="c3b70-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-164">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-165">False</span></span>                                      |
| <span data-ttu-id="c3b70-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-170">Search-Flags</span></span>           | <span data-ttu-id="c3b70-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-171">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-172">System-Flags</span></span>           | <span data-ttu-id="c3b70-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-173">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-174">Classes used in</span></span>        | [<span data-ttu-id="c3b70-175">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3b70-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3b70-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3b70-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-177">Entry</span></span> | <span data-ttu-id="c3b70-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-181">System-Only</span></span>            | <span data-ttu-id="c3b70-182">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-182">False</span></span>                                      |
| <span data-ttu-id="c3b70-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-184">True</span></span>                                       |
| <span data-ttu-id="c3b70-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-185">Is Indexed</span></span>             | <span data-ttu-id="c3b70-186">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-186">False</span></span>                                      |
| <span data-ttu-id="c3b70-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-187">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-188">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-188">False</span></span>                                      |
| <span data-ttu-id="c3b70-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-193">Search-Flags</span></span>           | <span data-ttu-id="c3b70-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-194">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-195">System-Flags</span></span>           | <span data-ttu-id="c3b70-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-196">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-197">Classes used in</span></span>        | [<span data-ttu-id="c3b70-198">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3b70-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3b70-199">Windows Server 2008</span></span>



| <span data-ttu-id="c3b70-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-200">Entry</span></span> | <span data-ttu-id="c3b70-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-204">System-Only</span></span>            | <span data-ttu-id="c3b70-205">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-205">False</span></span>                                      |
| <span data-ttu-id="c3b70-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-207">True</span></span>                                       |
| <span data-ttu-id="c3b70-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-208">Is Indexed</span></span>             | <span data-ttu-id="c3b70-209">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-209">False</span></span>                                      |
| <span data-ttu-id="c3b70-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-210">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-211">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-211">False</span></span>                                      |
| <span data-ttu-id="c3b70-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-216">Search-Flags</span></span>           | <span data-ttu-id="c3b70-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-217">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-218">System-Flags</span></span>           | <span data-ttu-id="c3b70-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-219">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-220">Classes used in</span></span>        | [<span data-ttu-id="c3b70-221">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3b70-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3b70-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3b70-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-223">Entry</span></span> | <span data-ttu-id="c3b70-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-227">System-Only</span></span>            | <span data-ttu-id="c3b70-228">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-228">False</span></span>                                      |
| <span data-ttu-id="c3b70-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-230">True</span></span>                                       |
| <span data-ttu-id="c3b70-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-231">Is Indexed</span></span>             | <span data-ttu-id="c3b70-232">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-232">False</span></span>                                      |
| <span data-ttu-id="c3b70-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-233">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-234">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-234">False</span></span>                                      |
| <span data-ttu-id="c3b70-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-239">Search-Flags</span></span>           | <span data-ttu-id="c3b70-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-240">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-241">System-Flags</span></span>           | <span data-ttu-id="c3b70-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-242">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-243">Classes used in</span></span>        | [<span data-ttu-id="c3b70-244">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3b70-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3b70-245">Windows Server 2012</span></span>



| <span data-ttu-id="c3b70-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3b70-246">Entry</span></span> | <span data-ttu-id="c3b70-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b70-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c3b70-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c3b70-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b70-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c3b70-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b70-250">System-Only</span></span>            | <span data-ttu-id="c3b70-251">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-251">False</span></span>                                      |
| <span data-ttu-id="c3b70-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c3b70-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b70-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="c3b70-253">True</span></span>                                       |
| <span data-ttu-id="c3b70-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c3b70-254">Is Indexed</span></span>             | <span data-ttu-id="c3b70-255">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-255">False</span></span>                                      |
| <span data-ttu-id="c3b70-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c3b70-256">In Global Catalog</span></span>      | <span data-ttu-id="c3b70-257">Faux</span><span class="sxs-lookup"><span data-stu-id="c3b70-257">False</span></span>                                      |
| <span data-ttu-id="c3b70-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c3b70-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b70-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c3b70-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c3b70-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b70-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b70-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c3b70-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-262">Search-Flags</span></span>           | <span data-ttu-id="c3b70-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3b70-263">0x00000000</span></span>                                 |
| <span data-ttu-id="c3b70-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b70-264">System-Flags</span></span>           | <span data-ttu-id="c3b70-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b70-265">0x00000010</span></span>                                 |
| <span data-ttu-id="c3b70-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c3b70-266">Classes used in</span></span>        | [<span data-ttu-id="c3b70-267">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="c3b70-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





