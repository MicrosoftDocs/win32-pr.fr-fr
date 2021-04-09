---
title: Attribut Object-Guid
description: Identificateur unique d’un objet.
ms.assetid: fc2d65a3-7472-41ef-9780-d1a7ec965804
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Guid
- Schéma AD de l’attribut objectGUID
topic_type:
- apiref
api_name:
- Object-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e3715c38b629869296e6f8df5dbebd9a515d1b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845374"
---
# <a name="object-guid-attribute"></a><span data-ttu-id="cdc4d-105">Attribut Object-Guid</span><span class="sxs-lookup"><span data-stu-id="cdc4d-105">Object-Guid attribute</span></span>

<span data-ttu-id="cdc4d-106">Identificateur unique d’un objet.</span><span class="sxs-lookup"><span data-stu-id="cdc4d-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="cdc4d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-107">Entry</span></span> | <span data-ttu-id="cdc4d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cdc4d-109">CN</span><span class="sxs-lookup"><span data-stu-id="cdc4d-109">CN</span></span>                | <span data-ttu-id="cdc4d-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="cdc4d-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="cdc4d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cdc4d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cdc4d-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="cdc4d-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="cdc4d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="cdc4d-113">Size</span></span>              | <span data-ttu-id="cdc4d-114">16 octets</span><span class="sxs-lookup"><span data-stu-id="cdc4d-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="cdc4d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cdc4d-115">Update Privilege</span></span>  | <span data-ttu-id="cdc4d-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="cdc4d-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="cdc4d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cdc4d-117">Update Frequency</span></span>  | <span data-ttu-id="cdc4d-118">Cette valeur est définie lorsque l’objet est créé et ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="cdc4d-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="cdc4d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-119">Attribute-Id</span></span>      | <span data-ttu-id="cdc4d-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="cdc4d-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="cdc4d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cdc4d-121">System-Id-Guid</span></span>    | <span data-ttu-id="cdc4d-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cdc4d-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="cdc4d-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdc4d-123">Syntax</span></span>            | [<span data-ttu-id="cdc4d-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="cdc4d-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cdc4d-125">Implementations</span></span>

-   [<span data-ttu-id="cdc4d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cdc4d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cdc4d-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cdc4d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cdc4d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cdc4d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cdc4d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cdc4d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cdc4d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cdc4d-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-134">Entry</span></span> | <span data-ttu-id="cdc4d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-137">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-138">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-139">System-Only</span></span>            | <span data-ttu-id="cdc4d-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-140">True</span></span>                            |
| <span data-ttu-id="cdc4d-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-142">True</span></span>                            |
| <span data-ttu-id="cdc4d-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-143">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-144">True</span></span>                            |
| <span data-ttu-id="cdc4d-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-145">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-146">True</span></span>                            |
| <span data-ttu-id="cdc4d-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-149">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-150">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-150">16</span></span>                              |
| <span data-ttu-id="cdc4d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-151">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-152">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-152">16</span></span>                              |
| <span data-ttu-id="cdc4d-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-153">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-154">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-155">System-Flags</span></span>           | <span data-ttu-id="cdc4d-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-156">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-157">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cdc4d-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cdc4d-159">Windows Server 2003</span></span>



| <span data-ttu-id="cdc4d-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-160">Entry</span></span> | <span data-ttu-id="cdc4d-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-163">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-164">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-165">System-Only</span></span>            | <span data-ttu-id="cdc4d-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-166">True</span></span>                            |
| <span data-ttu-id="cdc4d-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-167">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-168">True</span></span>                            |
| <span data-ttu-id="cdc4d-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-169">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-170">True</span></span>                            |
| <span data-ttu-id="cdc4d-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-171">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-172">True</span></span>                            |
| <span data-ttu-id="cdc4d-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-175">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-176">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-176">16</span></span>                              |
| <span data-ttu-id="cdc4d-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-177">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-178">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-178">16</span></span>                              |
| <span data-ttu-id="cdc4d-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-179">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-180">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-181">System-Flags</span></span>           | <span data-ttu-id="cdc4d-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-182">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-183">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-183">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-184">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cdc4d-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="cdc4d-185">ADAM</span></span>



| <span data-ttu-id="cdc4d-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-186">Entry</span></span> | <span data-ttu-id="cdc4d-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-189">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-190">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-191">System-Only</span></span>            | <span data-ttu-id="cdc4d-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-192">True</span></span>                            |
| <span data-ttu-id="cdc4d-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-193">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-194">True</span></span>                            |
| <span data-ttu-id="cdc4d-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-195">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-196">True</span></span>                            |
| <span data-ttu-id="cdc4d-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-197">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-198">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-198">True</span></span>                            |
| <span data-ttu-id="cdc4d-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-201">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-202">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-202">16</span></span>                              |
| <span data-ttu-id="cdc4d-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-203">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-204">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-204">16</span></span>                              |
| <span data-ttu-id="cdc4d-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-205">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-206">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-207">System-Flags</span></span>           | <span data-ttu-id="cdc4d-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-208">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-209">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-210">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cdc4d-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cdc4d-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cdc4d-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-212">Entry</span></span> | <span data-ttu-id="cdc4d-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-215">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-216">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-217">System-Only</span></span>            | <span data-ttu-id="cdc4d-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-218">True</span></span>                            |
| <span data-ttu-id="cdc4d-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-219">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-220">True</span></span>                            |
| <span data-ttu-id="cdc4d-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-221">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-222">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-222">True</span></span>                            |
| <span data-ttu-id="cdc4d-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-223">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-224">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-224">True</span></span>                            |
| <span data-ttu-id="cdc4d-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-227">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-228">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-228">16</span></span>                              |
| <span data-ttu-id="cdc4d-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-229">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-230">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-230">16</span></span>                              |
| <span data-ttu-id="cdc4d-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-231">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-232">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-233">System-Flags</span></span>           | <span data-ttu-id="cdc4d-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-234">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-235">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-235">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-236">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cdc4d-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdc4d-237">Windows Server 2008</span></span>



| <span data-ttu-id="cdc4d-238">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-238">Entry</span></span> | <span data-ttu-id="cdc4d-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-240">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-241">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-242">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-243">System-Only</span></span>            | <span data-ttu-id="cdc4d-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-244">True</span></span>                            |
| <span data-ttu-id="cdc4d-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-245">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-246">True</span></span>                            |
| <span data-ttu-id="cdc4d-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-247">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-248">True</span></span>                            |
| <span data-ttu-id="cdc4d-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-249">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-250">True</span></span>                            |
| <span data-ttu-id="cdc4d-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-253">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-254">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-254">16</span></span>                              |
| <span data-ttu-id="cdc4d-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-255">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-256">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-256">16</span></span>                              |
| <span data-ttu-id="cdc4d-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-257">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-258">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-259">System-Flags</span></span>           | <span data-ttu-id="cdc4d-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-260">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-261">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-261">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-262">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cdc4d-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cdc4d-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cdc4d-264">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-264">Entry</span></span> | <span data-ttu-id="cdc4d-265">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-266">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-267">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-268">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-269">System-Only</span></span>            | <span data-ttu-id="cdc4d-270">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-270">True</span></span>                            |
| <span data-ttu-id="cdc4d-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-271">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-272">True</span></span>                            |
| <span data-ttu-id="cdc4d-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-273">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-274">True</span></span>                            |
| <span data-ttu-id="cdc4d-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-275">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-276">True</span></span>                            |
| <span data-ttu-id="cdc4d-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-279">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-280">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-280">16</span></span>                              |
| <span data-ttu-id="cdc4d-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-281">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-282">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-282">16</span></span>                              |
| <span data-ttu-id="cdc4d-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-283">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-284">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-285">System-Flags</span></span>           | <span data-ttu-id="cdc4d-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-286">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-287">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-287">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-288">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cdc4d-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdc4d-289">Windows Server 2012</span></span>



| <span data-ttu-id="cdc4d-290">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdc4d-290">Entry</span></span> | <span data-ttu-id="cdc4d-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc4d-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdc4d-292">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdc4d-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdc4d-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdc4d-293">MAPI-Id</span></span>                | <span data-ttu-id="cdc4d-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="cdc4d-294">0x8C6D</span></span>                          |
| <span data-ttu-id="cdc4d-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdc4d-295">System-Only</span></span>            | <span data-ttu-id="cdc4d-296">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-296">True</span></span>                            |
| <span data-ttu-id="cdc4d-297">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdc4d-297">Is-Single-Valued</span></span>       | <span data-ttu-id="cdc4d-298">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-298">True</span></span>                            |
| <span data-ttu-id="cdc4d-299">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdc4d-299">Is Indexed</span></span>             | <span data-ttu-id="cdc4d-300">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-300">True</span></span>                            |
| <span data-ttu-id="cdc4d-301">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdc4d-301">In Global Catalog</span></span>      | <span data-ttu-id="cdc4d-302">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdc4d-302">True</span></span>                            |
| <span data-ttu-id="cdc4d-303">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdc4d-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdc4d-304">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdc4d-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdc4d-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdc4d-305">Range-Lower</span></span>            | <span data-ttu-id="cdc4d-306">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-306">16</span></span>                              |
| <span data-ttu-id="cdc4d-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdc4d-307">Range-Upper</span></span>            | <span data-ttu-id="cdc4d-308">16</span><span class="sxs-lookup"><span data-stu-id="cdc4d-308">16</span></span>                              |
| <span data-ttu-id="cdc4d-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-309">Search-Flags</span></span>           | <span data-ttu-id="cdc4d-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cdc4d-310">0x00000009</span></span>                      |
| <span data-ttu-id="cdc4d-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdc4d-311">System-Flags</span></span>           | <span data-ttu-id="cdc4d-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cdc4d-312">0x00000013</span></span>                      |
| <span data-ttu-id="cdc4d-313">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdc4d-313">Classes used in</span></span>        | [<span data-ttu-id="cdc4d-314">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdc4d-314">**Top**</span></span>](c-top.md)<br/> |



 

 





