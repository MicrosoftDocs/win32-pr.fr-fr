---
title: Attribut Force-Logoff
description: Utilisé pour calculer l’heure de lancement dans SamIGetAccountRestrictions. Délai de déconnexion moins forcer la fermeture de session est égal à heure de lancement.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Force-Logoff
- Schéma AD de l’attribut forceLogoff
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e31cb241cde4deb40d5978594b4354fbcc564b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107086"
---
# <a name="force-logoff-attribute"></a><span data-ttu-id="8ebbd-106">Attribut Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="8ebbd-106">Force-Logoff attribute</span></span>

<span data-ttu-id="8ebbd-107">Utilisé pour calculer l’heure de lancement dans SamIGetAccountRestrictions.</span><span class="sxs-lookup"><span data-stu-id="8ebbd-107">Used in computing the kick off time in SamIGetAccountRestrictions.</span></span> <span data-ttu-id="8ebbd-108">Délai de déconnexion moins forcer la fermeture de session est égal à heure de lancement.</span><span class="sxs-lookup"><span data-stu-id="8ebbd-108">Logoff time minus Force Log off equals kick off time.</span></span>



| <span data-ttu-id="8ebbd-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-109">Entry</span></span> | <span data-ttu-id="8ebbd-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8ebbd-111">CN</span><span class="sxs-lookup"><span data-stu-id="8ebbd-111">CN</span></span>                | <span data-ttu-id="8ebbd-112">Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="8ebbd-112">Force-Logoff</span></span>                         |
| <span data-ttu-id="8ebbd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8ebbd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8ebbd-114">forceLogoff</span><span class="sxs-lookup"><span data-stu-id="8ebbd-114">forceLogoff</span></span>                          |
| <span data-ttu-id="8ebbd-115">Taille</span><span class="sxs-lookup"><span data-stu-id="8ebbd-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="8ebbd-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8ebbd-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8ebbd-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8ebbd-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8ebbd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-118">Attribute-Id</span></span>      | <span data-ttu-id="8ebbd-119">1.2.840.113556.1.4.39</span><span class="sxs-lookup"><span data-stu-id="8ebbd-119">1.2.840.113556.1.4.39</span></span>                |
| <span data-ttu-id="8ebbd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8ebbd-120">System-Id-Guid</span></span>    | <span data-ttu-id="8ebbd-121">bf967977-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8ebbd-121">bf967977-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8ebbd-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ebbd-122">Syntax</span></span>            | [<span data-ttu-id="8ebbd-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8ebbd-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8ebbd-124">Implementations</span></span>

-   [<span data-ttu-id="8ebbd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8ebbd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8ebbd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8ebbd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8ebbd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8ebbd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8ebbd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ebbd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8ebbd-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-132">Entry</span></span> | <span data-ttu-id="8ebbd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-133">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-134">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-135">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-136">System-Only</span></span>            | <span data-ttu-id="8ebbd-137">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-137">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-139">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-140">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-141">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-141">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-142">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-143">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-143">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-145">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-146">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-147">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-148">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-149">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-150">System-Flags</span></span>           | <span data-ttu-id="8ebbd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-151">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-152">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-153">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-154">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8ebbd-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ebbd-155">Windows Server 2003</span></span>



| <span data-ttu-id="8ebbd-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-156">Entry</span></span> | <span data-ttu-id="8ebbd-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-157">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-158">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-159">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-160">System-Only</span></span>            | <span data-ttu-id="8ebbd-161">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-161">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-163">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-164">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-165">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-165">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-166">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-167">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-167">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-169">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-170">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-171">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-172">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-173">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-174">System-Flags</span></span>           | <span data-ttu-id="8ebbd-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-175">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-176">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-177">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-178">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8ebbd-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8ebbd-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8ebbd-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-180">Entry</span></span> | <span data-ttu-id="8ebbd-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-181">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-182">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-183">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-184">System-Only</span></span>            | <span data-ttu-id="8ebbd-185">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-185">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-187">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-188">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-189">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-189">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-190">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-191">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-191">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-193">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-194">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-195">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-196">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-197">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-198">System-Flags</span></span>           | <span data-ttu-id="8ebbd-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-199">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-200">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-201">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-201">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-202">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8ebbd-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ebbd-203">Windows Server 2008</span></span>



| <span data-ttu-id="8ebbd-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-204">Entry</span></span> | <span data-ttu-id="8ebbd-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-205">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-206">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-207">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-208">System-Only</span></span>            | <span data-ttu-id="8ebbd-209">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-209">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-210">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-211">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-212">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-213">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-213">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-214">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-215">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-215">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-217">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-218">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-219">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-220">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-221">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-222">System-Flags</span></span>           | <span data-ttu-id="8ebbd-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-223">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-224">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-225">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-225">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-226">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-226">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8ebbd-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ebbd-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8ebbd-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-228">Entry</span></span> | <span data-ttu-id="8ebbd-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-229">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-230">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-231">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-232">System-Only</span></span>            | <span data-ttu-id="8ebbd-233">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-233">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-234">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-235">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-236">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-237">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-237">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-238">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-239">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-239">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-241">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-242">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-243">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-244">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-245">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-246">System-Flags</span></span>           | <span data-ttu-id="8ebbd-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-247">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-248">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-249">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-249">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-250">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-250">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8ebbd-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ebbd-251">Windows Server 2012</span></span>



| <span data-ttu-id="8ebbd-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ebbd-252">Entry</span></span> | <span data-ttu-id="8ebbd-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebbd-253">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebbd-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8ebbd-254">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ebbd-255">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="8ebbd-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ebbd-256">System-Only</span></span>            | <span data-ttu-id="8ebbd-257">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-257">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8ebbd-258">Is-Single-Valued</span></span>       | <span data-ttu-id="8ebbd-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="8ebbd-259">True</span></span>                                                                                                     |
| <span data-ttu-id="8ebbd-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8ebbd-260">Is Indexed</span></span>             | <span data-ttu-id="8ebbd-261">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-261">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8ebbd-262">In Global Catalog</span></span>      | <span data-ttu-id="8ebbd-263">Faux</span><span class="sxs-lookup"><span data-stu-id="8ebbd-263">False</span></span>                                                                                                    |
| <span data-ttu-id="8ebbd-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8ebbd-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ebbd-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8ebbd-265">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="8ebbd-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ebbd-266">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ebbd-267">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="8ebbd-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-268">Search-Flags</span></span>           | <span data-ttu-id="8ebbd-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ebbd-269">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ebbd-270">System-Flags</span></span>           | <span data-ttu-id="8ebbd-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ebbd-271">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="8ebbd-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8ebbd-272">Classes used in</span></span>        | [<span data-ttu-id="8ebbd-273">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-273">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8ebbd-274">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="8ebbd-274">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





