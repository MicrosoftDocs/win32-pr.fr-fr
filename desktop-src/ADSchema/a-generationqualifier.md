---
title: Attribut Generation-Qualifier
description: Indique la génération d’une personne. Par exemple, Jr. ou II.
ms.assetid: 6b882114-3273-43ff-8df3-5b23c98a2dae
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Generation-Qualifier
- Schéma AD de l’attribut generationQualifier
topic_type:
- apiref
api_name:
- Generation-Qualifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc29fdc6bc32273113c5daab2482465535dee145
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515711"
---
# <a name="generation-qualifier-attribute"></a><span data-ttu-id="c9fb8-106">Attribut Generation-Qualifier</span><span class="sxs-lookup"><span data-stu-id="c9fb8-106">Generation-Qualifier attribute</span></span>

<span data-ttu-id="c9fb8-107">Indique la génération d’une personne.</span><span class="sxs-lookup"><span data-stu-id="c9fb8-107">Indicates a person generation.</span></span> <span data-ttu-id="c9fb8-108">Par exemple, Jr. ou II.</span><span class="sxs-lookup"><span data-stu-id="c9fb8-108">For example, Jr. or II.</span></span>



| <span data-ttu-id="c9fb8-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-109">Entry</span></span> | <span data-ttu-id="c9fb8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9fb8-111">CN</span><span class="sxs-lookup"><span data-stu-id="c9fb8-111">CN</span></span>                | <span data-ttu-id="c9fb8-112">Generation-Qualifier</span><span class="sxs-lookup"><span data-stu-id="c9fb8-112">Generation-Qualifier</span></span>                        |
| <span data-ttu-id="c9fb8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9fb8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c9fb8-114">generationQualifier</span><span class="sxs-lookup"><span data-stu-id="c9fb8-114">generationQualifier</span></span>                         |
| <span data-ttu-id="c9fb8-115">Taille</span><span class="sxs-lookup"><span data-stu-id="c9fb8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9fb8-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c9fb8-116">Update Privilege</span></span>  | <span data-ttu-id="c9fb8-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="c9fb8-117">Domain Administrator</span></span>                        |
| <span data-ttu-id="c9fb8-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c9fb8-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c9fb8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-119">Attribute-Id</span></span>      | <span data-ttu-id="c9fb8-120">2.5.4.44</span><span class="sxs-lookup"><span data-stu-id="c9fb8-120">2.5.4.44</span></span>                                    |
| <span data-ttu-id="c9fb8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9fb8-121">System-Id-Guid</span></span>    | <span data-ttu-id="c9fb8-122">16775804-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-122">16775804-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="c9fb8-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9fb8-123">Syntax</span></span>            | [<span data-ttu-id="c9fb8-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9fb8-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c9fb8-125">Implementations</span></span>

-   [<span data-ttu-id="c9fb8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9fb8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9fb8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9fb8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9fb8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9fb8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9fb8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9fb8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c9fb8-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-133">Entry</span></span> | <span data-ttu-id="c9fb8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-136">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-137">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-137">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-138">System-Only</span></span>            | <span data-ttu-id="c9fb8-139">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-139">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-141">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-142">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-143">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-143">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-144">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-145">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-145">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-148">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-149">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-149">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-150">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-151">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-151">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-152">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-154">System-Flags</span></span>           | <span data-ttu-id="c9fb8-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-156">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9fb8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9fb8-158">Windows Server 2003</span></span>



| <span data-ttu-id="c9fb8-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-159">Entry</span></span> | <span data-ttu-id="c9fb8-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-160">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-161">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-162">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-163">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-163">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-164">System-Only</span></span>            | <span data-ttu-id="c9fb8-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-165">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-167">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-168">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-169">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-169">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-170">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-171">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-171">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-173">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-174">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-175">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-175">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-176">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-177">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-177">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-178">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-179">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-180">System-Flags</span></span>           | <span data-ttu-id="c9fb8-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-181">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-182">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9fb8-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9fb8-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9fb8-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-185">Entry</span></span> | <span data-ttu-id="c9fb8-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-186">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-187">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-188">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-189">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-189">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-190">System-Only</span></span>            | <span data-ttu-id="c9fb8-191">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-191">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-192">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-192">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-193">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-194">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-194">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-195">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-195">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-196">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-196">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-197">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-197">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-198">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-199">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-199">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-200">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-201">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-201">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-202">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-203">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-203">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-204">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-205">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-206">System-Flags</span></span>           | <span data-ttu-id="c9fb8-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-207">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-208">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9fb8-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9fb8-210">Windows Server 2008</span></span>



| <span data-ttu-id="c9fb8-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-211">Entry</span></span> | <span data-ttu-id="c9fb8-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-213">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-214">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-215">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-215">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-216">System-Only</span></span>            | <span data-ttu-id="c9fb8-217">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-217">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-218">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-218">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-219">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-220">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-220">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-221">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-221">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-222">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-222">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-223">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-223">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-224">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-225">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-225">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-226">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-227">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-227">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-228">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-229">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-229">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-230">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-231">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-232">System-Flags</span></span>           | <span data-ttu-id="c9fb8-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-233">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-234">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-234">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9fb8-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9fb8-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9fb8-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-237">Entry</span></span> | <span data-ttu-id="c9fb8-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-238">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-239">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-240">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-241">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-241">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-242">System-Only</span></span>            | <span data-ttu-id="c9fb8-243">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-243">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-244">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-244">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-245">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-245">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-246">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-246">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-247">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-247">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-248">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-248">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-249">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-249">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-250">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-251">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-251">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-252">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-253">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-253">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-254">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-255">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-255">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-256">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-257">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-258">System-Flags</span></span>           | <span data-ttu-id="c9fb8-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-259">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-260">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9fb8-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9fb8-262">Windows Server 2012</span></span>



| <span data-ttu-id="c9fb8-263">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9fb8-263">Entry</span></span> | <span data-ttu-id="c9fb8-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fb8-264">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9fb8-265">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9fb8-265">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9fb8-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9fb8-266">MAPI-Id</span></span>                | <span data-ttu-id="c9fb8-267">0x8C53</span><span class="sxs-lookup"><span data-stu-id="c9fb8-267">0x8C53</span></span>                                                             |
| <span data-ttu-id="c9fb8-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9fb8-268">System-Only</span></span>            | <span data-ttu-id="c9fb8-269">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-269">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-270">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9fb8-270">Is-Single-Valued</span></span>       | <span data-ttu-id="c9fb8-271">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9fb8-271">True</span></span>                                                               |
| <span data-ttu-id="c9fb8-272">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9fb8-272">Is Indexed</span></span>             | <span data-ttu-id="c9fb8-273">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-273">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-274">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9fb8-274">In Global Catalog</span></span>      | <span data-ttu-id="c9fb8-275">Faux</span><span class="sxs-lookup"><span data-stu-id="c9fb8-275">False</span></span>                                                              |
| <span data-ttu-id="c9fb8-276">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9fb8-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9fb8-277">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9fb8-277">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9fb8-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9fb8-278">Range-Lower</span></span>            | <span data-ttu-id="c9fb8-279">1</span><span class="sxs-lookup"><span data-stu-id="c9fb8-279">1</span></span>                                                                  |
| <span data-ttu-id="c9fb8-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9fb8-280">Range-Upper</span></span>            | <span data-ttu-id="c9fb8-281">64</span><span class="sxs-lookup"><span data-stu-id="c9fb8-281">64</span></span>                                                                 |
| <span data-ttu-id="c9fb8-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-282">Search-Flags</span></span>           | <span data-ttu-id="c9fb8-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9fb8-283">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9fb8-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9fb8-284">System-Flags</span></span>           | <span data-ttu-id="c9fb8-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9fb8-285">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9fb8-286">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9fb8-286">Classes used in</span></span>        | [<span data-ttu-id="c9fb8-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9fb8-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





