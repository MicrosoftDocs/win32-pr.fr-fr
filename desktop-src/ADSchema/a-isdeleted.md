---
title: Attribut Is-Deleted
description: Si la valeur est TRUE, cet objet a été marqué pour suppression et ne peut pas être instancié. Une fois la période de désactivation expirée, elle sera supprimée du système.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Is-Deleted
- Schéma AD de l’attribut isDeleted
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514664"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="91b1f-106">Attribut Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="91b1f-106">Is-Deleted attribute</span></span>

<span data-ttu-id="91b1f-107">Si la **valeur est true**, cet objet a été marqué pour suppression et ne peut pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="91b1f-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="91b1f-108">Une fois la période de désactivation expirée, elle sera supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="91b1f-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="91b1f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-109">Entry</span></span> | <span data-ttu-id="91b1f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="91b1f-111">CN</span><span class="sxs-lookup"><span data-stu-id="91b1f-111">CN</span></span>                | <span data-ttu-id="91b1f-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="91b1f-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="91b1f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="91b1f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="91b1f-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="91b1f-114">isDeleted</span></span>                            |
| <span data-ttu-id="91b1f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="91b1f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="91b1f-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="91b1f-116">Update Privilege</span></span>  | <span data-ttu-id="91b1f-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="91b1f-117">Domain administrator</span></span>                 |
| <span data-ttu-id="91b1f-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="91b1f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="91b1f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-119">Attribute-Id</span></span>      | <span data-ttu-id="91b1f-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="91b1f-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="91b1f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="91b1f-121">System-Id-Guid</span></span>    | <span data-ttu-id="91b1f-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="91b1f-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="91b1f-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91b1f-123">Syntax</span></span>            | [<span data-ttu-id="91b1f-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="91b1f-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="91b1f-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="91b1f-125">Implementations</span></span>

-   [<span data-ttu-id="91b1f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91b1f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91b1f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91b1f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91b1f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="91b1f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="91b1f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91b1f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91b1f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91b1f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91b1f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91b1f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91b1f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91b1f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91b1f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91b1f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="91b1f-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-134">Entry</span></span> | <span data-ttu-id="91b1f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-137">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-138">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-139">System-Only</span></span>            | <span data-ttu-id="91b1f-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-140">True</span></span>                            |
| <span data-ttu-id="91b1f-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-142">True</span></span>                            |
| <span data-ttu-id="91b1f-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-143">Is Indexed</span></span>             | <span data-ttu-id="91b1f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-144">False</span></span>                           |
| <span data-ttu-id="91b1f-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-145">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-146">True</span></span>                            |
| <span data-ttu-id="91b1f-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-151">Search-Flags</span></span>           | <span data-ttu-id="91b1f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-152">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-153">System-Flags</span></span>           | <span data-ttu-id="91b1f-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-154">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-155">Classes used in</span></span>        | [<span data-ttu-id="91b1f-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91b1f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91b1f-157">Windows Server 2003</span></span>



| <span data-ttu-id="91b1f-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-158">Entry</span></span> | <span data-ttu-id="91b1f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-161">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-162">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-163">System-Only</span></span>            | <span data-ttu-id="91b1f-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-164">True</span></span>                            |
| <span data-ttu-id="91b1f-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-166">True</span></span>                            |
| <span data-ttu-id="91b1f-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-167">Is Indexed</span></span>             | <span data-ttu-id="91b1f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-168">False</span></span>                           |
| <span data-ttu-id="91b1f-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-169">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-170">True</span></span>                            |
| <span data-ttu-id="91b1f-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-175">Search-Flags</span></span>           | <span data-ttu-id="91b1f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-176">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-177">System-Flags</span></span>           | <span data-ttu-id="91b1f-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-178">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-179">Classes used in</span></span>        | [<span data-ttu-id="91b1f-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="91b1f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="91b1f-181">ADAM</span></span>



| <span data-ttu-id="91b1f-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-182">Entry</span></span> | <span data-ttu-id="91b1f-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-185">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-186">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-187">System-Only</span></span>            | <span data-ttu-id="91b1f-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-188">True</span></span>                            |
| <span data-ttu-id="91b1f-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-190">True</span></span>                            |
| <span data-ttu-id="91b1f-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-191">Is Indexed</span></span>             | <span data-ttu-id="91b1f-192">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-192">False</span></span>                           |
| <span data-ttu-id="91b1f-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-193">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-194">True</span></span>                            |
| <span data-ttu-id="91b1f-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-199">Search-Flags</span></span>           | <span data-ttu-id="91b1f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-200">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-201">System-Flags</span></span>           | <span data-ttu-id="91b1f-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-202">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-203">Classes used in</span></span>        | [<span data-ttu-id="91b1f-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91b1f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91b1f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91b1f-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-206">Entry</span></span> | <span data-ttu-id="91b1f-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-209">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-210">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-211">System-Only</span></span>            | <span data-ttu-id="91b1f-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-212">True</span></span>                            |
| <span data-ttu-id="91b1f-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-214">True</span></span>                            |
| <span data-ttu-id="91b1f-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-215">Is Indexed</span></span>             | <span data-ttu-id="91b1f-216">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-216">False</span></span>                           |
| <span data-ttu-id="91b1f-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-217">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-218">True</span></span>                            |
| <span data-ttu-id="91b1f-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-223">Search-Flags</span></span>           | <span data-ttu-id="91b1f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-224">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-225">System-Flags</span></span>           | <span data-ttu-id="91b1f-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-226">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-227">Classes used in</span></span>        | [<span data-ttu-id="91b1f-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91b1f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91b1f-229">Windows Server 2008</span></span>



| <span data-ttu-id="91b1f-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-230">Entry</span></span> | <span data-ttu-id="91b1f-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-233">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-234">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-235">System-Only</span></span>            | <span data-ttu-id="91b1f-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-236">True</span></span>                            |
| <span data-ttu-id="91b1f-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-238">True</span></span>                            |
| <span data-ttu-id="91b1f-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-239">Is Indexed</span></span>             | <span data-ttu-id="91b1f-240">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-240">False</span></span>                           |
| <span data-ttu-id="91b1f-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-241">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-242">True</span></span>                            |
| <span data-ttu-id="91b1f-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-247">Search-Flags</span></span>           | <span data-ttu-id="91b1f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-248">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-249">System-Flags</span></span>           | <span data-ttu-id="91b1f-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-250">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-251">Classes used in</span></span>        | [<span data-ttu-id="91b1f-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91b1f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91b1f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91b1f-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-254">Entry</span></span> | <span data-ttu-id="91b1f-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-257">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-258">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-259">System-Only</span></span>            | <span data-ttu-id="91b1f-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-260">True</span></span>                            |
| <span data-ttu-id="91b1f-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-262">True</span></span>                            |
| <span data-ttu-id="91b1f-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-263">Is Indexed</span></span>             | <span data-ttu-id="91b1f-264">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-264">False</span></span>                           |
| <span data-ttu-id="91b1f-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-265">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-266">True</span></span>                            |
| <span data-ttu-id="91b1f-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-271">Search-Flags</span></span>           | <span data-ttu-id="91b1f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-272">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-273">System-Flags</span></span>           | <span data-ttu-id="91b1f-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-274">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-275">Classes used in</span></span>        | [<span data-ttu-id="91b1f-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91b1f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91b1f-277">Windows Server 2012</span></span>



| <span data-ttu-id="91b1f-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="91b1f-278">Entry</span></span> | <span data-ttu-id="91b1f-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b1f-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91b1f-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="91b1f-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91b1f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91b1f-281">MAPI-Id</span></span>                | <span data-ttu-id="91b1f-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="91b1f-282">0x80C0</span></span>                          |
| <span data-ttu-id="91b1f-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="91b1f-283">System-Only</span></span>            | <span data-ttu-id="91b1f-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-284">True</span></span>                            |
| <span data-ttu-id="91b1f-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="91b1f-285">Is-Single-Valued</span></span>       | <span data-ttu-id="91b1f-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-286">True</span></span>                            |
| <span data-ttu-id="91b1f-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="91b1f-287">Is Indexed</span></span>             | <span data-ttu-id="91b1f-288">Faux</span><span class="sxs-lookup"><span data-stu-id="91b1f-288">False</span></span>                           |
| <span data-ttu-id="91b1f-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="91b1f-289">In Global Catalog</span></span>      | <span data-ttu-id="91b1f-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="91b1f-290">True</span></span>                            |
| <span data-ttu-id="91b1f-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="91b1f-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="91b1f-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="91b1f-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91b1f-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91b1f-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91b1f-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91b1f-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91b1f-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-295">Search-Flags</span></span>           | <span data-ttu-id="91b1f-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91b1f-296">0x00000000</span></span>                      |
| <span data-ttu-id="91b1f-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91b1f-297">System-Flags</span></span>           | <span data-ttu-id="91b1f-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="91b1f-298">0x00000012</span></span>                      |
| <span data-ttu-id="91b1f-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="91b1f-299">Classes used in</span></span>        | [<span data-ttu-id="91b1f-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="91b1f-300">**Top**</span></span>](c-top.md)<br/> |



 

 





