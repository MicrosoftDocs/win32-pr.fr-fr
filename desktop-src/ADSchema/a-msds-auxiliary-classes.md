---
title: attribut ms-DS-auxiliaire-classes
description: Cet attribut répertorie les classes auxiliaires qui ont été attachées dynamiquement à un objet. Cet attribut n’est pas associé à une classe. Elle est automatiquement renseignée par le système.
ms.assetid: bf41f15d-9af9-43de-8425-33d50880c3fa
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-auxiliaire-classes
- Schéma AD de l’attribut msDS-auxiliaire-classes
topic_type:
- apiref
api_name:
- ms-DS-Auxiliary-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24608d0626ae4bcd6adb70a646d95121615c29e5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845182"
---
# <a name="ms-ds-auxiliary-classes-attribute"></a><span data-ttu-id="336b2-107">attribut ms-DS-auxiliaire-classes</span><span class="sxs-lookup"><span data-stu-id="336b2-107">ms-DS-Auxiliary-Classes attribute</span></span>

<span data-ttu-id="336b2-108">Cet attribut répertorie les classes auxiliaires qui ont été attachées dynamiquement à un objet.</span><span class="sxs-lookup"><span data-stu-id="336b2-108">This attribute lists the auxiliary classes that have been dynamically attached to an object.</span></span> <span data-ttu-id="336b2-109">Cet attribut n’est pas associé à une classe.</span><span class="sxs-lookup"><span data-stu-id="336b2-109">This attribute is not associated with a class.</span></span> <span data-ttu-id="336b2-110">Elle est automatiquement renseignée par le système.</span><span class="sxs-lookup"><span data-stu-id="336b2-110">It is automatically populated by the system.</span></span>



| <span data-ttu-id="336b2-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-111">Entry</span></span> | <span data-ttu-id="336b2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="336b2-113">CN</span><span class="sxs-lookup"><span data-stu-id="336b2-113">CN</span></span>                | <span data-ttu-id="336b2-114">ms-DS-auxiliaire-classes</span><span class="sxs-lookup"><span data-stu-id="336b2-114">ms-DS-Auxiliary-Classes</span></span>                                         |
| <span data-ttu-id="336b2-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="336b2-115">Ldap-Display-Name</span></span> | <span data-ttu-id="336b2-116">msDS-auxiliaire-classes</span><span class="sxs-lookup"><span data-stu-id="336b2-116">msDS-Auxiliary-Classes</span></span>                                          |
| <span data-ttu-id="336b2-117">Taille</span><span class="sxs-lookup"><span data-stu-id="336b2-117">Size</span></span>              | \-                                                              |
| <span data-ttu-id="336b2-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="336b2-118">Update Privilege</span></span>  | <span data-ttu-id="336b2-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="336b2-119">This value is set by the system.</span></span>                                |
| <span data-ttu-id="336b2-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="336b2-120">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="336b2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-121">Attribute-Id</span></span>      | <span data-ttu-id="336b2-122">1.2.840.113556.1.4.1458</span><span class="sxs-lookup"><span data-stu-id="336b2-122">1.2.840.113556.1.4.1458</span></span>                                         |
| <span data-ttu-id="336b2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="336b2-123">System-Id-Guid</span></span>    | <span data-ttu-id="336b2-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span><span class="sxs-lookup"><span data-stu-id="336b2-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span></span>                            |
| <span data-ttu-id="336b2-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="336b2-125">Syntax</span></span>            | [<span data-ttu-id="336b2-126">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="336b2-126">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="336b2-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="336b2-127">Implementations</span></span>

-   [<span data-ttu-id="336b2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="336b2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="336b2-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="336b2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="336b2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="336b2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="336b2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="336b2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="336b2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="336b2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="336b2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="336b2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="336b2-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="336b2-134">Windows Server 2003</span></span>



| <span data-ttu-id="336b2-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-135">Entry</span></span> | <span data-ttu-id="336b2-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-136">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-137">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-138">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-139">System-Only</span></span>            | <span data-ttu-id="336b2-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-140">True</span></span>         |
| <span data-ttu-id="336b2-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-142">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-142">False</span></span>        |
| <span data-ttu-id="336b2-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-143">Is Indexed</span></span>             | <span data-ttu-id="336b2-144">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-144">False</span></span>        |
| <span data-ttu-id="336b2-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-145">In Global Catalog</span></span>      | <span data-ttu-id="336b2-146">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-146">False</span></span>        |
| <span data-ttu-id="336b2-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-148">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-149">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-150">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-151">Search-Flags</span></span>           | <span data-ttu-id="336b2-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-152">0x00000008</span></span>   |
| <span data-ttu-id="336b2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-153">System-Flags</span></span>           | <span data-ttu-id="336b2-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-154">0x00000014</span></span>   |
| <span data-ttu-id="336b2-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-155">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="336b2-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="336b2-156">ADAM</span></span>



| <span data-ttu-id="336b2-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-157">Entry</span></span> | <span data-ttu-id="336b2-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-158">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-159">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-160">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-161">System-Only</span></span>            | <span data-ttu-id="336b2-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-162">True</span></span>         |
| <span data-ttu-id="336b2-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-164">False</span></span>        |
| <span data-ttu-id="336b2-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-165">Is Indexed</span></span>             | <span data-ttu-id="336b2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-166">False</span></span>        |
| <span data-ttu-id="336b2-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-167">In Global Catalog</span></span>      | <span data-ttu-id="336b2-168">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-168">False</span></span>        |
| <span data-ttu-id="336b2-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-171">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-172">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-173">Search-Flags</span></span>           | <span data-ttu-id="336b2-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-174">0x00000008</span></span>   |
| <span data-ttu-id="336b2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-175">System-Flags</span></span>           | <span data-ttu-id="336b2-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-176">0x00000014</span></span>   |
| <span data-ttu-id="336b2-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-177">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="336b2-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="336b2-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="336b2-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-179">Entry</span></span> | <span data-ttu-id="336b2-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-183">System-Only</span></span>            | <span data-ttu-id="336b2-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-184">True</span></span>         |
| <span data-ttu-id="336b2-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-185">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-186">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-186">False</span></span>        |
| <span data-ttu-id="336b2-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-187">Is Indexed</span></span>             | <span data-ttu-id="336b2-188">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-188">False</span></span>        |
| <span data-ttu-id="336b2-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-189">In Global Catalog</span></span>      | <span data-ttu-id="336b2-190">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-190">False</span></span>        |
| <span data-ttu-id="336b2-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-195">Search-Flags</span></span>           | <span data-ttu-id="336b2-196">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-196">0x00000008</span></span>   |
| <span data-ttu-id="336b2-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-197">System-Flags</span></span>           | <span data-ttu-id="336b2-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-198">0x00000014</span></span>   |
| <span data-ttu-id="336b2-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="336b2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="336b2-200">Windows Server 2008</span></span>



| <span data-ttu-id="336b2-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-201">Entry</span></span> | <span data-ttu-id="336b2-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-202">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-203">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-204">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-205">System-Only</span></span>            | <span data-ttu-id="336b2-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-206">True</span></span>         |
| <span data-ttu-id="336b2-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-208">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-208">False</span></span>        |
| <span data-ttu-id="336b2-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-209">Is Indexed</span></span>             | <span data-ttu-id="336b2-210">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-210">False</span></span>        |
| <span data-ttu-id="336b2-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-211">In Global Catalog</span></span>      | <span data-ttu-id="336b2-212">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-212">False</span></span>        |
| <span data-ttu-id="336b2-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-214">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-215">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-216">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-217">Search-Flags</span></span>           | <span data-ttu-id="336b2-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-218">0x00000008</span></span>   |
| <span data-ttu-id="336b2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-219">System-Flags</span></span>           | <span data-ttu-id="336b2-220">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-220">0x00000014</span></span>   |
| <span data-ttu-id="336b2-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-221">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="336b2-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="336b2-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="336b2-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-223">Entry</span></span> | <span data-ttu-id="336b2-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-224">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-225">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-227">System-Only</span></span>            | <span data-ttu-id="336b2-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-228">True</span></span>         |
| <span data-ttu-id="336b2-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-230">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-230">False</span></span>        |
| <span data-ttu-id="336b2-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-231">Is Indexed</span></span>             | <span data-ttu-id="336b2-232">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-232">False</span></span>        |
| <span data-ttu-id="336b2-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-233">In Global Catalog</span></span>      | <span data-ttu-id="336b2-234">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-234">False</span></span>        |
| <span data-ttu-id="336b2-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-239">Search-Flags</span></span>           | <span data-ttu-id="336b2-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-240">0x00000008</span></span>   |
| <span data-ttu-id="336b2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-241">System-Flags</span></span>           | <span data-ttu-id="336b2-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-242">0x00000014</span></span>   |
| <span data-ttu-id="336b2-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="336b2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="336b2-244">Windows Server 2012</span></span>



| <span data-ttu-id="336b2-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="336b2-245">Entry</span></span> | <span data-ttu-id="336b2-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="336b2-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="336b2-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="336b2-247">Link-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="336b2-248">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="336b2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="336b2-249">System-Only</span></span>            | <span data-ttu-id="336b2-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="336b2-250">True</span></span>         |
| <span data-ttu-id="336b2-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="336b2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="336b2-252">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-252">False</span></span>        |
| <span data-ttu-id="336b2-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="336b2-253">Is Indexed</span></span>             | <span data-ttu-id="336b2-254">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-254">False</span></span>        |
| <span data-ttu-id="336b2-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="336b2-255">In Global Catalog</span></span>      | <span data-ttu-id="336b2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="336b2-256">False</span></span>        |
| <span data-ttu-id="336b2-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="336b2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="336b2-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="336b2-258">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="336b2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="336b2-259">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="336b2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="336b2-260">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="336b2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-261">Search-Flags</span></span>           | <span data-ttu-id="336b2-262">0x00000008</span><span class="sxs-lookup"><span data-stu-id="336b2-262">0x00000008</span></span>   |
| <span data-ttu-id="336b2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="336b2-263">System-Flags</span></span>           | <span data-ttu-id="336b2-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="336b2-264">0x00000014</span></span>   |
| <span data-ttu-id="336b2-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="336b2-265">Classes used in</span></span>        | \-           |



 

 




