---
title: Attribut FSMO de rôle-propriétaire
description: Opération de Single-Master flexible nom unique du contrôleur de l’emplacement où le schéma peut être modifié.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- 'FSMO : schéma AD de l’attribut propriétaire du rôle'
- Schéma AD de l’attribut fSMORoleOwner
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845257"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="60ef7-105">Attribut FSMO de rôle-propriétaire</span><span class="sxs-lookup"><span data-stu-id="60ef7-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="60ef7-106">Opération de Single-Master flexible : nom unique du contrôleur de l’emplacement où le schéma peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="60ef7-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="60ef7-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-107">Entry</span></span> | <span data-ttu-id="60ef7-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="60ef7-109">CN</span><span class="sxs-lookup"><span data-stu-id="60ef7-109">CN</span></span>                | <span data-ttu-id="60ef7-110">FSMO-Role-owner</span><span class="sxs-lookup"><span data-stu-id="60ef7-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="60ef7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="60ef7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="60ef7-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="60ef7-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="60ef7-113">Taille</span><span class="sxs-lookup"><span data-stu-id="60ef7-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="60ef7-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="60ef7-114">Update Privilege</span></span>  | <span data-ttu-id="60ef7-115">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="60ef7-115">Schema administrator</span></span>                    |
| <span data-ttu-id="60ef7-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="60ef7-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="60ef7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-117">Attribute-Id</span></span>      | <span data-ttu-id="60ef7-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="60ef7-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="60ef7-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="60ef7-119">System-Id-Guid</span></span>    | <span data-ttu-id="60ef7-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="60ef7-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="60ef7-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60ef7-121">Syntax</span></span>            | [<span data-ttu-id="60ef7-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="60ef7-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="60ef7-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="60ef7-123">Implementations</span></span>

-   [<span data-ttu-id="60ef7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="60ef7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="60ef7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="60ef7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="60ef7-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="60ef7-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="60ef7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="60ef7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="60ef7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="60ef7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="60ef7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="60ef7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="60ef7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="60ef7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="60ef7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60ef7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="60ef7-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-132">Entry</span></span> | <span data-ttu-id="60ef7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-136">System-Only</span></span>            | <span data-ttu-id="60ef7-137">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-137">False</span></span>                           |
| <span data-ttu-id="60ef7-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-139">True</span></span>                            |
| <span data-ttu-id="60ef7-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-140">Is Indexed</span></span>             | <span data-ttu-id="60ef7-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-141">True</span></span>                            |
| <span data-ttu-id="60ef7-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-142">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-143">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-143">False</span></span>                           |
| <span data-ttu-id="60ef7-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-148">Search-Flags</span></span>           | <span data-ttu-id="60ef7-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-149">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-150">System-Flags</span></span>           | <span data-ttu-id="60ef7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-151">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-152">Classes used in</span></span>        | [<span data-ttu-id="60ef7-153">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="60ef7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60ef7-154">Windows Server 2003</span></span>



| <span data-ttu-id="60ef7-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-155">Entry</span></span> | <span data-ttu-id="60ef7-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-159">System-Only</span></span>            | <span data-ttu-id="60ef7-160">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-160">False</span></span>                           |
| <span data-ttu-id="60ef7-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-162">True</span></span>                            |
| <span data-ttu-id="60ef7-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-163">Is Indexed</span></span>             | <span data-ttu-id="60ef7-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-164">True</span></span>                            |
| <span data-ttu-id="60ef7-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-165">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-166">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-166">False</span></span>                           |
| <span data-ttu-id="60ef7-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-171">Search-Flags</span></span>           | <span data-ttu-id="60ef7-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-172">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-173">System-Flags</span></span>           | <span data-ttu-id="60ef7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-174">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-175">Classes used in</span></span>        | [<span data-ttu-id="60ef7-176">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="60ef7-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="60ef7-177">ADAM</span></span>



| <span data-ttu-id="60ef7-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-178">Entry</span></span> | <span data-ttu-id="60ef7-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-182">System-Only</span></span>            | <span data-ttu-id="60ef7-183">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-183">False</span></span>                           |
| <span data-ttu-id="60ef7-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-185">True</span></span>                            |
| <span data-ttu-id="60ef7-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-186">Is Indexed</span></span>             | <span data-ttu-id="60ef7-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-187">True</span></span>                            |
| <span data-ttu-id="60ef7-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-188">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-189">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-189">False</span></span>                           |
| <span data-ttu-id="60ef7-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-194">Search-Flags</span></span>           | <span data-ttu-id="60ef7-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-195">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-196">System-Flags</span></span>           | <span data-ttu-id="60ef7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-197">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-198">Classes used in</span></span>        | [<span data-ttu-id="60ef7-199">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="60ef7-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="60ef7-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="60ef7-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-201">Entry</span></span> | <span data-ttu-id="60ef7-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-205">System-Only</span></span>            | <span data-ttu-id="60ef7-206">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-206">False</span></span>                           |
| <span data-ttu-id="60ef7-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-208">True</span></span>                            |
| <span data-ttu-id="60ef7-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-209">Is Indexed</span></span>             | <span data-ttu-id="60ef7-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-210">True</span></span>                            |
| <span data-ttu-id="60ef7-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-211">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-212">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-212">False</span></span>                           |
| <span data-ttu-id="60ef7-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-217">Search-Flags</span></span>           | <span data-ttu-id="60ef7-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-218">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-219">System-Flags</span></span>           | <span data-ttu-id="60ef7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-220">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-221">Classes used in</span></span>        | [<span data-ttu-id="60ef7-222">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="60ef7-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60ef7-223">Windows Server 2008</span></span>



| <span data-ttu-id="60ef7-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-224">Entry</span></span> | <span data-ttu-id="60ef7-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-228">System-Only</span></span>            | <span data-ttu-id="60ef7-229">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-229">False</span></span>                           |
| <span data-ttu-id="60ef7-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-231">True</span></span>                            |
| <span data-ttu-id="60ef7-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-232">Is Indexed</span></span>             | <span data-ttu-id="60ef7-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-233">True</span></span>                            |
| <span data-ttu-id="60ef7-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-234">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-235">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-235">False</span></span>                           |
| <span data-ttu-id="60ef7-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-240">Search-Flags</span></span>           | <span data-ttu-id="60ef7-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-241">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-242">System-Flags</span></span>           | <span data-ttu-id="60ef7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-243">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-244">Classes used in</span></span>        | [<span data-ttu-id="60ef7-245">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="60ef7-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60ef7-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="60ef7-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-247">Entry</span></span> | <span data-ttu-id="60ef7-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-251">System-Only</span></span>            | <span data-ttu-id="60ef7-252">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-252">False</span></span>                           |
| <span data-ttu-id="60ef7-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-254">True</span></span>                            |
| <span data-ttu-id="60ef7-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-255">Is Indexed</span></span>             | <span data-ttu-id="60ef7-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-256">True</span></span>                            |
| <span data-ttu-id="60ef7-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-257">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-258">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-258">False</span></span>                           |
| <span data-ttu-id="60ef7-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-263">Search-Flags</span></span>           | <span data-ttu-id="60ef7-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-264">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-265">System-Flags</span></span>           | <span data-ttu-id="60ef7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-266">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-267">Classes used in</span></span>        | [<span data-ttu-id="60ef7-268">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="60ef7-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60ef7-269">Windows Server 2012</span></span>



| <span data-ttu-id="60ef7-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="60ef7-270">Entry</span></span> | <span data-ttu-id="60ef7-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ef7-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60ef7-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="60ef7-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ef7-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60ef7-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ef7-274">System-Only</span></span>            | <span data-ttu-id="60ef7-275">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-275">False</span></span>                           |
| <span data-ttu-id="60ef7-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="60ef7-276">Is-Single-Valued</span></span>       | <span data-ttu-id="60ef7-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-277">True</span></span>                            |
| <span data-ttu-id="60ef7-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="60ef7-278">Is Indexed</span></span>             | <span data-ttu-id="60ef7-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="60ef7-279">True</span></span>                            |
| <span data-ttu-id="60ef7-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="60ef7-280">In Global Catalog</span></span>      | <span data-ttu-id="60ef7-281">Faux</span><span class="sxs-lookup"><span data-stu-id="60ef7-281">False</span></span>                           |
| <span data-ttu-id="60ef7-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="60ef7-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ef7-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="60ef7-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60ef7-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ef7-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60ef7-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ef7-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60ef7-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-286">Search-Flags</span></span>           | <span data-ttu-id="60ef7-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60ef7-287">0x00000001</span></span>                      |
| <span data-ttu-id="60ef7-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ef7-288">System-Flags</span></span>           | <span data-ttu-id="60ef7-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ef7-289">0x00000010</span></span>                      |
| <span data-ttu-id="60ef7-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="60ef7-290">Classes used in</span></span>        | [<span data-ttu-id="60ef7-291">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="60ef7-291">**Top**</span></span>](c-top.md)<br/> |



 

 





