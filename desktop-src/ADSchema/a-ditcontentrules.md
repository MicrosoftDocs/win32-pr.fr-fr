---
title: DIT-content-Rules (attribut)
description: Cela spécifie le contenu autorisé des entrées d’une classe d’objets structurels particulière à l’aide de l’identification d’un ensemble facultatif de classes d’objets auxiliaires, ainsi que des attributs obligatoires, facultatifs et interdits.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut DIT-content-Rules
- Schéma AD de l’attribut dITContentRules
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108223"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="4ae87-105">DIT-content-Rules (attribut)</span><span class="sxs-lookup"><span data-stu-id="4ae87-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="4ae87-106">Cela spécifie le contenu autorisé des entrées d’une classe d’objets structurels particulière à l’aide de l’identification d’un ensemble facultatif de classes d’objets auxiliaires, ainsi que des attributs obligatoires, facultatifs et interdits.</span><span class="sxs-lookup"><span data-stu-id="4ae87-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="4ae87-107">Les attributs collectifs sont inclus dans DIT-content-Rules, comme défini dans la norme RFC 2251.</span><span class="sxs-lookup"><span data-stu-id="4ae87-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="4ae87-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-108">Entry</span></span> | <span data-ttu-id="4ae87-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-110">CN</span><span class="sxs-lookup"><span data-stu-id="4ae87-110">CN</span></span>                | <span data-ttu-id="4ae87-111">DIT-content-Rules</span><span class="sxs-lookup"><span data-stu-id="4ae87-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="4ae87-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4ae87-112">Ldap-Display-Name</span></span> | <span data-ttu-id="4ae87-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="4ae87-113">dITContentRules</span></span>                             |
| <span data-ttu-id="4ae87-114">Taille</span><span class="sxs-lookup"><span data-stu-id="4ae87-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="4ae87-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4ae87-115">Update Privilege</span></span>  | <span data-ttu-id="4ae87-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="4ae87-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="4ae87-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4ae87-117">Update Frequency</span></span>  | <span data-ttu-id="4ae87-118">Chaque fois qu’une nouvelle classe est créée.</span><span class="sxs-lookup"><span data-stu-id="4ae87-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="4ae87-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-119">Attribute-Id</span></span>      | <span data-ttu-id="4ae87-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="4ae87-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="4ae87-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4ae87-121">System-Id-Guid</span></span>    | <span data-ttu-id="4ae87-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="4ae87-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="4ae87-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ae87-123">Syntax</span></span>            | [<span data-ttu-id="4ae87-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4ae87-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4ae87-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4ae87-125">Implementations</span></span>

-   [<span data-ttu-id="4ae87-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ae87-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ae87-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ae87-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ae87-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4ae87-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4ae87-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ae87-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ae87-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ae87-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ae87-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ae87-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ae87-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ae87-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ae87-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ae87-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4ae87-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-134">Entry</span></span> | <span data-ttu-id="4ae87-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-138">System-Only</span></span>            | <span data-ttu-id="4ae87-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-139">True</span></span>                                        |
| <span data-ttu-id="4ae87-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-140">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-141">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-141">False</span></span>                                       |
| <span data-ttu-id="4ae87-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-142">Is Indexed</span></span>             | <span data-ttu-id="4ae87-143">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-143">False</span></span>                                       |
| <span data-ttu-id="4ae87-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-144">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-145">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-145">False</span></span>                                       |
| <span data-ttu-id="4ae87-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-150">Search-Flags</span></span>           | <span data-ttu-id="4ae87-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-151">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-152">System-Flags</span></span>           | <span data-ttu-id="4ae87-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-153">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-154">Classes used in</span></span>        | [<span data-ttu-id="4ae87-155">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ae87-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ae87-156">Windows Server 2003</span></span>



| <span data-ttu-id="4ae87-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-157">Entry</span></span> | <span data-ttu-id="4ae87-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-161">System-Only</span></span>            | <span data-ttu-id="4ae87-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-162">True</span></span>                                        |
| <span data-ttu-id="4ae87-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-164">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-164">False</span></span>                                       |
| <span data-ttu-id="4ae87-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-165">Is Indexed</span></span>             | <span data-ttu-id="4ae87-166">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-166">False</span></span>                                       |
| <span data-ttu-id="4ae87-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-167">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-168">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-168">False</span></span>                                       |
| <span data-ttu-id="4ae87-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-173">Search-Flags</span></span>           | <span data-ttu-id="4ae87-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-174">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-175">System-Flags</span></span>           | <span data-ttu-id="4ae87-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-176">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-177">Classes used in</span></span>        | [<span data-ttu-id="4ae87-178">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4ae87-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="4ae87-179">ADAM</span></span>



| <span data-ttu-id="4ae87-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-180">Entry</span></span> | <span data-ttu-id="4ae87-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-184">System-Only</span></span>            | <span data-ttu-id="4ae87-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-185">True</span></span>                                        |
| <span data-ttu-id="4ae87-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-187">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-187">False</span></span>                                       |
| <span data-ttu-id="4ae87-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-188">Is Indexed</span></span>             | <span data-ttu-id="4ae87-189">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-189">False</span></span>                                       |
| <span data-ttu-id="4ae87-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-190">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-191">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-191">False</span></span>                                       |
| <span data-ttu-id="4ae87-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-196">Search-Flags</span></span>           | <span data-ttu-id="4ae87-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-197">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-198">System-Flags</span></span>           | <span data-ttu-id="4ae87-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-199">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-200">Classes used in</span></span>        | [<span data-ttu-id="4ae87-201">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ae87-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ae87-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ae87-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-203">Entry</span></span> | <span data-ttu-id="4ae87-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-207">System-Only</span></span>            | <span data-ttu-id="4ae87-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-208">True</span></span>                                        |
| <span data-ttu-id="4ae87-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-209">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-210">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-210">False</span></span>                                       |
| <span data-ttu-id="4ae87-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-211">Is Indexed</span></span>             | <span data-ttu-id="4ae87-212">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-212">False</span></span>                                       |
| <span data-ttu-id="4ae87-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-213">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-214">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-214">False</span></span>                                       |
| <span data-ttu-id="4ae87-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-219">Search-Flags</span></span>           | <span data-ttu-id="4ae87-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-220">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-221">System-Flags</span></span>           | <span data-ttu-id="4ae87-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-222">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-223">Classes used in</span></span>        | [<span data-ttu-id="4ae87-224">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ae87-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ae87-225">Windows Server 2008</span></span>



| <span data-ttu-id="4ae87-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-226">Entry</span></span> | <span data-ttu-id="4ae87-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-230">System-Only</span></span>            | <span data-ttu-id="4ae87-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-231">True</span></span>                                        |
| <span data-ttu-id="4ae87-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-232">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-233">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-233">False</span></span>                                       |
| <span data-ttu-id="4ae87-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-234">Is Indexed</span></span>             | <span data-ttu-id="4ae87-235">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-235">False</span></span>                                       |
| <span data-ttu-id="4ae87-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-236">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-237">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-237">False</span></span>                                       |
| <span data-ttu-id="4ae87-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-242">Search-Flags</span></span>           | <span data-ttu-id="4ae87-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-243">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-244">System-Flags</span></span>           | <span data-ttu-id="4ae87-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-245">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-246">Classes used in</span></span>        | [<span data-ttu-id="4ae87-247">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ae87-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ae87-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ae87-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-249">Entry</span></span> | <span data-ttu-id="4ae87-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-253">System-Only</span></span>            | <span data-ttu-id="4ae87-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-254">True</span></span>                                        |
| <span data-ttu-id="4ae87-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-255">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-256">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-256">False</span></span>                                       |
| <span data-ttu-id="4ae87-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-257">Is Indexed</span></span>             | <span data-ttu-id="4ae87-258">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-258">False</span></span>                                       |
| <span data-ttu-id="4ae87-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-259">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-260">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-260">False</span></span>                                       |
| <span data-ttu-id="4ae87-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-265">Search-Flags</span></span>           | <span data-ttu-id="4ae87-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-266">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-267">System-Flags</span></span>           | <span data-ttu-id="4ae87-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-268">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-269">Classes used in</span></span>        | [<span data-ttu-id="4ae87-270">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ae87-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ae87-271">Windows Server 2012</span></span>



| <span data-ttu-id="4ae87-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="4ae87-272">Entry</span></span> | <span data-ttu-id="4ae87-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae87-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4ae87-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4ae87-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ae87-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4ae87-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ae87-276">System-Only</span></span>            | <span data-ttu-id="4ae87-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="4ae87-277">True</span></span>                                        |
| <span data-ttu-id="4ae87-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4ae87-278">Is-Single-Valued</span></span>       | <span data-ttu-id="4ae87-279">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-279">False</span></span>                                       |
| <span data-ttu-id="4ae87-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4ae87-280">Is Indexed</span></span>             | <span data-ttu-id="4ae87-281">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-281">False</span></span>                                       |
| <span data-ttu-id="4ae87-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4ae87-282">In Global Catalog</span></span>      | <span data-ttu-id="4ae87-283">Faux</span><span class="sxs-lookup"><span data-stu-id="4ae87-283">False</span></span>                                       |
| <span data-ttu-id="4ae87-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4ae87-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ae87-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4ae87-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4ae87-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ae87-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ae87-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4ae87-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-288">Search-Flags</span></span>           | <span data-ttu-id="4ae87-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ae87-289">0x00000000</span></span>                                  |
| <span data-ttu-id="4ae87-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ae87-290">System-Flags</span></span>           | <span data-ttu-id="4ae87-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4ae87-291">0x08000014</span></span>                                  |
| <span data-ttu-id="4ae87-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4ae87-292">Classes used in</span></span>        | [<span data-ttu-id="4ae87-293">**Sous-schéma**</span><span class="sxs-lookup"><span data-stu-id="4ae87-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





