---
title: Attribut USN-Source
description: Valeur de l’attribut USN-Changed de l’objet à partir du répertoire distant qui a répliqué la modification sur le serveur local.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut USN-Source
- Schéma AD de l’attribut uSNSource
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385363"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="c080b-105">Attribut USN-Source</span><span class="sxs-lookup"><span data-stu-id="c080b-105">USN-Source attribute</span></span>

<span data-ttu-id="c080b-106">Valeur de l’attribut [**USN modifié**](a-usnchanged.md) de l’objet à partir du répertoire distant qui a répliqué la modification sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="c080b-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="c080b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-107">Entry</span></span> | <span data-ttu-id="c080b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c080b-109">CN</span><span class="sxs-lookup"><span data-stu-id="c080b-109">CN</span></span>                | <span data-ttu-id="c080b-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="c080b-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="c080b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c080b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c080b-112">uSNSource</span><span class="sxs-lookup"><span data-stu-id="c080b-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="c080b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c080b-113">Size</span></span>              | <span data-ttu-id="c080b-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="c080b-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="c080b-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c080b-115">Update Privilege</span></span>  | <span data-ttu-id="c080b-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="c080b-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="c080b-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c080b-117">Update Frequency</span></span>  | <span data-ttu-id="c080b-118">Lorsque l’objet est modifié sur un répertoire distant qui a répliqué la modification dans le répertoire local.</span><span class="sxs-lookup"><span data-stu-id="c080b-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="c080b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-119">Attribute-Id</span></span>      | <span data-ttu-id="c080b-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="c080b-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="c080b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c080b-121">System-Id-Guid</span></span>    | <span data-ttu-id="c080b-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c080b-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="c080b-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c080b-123">Syntax</span></span>            | [<span data-ttu-id="c080b-124">**Défini**</span><span class="sxs-lookup"><span data-stu-id="c080b-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="c080b-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c080b-125">Implementations</span></span>

-   [<span data-ttu-id="c080b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c080b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c080b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c080b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c080b-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c080b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c080b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c080b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c080b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c080b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c080b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c080b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c080b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c080b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c080b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c080b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="c080b-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-134">Entry</span></span> | <span data-ttu-id="c080b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-137">MAPI-Id</span></span>                | <span data-ttu-id="c080b-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-138">0x8157</span></span>                          |
| <span data-ttu-id="c080b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-139">System-Only</span></span>            | <span data-ttu-id="c080b-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-140">False</span></span>                           |
| <span data-ttu-id="c080b-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-142">True</span></span>                            |
| <span data-ttu-id="c080b-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-143">Is Indexed</span></span>             | <span data-ttu-id="c080b-144">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-144">False</span></span>                           |
| <span data-ttu-id="c080b-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-145">In Global Catalog</span></span>      | <span data-ttu-id="c080b-146">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-146">False</span></span>                           |
| <span data-ttu-id="c080b-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-151">Search-Flags</span></span>           | <span data-ttu-id="c080b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-152">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-153">System-Flags</span></span>           | <span data-ttu-id="c080b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-154">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-155">Classes used in</span></span>        | [<span data-ttu-id="c080b-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c080b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c080b-157">Windows Server 2003</span></span>



| <span data-ttu-id="c080b-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-158">Entry</span></span> | <span data-ttu-id="c080b-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-161">MAPI-Id</span></span>                | <span data-ttu-id="c080b-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-162">0x8157</span></span>                          |
| <span data-ttu-id="c080b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-163">System-Only</span></span>            | <span data-ttu-id="c080b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-164">False</span></span>                           |
| <span data-ttu-id="c080b-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-166">True</span></span>                            |
| <span data-ttu-id="c080b-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-167">Is Indexed</span></span>             | <span data-ttu-id="c080b-168">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-168">False</span></span>                           |
| <span data-ttu-id="c080b-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-169">In Global Catalog</span></span>      | <span data-ttu-id="c080b-170">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-170">False</span></span>                           |
| <span data-ttu-id="c080b-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-175">Search-Flags</span></span>           | <span data-ttu-id="c080b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-176">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-177">System-Flags</span></span>           | <span data-ttu-id="c080b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-178">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-179">Classes used in</span></span>        | [<span data-ttu-id="c080b-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c080b-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="c080b-181">ADAM</span></span>



| <span data-ttu-id="c080b-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-182">Entry</span></span> | <span data-ttu-id="c080b-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-185">MAPI-Id</span></span>                | <span data-ttu-id="c080b-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-186">0x8157</span></span>                          |
| <span data-ttu-id="c080b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-187">System-Only</span></span>            | <span data-ttu-id="c080b-188">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-188">False</span></span>                           |
| <span data-ttu-id="c080b-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-190">True</span></span>                            |
| <span data-ttu-id="c080b-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-191">Is Indexed</span></span>             | <span data-ttu-id="c080b-192">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-192">False</span></span>                           |
| <span data-ttu-id="c080b-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-193">In Global Catalog</span></span>      | <span data-ttu-id="c080b-194">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-194">False</span></span>                           |
| <span data-ttu-id="c080b-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-199">Search-Flags</span></span>           | <span data-ttu-id="c080b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-200">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-201">System-Flags</span></span>           | <span data-ttu-id="c080b-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-202">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-203">Classes used in</span></span>        | [<span data-ttu-id="c080b-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c080b-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c080b-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c080b-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-206">Entry</span></span> | <span data-ttu-id="c080b-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-209">MAPI-Id</span></span>                | <span data-ttu-id="c080b-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-210">0x8157</span></span>                          |
| <span data-ttu-id="c080b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-211">System-Only</span></span>            | <span data-ttu-id="c080b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-212">False</span></span>                           |
| <span data-ttu-id="c080b-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-214">True</span></span>                            |
| <span data-ttu-id="c080b-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-215">Is Indexed</span></span>             | <span data-ttu-id="c080b-216">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-216">False</span></span>                           |
| <span data-ttu-id="c080b-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-217">In Global Catalog</span></span>      | <span data-ttu-id="c080b-218">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-218">False</span></span>                           |
| <span data-ttu-id="c080b-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-223">Search-Flags</span></span>           | <span data-ttu-id="c080b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-224">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-225">System-Flags</span></span>           | <span data-ttu-id="c080b-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-226">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-227">Classes used in</span></span>        | [<span data-ttu-id="c080b-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c080b-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c080b-229">Windows Server 2008</span></span>



| <span data-ttu-id="c080b-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-230">Entry</span></span> | <span data-ttu-id="c080b-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-233">MAPI-Id</span></span>                | <span data-ttu-id="c080b-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-234">0x8157</span></span>                          |
| <span data-ttu-id="c080b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-235">System-Only</span></span>            | <span data-ttu-id="c080b-236">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-236">False</span></span>                           |
| <span data-ttu-id="c080b-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-238">True</span></span>                            |
| <span data-ttu-id="c080b-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-239">Is Indexed</span></span>             | <span data-ttu-id="c080b-240">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-240">False</span></span>                           |
| <span data-ttu-id="c080b-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-241">In Global Catalog</span></span>      | <span data-ttu-id="c080b-242">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-242">False</span></span>                           |
| <span data-ttu-id="c080b-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-247">Search-Flags</span></span>           | <span data-ttu-id="c080b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-248">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-249">System-Flags</span></span>           | <span data-ttu-id="c080b-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-250">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-251">Classes used in</span></span>        | [<span data-ttu-id="c080b-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c080b-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c080b-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c080b-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-254">Entry</span></span> | <span data-ttu-id="c080b-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-257">MAPI-Id</span></span>                | <span data-ttu-id="c080b-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-258">0x8157</span></span>                          |
| <span data-ttu-id="c080b-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-259">System-Only</span></span>            | <span data-ttu-id="c080b-260">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-260">False</span></span>                           |
| <span data-ttu-id="c080b-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-261">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-262">True</span></span>                            |
| <span data-ttu-id="c080b-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-263">Is Indexed</span></span>             | <span data-ttu-id="c080b-264">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-264">False</span></span>                           |
| <span data-ttu-id="c080b-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-265">In Global Catalog</span></span>      | <span data-ttu-id="c080b-266">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-266">False</span></span>                           |
| <span data-ttu-id="c080b-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-271">Search-Flags</span></span>           | <span data-ttu-id="c080b-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-272">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-273">System-Flags</span></span>           | <span data-ttu-id="c080b-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-274">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-275">Classes used in</span></span>        | [<span data-ttu-id="c080b-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c080b-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c080b-277">Windows Server 2012</span></span>



| <span data-ttu-id="c080b-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="c080b-278">Entry</span></span> | <span data-ttu-id="c080b-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="c080b-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c080b-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c080b-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c080b-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c080b-281">MAPI-Id</span></span>                | <span data-ttu-id="c080b-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="c080b-282">0x8157</span></span>                          |
| <span data-ttu-id="c080b-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="c080b-283">System-Only</span></span>            | <span data-ttu-id="c080b-284">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-284">False</span></span>                           |
| <span data-ttu-id="c080b-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c080b-285">Is-Single-Valued</span></span>       | <span data-ttu-id="c080b-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="c080b-286">True</span></span>                            |
| <span data-ttu-id="c080b-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c080b-287">Is Indexed</span></span>             | <span data-ttu-id="c080b-288">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-288">False</span></span>                           |
| <span data-ttu-id="c080b-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c080b-289">In Global Catalog</span></span>      | <span data-ttu-id="c080b-290">Faux</span><span class="sxs-lookup"><span data-stu-id="c080b-290">False</span></span>                           |
| <span data-ttu-id="c080b-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c080b-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="c080b-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c080b-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c080b-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c080b-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c080b-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c080b-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c080b-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-295">Search-Flags</span></span>           | <span data-ttu-id="c080b-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c080b-296">0x00000000</span></span>                      |
| <span data-ttu-id="c080b-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c080b-297">System-Flags</span></span>           | <span data-ttu-id="c080b-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c080b-298">0x00000010</span></span>                      |
| <span data-ttu-id="c080b-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c080b-299">Classes used in</span></span>        | [<span data-ttu-id="c080b-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="c080b-300">**Top**</span></span>](c-top.md)<br/> |



 

 





