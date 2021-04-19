---
title: Attribut Server-State
description: Indique si le serveur est activé ou désactivé.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Server-State
- Schéma AD de l’attribut serverState
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514467"
---
# <a name="server-state-attribute"></a><span data-ttu-id="6562a-105">Attribut Server-State</span><span class="sxs-lookup"><span data-stu-id="6562a-105">Server-State attribute</span></span>

<span data-ttu-id="6562a-106">Indique si le serveur est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="6562a-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="6562a-107">La valeur 1 indique que le serveur est activé.</span><span class="sxs-lookup"><span data-stu-id="6562a-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="6562a-108">La valeur 2 indique que le serveur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6562a-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="6562a-109">Toutes les autres valeurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="6562a-109">All other values are invalid.</span></span>



| <span data-ttu-id="6562a-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-110">Entry</span></span> | <span data-ttu-id="6562a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6562a-112">CN</span><span class="sxs-lookup"><span data-stu-id="6562a-112">CN</span></span>                | <span data-ttu-id="6562a-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="6562a-113">Server-State</span></span>                         |
| <span data-ttu-id="6562a-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6562a-114">Ldap-Display-Name</span></span> | <span data-ttu-id="6562a-115">serverState</span><span class="sxs-lookup"><span data-stu-id="6562a-115">serverState</span></span>                          |
| <span data-ttu-id="6562a-116">Taille</span><span class="sxs-lookup"><span data-stu-id="6562a-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="6562a-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6562a-117">Update Privilege</span></span>  | <span data-ttu-id="6562a-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="6562a-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="6562a-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6562a-119">Update Frequency</span></span>  | <span data-ttu-id="6562a-120">Lorsque la stratégie d’un utilisateur change.</span><span class="sxs-lookup"><span data-stu-id="6562a-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="6562a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-121">Attribute-Id</span></span>      | <span data-ttu-id="6562a-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="6562a-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="6562a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6562a-123">System-Id-Guid</span></span>    | <span data-ttu-id="6562a-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6562a-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6562a-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6562a-125">Syntax</span></span>            | [<span data-ttu-id="6562a-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6562a-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6562a-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6562a-127">Implementations</span></span>

-   [<span data-ttu-id="6562a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6562a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6562a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6562a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6562a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6562a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6562a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6562a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6562a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6562a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6562a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6562a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6562a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6562a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6562a-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-135">Entry</span></span> | <span data-ttu-id="6562a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-139">System-Only</span></span>            | <span data-ttu-id="6562a-140">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-140">False</span></span>                                                 |
| <span data-ttu-id="6562a-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-142">True</span></span>                                                  |
| <span data-ttu-id="6562a-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-143">Is Indexed</span></span>             | <span data-ttu-id="6562a-144">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-144">False</span></span>                                                 |
| <span data-ttu-id="6562a-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-145">In Global Catalog</span></span>      | <span data-ttu-id="6562a-146">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-146">False</span></span>                                                 |
| <span data-ttu-id="6562a-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-151">Search-Flags</span></span>           | <span data-ttu-id="6562a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-152">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-153">System-Flags</span></span>           | <span data-ttu-id="6562a-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-154">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-155">Classes used in</span></span>        | [<span data-ttu-id="6562a-156">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6562a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6562a-157">Windows Server 2003</span></span>



| <span data-ttu-id="6562a-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-158">Entry</span></span> | <span data-ttu-id="6562a-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-162">System-Only</span></span>            | <span data-ttu-id="6562a-163">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-163">False</span></span>                                                 |
| <span data-ttu-id="6562a-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-165">True</span></span>                                                  |
| <span data-ttu-id="6562a-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-166">Is Indexed</span></span>             | <span data-ttu-id="6562a-167">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-167">False</span></span>                                                 |
| <span data-ttu-id="6562a-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-168">In Global Catalog</span></span>      | <span data-ttu-id="6562a-169">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-169">False</span></span>                                                 |
| <span data-ttu-id="6562a-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-174">Search-Flags</span></span>           | <span data-ttu-id="6562a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-175">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-176">System-Flags</span></span>           | <span data-ttu-id="6562a-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-177">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-178">Classes used in</span></span>        | [<span data-ttu-id="6562a-179">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6562a-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6562a-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6562a-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-181">Entry</span></span> | <span data-ttu-id="6562a-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-185">System-Only</span></span>            | <span data-ttu-id="6562a-186">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-186">False</span></span>                                                 |
| <span data-ttu-id="6562a-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-188">True</span></span>                                                  |
| <span data-ttu-id="6562a-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-189">Is Indexed</span></span>             | <span data-ttu-id="6562a-190">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-190">False</span></span>                                                 |
| <span data-ttu-id="6562a-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-191">In Global Catalog</span></span>      | <span data-ttu-id="6562a-192">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-192">False</span></span>                                                 |
| <span data-ttu-id="6562a-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-197">Search-Flags</span></span>           | <span data-ttu-id="6562a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-198">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-199">System-Flags</span></span>           | <span data-ttu-id="6562a-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-200">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-201">Classes used in</span></span>        | [<span data-ttu-id="6562a-202">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6562a-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6562a-203">Windows Server 2008</span></span>



| <span data-ttu-id="6562a-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-204">Entry</span></span> | <span data-ttu-id="6562a-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-208">System-Only</span></span>            | <span data-ttu-id="6562a-209">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-209">False</span></span>                                                 |
| <span data-ttu-id="6562a-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-211">True</span></span>                                                  |
| <span data-ttu-id="6562a-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-212">Is Indexed</span></span>             | <span data-ttu-id="6562a-213">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-213">False</span></span>                                                 |
| <span data-ttu-id="6562a-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-214">In Global Catalog</span></span>      | <span data-ttu-id="6562a-215">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-215">False</span></span>                                                 |
| <span data-ttu-id="6562a-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-220">Search-Flags</span></span>           | <span data-ttu-id="6562a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-221">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-222">System-Flags</span></span>           | <span data-ttu-id="6562a-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-223">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-224">Classes used in</span></span>        | [<span data-ttu-id="6562a-225">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6562a-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6562a-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6562a-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-227">Entry</span></span> | <span data-ttu-id="6562a-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-231">System-Only</span></span>            | <span data-ttu-id="6562a-232">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-232">False</span></span>                                                 |
| <span data-ttu-id="6562a-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-234">True</span></span>                                                  |
| <span data-ttu-id="6562a-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-235">Is Indexed</span></span>             | <span data-ttu-id="6562a-236">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-236">False</span></span>                                                 |
| <span data-ttu-id="6562a-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-237">In Global Catalog</span></span>      | <span data-ttu-id="6562a-238">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-238">False</span></span>                                                 |
| <span data-ttu-id="6562a-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-243">Search-Flags</span></span>           | <span data-ttu-id="6562a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-244">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-245">System-Flags</span></span>           | <span data-ttu-id="6562a-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-246">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-247">Classes used in</span></span>        | [<span data-ttu-id="6562a-248">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6562a-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6562a-249">Windows Server 2012</span></span>



| <span data-ttu-id="6562a-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="6562a-250">Entry</span></span> | <span data-ttu-id="6562a-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="6562a-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6562a-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6562a-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6562a-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="6562a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6562a-254">System-Only</span></span>            | <span data-ttu-id="6562a-255">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-255">False</span></span>                                                 |
| <span data-ttu-id="6562a-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6562a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6562a-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="6562a-257">True</span></span>                                                  |
| <span data-ttu-id="6562a-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6562a-258">Is Indexed</span></span>             | <span data-ttu-id="6562a-259">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-259">False</span></span>                                                 |
| <span data-ttu-id="6562a-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6562a-260">In Global Catalog</span></span>      | <span data-ttu-id="6562a-261">Faux</span><span class="sxs-lookup"><span data-stu-id="6562a-261">False</span></span>                                                 |
| <span data-ttu-id="6562a-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6562a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6562a-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6562a-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="6562a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6562a-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6562a-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="6562a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-266">Search-Flags</span></span>           | <span data-ttu-id="6562a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6562a-267">0x00000000</span></span>                                            |
| <span data-ttu-id="6562a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6562a-268">System-Flags</span></span>           | <span data-ttu-id="6562a-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6562a-269">0x00000011</span></span>                                            |
| <span data-ttu-id="6562a-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6562a-270">Classes used in</span></span>        | [<span data-ttu-id="6562a-271">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="6562a-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





