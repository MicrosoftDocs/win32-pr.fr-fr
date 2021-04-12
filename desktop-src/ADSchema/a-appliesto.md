---
title: Attribut Applies-To
description: Contient la liste des classes d’objets auxquelles s’applique le droit étendu. Dans la liste, une classe d’objet est représentée par la propriété schemaIDGUID pour son objet schemaClass.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Applies-To
- Schéma AD d’attribut appliesTo
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108299"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="ac96d-106">Attribut Applies-To</span><span class="sxs-lookup"><span data-stu-id="ac96d-106">Applies-To attribute</span></span>

<span data-ttu-id="ac96d-107">Contient la liste des classes d’objets auxquelles s’applique le droit étendu.</span><span class="sxs-lookup"><span data-stu-id="ac96d-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="ac96d-108">Dans la liste, une classe d’objet est représentée par la propriété schemaIDGUID pour son objet schemaClass.</span><span class="sxs-lookup"><span data-stu-id="ac96d-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="ac96d-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-109">Entry</span></span> | <span data-ttu-id="ac96d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ac96d-111">CN</span><span class="sxs-lookup"><span data-stu-id="ac96d-111">CN</span></span>                | <span data-ttu-id="ac96d-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ac96d-112">Applies-To</span></span>                                  |
| <span data-ttu-id="ac96d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ac96d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ac96d-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="ac96d-114">appliesTo</span></span>                                   |
| <span data-ttu-id="ac96d-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ac96d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ac96d-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ac96d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ac96d-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ac96d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ac96d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-118">Attribute-Id</span></span>      | <span data-ttu-id="ac96d-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="ac96d-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="ac96d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac96d-120">System-Id-Guid</span></span>    | <span data-ttu-id="ac96d-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ac96d-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="ac96d-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac96d-122">Syntax</span></span>            | [<span data-ttu-id="ac96d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ac96d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ac96d-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ac96d-124">Implementations</span></span>

-   [<span data-ttu-id="ac96d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac96d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac96d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac96d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac96d-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ac96d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ac96d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac96d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac96d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac96d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac96d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac96d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac96d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac96d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac96d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac96d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ac96d-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-133">Entry</span></span> | <span data-ttu-id="ac96d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-137">System-Only</span></span>            | <span data-ttu-id="ac96d-138">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-138">False</span></span>                                                           |
| <span data-ttu-id="ac96d-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-140">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-140">False</span></span>                                                           |
| <span data-ttu-id="ac96d-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-141">Is Indexed</span></span>             | <span data-ttu-id="ac96d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-142">False</span></span>                                                           |
| <span data-ttu-id="ac96d-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-143">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-144">False</span></span>                                                           |
| <span data-ttu-id="ac96d-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-147">Range-Lower</span></span>            | <span data-ttu-id="ac96d-148">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-148">36</span></span>                                                              |
| <span data-ttu-id="ac96d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-149">Range-Upper</span></span>            | <span data-ttu-id="ac96d-150">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-150">36</span></span>                                                              |
| <span data-ttu-id="ac96d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-151">Search-Flags</span></span>           | <span data-ttu-id="ac96d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-153">System-Flags</span></span>           | <span data-ttu-id="ac96d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-155">Classes used in</span></span>        | [<span data-ttu-id="ac96d-156">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac96d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac96d-157">Windows Server 2003</span></span>



| <span data-ttu-id="ac96d-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-158">Entry</span></span> | <span data-ttu-id="ac96d-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-162">System-Only</span></span>            | <span data-ttu-id="ac96d-163">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-163">False</span></span>                                                           |
| <span data-ttu-id="ac96d-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-165">False</span></span>                                                           |
| <span data-ttu-id="ac96d-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-166">Is Indexed</span></span>             | <span data-ttu-id="ac96d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-167">False</span></span>                                                           |
| <span data-ttu-id="ac96d-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-168">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-169">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-169">False</span></span>                                                           |
| <span data-ttu-id="ac96d-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-172">Range-Lower</span></span>            | <span data-ttu-id="ac96d-173">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-173">36</span></span>                                                              |
| <span data-ttu-id="ac96d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-174">Range-Upper</span></span>            | <span data-ttu-id="ac96d-175">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-175">36</span></span>                                                              |
| <span data-ttu-id="ac96d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-176">Search-Flags</span></span>           | <span data-ttu-id="ac96d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-178">System-Flags</span></span>           | <span data-ttu-id="ac96d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-180">Classes used in</span></span>        | [<span data-ttu-id="ac96d-181">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ac96d-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="ac96d-182">ADAM</span></span>



| <span data-ttu-id="ac96d-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-183">Entry</span></span> | <span data-ttu-id="ac96d-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-187">System-Only</span></span>            | <span data-ttu-id="ac96d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-188">False</span></span>                                                           |
| <span data-ttu-id="ac96d-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-190">False</span></span>                                                           |
| <span data-ttu-id="ac96d-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-191">Is Indexed</span></span>             | <span data-ttu-id="ac96d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-192">False</span></span>                                                           |
| <span data-ttu-id="ac96d-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-193">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-194">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-194">False</span></span>                                                           |
| <span data-ttu-id="ac96d-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-197">Range-Lower</span></span>            | <span data-ttu-id="ac96d-198">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-198">36</span></span>                                                              |
| <span data-ttu-id="ac96d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-199">Range-Upper</span></span>            | <span data-ttu-id="ac96d-200">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-200">36</span></span>                                                              |
| <span data-ttu-id="ac96d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-201">Search-Flags</span></span>           | <span data-ttu-id="ac96d-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-203">System-Flags</span></span>           | <span data-ttu-id="ac96d-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-205">Classes used in</span></span>        | [<span data-ttu-id="ac96d-206">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac96d-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac96d-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac96d-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-208">Entry</span></span> | <span data-ttu-id="ac96d-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-212">System-Only</span></span>            | <span data-ttu-id="ac96d-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-213">False</span></span>                                                           |
| <span data-ttu-id="ac96d-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-215">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-215">False</span></span>                                                           |
| <span data-ttu-id="ac96d-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-216">Is Indexed</span></span>             | <span data-ttu-id="ac96d-217">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-217">False</span></span>                                                           |
| <span data-ttu-id="ac96d-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-218">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-219">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-219">False</span></span>                                                           |
| <span data-ttu-id="ac96d-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-222">Range-Lower</span></span>            | <span data-ttu-id="ac96d-223">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-223">36</span></span>                                                              |
| <span data-ttu-id="ac96d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-224">Range-Upper</span></span>            | <span data-ttu-id="ac96d-225">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-225">36</span></span>                                                              |
| <span data-ttu-id="ac96d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-226">Search-Flags</span></span>           | <span data-ttu-id="ac96d-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-228">System-Flags</span></span>           | <span data-ttu-id="ac96d-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-230">Classes used in</span></span>        | [<span data-ttu-id="ac96d-231">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac96d-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac96d-232">Windows Server 2008</span></span>



| <span data-ttu-id="ac96d-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-233">Entry</span></span> | <span data-ttu-id="ac96d-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-237">System-Only</span></span>            | <span data-ttu-id="ac96d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-238">False</span></span>                                                           |
| <span data-ttu-id="ac96d-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-240">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-240">False</span></span>                                                           |
| <span data-ttu-id="ac96d-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-241">Is Indexed</span></span>             | <span data-ttu-id="ac96d-242">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-242">False</span></span>                                                           |
| <span data-ttu-id="ac96d-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-243">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-244">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-244">False</span></span>                                                           |
| <span data-ttu-id="ac96d-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-247">Range-Lower</span></span>            | <span data-ttu-id="ac96d-248">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-248">36</span></span>                                                              |
| <span data-ttu-id="ac96d-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-249">Range-Upper</span></span>            | <span data-ttu-id="ac96d-250">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-250">36</span></span>                                                              |
| <span data-ttu-id="ac96d-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-251">Search-Flags</span></span>           | <span data-ttu-id="ac96d-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-253">System-Flags</span></span>           | <span data-ttu-id="ac96d-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-255">Classes used in</span></span>        | [<span data-ttu-id="ac96d-256">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac96d-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac96d-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac96d-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-258">Entry</span></span> | <span data-ttu-id="ac96d-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-262">System-Only</span></span>            | <span data-ttu-id="ac96d-263">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-263">False</span></span>                                                           |
| <span data-ttu-id="ac96d-264">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-265">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-265">False</span></span>                                                           |
| <span data-ttu-id="ac96d-266">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-266">Is Indexed</span></span>             | <span data-ttu-id="ac96d-267">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-267">False</span></span>                                                           |
| <span data-ttu-id="ac96d-268">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-268">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-269">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-269">False</span></span>                                                           |
| <span data-ttu-id="ac96d-270">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-271">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-272">Range-Lower</span></span>            | <span data-ttu-id="ac96d-273">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-273">36</span></span>                                                              |
| <span data-ttu-id="ac96d-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-274">Range-Upper</span></span>            | <span data-ttu-id="ac96d-275">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-275">36</span></span>                                                              |
| <span data-ttu-id="ac96d-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-276">Search-Flags</span></span>           | <span data-ttu-id="ac96d-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-278">System-Flags</span></span>           | <span data-ttu-id="ac96d-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-280">Classes used in</span></span>        | [<span data-ttu-id="ac96d-281">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac96d-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac96d-282">Windows Server 2012</span></span>



| <span data-ttu-id="ac96d-283">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac96d-283">Entry</span></span> | <span data-ttu-id="ac96d-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac96d-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ac96d-285">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac96d-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac96d-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="ac96d-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac96d-287">System-Only</span></span>            | <span data-ttu-id="ac96d-288">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-288">False</span></span>                                                           |
| <span data-ttu-id="ac96d-289">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac96d-289">Is-Single-Valued</span></span>       | <span data-ttu-id="ac96d-290">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-290">False</span></span>                                                           |
| <span data-ttu-id="ac96d-291">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac96d-291">Is Indexed</span></span>             | <span data-ttu-id="ac96d-292">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-292">False</span></span>                                                           |
| <span data-ttu-id="ac96d-293">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac96d-293">In Global Catalog</span></span>      | <span data-ttu-id="ac96d-294">Faux</span><span class="sxs-lookup"><span data-stu-id="ac96d-294">False</span></span>                                                           |
| <span data-ttu-id="ac96d-295">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac96d-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac96d-296">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac96d-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="ac96d-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac96d-297">Range-Lower</span></span>            | <span data-ttu-id="ac96d-298">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-298">36</span></span>                                                              |
| <span data-ttu-id="ac96d-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac96d-299">Range-Upper</span></span>            | <span data-ttu-id="ac96d-300">36</span><span class="sxs-lookup"><span data-stu-id="ac96d-300">36</span></span>                                                              |
| <span data-ttu-id="ac96d-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-301">Search-Flags</span></span>           | <span data-ttu-id="ac96d-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac96d-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="ac96d-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac96d-303">System-Flags</span></span>           | <span data-ttu-id="ac96d-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac96d-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="ac96d-305">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac96d-305">Classes used in</span></span>        | [<span data-ttu-id="ac96d-306">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="ac96d-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





