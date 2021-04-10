---
title: Attribut Product-Code
description: Cet attribut contient un identificateur unique pour une application pour une version de produit particulière, représentée sous la forme d’un GUID de chaîne, par exemple \ 0034 ; 12345678-1234-1234-1234-123456789012 \ 0034 ;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Product-Code
- Schéma AD de l’attribut productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103942980"
---
# <a name="product-code-attribute"></a><span data-ttu-id="09b82-105">Attribut Product-Code</span><span class="sxs-lookup"><span data-stu-id="09b82-105">Product-Code attribute</span></span>

<span data-ttu-id="09b82-106">Cet attribut contient un identificateur unique pour une application pour une version de produit particulière, représentée sous la forme d’un GUID de chaîne, par exemple « {12345678-1234-1234-1234-123456789012} ».</span><span class="sxs-lookup"><span data-stu-id="09b82-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="09b82-107">Les lettres utilisées dans ce GUID doivent être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="09b82-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="09b82-108">Cet ID doit varier en fonction des versions et des langues.</span><span class="sxs-lookup"><span data-stu-id="09b82-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="09b82-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-109">Entry</span></span> | <span data-ttu-id="09b82-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="09b82-111">CN</span><span class="sxs-lookup"><span data-stu-id="09b82-111">CN</span></span>                | <span data-ttu-id="09b82-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="09b82-112">Product-Code</span></span>                                          |
| <span data-ttu-id="09b82-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="09b82-113">Ldap-Display-Name</span></span> | <span data-ttu-id="09b82-114">productCode</span><span class="sxs-lookup"><span data-stu-id="09b82-114">productCode</span></span>                                           |
| <span data-ttu-id="09b82-115">Taille</span><span class="sxs-lookup"><span data-stu-id="09b82-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="09b82-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="09b82-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="09b82-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="09b82-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="09b82-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-118">Attribute-Id</span></span>      | <span data-ttu-id="09b82-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="09b82-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="09b82-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09b82-120">System-Id-Guid</span></span>    | <span data-ttu-id="09b82-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="09b82-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="09b82-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09b82-122">Syntax</span></span>            | [<span data-ttu-id="09b82-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="09b82-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="09b82-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="09b82-124">Implementations</span></span>

-   [<span data-ttu-id="09b82-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09b82-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09b82-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09b82-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09b82-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09b82-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09b82-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09b82-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09b82-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09b82-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09b82-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09b82-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09b82-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09b82-131">Windows 2000 Server</span></span>



| <span data-ttu-id="09b82-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-132">Entry</span></span> | <span data-ttu-id="09b82-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-136">System-Only</span></span>            | <span data-ttu-id="09b82-137">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-137">False</span></span>                                                            |
| <span data-ttu-id="09b82-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-138">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-139">True</span></span>                                                             |
| <span data-ttu-id="09b82-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-140">Is Indexed</span></span>             | <span data-ttu-id="09b82-141">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-141">False</span></span>                                                            |
| <span data-ttu-id="09b82-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-142">In Global Catalog</span></span>      | <span data-ttu-id="09b82-143">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-143">False</span></span>                                                            |
| <span data-ttu-id="09b82-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-146">Range-Lower</span></span>            | <span data-ttu-id="09b82-147">0</span><span class="sxs-lookup"><span data-stu-id="09b82-147">0</span></span>                                                                |
| <span data-ttu-id="09b82-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-148">Range-Upper</span></span>            | <span data-ttu-id="09b82-149">16</span><span class="sxs-lookup"><span data-stu-id="09b82-149">16</span></span>                                                               |
| <span data-ttu-id="09b82-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-150">Search-Flags</span></span>           | <span data-ttu-id="09b82-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-152">System-Flags</span></span>           | <span data-ttu-id="09b82-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-154">Classes used in</span></span>        | [<span data-ttu-id="09b82-155">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09b82-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09b82-156">Windows Server 2003</span></span>



| <span data-ttu-id="09b82-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-157">Entry</span></span> | <span data-ttu-id="09b82-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-161">System-Only</span></span>            | <span data-ttu-id="09b82-162">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-162">False</span></span>                                                            |
| <span data-ttu-id="09b82-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-163">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-164">True</span></span>                                                             |
| <span data-ttu-id="09b82-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-165">Is Indexed</span></span>             | <span data-ttu-id="09b82-166">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-166">False</span></span>                                                            |
| <span data-ttu-id="09b82-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-167">In Global Catalog</span></span>      | <span data-ttu-id="09b82-168">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-168">False</span></span>                                                            |
| <span data-ttu-id="09b82-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-171">Range-Lower</span></span>            | <span data-ttu-id="09b82-172">0</span><span class="sxs-lookup"><span data-stu-id="09b82-172">0</span></span>                                                                |
| <span data-ttu-id="09b82-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-173">Range-Upper</span></span>            | <span data-ttu-id="09b82-174">16</span><span class="sxs-lookup"><span data-stu-id="09b82-174">16</span></span>                                                               |
| <span data-ttu-id="09b82-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-175">Search-Flags</span></span>           | <span data-ttu-id="09b82-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-177">System-Flags</span></span>           | <span data-ttu-id="09b82-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-179">Classes used in</span></span>        | [<span data-ttu-id="09b82-180">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09b82-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09b82-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09b82-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-182">Entry</span></span> | <span data-ttu-id="09b82-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-186">System-Only</span></span>            | <span data-ttu-id="09b82-187">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-187">False</span></span>                                                            |
| <span data-ttu-id="09b82-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-188">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-189">True</span></span>                                                             |
| <span data-ttu-id="09b82-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-190">Is Indexed</span></span>             | <span data-ttu-id="09b82-191">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-191">False</span></span>                                                            |
| <span data-ttu-id="09b82-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-192">In Global Catalog</span></span>      | <span data-ttu-id="09b82-193">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-193">False</span></span>                                                            |
| <span data-ttu-id="09b82-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-196">Range-Lower</span></span>            | <span data-ttu-id="09b82-197">0</span><span class="sxs-lookup"><span data-stu-id="09b82-197">0</span></span>                                                                |
| <span data-ttu-id="09b82-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-198">Range-Upper</span></span>            | <span data-ttu-id="09b82-199">16</span><span class="sxs-lookup"><span data-stu-id="09b82-199">16</span></span>                                                               |
| <span data-ttu-id="09b82-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-200">Search-Flags</span></span>           | <span data-ttu-id="09b82-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-202">System-Flags</span></span>           | <span data-ttu-id="09b82-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-204">Classes used in</span></span>        | [<span data-ttu-id="09b82-205">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09b82-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09b82-206">Windows Server 2008</span></span>



| <span data-ttu-id="09b82-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-207">Entry</span></span> | <span data-ttu-id="09b82-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-211">System-Only</span></span>            | <span data-ttu-id="09b82-212">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-212">False</span></span>                                                            |
| <span data-ttu-id="09b82-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-213">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-214">True</span></span>                                                             |
| <span data-ttu-id="09b82-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-215">Is Indexed</span></span>             | <span data-ttu-id="09b82-216">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-216">False</span></span>                                                            |
| <span data-ttu-id="09b82-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-217">In Global Catalog</span></span>      | <span data-ttu-id="09b82-218">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-218">False</span></span>                                                            |
| <span data-ttu-id="09b82-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-221">Range-Lower</span></span>            | <span data-ttu-id="09b82-222">0</span><span class="sxs-lookup"><span data-stu-id="09b82-222">0</span></span>                                                                |
| <span data-ttu-id="09b82-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-223">Range-Upper</span></span>            | <span data-ttu-id="09b82-224">16</span><span class="sxs-lookup"><span data-stu-id="09b82-224">16</span></span>                                                               |
| <span data-ttu-id="09b82-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-225">Search-Flags</span></span>           | <span data-ttu-id="09b82-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-227">System-Flags</span></span>           | <span data-ttu-id="09b82-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-229">Classes used in</span></span>        | [<span data-ttu-id="09b82-230">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09b82-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09b82-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09b82-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-232">Entry</span></span> | <span data-ttu-id="09b82-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-236">System-Only</span></span>            | <span data-ttu-id="09b82-237">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-237">False</span></span>                                                            |
| <span data-ttu-id="09b82-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-238">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-239">True</span></span>                                                             |
| <span data-ttu-id="09b82-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-240">Is Indexed</span></span>             | <span data-ttu-id="09b82-241">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-241">False</span></span>                                                            |
| <span data-ttu-id="09b82-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-242">In Global Catalog</span></span>      | <span data-ttu-id="09b82-243">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-243">False</span></span>                                                            |
| <span data-ttu-id="09b82-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-246">Range-Lower</span></span>            | <span data-ttu-id="09b82-247">0</span><span class="sxs-lookup"><span data-stu-id="09b82-247">0</span></span>                                                                |
| <span data-ttu-id="09b82-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-248">Range-Upper</span></span>            | <span data-ttu-id="09b82-249">16</span><span class="sxs-lookup"><span data-stu-id="09b82-249">16</span></span>                                                               |
| <span data-ttu-id="09b82-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-250">Search-Flags</span></span>           | <span data-ttu-id="09b82-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-252">System-Flags</span></span>           | <span data-ttu-id="09b82-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-254">Classes used in</span></span>        | [<span data-ttu-id="09b82-255">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09b82-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09b82-256">Windows Server 2012</span></span>



| <span data-ttu-id="09b82-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="09b82-257">Entry</span></span> | <span data-ttu-id="09b82-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b82-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="09b82-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="09b82-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09b82-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="09b82-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="09b82-261">System-Only</span></span>            | <span data-ttu-id="09b82-262">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-262">False</span></span>                                                            |
| <span data-ttu-id="09b82-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="09b82-263">Is-Single-Valued</span></span>       | <span data-ttu-id="09b82-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="09b82-264">True</span></span>                                                             |
| <span data-ttu-id="09b82-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="09b82-265">Is Indexed</span></span>             | <span data-ttu-id="09b82-266">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-266">False</span></span>                                                            |
| <span data-ttu-id="09b82-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="09b82-267">In Global Catalog</span></span>      | <span data-ttu-id="09b82-268">Faux</span><span class="sxs-lookup"><span data-stu-id="09b82-268">False</span></span>                                                            |
| <span data-ttu-id="09b82-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="09b82-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="09b82-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="09b82-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="09b82-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09b82-271">Range-Lower</span></span>            | <span data-ttu-id="09b82-272">0</span><span class="sxs-lookup"><span data-stu-id="09b82-272">0</span></span>                                                                |
| <span data-ttu-id="09b82-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09b82-273">Range-Upper</span></span>            | <span data-ttu-id="09b82-274">16</span><span class="sxs-lookup"><span data-stu-id="09b82-274">16</span></span>                                                               |
| <span data-ttu-id="09b82-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-275">Search-Flags</span></span>           | <span data-ttu-id="09b82-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09b82-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="09b82-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09b82-277">System-Flags</span></span>           | <span data-ttu-id="09b82-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09b82-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="09b82-279">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="09b82-279">Classes used in</span></span>        | [<span data-ttu-id="09b82-280">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="09b82-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





