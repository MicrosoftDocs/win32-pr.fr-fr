---
title: Attribut Server-Role
description: Pour la compatibilité avec les serveurs de serveurs antérieurs à Windows 2000. Un ordinateur exécutant Windows NT Server peut être un serveur autonome, un contrôleur de domaine principal (PDC) ou un contrôleur de domaine secondaire (BDC).
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Server-Role
- Schéma AD de l’attribut serverRole
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514685"
---
# <a name="server-role-attribute"></a><span data-ttu-id="ac9c1-106">Attribut Server-Role</span><span class="sxs-lookup"><span data-stu-id="ac9c1-106">Server-Role attribute</span></span>

<span data-ttu-id="ac9c1-107">Pour la compatibilité avec les serveurs de serveurs antérieurs à Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="ac9c1-108">Un ordinateur exécutant Windows NT Server peut être un serveur autonome, un contrôleur de domaine principal (PDC) ou un contrôleur de domaine secondaire (BDC).</span><span class="sxs-lookup"><span data-stu-id="ac9c1-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="ac9c1-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-109">Entry</span></span> | <span data-ttu-id="ac9c1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ac9c1-111">CN</span><span class="sxs-lookup"><span data-stu-id="ac9c1-111">CN</span></span>                | <span data-ttu-id="ac9c1-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="ac9c1-112">Server-Role</span></span>                          |
| <span data-ttu-id="ac9c1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ac9c1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ac9c1-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="ac9c1-114">serverRole</span></span>                           |
| <span data-ttu-id="ac9c1-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ac9c1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ac9c1-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ac9c1-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ac9c1-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ac9c1-117">Update Frequency</span></span>  | <span data-ttu-id="ac9c1-118">4 octets</span><span class="sxs-lookup"><span data-stu-id="ac9c1-118">4 bytes</span></span>                              |
| <span data-ttu-id="ac9c1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-119">Attribute-Id</span></span>      | <span data-ttu-id="ac9c1-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="ac9c1-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="ac9c1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac9c1-121">System-Id-Guid</span></span>    | <span data-ttu-id="ac9c1-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ac9c1-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ac9c1-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac9c1-123">Syntax</span></span>            | [<span data-ttu-id="ac9c1-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ac9c1-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ac9c1-125">Implementations</span></span>

-   [<span data-ttu-id="ac9c1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac9c1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac9c1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac9c1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac9c1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac9c1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac9c1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac9c1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ac9c1-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-133">Entry</span></span> | <span data-ttu-id="ac9c1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-137">System-Only</span></span>            | <span data-ttu-id="ac9c1-138">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-138">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-140">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-141">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-142">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-142">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-143">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-144">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-149">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-150">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-151">System-Flags</span></span>           | <span data-ttu-id="ac9c1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-152">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-153">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-154">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac9c1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac9c1-155">Windows Server 2003</span></span>



| <span data-ttu-id="ac9c1-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-156">Entry</span></span> | <span data-ttu-id="ac9c1-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-160">System-Only</span></span>            | <span data-ttu-id="ac9c1-161">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-161">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-163">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-164">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-165">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-166">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-167">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-172">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-173">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-174">System-Flags</span></span>           | <span data-ttu-id="ac9c1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-175">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-176">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-177">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac9c1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac9c1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac9c1-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-179">Entry</span></span> | <span data-ttu-id="ac9c1-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-183">System-Only</span></span>            | <span data-ttu-id="ac9c1-184">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-184">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-186">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-187">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-188">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-189">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-190">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-190">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-195">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-196">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-197">System-Flags</span></span>           | <span data-ttu-id="ac9c1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-198">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-199">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-200">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac9c1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac9c1-201">Windows Server 2008</span></span>



| <span data-ttu-id="ac9c1-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-202">Entry</span></span> | <span data-ttu-id="ac9c1-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-206">System-Only</span></span>            | <span data-ttu-id="ac9c1-207">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-207">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-209">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-210">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-211">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-211">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-212">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-213">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-218">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-219">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-220">System-Flags</span></span>           | <span data-ttu-id="ac9c1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-221">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-222">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-223">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac9c1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac9c1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac9c1-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-225">Entry</span></span> | <span data-ttu-id="ac9c1-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-229">System-Only</span></span>            | <span data-ttu-id="ac9c1-230">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-230">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-232">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-233">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-234">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-234">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-235">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-236">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-236">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-241">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-242">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-243">System-Flags</span></span>           | <span data-ttu-id="ac9c1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-244">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-245">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-246">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac9c1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac9c1-247">Windows Server 2012</span></span>



| <span data-ttu-id="ac9c1-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac9c1-248">Entry</span></span> | <span data-ttu-id="ac9c1-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9c1-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ac9c1-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac9c1-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac9c1-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="ac9c1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac9c1-252">System-Only</span></span>            | <span data-ttu-id="ac9c1-253">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-253">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac9c1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ac9c1-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac9c1-255">True</span></span>                                                  |
| <span data-ttu-id="ac9c1-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac9c1-256">Is Indexed</span></span>             | <span data-ttu-id="ac9c1-257">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-257">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac9c1-258">In Global Catalog</span></span>      | <span data-ttu-id="ac9c1-259">Faux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-259">False</span></span>                                                 |
| <span data-ttu-id="ac9c1-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac9c1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac9c1-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac9c1-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="ac9c1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac9c1-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac9c1-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="ac9c1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-264">Search-Flags</span></span>           | <span data-ttu-id="ac9c1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac9c1-265">0x00000000</span></span>                                            |
| <span data-ttu-id="ac9c1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac9c1-266">System-Flags</span></span>           | <span data-ttu-id="ac9c1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac9c1-267">0x00000010</span></span>                                            |
| <span data-ttu-id="ac9c1-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac9c1-268">Classes used in</span></span>        | [<span data-ttu-id="ac9c1-269">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ac9c1-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





