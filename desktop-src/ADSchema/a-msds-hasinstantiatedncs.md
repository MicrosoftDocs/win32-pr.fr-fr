---
title: attribut ms-DS-has-instancied-NC
description: Les informations d’état de la réplication DS, similaires à (et sur un sur-ensemble), les attributs existants hasMasterNCs et hasPartialReplicaNCs. À utiliser par le KCC lors de la configuration des partenaires de réplication.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-a-instancié-NC
- Schéma Active Directory de l’attribut msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480093"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="25b40-106">attribut ms-DS-has-instancied-NC</span><span class="sxs-lookup"><span data-stu-id="25b40-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="25b40-107">Les informations d’état de la réplication DS, similaires à (et sur un sur-ensemble), les attributs existants hasMasterNCs et hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="25b40-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="25b40-108">À utiliser par le KCC lors de la configuration des partenaires de réplication.</span><span class="sxs-lookup"><span data-stu-id="25b40-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="25b40-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-109">Entry</span></span> | <span data-ttu-id="25b40-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b40-111">CN</span><span class="sxs-lookup"><span data-stu-id="25b40-111">CN</span></span>                | <span data-ttu-id="25b40-112">ms-DS-a-instancié-NC</span><span class="sxs-lookup"><span data-stu-id="25b40-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="25b40-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="25b40-113">Ldap-Display-Name</span></span> | <span data-ttu-id="25b40-114">msDS-HasInstantiatedNCs</span><span class="sxs-lookup"><span data-stu-id="25b40-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="25b40-115">Taille</span><span class="sxs-lookup"><span data-stu-id="25b40-115">Size</span></span>              | <span data-ttu-id="25b40-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="25b40-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="25b40-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="25b40-117">Update Privilege</span></span>  | <span data-ttu-id="25b40-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="25b40-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="25b40-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="25b40-119">Update Frequency</span></span>  | <span data-ttu-id="25b40-120">Environ deux fois plus souvent que hasMasterNCs/hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="25b40-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="25b40-121">Ces attributs existants sont mis à jour uniquement lorsque le contrôleur de périphérique ajoute ou supprime une partition (par exemple, lors du passage de DC à GC ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="25b40-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="25b40-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-122">Attribute-Id</span></span>      | <span data-ttu-id="25b40-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="25b40-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="25b40-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="25b40-124">System-Id-Guid</span></span>    | <span data-ttu-id="25b40-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="25b40-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="25b40-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25b40-126">Syntax</span></span>            | [<span data-ttu-id="25b40-127">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="25b40-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="25b40-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="25b40-128">Implementations</span></span>

-   [<span data-ttu-id="25b40-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="25b40-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="25b40-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="25b40-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="25b40-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="25b40-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="25b40-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="25b40-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="25b40-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="25b40-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="25b40-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="25b40-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="25b40-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25b40-135">Windows Server 2003</span></span>



| <span data-ttu-id="25b40-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-136">Entry</span></span> | <span data-ttu-id="25b40-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-138">Link-Id</span></span>                | <span data-ttu-id="25b40-139">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-139">2002</span></span>                                     |
| <span data-ttu-id="25b40-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-141">System-Only</span></span>            | <span data-ttu-id="25b40-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-142">True</span></span>                                     |
| <span data-ttu-id="25b40-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-143">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-144">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-144">False</span></span>                                    |
| <span data-ttu-id="25b40-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-145">Is Indexed</span></span>             | <span data-ttu-id="25b40-146">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-146">False</span></span>                                    |
| <span data-ttu-id="25b40-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-147">In Global Catalog</span></span>      | <span data-ttu-id="25b40-148">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-148">False</span></span>                                    |
| <span data-ttu-id="25b40-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-151">Range-Lower</span></span>            | <span data-ttu-id="25b40-152">4</span><span class="sxs-lookup"><span data-stu-id="25b40-152">4</span></span>                                        |
| <span data-ttu-id="25b40-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-153">Range-Upper</span></span>            | <span data-ttu-id="25b40-154">4</span><span class="sxs-lookup"><span data-stu-id="25b40-154">4</span></span>                                        |
| <span data-ttu-id="25b40-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-155">Search-Flags</span></span>           | <span data-ttu-id="25b40-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-156">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-157">System-Flags</span></span>           | <span data-ttu-id="25b40-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-158">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-159">Classes used in</span></span>        | [<span data-ttu-id="25b40-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="25b40-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="25b40-161">ADAM</span></span>



| <span data-ttu-id="25b40-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-162">Entry</span></span> | <span data-ttu-id="25b40-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-164">Link-Id</span></span>                | <span data-ttu-id="25b40-165">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-165">2002</span></span>                                     |
| <span data-ttu-id="25b40-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-167">System-Only</span></span>            | <span data-ttu-id="25b40-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-168">True</span></span>                                     |
| <span data-ttu-id="25b40-169">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-169">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-170">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-170">False</span></span>                                    |
| <span data-ttu-id="25b40-171">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-171">Is Indexed</span></span>             | <span data-ttu-id="25b40-172">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-172">False</span></span>                                    |
| <span data-ttu-id="25b40-173">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-173">In Global Catalog</span></span>      | <span data-ttu-id="25b40-174">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-174">False</span></span>                                    |
| <span data-ttu-id="25b40-175">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-176">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-177">Range-Lower</span></span>            | <span data-ttu-id="25b40-178">4</span><span class="sxs-lookup"><span data-stu-id="25b40-178">4</span></span>                                        |
| <span data-ttu-id="25b40-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-179">Range-Upper</span></span>            | <span data-ttu-id="25b40-180">4</span><span class="sxs-lookup"><span data-stu-id="25b40-180">4</span></span>                                        |
| <span data-ttu-id="25b40-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-181">Search-Flags</span></span>           | <span data-ttu-id="25b40-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-182">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-183">System-Flags</span></span>           | <span data-ttu-id="25b40-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-184">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-185">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-185">Classes used in</span></span>        | [<span data-ttu-id="25b40-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="25b40-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="25b40-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="25b40-188">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-188">Entry</span></span> | <span data-ttu-id="25b40-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-190">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-190">Link-Id</span></span>                | <span data-ttu-id="25b40-191">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-191">2002</span></span>                                     |
| <span data-ttu-id="25b40-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-193">System-Only</span></span>            | <span data-ttu-id="25b40-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-194">True</span></span>                                     |
| <span data-ttu-id="25b40-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-195">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-196">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-196">False</span></span>                                    |
| <span data-ttu-id="25b40-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-197">Is Indexed</span></span>             | <span data-ttu-id="25b40-198">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-198">False</span></span>                                    |
| <span data-ttu-id="25b40-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-199">In Global Catalog</span></span>      | <span data-ttu-id="25b40-200">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-200">False</span></span>                                    |
| <span data-ttu-id="25b40-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-203">Range-Lower</span></span>            | <span data-ttu-id="25b40-204">4</span><span class="sxs-lookup"><span data-stu-id="25b40-204">4</span></span>                                        |
| <span data-ttu-id="25b40-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-205">Range-Upper</span></span>            | <span data-ttu-id="25b40-206">4</span><span class="sxs-lookup"><span data-stu-id="25b40-206">4</span></span>                                        |
| <span data-ttu-id="25b40-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-207">Search-Flags</span></span>           | <span data-ttu-id="25b40-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-208">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-209">System-Flags</span></span>           | <span data-ttu-id="25b40-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-210">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-211">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-211">Classes used in</span></span>        | [<span data-ttu-id="25b40-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="25b40-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25b40-213">Windows Server 2008</span></span>



| <span data-ttu-id="25b40-214">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-214">Entry</span></span> | <span data-ttu-id="25b40-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-216">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-216">Link-Id</span></span>                | <span data-ttu-id="25b40-217">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-217">2002</span></span>                                     |
| <span data-ttu-id="25b40-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-219">System-Only</span></span>            | <span data-ttu-id="25b40-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-220">True</span></span>                                     |
| <span data-ttu-id="25b40-221">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-221">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-222">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-222">False</span></span>                                    |
| <span data-ttu-id="25b40-223">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-223">Is Indexed</span></span>             | <span data-ttu-id="25b40-224">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-224">False</span></span>                                    |
| <span data-ttu-id="25b40-225">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-225">In Global Catalog</span></span>      | <span data-ttu-id="25b40-226">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-226">False</span></span>                                    |
| <span data-ttu-id="25b40-227">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-228">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-229">Range-Lower</span></span>            | <span data-ttu-id="25b40-230">4</span><span class="sxs-lookup"><span data-stu-id="25b40-230">4</span></span>                                        |
| <span data-ttu-id="25b40-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-231">Range-Upper</span></span>            | <span data-ttu-id="25b40-232">4</span><span class="sxs-lookup"><span data-stu-id="25b40-232">4</span></span>                                        |
| <span data-ttu-id="25b40-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-233">Search-Flags</span></span>           | <span data-ttu-id="25b40-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-234">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-235">System-Flags</span></span>           | <span data-ttu-id="25b40-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-236">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-237">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-237">Classes used in</span></span>        | [<span data-ttu-id="25b40-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="25b40-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="25b40-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="25b40-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-240">Entry</span></span> | <span data-ttu-id="25b40-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-242">Link-Id</span></span>                | <span data-ttu-id="25b40-243">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-243">2002</span></span>                                     |
| <span data-ttu-id="25b40-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-245">System-Only</span></span>            | <span data-ttu-id="25b40-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-246">True</span></span>                                     |
| <span data-ttu-id="25b40-247">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-247">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-248">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-248">False</span></span>                                    |
| <span data-ttu-id="25b40-249">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-249">Is Indexed</span></span>             | <span data-ttu-id="25b40-250">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-250">False</span></span>                                    |
| <span data-ttu-id="25b40-251">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-251">In Global Catalog</span></span>      | <span data-ttu-id="25b40-252">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-252">False</span></span>                                    |
| <span data-ttu-id="25b40-253">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-254">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-255">Range-Lower</span></span>            | <span data-ttu-id="25b40-256">4</span><span class="sxs-lookup"><span data-stu-id="25b40-256">4</span></span>                                        |
| <span data-ttu-id="25b40-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-257">Range-Upper</span></span>            | <span data-ttu-id="25b40-258">4</span><span class="sxs-lookup"><span data-stu-id="25b40-258">4</span></span>                                        |
| <span data-ttu-id="25b40-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-259">Search-Flags</span></span>           | <span data-ttu-id="25b40-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-260">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-261">System-Flags</span></span>           | <span data-ttu-id="25b40-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-262">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-263">Classes used in</span></span>        | [<span data-ttu-id="25b40-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="25b40-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25b40-265">Windows Server 2012</span></span>



| <span data-ttu-id="25b40-266">Entrée</span><span class="sxs-lookup"><span data-stu-id="25b40-266">Entry</span></span> | <span data-ttu-id="25b40-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b40-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="25b40-268">ID de lien</span><span class="sxs-lookup"><span data-stu-id="25b40-268">Link-Id</span></span>                | <span data-ttu-id="25b40-269">2002</span><span class="sxs-lookup"><span data-stu-id="25b40-269">2002</span></span>                                     |
| <span data-ttu-id="25b40-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25b40-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="25b40-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="25b40-271">System-Only</span></span>            | <span data-ttu-id="25b40-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="25b40-272">True</span></span>                                     |
| <span data-ttu-id="25b40-273">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="25b40-273">Is-Single-Valued</span></span>       | <span data-ttu-id="25b40-274">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-274">False</span></span>                                    |
| <span data-ttu-id="25b40-275">Est indexé</span><span class="sxs-lookup"><span data-stu-id="25b40-275">Is Indexed</span></span>             | <span data-ttu-id="25b40-276">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-276">False</span></span>                                    |
| <span data-ttu-id="25b40-277">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="25b40-277">In Global Catalog</span></span>      | <span data-ttu-id="25b40-278">Faux</span><span class="sxs-lookup"><span data-stu-id="25b40-278">False</span></span>                                    |
| <span data-ttu-id="25b40-279">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="25b40-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="25b40-280">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="25b40-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="25b40-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25b40-281">Range-Lower</span></span>            | <span data-ttu-id="25b40-282">4</span><span class="sxs-lookup"><span data-stu-id="25b40-282">4</span></span>                                        |
| <span data-ttu-id="25b40-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25b40-283">Range-Upper</span></span>            | <span data-ttu-id="25b40-284">4</span><span class="sxs-lookup"><span data-stu-id="25b40-284">4</span></span>                                        |
| <span data-ttu-id="25b40-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-285">Search-Flags</span></span>           | <span data-ttu-id="25b40-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25b40-286">0x00000000</span></span>                               |
| <span data-ttu-id="25b40-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25b40-287">System-Flags</span></span>           | <span data-ttu-id="25b40-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25b40-288">0x00000010</span></span>                               |
| <span data-ttu-id="25b40-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="25b40-289">Classes used in</span></span>        | [<span data-ttu-id="25b40-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="25b40-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





