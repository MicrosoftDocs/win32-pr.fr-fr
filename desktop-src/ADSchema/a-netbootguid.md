---
title: Attribut netboot-GUID
description: Démarrage sans disque de l’identificateur global unique (GUID) de l’ordinateur. Correspond à l’adresse MAC de la carte réseau de l’ordinateur.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut netboot-GUID
- Schéma AD de l’attribut netbootGUID
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845386"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="ad8a8-106">Attribut netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="ad8a8-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="ad8a8-107">Démarrage sans disque : GUID intégré à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ad8a8-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="ad8a8-108">Correspond à l’adresse MAC de la carte réseau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ad8a8-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="ad8a8-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-109">Entry</span></span> | <span data-ttu-id="ad8a8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ad8a8-111">CN</span><span class="sxs-lookup"><span data-stu-id="ad8a8-111">CN</span></span>                | <span data-ttu-id="ad8a8-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="ad8a8-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="ad8a8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ad8a8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ad8a8-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="ad8a8-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="ad8a8-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ad8a8-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ad8a8-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ad8a8-116">Update Privilege</span></span>  | <span data-ttu-id="ad8a8-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ad8a8-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="ad8a8-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ad8a8-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ad8a8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-119">Attribute-Id</span></span>      | <span data-ttu-id="ad8a8-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="ad8a8-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="ad8a8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad8a8-121">System-Id-Guid</span></span>    | <span data-ttu-id="ad8a8-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ad8a8-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="ad8a8-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad8a8-123">Syntax</span></span>            | [<span data-ttu-id="ad8a8-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ad8a8-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ad8a8-125">Implementations</span></span>

-   [<span data-ttu-id="ad8a8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ad8a8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad8a8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad8a8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad8a8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad8a8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ad8a8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad8a8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ad8a8-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-133">Entry</span></span> | <span data-ttu-id="ad8a8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-137">System-Only</span></span>            | <span data-ttu-id="ad8a8-138">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-138">False</span></span>                                     |
| <span data-ttu-id="ad8a8-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-140">True</span></span>                                      |
| <span data-ttu-id="ad8a8-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-141">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-142">True</span></span>                                      |
| <span data-ttu-id="ad8a8-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-143">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-144">True</span></span>                                      |
| <span data-ttu-id="ad8a8-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-147">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-148">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-148">16</span></span>                                        |
| <span data-ttu-id="ad8a8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-149">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-150">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-150">16</span></span>                                        |
| <span data-ttu-id="ad8a8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-151">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-152">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-153">System-Flags</span></span>           | <span data-ttu-id="ad8a8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-154">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-155">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ad8a8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad8a8-157">Windows Server 2003</span></span>



| <span data-ttu-id="ad8a8-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-158">Entry</span></span> | <span data-ttu-id="ad8a8-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-162">System-Only</span></span>            | <span data-ttu-id="ad8a8-163">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-163">False</span></span>                                     |
| <span data-ttu-id="ad8a8-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-165">True</span></span>                                      |
| <span data-ttu-id="ad8a8-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-166">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-167">True</span></span>                                      |
| <span data-ttu-id="ad8a8-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-168">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-169">True</span></span>                                      |
| <span data-ttu-id="ad8a8-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-172">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-173">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-173">16</span></span>                                        |
| <span data-ttu-id="ad8a8-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-174">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-175">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-175">16</span></span>                                        |
| <span data-ttu-id="ad8a8-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-176">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-177">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-178">System-Flags</span></span>           | <span data-ttu-id="ad8a8-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-179">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-180">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad8a8-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad8a8-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad8a8-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-183">Entry</span></span> | <span data-ttu-id="ad8a8-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-187">System-Only</span></span>            | <span data-ttu-id="ad8a8-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-188">False</span></span>                                     |
| <span data-ttu-id="ad8a8-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-190">True</span></span>                                      |
| <span data-ttu-id="ad8a8-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-191">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-192">True</span></span>                                      |
| <span data-ttu-id="ad8a8-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-193">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-194">True</span></span>                                      |
| <span data-ttu-id="ad8a8-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-197">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-198">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-198">16</span></span>                                        |
| <span data-ttu-id="ad8a8-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-199">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-200">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-200">16</span></span>                                        |
| <span data-ttu-id="ad8a8-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-201">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-202">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-203">System-Flags</span></span>           | <span data-ttu-id="ad8a8-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-204">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-205">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad8a8-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad8a8-207">Windows Server 2008</span></span>



| <span data-ttu-id="ad8a8-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-208">Entry</span></span> | <span data-ttu-id="ad8a8-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-212">System-Only</span></span>            | <span data-ttu-id="ad8a8-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-213">False</span></span>                                     |
| <span data-ttu-id="ad8a8-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-215">True</span></span>                                      |
| <span data-ttu-id="ad8a8-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-216">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-217">True</span></span>                                      |
| <span data-ttu-id="ad8a8-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-218">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-219">True</span></span>                                      |
| <span data-ttu-id="ad8a8-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-222">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-223">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-223">16</span></span>                                        |
| <span data-ttu-id="ad8a8-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-224">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-225">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-225">16</span></span>                                        |
| <span data-ttu-id="ad8a8-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-226">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-227">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-228">System-Flags</span></span>           | <span data-ttu-id="ad8a8-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-229">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-230">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad8a8-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad8a8-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad8a8-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-233">Entry</span></span> | <span data-ttu-id="ad8a8-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-237">System-Only</span></span>            | <span data-ttu-id="ad8a8-238">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-238">False</span></span>                                     |
| <span data-ttu-id="ad8a8-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-240">True</span></span>                                      |
| <span data-ttu-id="ad8a8-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-241">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-242">True</span></span>                                      |
| <span data-ttu-id="ad8a8-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-243">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-244">True</span></span>                                      |
| <span data-ttu-id="ad8a8-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-247">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-248">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-248">16</span></span>                                        |
| <span data-ttu-id="ad8a8-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-249">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-250">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-250">16</span></span>                                        |
| <span data-ttu-id="ad8a8-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-251">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-252">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-253">System-Flags</span></span>           | <span data-ttu-id="ad8a8-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-254">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-255">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad8a8-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad8a8-257">Windows Server 2012</span></span>



| <span data-ttu-id="ad8a8-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="ad8a8-258">Entry</span></span> | <span data-ttu-id="ad8a8-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a8-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ad8a8-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ad8a8-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8a8-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ad8a8-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8a8-262">System-Only</span></span>            | <span data-ttu-id="ad8a8-263">Faux</span><span class="sxs-lookup"><span data-stu-id="ad8a8-263">False</span></span>                                     |
| <span data-ttu-id="ad8a8-264">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ad8a8-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8a8-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-265">True</span></span>                                      |
| <span data-ttu-id="ad8a8-266">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ad8a8-266">Is Indexed</span></span>             | <span data-ttu-id="ad8a8-267">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-267">True</span></span>                                      |
| <span data-ttu-id="ad8a8-268">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ad8a8-268">In Global Catalog</span></span>      | <span data-ttu-id="ad8a8-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="ad8a8-269">True</span></span>                                      |
| <span data-ttu-id="ad8a8-270">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ad8a8-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8a8-271">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ad8a8-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ad8a8-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8a8-272">Range-Lower</span></span>            | <span data-ttu-id="ad8a8-273">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-273">16</span></span>                                        |
| <span data-ttu-id="ad8a8-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8a8-274">Range-Upper</span></span>            | <span data-ttu-id="ad8a8-275">16</span><span class="sxs-lookup"><span data-stu-id="ad8a8-275">16</span></span>                                        |
| <span data-ttu-id="ad8a8-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-276">Search-Flags</span></span>           | <span data-ttu-id="ad8a8-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad8a8-277">0x00000001</span></span>                                |
| <span data-ttu-id="ad8a8-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8a8-278">System-Flags</span></span>           | <span data-ttu-id="ad8a8-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8a8-279">0x00000010</span></span>                                |
| <span data-ttu-id="ad8a8-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ad8a8-280">Classes used in</span></span>        | [<span data-ttu-id="ad8a8-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ad8a8-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





