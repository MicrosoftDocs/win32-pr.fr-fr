---
title: Attribut USN-Changed
description: Numéro de séquence de mise à jour (USN) affecté par le répertoire local pour la modification la plus récente, y compris la création. Voir aussi, USN-créé.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut USN-Changed
- Schéma AD de l’attribut uSNChanged
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744868"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="8f91e-106">Attribut USN-Changed</span><span class="sxs-lookup"><span data-stu-id="8f91e-106">USN-Changed attribute</span></span>

<span data-ttu-id="8f91e-107">Numéro de séquence de mise à jour (USN) affecté par le répertoire local pour la modification la plus récente, y compris la création.</span><span class="sxs-lookup"><span data-stu-id="8f91e-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="8f91e-108">Voir aussi, [**USN-créé**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="8f91e-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="8f91e-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-109">Entry</span></span> | <span data-ttu-id="8f91e-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8f91e-111">CN</span><span class="sxs-lookup"><span data-stu-id="8f91e-111">CN</span></span>                | <span data-ttu-id="8f91e-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="8f91e-112">USN-Changed</span></span>                          |
| <span data-ttu-id="8f91e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8f91e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8f91e-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="8f91e-114">uSNChanged</span></span>                           |
| <span data-ttu-id="8f91e-115">Taille</span><span class="sxs-lookup"><span data-stu-id="8f91e-115">Size</span></span>              | <span data-ttu-id="8f91e-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="8f91e-116">8 bytes</span></span>                              |
| <span data-ttu-id="8f91e-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8f91e-117">Update Privilege</span></span>  | <span data-ttu-id="8f91e-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="8f91e-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="8f91e-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8f91e-119">Update Frequency</span></span>  | <span data-ttu-id="8f91e-120">Lorsque l’objet est modifié.</span><span class="sxs-lookup"><span data-stu-id="8f91e-120">When the object is changed.</span></span>          |
| <span data-ttu-id="8f91e-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-121">Attribute-Id</span></span>      | <span data-ttu-id="8f91e-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="8f91e-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="8f91e-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8f91e-123">System-Id-Guid</span></span>    | <span data-ttu-id="8f91e-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8f91e-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8f91e-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f91e-125">Syntax</span></span>            | [<span data-ttu-id="8f91e-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="8f91e-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8f91e-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8f91e-127">Implementations</span></span>

-   [<span data-ttu-id="8f91e-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f91e-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f91e-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f91e-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f91e-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8f91e-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8f91e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f91e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f91e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f91e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f91e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f91e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f91e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f91e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f91e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f91e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8f91e-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-136">Entry</span></span> | <span data-ttu-id="8f91e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-139">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-140">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-141">System-Only</span></span>            | <span data-ttu-id="8f91e-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-142">True</span></span>                            |
| <span data-ttu-id="8f91e-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-144">True</span></span>                            |
| <span data-ttu-id="8f91e-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-145">Is Indexed</span></span>             | <span data-ttu-id="8f91e-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-146">True</span></span>                            |
| <span data-ttu-id="8f91e-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-147">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-148">True</span></span>                            |
| <span data-ttu-id="8f91e-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-153">Search-Flags</span></span>           | <span data-ttu-id="8f91e-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-154">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-155">System-Flags</span></span>           | <span data-ttu-id="8f91e-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-156">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-157">Classes used in</span></span>        | [<span data-ttu-id="8f91e-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f91e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f91e-159">Windows Server 2003</span></span>



| <span data-ttu-id="8f91e-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-160">Entry</span></span> | <span data-ttu-id="8f91e-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-163">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-164">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-165">System-Only</span></span>            | <span data-ttu-id="8f91e-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-166">True</span></span>                            |
| <span data-ttu-id="8f91e-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-167">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-168">True</span></span>                            |
| <span data-ttu-id="8f91e-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-169">Is Indexed</span></span>             | <span data-ttu-id="8f91e-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-170">True</span></span>                            |
| <span data-ttu-id="8f91e-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-171">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-172">True</span></span>                            |
| <span data-ttu-id="8f91e-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-177">Search-Flags</span></span>           | <span data-ttu-id="8f91e-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-178">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-179">System-Flags</span></span>           | <span data-ttu-id="8f91e-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-180">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-181">Classes used in</span></span>        | [<span data-ttu-id="8f91e-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8f91e-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="8f91e-183">ADAM</span></span>



| <span data-ttu-id="8f91e-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-184">Entry</span></span> | <span data-ttu-id="8f91e-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-187">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-188">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-189">System-Only</span></span>            | <span data-ttu-id="8f91e-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-190">True</span></span>                            |
| <span data-ttu-id="8f91e-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-192">True</span></span>                            |
| <span data-ttu-id="8f91e-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-193">Is Indexed</span></span>             | <span data-ttu-id="8f91e-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-194">True</span></span>                            |
| <span data-ttu-id="8f91e-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-195">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-196">True</span></span>                            |
| <span data-ttu-id="8f91e-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-201">Search-Flags</span></span>           | <span data-ttu-id="8f91e-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-202">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-203">System-Flags</span></span>           | <span data-ttu-id="8f91e-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-204">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-205">Classes used in</span></span>        | [<span data-ttu-id="8f91e-206">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f91e-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f91e-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f91e-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-208">Entry</span></span> | <span data-ttu-id="8f91e-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-211">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-212">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-213">System-Only</span></span>            | <span data-ttu-id="8f91e-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-214">True</span></span>                            |
| <span data-ttu-id="8f91e-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-215">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-216">True</span></span>                            |
| <span data-ttu-id="8f91e-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-217">Is Indexed</span></span>             | <span data-ttu-id="8f91e-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-218">True</span></span>                            |
| <span data-ttu-id="8f91e-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-219">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-220">True</span></span>                            |
| <span data-ttu-id="8f91e-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-225">Search-Flags</span></span>           | <span data-ttu-id="8f91e-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-226">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-227">System-Flags</span></span>           | <span data-ttu-id="8f91e-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-228">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-229">Classes used in</span></span>        | [<span data-ttu-id="8f91e-230">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f91e-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f91e-231">Windows Server 2008</span></span>



| <span data-ttu-id="8f91e-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-232">Entry</span></span> | <span data-ttu-id="8f91e-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-235">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-236">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-237">System-Only</span></span>            | <span data-ttu-id="8f91e-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-238">True</span></span>                            |
| <span data-ttu-id="8f91e-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-239">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-240">True</span></span>                            |
| <span data-ttu-id="8f91e-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-241">Is Indexed</span></span>             | <span data-ttu-id="8f91e-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-242">True</span></span>                            |
| <span data-ttu-id="8f91e-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-243">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-244">True</span></span>                            |
| <span data-ttu-id="8f91e-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-249">Search-Flags</span></span>           | <span data-ttu-id="8f91e-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-250">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-251">System-Flags</span></span>           | <span data-ttu-id="8f91e-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-252">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-253">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-253">Classes used in</span></span>        | [<span data-ttu-id="8f91e-254">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f91e-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f91e-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f91e-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-256">Entry</span></span> | <span data-ttu-id="8f91e-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-258">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-259">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-260">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-261">System-Only</span></span>            | <span data-ttu-id="8f91e-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-262">True</span></span>                            |
| <span data-ttu-id="8f91e-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-264">True</span></span>                            |
| <span data-ttu-id="8f91e-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-265">Is Indexed</span></span>             | <span data-ttu-id="8f91e-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-266">True</span></span>                            |
| <span data-ttu-id="8f91e-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-267">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-268">True</span></span>                            |
| <span data-ttu-id="8f91e-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-273">Search-Flags</span></span>           | <span data-ttu-id="8f91e-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-274">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-275">System-Flags</span></span>           | <span data-ttu-id="8f91e-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-276">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-277">Classes used in</span></span>        | [<span data-ttu-id="8f91e-278">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f91e-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f91e-279">Windows Server 2012</span></span>



| <span data-ttu-id="8f91e-280">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f91e-280">Entry</span></span> | <span data-ttu-id="8f91e-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f91e-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8f91e-282">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f91e-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8f91e-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f91e-283">MAPI-Id</span></span>                | <span data-ttu-id="8f91e-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="8f91e-284">0x8029</span></span>                          |
| <span data-ttu-id="8f91e-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f91e-285">System-Only</span></span>            | <span data-ttu-id="8f91e-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-286">True</span></span>                            |
| <span data-ttu-id="8f91e-287">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f91e-287">Is-Single-Valued</span></span>       | <span data-ttu-id="8f91e-288">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-288">True</span></span>                            |
| <span data-ttu-id="8f91e-289">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f91e-289">Is Indexed</span></span>             | <span data-ttu-id="8f91e-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-290">True</span></span>                            |
| <span data-ttu-id="8f91e-291">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f91e-291">In Global Catalog</span></span>      | <span data-ttu-id="8f91e-292">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f91e-292">True</span></span>                            |
| <span data-ttu-id="8f91e-293">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f91e-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f91e-294">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f91e-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8f91e-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f91e-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8f91e-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f91e-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8f91e-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-297">Search-Flags</span></span>           | <span data-ttu-id="8f91e-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8f91e-298">0x00000009</span></span>                      |
| <span data-ttu-id="8f91e-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f91e-299">System-Flags</span></span>           | <span data-ttu-id="8f91e-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8f91e-300">0x00000013</span></span>                      |
| <span data-ttu-id="8f91e-301">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f91e-301">Classes used in</span></span>        | [<span data-ttu-id="8f91e-302">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="8f91e-302">**Top**</span></span>](c-top.md)<br/> |



 

 





