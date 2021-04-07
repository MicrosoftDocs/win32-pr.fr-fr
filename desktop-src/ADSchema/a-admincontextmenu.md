---
title: Attribut de menu de contexte d’administration
description: Le numéro d’ordre et le GUID du menu contextuel à utiliser sur les écrans d’administration.
ms.assetid: da388bf3-1c44-4d34-b763-e45b784d3c9e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de menu contextuel d’administration
- Schéma AD de l’attribut adminContextMenu
topic_type:
- apiref
api_name:
- Admin-Context-Menu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 955267bf1e494d6bb0c98b3f5d25832896393ff2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844790"
---
# <a name="admin-context-menu-attribute"></a><span data-ttu-id="9e1c9-105">Attribut de menu de contexte d’administration</span><span class="sxs-lookup"><span data-stu-id="9e1c9-105">Admin-Context-Menu attribute</span></span>

<span data-ttu-id="9e1c9-106">Le numéro d’ordre et le GUID du menu contextuel à utiliser sur les écrans d’administration.</span><span class="sxs-lookup"><span data-stu-id="9e1c9-106">The order number and GUID of the context menu to be used on administration screens.</span></span>



| <span data-ttu-id="9e1c9-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-107">Entry</span></span> | <span data-ttu-id="9e1c9-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9e1c9-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e1c9-109">CN</span></span>                | <span data-ttu-id="9e1c9-110">Menu contextuel d’administration</span><span class="sxs-lookup"><span data-stu-id="9e1c9-110">Admin-Context-Menu</span></span>                          |
| <span data-ttu-id="9e1c9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9e1c9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e1c9-112">adminContextMenu</span><span class="sxs-lookup"><span data-stu-id="9e1c9-112">adminContextMenu</span></span>                            |
| <span data-ttu-id="9e1c9-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9e1c9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9e1c9-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9e1c9-114">Update Privilege</span></span>  | <span data-ttu-id="9e1c9-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="9e1c9-115">Domain administrator</span></span>                        |
| <span data-ttu-id="9e1c9-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9e1c9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9e1c9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-117">Attribute-Id</span></span>      | <span data-ttu-id="9e1c9-118">1.2.840.113556.1.4.614</span><span class="sxs-lookup"><span data-stu-id="9e1c9-118">1.2.840.113556.1.4.614</span></span>                      |
| <span data-ttu-id="9e1c9-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e1c9-119">System-Id-Guid</span></span>    | <span data-ttu-id="9e1c9-120">553fd038-f32e-11d0-b0bc-00c04fd8dca6</span><span class="sxs-lookup"><span data-stu-id="9e1c9-120">553fd038-f32e-11d0-b0bc-00c04fd8dca6</span></span>        |
| <span data-ttu-id="9e1c9-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e1c9-121">Syntax</span></span>            | [<span data-ttu-id="9e1c9-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9e1c9-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9e1c9-123">Implementations</span></span>

-   [<span data-ttu-id="9e1c9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e1c9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e1c9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e1c9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e1c9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e1c9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e1c9-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e1c9-130">Windows 2000 Server</span></span>



| <span data-ttu-id="9e1c9-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-131">Entry</span></span> | <span data-ttu-id="9e1c9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-135">System-Only</span></span>            | <span data-ttu-id="9e1c9-136">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-136">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-138">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-138">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-139">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-140">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-140">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-141">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-142">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-142">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-147">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-149">System-Flags</span></span>           | <span data-ttu-id="9e1c9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-151">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-152">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-152">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e1c9-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e1c9-153">Windows Server 2003</span></span>



| <span data-ttu-id="9e1c9-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-154">Entry</span></span> | <span data-ttu-id="9e1c9-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-158">System-Only</span></span>            | <span data-ttu-id="9e1c9-159">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-159">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-161">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-161">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-162">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-163">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-163">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-164">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-165">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-165">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-170">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-172">System-Flags</span></span>           | <span data-ttu-id="9e1c9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-174">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-175">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-175">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e1c9-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e1c9-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e1c9-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-177">Entry</span></span> | <span data-ttu-id="9e1c9-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-181">System-Only</span></span>            | <span data-ttu-id="9e1c9-182">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-182">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-184">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-184">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-185">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-186">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-186">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-187">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-188">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-188">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-193">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-195">System-Flags</span></span>           | <span data-ttu-id="9e1c9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-197">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-198">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-198">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e1c9-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e1c9-199">Windows Server 2008</span></span>



| <span data-ttu-id="9e1c9-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-200">Entry</span></span> | <span data-ttu-id="9e1c9-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-204">System-Only</span></span>            | <span data-ttu-id="9e1c9-205">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-205">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-207">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-207">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-208">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-209">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-209">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-210">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-211">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-211">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-216">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-218">System-Flags</span></span>           | <span data-ttu-id="9e1c9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-220">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-221">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-221">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e1c9-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e1c9-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e1c9-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-223">Entry</span></span> | <span data-ttu-id="9e1c9-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-227">System-Only</span></span>            | <span data-ttu-id="9e1c9-228">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-228">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-230">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-230">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-231">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-232">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-232">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-233">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-234">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-234">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-239">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-241">System-Flags</span></span>           | <span data-ttu-id="9e1c9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-243">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-244">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-244">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e1c9-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e1c9-245">Windows Server 2012</span></span>



| <span data-ttu-id="9e1c9-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e1c9-246">Entry</span></span> | <span data-ttu-id="9e1c9-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c9-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e1c9-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e1c9-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e1c9-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9e1c9-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e1c9-250">System-Only</span></span>            | <span data-ttu-id="9e1c9-251">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-251">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e1c9-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9e1c9-253">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-253">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e1c9-254">Is Indexed</span></span>             | <span data-ttu-id="9e1c9-255">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-255">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e1c9-256">In Global Catalog</span></span>      | <span data-ttu-id="9e1c9-257">Faux</span><span class="sxs-lookup"><span data-stu-id="9e1c9-257">False</span></span>                                                      |
| <span data-ttu-id="9e1c9-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e1c9-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e1c9-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e1c9-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9e1c9-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e1c9-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e1c9-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9e1c9-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-262">Search-Flags</span></span>           | <span data-ttu-id="9e1c9-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e1c9-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="9e1c9-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e1c9-264">System-Flags</span></span>           | <span data-ttu-id="9e1c9-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e1c9-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="9e1c9-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e1c9-266">Classes used in</span></span>        | [<span data-ttu-id="9e1c9-267">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="9e1c9-267">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





