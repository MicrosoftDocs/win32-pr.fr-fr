---
title: Attribut LM-pwd-History
description: Historique des mots de passe de l’utilisateur dans le format à sens unique (OWF) LAN Manager (LM). LM avec LM est utilisé pour la compatibilité avec les clients LAN Manager 2. x, Windows 95 et Windows 98.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut LM-pwd-History
- Schéma AD de l’attribut lmPwdHistory
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845230"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="e0ceb-106">Attribut LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="e0ceb-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="e0ceb-107">Historique des mots de passe de l’utilisateur dans le format à sens unique (OWF) LAN Manager (LM).</span><span class="sxs-lookup"><span data-stu-id="e0ceb-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="e0ceb-108">Le niveau de compatibilité LM est utilisé pour la compatibilité avec LAN Manager 2. *x* clients, Windows 95 et Windows 98.</span><span class="sxs-lookup"><span data-stu-id="e0ceb-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="e0ceb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-109">Entry</span></span> | <span data-ttu-id="e0ceb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e0ceb-111">CN</span><span class="sxs-lookup"><span data-stu-id="e0ceb-111">CN</span></span>                | <span data-ttu-id="e0ceb-112">LM-pwd-historique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="e0ceb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e0ceb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e0ceb-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="e0ceb-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="e0ceb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e0ceb-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e0ceb-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e0ceb-116">Update Privilege</span></span>  | <span data-ttu-id="e0ceb-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="e0ceb-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="e0ceb-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e0ceb-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="e0ceb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-119">Attribute-Id</span></span>      | <span data-ttu-id="e0ceb-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="e0ceb-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="e0ceb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e0ceb-121">System-Id-Guid</span></span>    | <span data-ttu-id="e0ceb-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e0ceb-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="e0ceb-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0ceb-123">Syntax</span></span>            | [<span data-ttu-id="e0ceb-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e0ceb-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e0ceb-125">Implementations</span></span>

-   [<span data-ttu-id="e0ceb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0ceb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0ceb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0ceb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0ceb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0ceb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0ceb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0ceb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e0ceb-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-133">Entry</span></span> | <span data-ttu-id="e0ceb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-137">System-Only</span></span>            | <span data-ttu-id="e0ceb-138">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-138">False</span></span>                             |
| <span data-ttu-id="e0ceb-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-140">False</span></span>                             |
| <span data-ttu-id="e0ceb-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-141">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-142">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-142">False</span></span>                             |
| <span data-ttu-id="e0ceb-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-143">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-144">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-144">False</span></span>                             |
| <span data-ttu-id="e0ceb-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-149">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-150">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-151">System-Flags</span></span>           | <span data-ttu-id="e0ceb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-152">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-153">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-154">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0ceb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0ceb-155">Windows Server 2003</span></span>



| <span data-ttu-id="e0ceb-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-156">Entry</span></span> | <span data-ttu-id="e0ceb-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-160">System-Only</span></span>            | <span data-ttu-id="e0ceb-161">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-161">False</span></span>                             |
| <span data-ttu-id="e0ceb-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-163">False</span></span>                             |
| <span data-ttu-id="e0ceb-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-164">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-165">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-165">False</span></span>                             |
| <span data-ttu-id="e0ceb-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-166">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-167">False</span></span>                             |
| <span data-ttu-id="e0ceb-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-172">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-173">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-174">System-Flags</span></span>           | <span data-ttu-id="e0ceb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-175">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-176">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-177">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0ceb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0ceb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0ceb-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-179">Entry</span></span> | <span data-ttu-id="e0ceb-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-183">System-Only</span></span>            | <span data-ttu-id="e0ceb-184">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-184">False</span></span>                             |
| <span data-ttu-id="e0ceb-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-186">False</span></span>                             |
| <span data-ttu-id="e0ceb-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-187">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-188">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-188">False</span></span>                             |
| <span data-ttu-id="e0ceb-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-189">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-190">False</span></span>                             |
| <span data-ttu-id="e0ceb-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-195">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-196">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-197">System-Flags</span></span>           | <span data-ttu-id="e0ceb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-198">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-199">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-200">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0ceb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0ceb-201">Windows Server 2008</span></span>



| <span data-ttu-id="e0ceb-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-202">Entry</span></span> | <span data-ttu-id="e0ceb-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-206">System-Only</span></span>            | <span data-ttu-id="e0ceb-207">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-207">False</span></span>                             |
| <span data-ttu-id="e0ceb-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-209">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-209">False</span></span>                             |
| <span data-ttu-id="e0ceb-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-210">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-211">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-211">False</span></span>                             |
| <span data-ttu-id="e0ceb-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-212">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-213">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-213">False</span></span>                             |
| <span data-ttu-id="e0ceb-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-218">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-219">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-220">System-Flags</span></span>           | <span data-ttu-id="e0ceb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-221">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-222">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-223">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0ceb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0ceb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0ceb-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-225">Entry</span></span> | <span data-ttu-id="e0ceb-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-229">System-Only</span></span>            | <span data-ttu-id="e0ceb-230">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-230">False</span></span>                             |
| <span data-ttu-id="e0ceb-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-232">False</span></span>                             |
| <span data-ttu-id="e0ceb-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-233">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-234">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-234">False</span></span>                             |
| <span data-ttu-id="e0ceb-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-235">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-236">False</span></span>                             |
| <span data-ttu-id="e0ceb-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-241">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-242">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-243">System-Flags</span></span>           | <span data-ttu-id="e0ceb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-244">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-245">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-246">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0ceb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0ceb-247">Windows Server 2012</span></span>



| <span data-ttu-id="e0ceb-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0ceb-248">Entry</span></span> | <span data-ttu-id="e0ceb-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ceb-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e0ceb-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0ceb-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0ceb-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e0ceb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0ceb-252">System-Only</span></span>            | <span data-ttu-id="e0ceb-253">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-253">False</span></span>                             |
| <span data-ttu-id="e0ceb-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0ceb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e0ceb-255">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-255">False</span></span>                             |
| <span data-ttu-id="e0ceb-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0ceb-256">Is Indexed</span></span>             | <span data-ttu-id="e0ceb-257">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-257">False</span></span>                             |
| <span data-ttu-id="e0ceb-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0ceb-258">In Global Catalog</span></span>      | <span data-ttu-id="e0ceb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="e0ceb-259">False</span></span>                             |
| <span data-ttu-id="e0ceb-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0ceb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0ceb-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0ceb-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e0ceb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0ceb-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0ceb-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e0ceb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-264">Search-Flags</span></span>           | <span data-ttu-id="e0ceb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0ceb-265">0x00000000</span></span>                        |
| <span data-ttu-id="e0ceb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0ceb-266">System-Flags</span></span>           | <span data-ttu-id="e0ceb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0ceb-267">0x00000010</span></span>                        |
| <span data-ttu-id="e0ceb-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0ceb-268">Classes used in</span></span>        | [<span data-ttu-id="e0ceb-269">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0ceb-269">**User**</span></span>](c-user.md)<br/> |



 

 





