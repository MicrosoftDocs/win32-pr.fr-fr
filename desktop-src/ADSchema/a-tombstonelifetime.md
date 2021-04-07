---
title: Attribut Tombstone-Lifetime
description: Nombre de jours avant la suppression d’un objet supprimé des services d’annuaire.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Tombstone-Lifetime
- Schéma AD de l’attribut tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845278"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="9ddca-105">Attribut Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="9ddca-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="9ddca-106">Nombre de jours avant la suppression d’un objet supprimé des services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="9ddca-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="9ddca-107">Cela vous aide à supprimer des objets des serveurs répliqués et à empêcher les restaurations de réintroduire un objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="9ddca-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="9ddca-108">Cette valeur se trouve dans l’objet service d’annuaire de la carte réseau de configuration.</span><span class="sxs-lookup"><span data-stu-id="9ddca-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="9ddca-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-109">Entry</span></span> | <span data-ttu-id="9ddca-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ddca-111">CN</span><span class="sxs-lookup"><span data-stu-id="9ddca-111">CN</span></span>                | <span data-ttu-id="9ddca-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="9ddca-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="9ddca-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9ddca-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9ddca-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="9ddca-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="9ddca-115">Taille</span><span class="sxs-lookup"><span data-stu-id="9ddca-115">Size</span></span>              | <span data-ttu-id="9ddca-116">4 octets.</span><span class="sxs-lookup"><span data-stu-id="9ddca-116">4 bytes.</span></span> <span data-ttu-id="9ddca-117">La valeur par défaut est de 60 jours quand aucune valeur n’est entrée.</span><span class="sxs-lookup"><span data-stu-id="9ddca-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="9ddca-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9ddca-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="9ddca-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9ddca-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="9ddca-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-120">Attribute-Id</span></span>      | <span data-ttu-id="9ddca-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="9ddca-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="9ddca-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9ddca-122">System-Id-Guid</span></span>    | <span data-ttu-id="9ddca-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="9ddca-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="9ddca-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ddca-124">Syntax</span></span>            | [<span data-ttu-id="9ddca-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="9ddca-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="9ddca-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9ddca-126">Implementations</span></span>

-   [<span data-ttu-id="9ddca-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9ddca-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9ddca-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ddca-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ddca-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9ddca-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9ddca-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ddca-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ddca-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ddca-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ddca-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ddca-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ddca-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ddca-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9ddca-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ddca-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9ddca-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-135">Entry</span></span> | <span data-ttu-id="9ddca-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-138">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-139">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-140">System-Only</span></span>            | <span data-ttu-id="9ddca-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-141">False</span></span>                                            |
| <span data-ttu-id="9ddca-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-143">True</span></span>                                             |
| <span data-ttu-id="9ddca-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-144">Is Indexed</span></span>             | <span data-ttu-id="9ddca-145">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-145">False</span></span>                                            |
| <span data-ttu-id="9ddca-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-146">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-147">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-147">False</span></span>                                            |
| <span data-ttu-id="9ddca-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-152">Search-Flags</span></span>           | <span data-ttu-id="9ddca-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-153">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-154">System-Flags</span></span>           | <span data-ttu-id="9ddca-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-155">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-156">Classes used in</span></span>        | [<span data-ttu-id="9ddca-157">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9ddca-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ddca-158">Windows Server 2003</span></span>



| <span data-ttu-id="9ddca-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-159">Entry</span></span> | <span data-ttu-id="9ddca-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-162">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-163">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-164">System-Only</span></span>            | <span data-ttu-id="9ddca-165">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-165">False</span></span>                                            |
| <span data-ttu-id="9ddca-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-167">True</span></span>                                             |
| <span data-ttu-id="9ddca-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-168">Is Indexed</span></span>             | <span data-ttu-id="9ddca-169">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-169">False</span></span>                                            |
| <span data-ttu-id="9ddca-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-170">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-171">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-171">False</span></span>                                            |
| <span data-ttu-id="9ddca-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-176">Search-Flags</span></span>           | <span data-ttu-id="9ddca-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-177">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-178">System-Flags</span></span>           | <span data-ttu-id="9ddca-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-179">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-180">Classes used in</span></span>        | [<span data-ttu-id="9ddca-181">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9ddca-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="9ddca-182">ADAM</span></span>



| <span data-ttu-id="9ddca-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-183">Entry</span></span> | <span data-ttu-id="9ddca-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-186">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-187">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-188">System-Only</span></span>            | <span data-ttu-id="9ddca-189">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-189">False</span></span>                                            |
| <span data-ttu-id="9ddca-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-190">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-191">True</span></span>                                             |
| <span data-ttu-id="9ddca-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-192">Is Indexed</span></span>             | <span data-ttu-id="9ddca-193">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-193">False</span></span>                                            |
| <span data-ttu-id="9ddca-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-194">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-195">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-195">False</span></span>                                            |
| <span data-ttu-id="9ddca-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-200">Search-Flags</span></span>           | <span data-ttu-id="9ddca-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-201">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-202">System-Flags</span></span>           | <span data-ttu-id="9ddca-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-203">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-204">Classes used in</span></span>        | [<span data-ttu-id="9ddca-205">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ddca-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ddca-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ddca-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-207">Entry</span></span> | <span data-ttu-id="9ddca-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-210">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-211">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-212">System-Only</span></span>            | <span data-ttu-id="9ddca-213">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-213">False</span></span>                                            |
| <span data-ttu-id="9ddca-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-215">True</span></span>                                             |
| <span data-ttu-id="9ddca-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-216">Is Indexed</span></span>             | <span data-ttu-id="9ddca-217">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-217">False</span></span>                                            |
| <span data-ttu-id="9ddca-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-218">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-219">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-219">False</span></span>                                            |
| <span data-ttu-id="9ddca-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-224">Search-Flags</span></span>           | <span data-ttu-id="9ddca-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-225">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-226">System-Flags</span></span>           | <span data-ttu-id="9ddca-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-227">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-228">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-228">Classes used in</span></span>        | [<span data-ttu-id="9ddca-229">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ddca-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ddca-230">Windows Server 2008</span></span>



| <span data-ttu-id="9ddca-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-231">Entry</span></span> | <span data-ttu-id="9ddca-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-234">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-235">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-236">System-Only</span></span>            | <span data-ttu-id="9ddca-237">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-237">False</span></span>                                            |
| <span data-ttu-id="9ddca-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-238">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-239">True</span></span>                                             |
| <span data-ttu-id="9ddca-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-240">Is Indexed</span></span>             | <span data-ttu-id="9ddca-241">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-241">False</span></span>                                            |
| <span data-ttu-id="9ddca-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-242">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-243">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-243">False</span></span>                                            |
| <span data-ttu-id="9ddca-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-248">Search-Flags</span></span>           | <span data-ttu-id="9ddca-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-249">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-250">System-Flags</span></span>           | <span data-ttu-id="9ddca-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-251">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-252">Classes used in</span></span>        | [<span data-ttu-id="9ddca-253">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ddca-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ddca-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ddca-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-255">Entry</span></span> | <span data-ttu-id="9ddca-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-258">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-259">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-260">System-Only</span></span>            | <span data-ttu-id="9ddca-261">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-261">False</span></span>                                            |
| <span data-ttu-id="9ddca-262">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-262">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-263">True</span></span>                                             |
| <span data-ttu-id="9ddca-264">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-264">Is Indexed</span></span>             | <span data-ttu-id="9ddca-265">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-265">False</span></span>                                            |
| <span data-ttu-id="9ddca-266">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-266">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-267">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-267">False</span></span>                                            |
| <span data-ttu-id="9ddca-268">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-269">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-272">Search-Flags</span></span>           | <span data-ttu-id="9ddca-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-273">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-274">System-Flags</span></span>           | <span data-ttu-id="9ddca-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-275">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-276">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-276">Classes used in</span></span>        | [<span data-ttu-id="9ddca-277">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ddca-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ddca-278">Windows Server 2012</span></span>



| <span data-ttu-id="9ddca-279">Entrée</span><span class="sxs-lookup"><span data-stu-id="9ddca-279">Entry</span></span> | <span data-ttu-id="9ddca-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddca-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9ddca-281">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9ddca-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9ddca-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ddca-282">MAPI-Id</span></span>                | <span data-ttu-id="9ddca-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="9ddca-283">0x8145</span></span>                                           |
| <span data-ttu-id="9ddca-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ddca-284">System-Only</span></span>            | <span data-ttu-id="9ddca-285">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-285">False</span></span>                                            |
| <span data-ttu-id="9ddca-286">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9ddca-286">Is-Single-Valued</span></span>       | <span data-ttu-id="9ddca-287">Vrai</span><span class="sxs-lookup"><span data-stu-id="9ddca-287">True</span></span>                                             |
| <span data-ttu-id="9ddca-288">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9ddca-288">Is Indexed</span></span>             | <span data-ttu-id="9ddca-289">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-289">False</span></span>                                            |
| <span data-ttu-id="9ddca-290">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9ddca-290">In Global Catalog</span></span>      | <span data-ttu-id="9ddca-291">Faux</span><span class="sxs-lookup"><span data-stu-id="9ddca-291">False</span></span>                                            |
| <span data-ttu-id="9ddca-292">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9ddca-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ddca-293">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9ddca-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9ddca-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ddca-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ddca-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9ddca-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-296">Search-Flags</span></span>           | <span data-ttu-id="9ddca-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ddca-297">0x00000000</span></span>                                       |
| <span data-ttu-id="9ddca-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ddca-298">System-Flags</span></span>           | <span data-ttu-id="9ddca-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ddca-299">0x00000010</span></span>                                       |
| <span data-ttu-id="9ddca-300">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9ddca-300">Classes used in</span></span>        | [<span data-ttu-id="9ddca-301">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="9ddca-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





