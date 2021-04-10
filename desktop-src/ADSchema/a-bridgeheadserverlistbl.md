---
title: Pont-serveur-List-BL (attribut)
description: Liste des serveurs qui sont des serveurs ponts pour la réplication.
ms.assetid: b84176af-c6d2-4390-92d1-d29949da0691
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut tête de pont-serveur-liste-BL
- Schéma AD de l’attribut bridgeheadServerListBL
topic_type:
- apiref
api_name:
- Bridgehead-Server-List-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df941f323916682158c6c1c3ac59856b31da03f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107278"
---
# <a name="bridgehead-server-list-bl-attribute"></a><span data-ttu-id="e21f6-105">Pont-serveur-List-BL (attribut)</span><span class="sxs-lookup"><span data-stu-id="e21f6-105">Bridgehead-Server-List-BL attribute</span></span>

<span data-ttu-id="e21f6-106">Liste des serveurs qui sont des serveurs ponts pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="e21f6-106">The list of servers that are bridgeheads for replication.</span></span>



| <span data-ttu-id="e21f6-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-107">Entry</span></span> | <span data-ttu-id="e21f6-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e21f6-109">CN</span><span class="sxs-lookup"><span data-stu-id="e21f6-109">CN</span></span>                | <span data-ttu-id="e21f6-110">Tête de pont-serveur-liste-BL</span><span class="sxs-lookup"><span data-stu-id="e21f6-110">Bridgehead-Server-List-BL</span></span>               |
| <span data-ttu-id="e21f6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e21f6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e21f6-112">bridgeheadServerListBL</span><span class="sxs-lookup"><span data-stu-id="e21f6-112">bridgeheadServerListBL</span></span>                  |
| <span data-ttu-id="e21f6-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e21f6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e21f6-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e21f6-114">Update Privilege</span></span>  | <span data-ttu-id="e21f6-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e21f6-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="e21f6-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e21f6-116">Update Frequency</span></span>  | <span data-ttu-id="e21f6-117">Chaque fois qu’un site est configuré.</span><span class="sxs-lookup"><span data-stu-id="e21f6-117">Whenever a site is setup.</span></span>               |
| <span data-ttu-id="e21f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-118">Attribute-Id</span></span>      | <span data-ttu-id="e21f6-119">1.2.840.113556.1.4.820</span><span class="sxs-lookup"><span data-stu-id="e21f6-119">1.2.840.113556.1.4.820</span></span>                  |
| <span data-ttu-id="e21f6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e21f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="e21f6-121">d50c2cdb-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e21f6-121">d50c2cdb-8951-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="e21f6-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e21f6-122">Syntax</span></span>            | [<span data-ttu-id="e21f6-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e21f6-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e21f6-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e21f6-124">Implementations</span></span>

-   [<span data-ttu-id="e21f6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e21f6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e21f6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e21f6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e21f6-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e21f6-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e21f6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e21f6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e21f6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e21f6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e21f6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e21f6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e21f6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e21f6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e21f6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e21f6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e21f6-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-133">Entry</span></span> | <span data-ttu-id="e21f6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-135">Link-Id</span></span>                | <span data-ttu-id="e21f6-136">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-136">99</span></span>                              |
| <span data-ttu-id="e21f6-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-138">System-Only</span></span>            | <span data-ttu-id="e21f6-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-139">True</span></span>                            |
| <span data-ttu-id="e21f6-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-141">False</span></span>                           |
| <span data-ttu-id="e21f6-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-142">Is Indexed</span></span>             | <span data-ttu-id="e21f6-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-143">False</span></span>                           |
| <span data-ttu-id="e21f6-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-144">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-145">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-145">False</span></span>                           |
| <span data-ttu-id="e21f6-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-150">Search-Flags</span></span>           | <span data-ttu-id="e21f6-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-151">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-152">System-Flags</span></span>           | <span data-ttu-id="e21f6-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-153">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-154">Classes used in</span></span>        | [<span data-ttu-id="e21f6-155">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e21f6-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e21f6-156">Windows Server 2003</span></span>



| <span data-ttu-id="e21f6-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-157">Entry</span></span> | <span data-ttu-id="e21f6-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-159">Link-Id</span></span>                | <span data-ttu-id="e21f6-160">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-160">99</span></span>                              |
| <span data-ttu-id="e21f6-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-162">System-Only</span></span>            | <span data-ttu-id="e21f6-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-163">True</span></span>                            |
| <span data-ttu-id="e21f6-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-165">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-165">False</span></span>                           |
| <span data-ttu-id="e21f6-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-166">Is Indexed</span></span>             | <span data-ttu-id="e21f6-167">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-167">False</span></span>                           |
| <span data-ttu-id="e21f6-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-168">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-169">False</span></span>                           |
| <span data-ttu-id="e21f6-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-174">Search-Flags</span></span>           | <span data-ttu-id="e21f6-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-175">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-176">System-Flags</span></span>           | <span data-ttu-id="e21f6-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-177">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-178">Classes used in</span></span>        | [<span data-ttu-id="e21f6-179">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e21f6-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="e21f6-180">ADAM</span></span>



| <span data-ttu-id="e21f6-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-181">Entry</span></span> | <span data-ttu-id="e21f6-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-183">Link-Id</span></span>                | <span data-ttu-id="e21f6-184">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-184">99</span></span>                              |
| <span data-ttu-id="e21f6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-186">System-Only</span></span>            | <span data-ttu-id="e21f6-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-187">True</span></span>                            |
| <span data-ttu-id="e21f6-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-189">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-189">False</span></span>                           |
| <span data-ttu-id="e21f6-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-190">Is Indexed</span></span>             | <span data-ttu-id="e21f6-191">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-191">False</span></span>                           |
| <span data-ttu-id="e21f6-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-192">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-193">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-193">False</span></span>                           |
| <span data-ttu-id="e21f6-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-198">Search-Flags</span></span>           | <span data-ttu-id="e21f6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-199">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-200">System-Flags</span></span>           | <span data-ttu-id="e21f6-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-201">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-202">Classes used in</span></span>        | [<span data-ttu-id="e21f6-203">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e21f6-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e21f6-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e21f6-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-205">Entry</span></span> | <span data-ttu-id="e21f6-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-207">Link-Id</span></span>                | <span data-ttu-id="e21f6-208">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-208">99</span></span>                              |
| <span data-ttu-id="e21f6-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-210">System-Only</span></span>            | <span data-ttu-id="e21f6-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-211">True</span></span>                            |
| <span data-ttu-id="e21f6-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-212">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-213">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-213">False</span></span>                           |
| <span data-ttu-id="e21f6-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-214">Is Indexed</span></span>             | <span data-ttu-id="e21f6-215">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-215">False</span></span>                           |
| <span data-ttu-id="e21f6-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-216">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-217">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-217">False</span></span>                           |
| <span data-ttu-id="e21f6-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-222">Search-Flags</span></span>           | <span data-ttu-id="e21f6-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-223">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-224">System-Flags</span></span>           | <span data-ttu-id="e21f6-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-225">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-226">Classes used in</span></span>        | [<span data-ttu-id="e21f6-227">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e21f6-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e21f6-228">Windows Server 2008</span></span>



| <span data-ttu-id="e21f6-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-229">Entry</span></span> | <span data-ttu-id="e21f6-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-231">Link-Id</span></span>                | <span data-ttu-id="e21f6-232">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-232">99</span></span>                              |
| <span data-ttu-id="e21f6-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-234">System-Only</span></span>            | <span data-ttu-id="e21f6-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-235">True</span></span>                            |
| <span data-ttu-id="e21f6-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-237">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-237">False</span></span>                           |
| <span data-ttu-id="e21f6-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-238">Is Indexed</span></span>             | <span data-ttu-id="e21f6-239">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-239">False</span></span>                           |
| <span data-ttu-id="e21f6-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-240">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-241">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-241">False</span></span>                           |
| <span data-ttu-id="e21f6-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-246">Search-Flags</span></span>           | <span data-ttu-id="e21f6-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-247">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-248">System-Flags</span></span>           | <span data-ttu-id="e21f6-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-249">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-250">Classes used in</span></span>        | [<span data-ttu-id="e21f6-251">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e21f6-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e21f6-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e21f6-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-253">Entry</span></span> | <span data-ttu-id="e21f6-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-255">Link-Id</span></span>                | <span data-ttu-id="e21f6-256">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-256">99</span></span>                              |
| <span data-ttu-id="e21f6-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-257">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-258">System-Only</span></span>            | <span data-ttu-id="e21f6-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-259">True</span></span>                            |
| <span data-ttu-id="e21f6-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-260">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-261">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-261">False</span></span>                           |
| <span data-ttu-id="e21f6-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-262">Is Indexed</span></span>             | <span data-ttu-id="e21f6-263">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-263">False</span></span>                           |
| <span data-ttu-id="e21f6-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-264">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-265">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-265">False</span></span>                           |
| <span data-ttu-id="e21f6-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-270">Search-Flags</span></span>           | <span data-ttu-id="e21f6-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-271">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-272">System-Flags</span></span>           | <span data-ttu-id="e21f6-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-273">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-274">Classes used in</span></span>        | [<span data-ttu-id="e21f6-275">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e21f6-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e21f6-276">Windows Server 2012</span></span>



| <span data-ttu-id="e21f6-277">Entrée</span><span class="sxs-lookup"><span data-stu-id="e21f6-277">Entry</span></span> | <span data-ttu-id="e21f6-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="e21f6-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e21f6-279">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e21f6-279">Link-Id</span></span>                | <span data-ttu-id="e21f6-280">99</span><span class="sxs-lookup"><span data-stu-id="e21f6-280">99</span></span>                              |
| <span data-ttu-id="e21f6-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e21f6-281">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e21f6-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="e21f6-282">System-Only</span></span>            | <span data-ttu-id="e21f6-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="e21f6-283">True</span></span>                            |
| <span data-ttu-id="e21f6-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e21f6-284">Is-Single-Valued</span></span>       | <span data-ttu-id="e21f6-285">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-285">False</span></span>                           |
| <span data-ttu-id="e21f6-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e21f6-286">Is Indexed</span></span>             | <span data-ttu-id="e21f6-287">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-287">False</span></span>                           |
| <span data-ttu-id="e21f6-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e21f6-288">In Global Catalog</span></span>      | <span data-ttu-id="e21f6-289">Faux</span><span class="sxs-lookup"><span data-stu-id="e21f6-289">False</span></span>                           |
| <span data-ttu-id="e21f6-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e21f6-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="e21f6-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e21f6-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e21f6-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e21f6-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e21f6-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e21f6-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e21f6-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-294">Search-Flags</span></span>           | <span data-ttu-id="e21f6-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21f6-295">0x00000000</span></span>                      |
| <span data-ttu-id="e21f6-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e21f6-296">System-Flags</span></span>           | <span data-ttu-id="e21f6-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e21f6-297">0x00000010</span></span>                      |
| <span data-ttu-id="e21f6-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e21f6-298">Classes used in</span></span>        | [<span data-ttu-id="e21f6-299">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e21f6-299">**Top**</span></span>](c-top.md)<br/> |



 

 





