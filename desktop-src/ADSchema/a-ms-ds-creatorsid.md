---
title: Attribut MS-DS-Creator-SID
description: ID de sécurité du créateur de l’objet qui contient cet attribut.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-DS-Creator-SID
- Schéma AD de l’attribut mS-DS-CreatorSID
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943030"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="0b1c0-105">Attribut MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="0b1c0-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="0b1c0-106">ID de sécurité du créateur de l’objet qui contient cet attribut.</span><span class="sxs-lookup"><span data-stu-id="0b1c0-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="0b1c0-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-107">Entry</span></span> | <span data-ttu-id="0b1c0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0b1c0-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b1c0-109">CN</span></span>                | <span data-ttu-id="0b1c0-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="0b1c0-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="0b1c0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0b1c0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b1c0-112">mS-DS-CreatorSID</span><span class="sxs-lookup"><span data-stu-id="0b1c0-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="0b1c0-113">Taille</span><span class="sxs-lookup"><span data-stu-id="0b1c0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="0b1c0-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="0b1c0-114">Update Privilege</span></span>  | <span data-ttu-id="0b1c0-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="0b1c0-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="0b1c0-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="0b1c0-116">Update Frequency</span></span>  | <span data-ttu-id="0b1c0-117">Chaque fois qu’un nouvel objet est créé.</span><span class="sxs-lookup"><span data-stu-id="0b1c0-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="0b1c0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-118">Attribute-Id</span></span>      | <span data-ttu-id="0b1c0-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="0b1c0-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="0b1c0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0b1c0-120">System-Id-Guid</span></span>    | <span data-ttu-id="0b1c0-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="0b1c0-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="0b1c0-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b1c0-122">Syntax</span></span>            | [<span data-ttu-id="0b1c0-123">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="0b1c0-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="0b1c0-124">Implementations</span></span>

-   [<span data-ttu-id="0b1c0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b1c0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b1c0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b1c0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b1c0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b1c0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b1c0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b1c0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0b1c0-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-132">Entry</span></span> | <span data-ttu-id="0b1c0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-136">System-Only</span></span>            | <span data-ttu-id="0b1c0-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-137">True</span></span>                              |
| <span data-ttu-id="0b1c0-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-139">True</span></span>                              |
| <span data-ttu-id="0b1c0-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-140">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-141">True</span></span>                              |
| <span data-ttu-id="0b1c0-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-142">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-143">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-143">False</span></span>                             |
| <span data-ttu-id="0b1c0-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-148">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-149">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-150">System-Flags</span></span>           | <span data-ttu-id="0b1c0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-151">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-152">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-153">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b1c0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b1c0-154">Windows Server 2003</span></span>



| <span data-ttu-id="0b1c0-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-155">Entry</span></span> | <span data-ttu-id="0b1c0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-159">System-Only</span></span>            | <span data-ttu-id="0b1c0-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-160">True</span></span>                              |
| <span data-ttu-id="0b1c0-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-162">True</span></span>                              |
| <span data-ttu-id="0b1c0-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-163">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-164">True</span></span>                              |
| <span data-ttu-id="0b1c0-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-165">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-166">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-166">False</span></span>                             |
| <span data-ttu-id="0b1c0-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-171">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-172">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-173">System-Flags</span></span>           | <span data-ttu-id="0b1c0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-174">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-175">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-176">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b1c0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b1c0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b1c0-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-178">Entry</span></span> | <span data-ttu-id="0b1c0-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-182">System-Only</span></span>            | <span data-ttu-id="0b1c0-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-183">True</span></span>                              |
| <span data-ttu-id="0b1c0-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-185">True</span></span>                              |
| <span data-ttu-id="0b1c0-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-186">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-187">True</span></span>                              |
| <span data-ttu-id="0b1c0-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-188">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-189">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-189">False</span></span>                             |
| <span data-ttu-id="0b1c0-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-194">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-195">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-196">System-Flags</span></span>           | <span data-ttu-id="0b1c0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-197">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-198">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-199">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b1c0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b1c0-200">Windows Server 2008</span></span>



| <span data-ttu-id="0b1c0-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-201">Entry</span></span> | <span data-ttu-id="0b1c0-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-205">System-Only</span></span>            | <span data-ttu-id="0b1c0-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-206">True</span></span>                              |
| <span data-ttu-id="0b1c0-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-208">True</span></span>                              |
| <span data-ttu-id="0b1c0-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-209">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-210">True</span></span>                              |
| <span data-ttu-id="0b1c0-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-211">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-212">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-212">False</span></span>                             |
| <span data-ttu-id="0b1c0-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-217">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-218">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-219">System-Flags</span></span>           | <span data-ttu-id="0b1c0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-220">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-221">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-222">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b1c0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b1c0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b1c0-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-224">Entry</span></span> | <span data-ttu-id="0b1c0-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-228">System-Only</span></span>            | <span data-ttu-id="0b1c0-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-229">True</span></span>                              |
| <span data-ttu-id="0b1c0-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-231">True</span></span>                              |
| <span data-ttu-id="0b1c0-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-232">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-233">True</span></span>                              |
| <span data-ttu-id="0b1c0-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-234">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-235">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-235">False</span></span>                             |
| <span data-ttu-id="0b1c0-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-240">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-241">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-242">System-Flags</span></span>           | <span data-ttu-id="0b1c0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-243">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-244">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-245">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b1c0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b1c0-246">Windows Server 2012</span></span>



| <span data-ttu-id="0b1c0-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="0b1c0-247">Entry</span></span> | <span data-ttu-id="0b1c0-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1c0-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0b1c0-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0b1c0-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b1c0-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0b1c0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b1c0-251">System-Only</span></span>            | <span data-ttu-id="0b1c0-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-252">True</span></span>                              |
| <span data-ttu-id="0b1c0-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0b1c0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0b1c0-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-254">True</span></span>                              |
| <span data-ttu-id="0b1c0-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0b1c0-255">Is Indexed</span></span>             | <span data-ttu-id="0b1c0-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="0b1c0-256">True</span></span>                              |
| <span data-ttu-id="0b1c0-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0b1c0-257">In Global Catalog</span></span>      | <span data-ttu-id="0b1c0-258">Faux</span><span class="sxs-lookup"><span data-stu-id="0b1c0-258">False</span></span>                             |
| <span data-ttu-id="0b1c0-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0b1c0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b1c0-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0b1c0-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0b1c0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b1c0-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b1c0-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0b1c0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-263">Search-Flags</span></span>           | <span data-ttu-id="0b1c0-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b1c0-264">0x00000001</span></span>                        |
| <span data-ttu-id="0b1c0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b1c0-265">System-Flags</span></span>           | <span data-ttu-id="0b1c0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b1c0-266">0x00000010</span></span>                        |
| <span data-ttu-id="0b1c0-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0b1c0-267">Classes used in</span></span>        | [<span data-ttu-id="0b1c0-268">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="0b1c0-268">**User**</span></span>](c-user.md)<br/> |



 

 





