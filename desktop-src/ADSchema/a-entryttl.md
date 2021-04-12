---
title: Attribut Entry-TTL
description: Cet attribut opérationnel est géré par le serveur et semble être présent dans chaque entrée dynamique.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Entry-TTL
- Schéma AD de l’attribut entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479709"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="30652-105">Attribut Entry-TTL</span><span class="sxs-lookup"><span data-stu-id="30652-105">Entry-TTL attribute</span></span>

<span data-ttu-id="30652-106">Cet attribut opérationnel est géré par le serveur et semble être présent dans chaque entrée dynamique.</span><span class="sxs-lookup"><span data-stu-id="30652-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="30652-107">L’attribut n’est pas présent lorsque l’entrée ne contient pas la classe d’objet dynamicObject.</span><span class="sxs-lookup"><span data-stu-id="30652-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="30652-108">La valeur de cet attribut est le temps, en secondes, pendant lequel l’entrée continuera d’exister avant d’apparaître dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="30652-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="30652-109">En l’absence d’opérations d’actualisation, il est garanti que les valeurs retournées en lisant l’attribut dans deux recherches successives sont sans importance.</span><span class="sxs-lookup"><span data-stu-id="30652-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="30652-110">La plus petite valeur autorisée est 0, ce qui indique que l’entrée peut disparaître sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="30652-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="30652-111">L’attribut est marqué non-MODIFICATION par l’utilisateur, car il ne peut être modifié qu’à l’aide de l’opération d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="30652-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="30652-112">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-112">Entry</span></span> | <span data-ttu-id="30652-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="30652-114">CN</span><span class="sxs-lookup"><span data-stu-id="30652-114">CN</span></span>                | <span data-ttu-id="30652-115">TTL d’entrée</span><span class="sxs-lookup"><span data-stu-id="30652-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="30652-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="30652-116">Ldap-Display-Name</span></span> | <span data-ttu-id="30652-117">entryTTL</span><span class="sxs-lookup"><span data-stu-id="30652-117">entryTTL</span></span>                                    |
| <span data-ttu-id="30652-118">Taille</span><span class="sxs-lookup"><span data-stu-id="30652-118">Size</span></span>              | <span data-ttu-id="30652-119">4 octets.</span><span class="sxs-lookup"><span data-stu-id="30652-119">4 bytes.</span></span> <span data-ttu-id="30652-120">Maximum = 1 an, valeur par défaut = 1 jour.</span><span class="sxs-lookup"><span data-stu-id="30652-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="30652-121">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="30652-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="30652-122">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="30652-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="30652-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30652-123">Attribute-Id</span></span>      | <span data-ttu-id="30652-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="30652-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="30652-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="30652-125">System-Id-Guid</span></span>    | <span data-ttu-id="30652-126">d213decc-d81a-4384-AAC2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="30652-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="30652-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30652-127">Syntax</span></span>            | [<span data-ttu-id="30652-128">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="30652-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="30652-129">Implémentations</span><span class="sxs-lookup"><span data-stu-id="30652-129">Implementations</span></span>

-   [<span data-ttu-id="30652-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30652-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30652-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="30652-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="30652-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30652-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30652-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30652-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30652-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30652-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30652-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30652-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="30652-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30652-136">Windows Server 2003</span></span>



| <span data-ttu-id="30652-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-137">Entry</span></span> | <span data-ttu-id="30652-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-141">System-Only</span></span>            | <span data-ttu-id="30652-142">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-142">False</span></span>                                                |
| <span data-ttu-id="30652-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-143">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-144">True</span></span>                                                 |
| <span data-ttu-id="30652-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-145">Is Indexed</span></span>             | <span data-ttu-id="30652-146">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-146">False</span></span>                                                |
| <span data-ttu-id="30652-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-147">In Global Catalog</span></span>      | <span data-ttu-id="30652-148">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-148">False</span></span>                                                |
| <span data-ttu-id="30652-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-151">Range-Lower</span></span>            | <span data-ttu-id="30652-152">0</span><span class="sxs-lookup"><span data-stu-id="30652-152">0</span></span>                                                    |
| <span data-ttu-id="30652-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-153">Range-Upper</span></span>            | <span data-ttu-id="30652-154">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-154">31557600</span></span>                                             |
| <span data-ttu-id="30652-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-155">Search-Flags</span></span>           | <span data-ttu-id="30652-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-156">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-157">System-Flags</span></span>           | <span data-ttu-id="30652-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-158">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-159">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-159">Classes used in</span></span>        | [<span data-ttu-id="30652-160">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="30652-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="30652-161">ADAM</span></span>



| <span data-ttu-id="30652-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-162">Entry</span></span> | <span data-ttu-id="30652-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-166">System-Only</span></span>            | <span data-ttu-id="30652-167">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-167">False</span></span>                                                |
| <span data-ttu-id="30652-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-168">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-169">True</span></span>                                                 |
| <span data-ttu-id="30652-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-170">Is Indexed</span></span>             | <span data-ttu-id="30652-171">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-171">False</span></span>                                                |
| <span data-ttu-id="30652-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-172">In Global Catalog</span></span>      | <span data-ttu-id="30652-173">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-173">False</span></span>                                                |
| <span data-ttu-id="30652-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-176">Range-Lower</span></span>            | <span data-ttu-id="30652-177">0</span><span class="sxs-lookup"><span data-stu-id="30652-177">0</span></span>                                                    |
| <span data-ttu-id="30652-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-178">Range-Upper</span></span>            | <span data-ttu-id="30652-179">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-179">31557600</span></span>                                             |
| <span data-ttu-id="30652-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-180">Search-Flags</span></span>           | <span data-ttu-id="30652-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-181">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-182">System-Flags</span></span>           | <span data-ttu-id="30652-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-183">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-184">Classes used in</span></span>        | [<span data-ttu-id="30652-185">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30652-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30652-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30652-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-187">Entry</span></span> | <span data-ttu-id="30652-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-191">System-Only</span></span>            | <span data-ttu-id="30652-192">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-192">False</span></span>                                                |
| <span data-ttu-id="30652-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-193">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-194">True</span></span>                                                 |
| <span data-ttu-id="30652-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-195">Is Indexed</span></span>             | <span data-ttu-id="30652-196">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-196">False</span></span>                                                |
| <span data-ttu-id="30652-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-197">In Global Catalog</span></span>      | <span data-ttu-id="30652-198">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-198">False</span></span>                                                |
| <span data-ttu-id="30652-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-201">Range-Lower</span></span>            | <span data-ttu-id="30652-202">0</span><span class="sxs-lookup"><span data-stu-id="30652-202">0</span></span>                                                    |
| <span data-ttu-id="30652-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-203">Range-Upper</span></span>            | <span data-ttu-id="30652-204">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-204">31557600</span></span>                                             |
| <span data-ttu-id="30652-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-205">Search-Flags</span></span>           | <span data-ttu-id="30652-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-206">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-207">System-Flags</span></span>           | <span data-ttu-id="30652-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-208">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-209">Classes used in</span></span>        | [<span data-ttu-id="30652-210">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30652-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30652-211">Windows Server 2008</span></span>



| <span data-ttu-id="30652-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-212">Entry</span></span> | <span data-ttu-id="30652-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-216">System-Only</span></span>            | <span data-ttu-id="30652-217">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-217">False</span></span>                                                |
| <span data-ttu-id="30652-218">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-218">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-219">True</span></span>                                                 |
| <span data-ttu-id="30652-220">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-220">Is Indexed</span></span>             | <span data-ttu-id="30652-221">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-221">False</span></span>                                                |
| <span data-ttu-id="30652-222">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-222">In Global Catalog</span></span>      | <span data-ttu-id="30652-223">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-223">False</span></span>                                                |
| <span data-ttu-id="30652-224">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-225">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-226">Range-Lower</span></span>            | <span data-ttu-id="30652-227">0</span><span class="sxs-lookup"><span data-stu-id="30652-227">0</span></span>                                                    |
| <span data-ttu-id="30652-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-228">Range-Upper</span></span>            | <span data-ttu-id="30652-229">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-229">31557600</span></span>                                             |
| <span data-ttu-id="30652-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-230">Search-Flags</span></span>           | <span data-ttu-id="30652-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-231">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-232">System-Flags</span></span>           | <span data-ttu-id="30652-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-233">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-234">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-234">Classes used in</span></span>        | [<span data-ttu-id="30652-235">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30652-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30652-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30652-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-237">Entry</span></span> | <span data-ttu-id="30652-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-241">System-Only</span></span>            | <span data-ttu-id="30652-242">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-242">False</span></span>                                                |
| <span data-ttu-id="30652-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-243">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-244">True</span></span>                                                 |
| <span data-ttu-id="30652-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-245">Is Indexed</span></span>             | <span data-ttu-id="30652-246">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-246">False</span></span>                                                |
| <span data-ttu-id="30652-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-247">In Global Catalog</span></span>      | <span data-ttu-id="30652-248">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-248">False</span></span>                                                |
| <span data-ttu-id="30652-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-251">Range-Lower</span></span>            | <span data-ttu-id="30652-252">0</span><span class="sxs-lookup"><span data-stu-id="30652-252">0</span></span>                                                    |
| <span data-ttu-id="30652-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-253">Range-Upper</span></span>            | <span data-ttu-id="30652-254">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-254">31557600</span></span>                                             |
| <span data-ttu-id="30652-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-255">Search-Flags</span></span>           | <span data-ttu-id="30652-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-256">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-257">System-Flags</span></span>           | <span data-ttu-id="30652-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-258">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-259">Classes used in</span></span>        | [<span data-ttu-id="30652-260">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30652-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30652-261">Windows Server 2012</span></span>



| <span data-ttu-id="30652-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="30652-262">Entry</span></span> | <span data-ttu-id="30652-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="30652-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="30652-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="30652-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30652-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="30652-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="30652-266">System-Only</span></span>            | <span data-ttu-id="30652-267">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-267">False</span></span>                                                |
| <span data-ttu-id="30652-268">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="30652-268">Is-Single-Valued</span></span>       | <span data-ttu-id="30652-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="30652-269">True</span></span>                                                 |
| <span data-ttu-id="30652-270">Est indexé</span><span class="sxs-lookup"><span data-stu-id="30652-270">Is Indexed</span></span>             | <span data-ttu-id="30652-271">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-271">False</span></span>                                                |
| <span data-ttu-id="30652-272">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="30652-272">In Global Catalog</span></span>      | <span data-ttu-id="30652-273">Faux</span><span class="sxs-lookup"><span data-stu-id="30652-273">False</span></span>                                                |
| <span data-ttu-id="30652-274">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="30652-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="30652-275">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="30652-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="30652-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30652-276">Range-Lower</span></span>            | <span data-ttu-id="30652-277">0</span><span class="sxs-lookup"><span data-stu-id="30652-277">0</span></span>                                                    |
| <span data-ttu-id="30652-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30652-278">Range-Upper</span></span>            | <span data-ttu-id="30652-279">31557600</span><span class="sxs-lookup"><span data-stu-id="30652-279">31557600</span></span>                                             |
| <span data-ttu-id="30652-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-280">Search-Flags</span></span>           | <span data-ttu-id="30652-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30652-281">0x00000000</span></span>                                           |
| <span data-ttu-id="30652-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30652-282">System-Flags</span></span>           | <span data-ttu-id="30652-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="30652-283">0x00000014</span></span>                                           |
| <span data-ttu-id="30652-284">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="30652-284">Classes used in</span></span>        | [<span data-ttu-id="30652-285">**Objet dynamique**</span><span class="sxs-lookup"><span data-stu-id="30652-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





