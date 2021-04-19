---
title: Attribut Managed-Objects
description: Contient la liste des objets gérés par l’utilisateur. Les objets répertoriés sont ceux dont la propriété managedBy de la propriété est définie sur cet utilisateur. Chaque élément de la liste est une référence liée à l’objet managé.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Managed-Objects
- Schéma AD de l’attribut managedObjects
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514671"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="c4808-107">Attribut Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="c4808-107">Managed-Objects attribute</span></span>

<span data-ttu-id="c4808-108">Contient la liste des objets gérés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4808-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="c4808-109">Les objets répertoriés sont ceux dont la propriété managedBy de la propriété est définie sur cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4808-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="c4808-110">Chaque élément de la liste est une référence liée à l’objet managé.</span><span class="sxs-lookup"><span data-stu-id="c4808-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="c4808-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-111">Entry</span></span> | <span data-ttu-id="c4808-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4808-113">CN</span><span class="sxs-lookup"><span data-stu-id="c4808-113">CN</span></span>                | <span data-ttu-id="c4808-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="c4808-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="c4808-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c4808-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c4808-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="c4808-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="c4808-117">Taille</span><span class="sxs-lookup"><span data-stu-id="c4808-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="c4808-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c4808-118">Update Privilege</span></span>  | <span data-ttu-id="c4808-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="c4808-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="c4808-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c4808-120">Update Frequency</span></span>  | <span data-ttu-id="c4808-121">Lorsque l’enregistrement des utilisateurs est créé et chaque fois que les objets gérés doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="c4808-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="c4808-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-122">Attribute-Id</span></span>      | <span data-ttu-id="c4808-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="c4808-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="c4808-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4808-124">System-Id-Guid</span></span>    | <span data-ttu-id="c4808-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c4808-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="c4808-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4808-126">Syntax</span></span>            | [<span data-ttu-id="c4808-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c4808-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="c4808-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c4808-128">Implementations</span></span>

-   [<span data-ttu-id="c4808-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4808-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4808-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4808-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4808-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c4808-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c4808-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4808-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4808-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4808-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4808-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4808-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4808-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4808-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4808-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4808-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c4808-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-137">Entry</span></span> | <span data-ttu-id="c4808-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-139">Link-Id</span></span>                | <span data-ttu-id="c4808-140">73</span><span class="sxs-lookup"><span data-stu-id="c4808-140">73</span></span>                              |
| <span data-ttu-id="c4808-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-141">MAPI-Id</span></span>                | <span data-ttu-id="c4808-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-142">0x8024</span></span>                          |
| <span data-ttu-id="c4808-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-143">System-Only</span></span>            | <span data-ttu-id="c4808-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-144">True</span></span>                            |
| <span data-ttu-id="c4808-145">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-145">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-146">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-146">False</span></span>                           |
| <span data-ttu-id="c4808-147">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-147">Is Indexed</span></span>             | <span data-ttu-id="c4808-148">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-148">False</span></span>                           |
| <span data-ttu-id="c4808-149">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-149">In Global Catalog</span></span>      | <span data-ttu-id="c4808-150">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-150">False</span></span>                           |
| <span data-ttu-id="c4808-151">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-152">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-155">Search-Flags</span></span>           | <span data-ttu-id="c4808-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-156">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-157">System-Flags</span></span>           | <span data-ttu-id="c4808-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-158">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-159">Classes used in</span></span>        | [<span data-ttu-id="c4808-160">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4808-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4808-161">Windows Server 2003</span></span>



| <span data-ttu-id="c4808-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-162">Entry</span></span> | <span data-ttu-id="c4808-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-164">Link-Id</span></span>                | <span data-ttu-id="c4808-165">73</span><span class="sxs-lookup"><span data-stu-id="c4808-165">73</span></span>                              |
| <span data-ttu-id="c4808-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-166">MAPI-Id</span></span>                | <span data-ttu-id="c4808-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-167">0x8024</span></span>                          |
| <span data-ttu-id="c4808-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-168">System-Only</span></span>            | <span data-ttu-id="c4808-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-169">True</span></span>                            |
| <span data-ttu-id="c4808-170">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-170">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-171">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-171">False</span></span>                           |
| <span data-ttu-id="c4808-172">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-172">Is Indexed</span></span>             | <span data-ttu-id="c4808-173">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-173">False</span></span>                           |
| <span data-ttu-id="c4808-174">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-174">In Global Catalog</span></span>      | <span data-ttu-id="c4808-175">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-175">False</span></span>                           |
| <span data-ttu-id="c4808-176">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-177">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-180">Search-Flags</span></span>           | <span data-ttu-id="c4808-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-181">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-182">System-Flags</span></span>           | <span data-ttu-id="c4808-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-183">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-184">Classes used in</span></span>        | [<span data-ttu-id="c4808-185">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c4808-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="c4808-186">ADAM</span></span>



| <span data-ttu-id="c4808-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-187">Entry</span></span> | <span data-ttu-id="c4808-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-189">Link-Id</span></span>                | <span data-ttu-id="c4808-190">73</span><span class="sxs-lookup"><span data-stu-id="c4808-190">73</span></span>                              |
| <span data-ttu-id="c4808-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-191">MAPI-Id</span></span>                | <span data-ttu-id="c4808-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-192">0x8024</span></span>                          |
| <span data-ttu-id="c4808-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-193">System-Only</span></span>            | <span data-ttu-id="c4808-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-194">True</span></span>                            |
| <span data-ttu-id="c4808-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-195">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-196">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-196">False</span></span>                           |
| <span data-ttu-id="c4808-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-197">Is Indexed</span></span>             | <span data-ttu-id="c4808-198">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-198">False</span></span>                           |
| <span data-ttu-id="c4808-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-199">In Global Catalog</span></span>      | <span data-ttu-id="c4808-200">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-200">False</span></span>                           |
| <span data-ttu-id="c4808-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-205">Search-Flags</span></span>           | <span data-ttu-id="c4808-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-206">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-207">System-Flags</span></span>           | <span data-ttu-id="c4808-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-208">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-209">Classes used in</span></span>        | [<span data-ttu-id="c4808-210">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4808-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4808-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4808-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-212">Entry</span></span> | <span data-ttu-id="c4808-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-214">Link-Id</span></span>                | <span data-ttu-id="c4808-215">73</span><span class="sxs-lookup"><span data-stu-id="c4808-215">73</span></span>                              |
| <span data-ttu-id="c4808-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-216">MAPI-Id</span></span>                | <span data-ttu-id="c4808-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-217">0x8024</span></span>                          |
| <span data-ttu-id="c4808-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-218">System-Only</span></span>            | <span data-ttu-id="c4808-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-219">True</span></span>                            |
| <span data-ttu-id="c4808-220">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-220">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-221">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-221">False</span></span>                           |
| <span data-ttu-id="c4808-222">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-222">Is Indexed</span></span>             | <span data-ttu-id="c4808-223">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-223">False</span></span>                           |
| <span data-ttu-id="c4808-224">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-224">In Global Catalog</span></span>      | <span data-ttu-id="c4808-225">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-225">False</span></span>                           |
| <span data-ttu-id="c4808-226">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-227">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-230">Search-Flags</span></span>           | <span data-ttu-id="c4808-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-231">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-232">System-Flags</span></span>           | <span data-ttu-id="c4808-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-233">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-234">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-234">Classes used in</span></span>        | [<span data-ttu-id="c4808-235">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4808-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4808-236">Windows Server 2008</span></span>



| <span data-ttu-id="c4808-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-237">Entry</span></span> | <span data-ttu-id="c4808-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-239">Link-Id</span></span>                | <span data-ttu-id="c4808-240">73</span><span class="sxs-lookup"><span data-stu-id="c4808-240">73</span></span>                              |
| <span data-ttu-id="c4808-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-241">MAPI-Id</span></span>                | <span data-ttu-id="c4808-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-242">0x8024</span></span>                          |
| <span data-ttu-id="c4808-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-243">System-Only</span></span>            | <span data-ttu-id="c4808-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-244">True</span></span>                            |
| <span data-ttu-id="c4808-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-245">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-246">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-246">False</span></span>                           |
| <span data-ttu-id="c4808-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-247">Is Indexed</span></span>             | <span data-ttu-id="c4808-248">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-248">False</span></span>                           |
| <span data-ttu-id="c4808-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-249">In Global Catalog</span></span>      | <span data-ttu-id="c4808-250">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-250">False</span></span>                           |
| <span data-ttu-id="c4808-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-255">Search-Flags</span></span>           | <span data-ttu-id="c4808-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-256">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-257">System-Flags</span></span>           | <span data-ttu-id="c4808-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-258">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-259">Classes used in</span></span>        | [<span data-ttu-id="c4808-260">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4808-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4808-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4808-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-262">Entry</span></span> | <span data-ttu-id="c4808-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-264">Link-Id</span></span>                | <span data-ttu-id="c4808-265">73</span><span class="sxs-lookup"><span data-stu-id="c4808-265">73</span></span>                              |
| <span data-ttu-id="c4808-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-266">MAPI-Id</span></span>                | <span data-ttu-id="c4808-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-267">0x8024</span></span>                          |
| <span data-ttu-id="c4808-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-268">System-Only</span></span>            | <span data-ttu-id="c4808-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-269">True</span></span>                            |
| <span data-ttu-id="c4808-270">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-270">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-271">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-271">False</span></span>                           |
| <span data-ttu-id="c4808-272">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-272">Is Indexed</span></span>             | <span data-ttu-id="c4808-273">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-273">False</span></span>                           |
| <span data-ttu-id="c4808-274">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-274">In Global Catalog</span></span>      | <span data-ttu-id="c4808-275">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-275">False</span></span>                           |
| <span data-ttu-id="c4808-276">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-277">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-280">Search-Flags</span></span>           | <span data-ttu-id="c4808-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-281">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-282">System-Flags</span></span>           | <span data-ttu-id="c4808-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-283">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-284">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-284">Classes used in</span></span>        | [<span data-ttu-id="c4808-285">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4808-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4808-286">Windows Server 2012</span></span>



| <span data-ttu-id="c4808-287">Entrée</span><span class="sxs-lookup"><span data-stu-id="c4808-287">Entry</span></span> | <span data-ttu-id="c4808-288">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4808-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4808-289">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c4808-289">Link-Id</span></span>                | <span data-ttu-id="c4808-290">73</span><span class="sxs-lookup"><span data-stu-id="c4808-290">73</span></span>                              |
| <span data-ttu-id="c4808-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4808-291">MAPI-Id</span></span>                | <span data-ttu-id="c4808-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="c4808-292">0x8024</span></span>                          |
| <span data-ttu-id="c4808-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4808-293">System-Only</span></span>            | <span data-ttu-id="c4808-294">Vrai</span><span class="sxs-lookup"><span data-stu-id="c4808-294">True</span></span>                            |
| <span data-ttu-id="c4808-295">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c4808-295">Is-Single-Valued</span></span>       | <span data-ttu-id="c4808-296">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-296">False</span></span>                           |
| <span data-ttu-id="c4808-297">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c4808-297">Is Indexed</span></span>             | <span data-ttu-id="c4808-298">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-298">False</span></span>                           |
| <span data-ttu-id="c4808-299">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c4808-299">In Global Catalog</span></span>      | <span data-ttu-id="c4808-300">Faux</span><span class="sxs-lookup"><span data-stu-id="c4808-300">False</span></span>                           |
| <span data-ttu-id="c4808-301">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c4808-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4808-302">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c4808-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4808-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4808-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c4808-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4808-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c4808-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-305">Search-Flags</span></span>           | <span data-ttu-id="c4808-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4808-306">0x00000000</span></span>                      |
| <span data-ttu-id="c4808-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4808-307">System-Flags</span></span>           | <span data-ttu-id="c4808-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4808-308">0x00000010</span></span>                      |
| <span data-ttu-id="c4808-309">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c4808-309">Classes used in</span></span>        | [<span data-ttu-id="c4808-310">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c4808-310">**Top**</span></span>](c-top.md)<br/> |



 

 





