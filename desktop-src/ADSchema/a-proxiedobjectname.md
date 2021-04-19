---
title: Proxyd-Object-Name (attribut)
description: Cet attribut est utilisé en interne par Active Directory pour faciliter le suivi des déplacements interdomaines.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Schéma ADd-Object-Name (attribut de nom)
- Schéma AD de l’attribut proxiedObjectName
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106530814"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="01432-105">Proxyd-Object-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="01432-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="01432-106">Cet attribut est utilisé en interne par Active Directory pour faciliter le suivi des déplacements interdomaines.</span><span class="sxs-lookup"><span data-stu-id="01432-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="01432-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-107">Entry</span></span> | <span data-ttu-id="01432-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="01432-109">CN</span><span class="sxs-lookup"><span data-stu-id="01432-109">CN</span></span>                | <span data-ttu-id="01432-110">Proxyd-Object-Name</span><span class="sxs-lookup"><span data-stu-id="01432-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="01432-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="01432-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01432-112">proxiedObjectName</span><span class="sxs-lookup"><span data-stu-id="01432-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="01432-113">Taille</span><span class="sxs-lookup"><span data-stu-id="01432-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="01432-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="01432-114">Update Privilege</span></span>  | <span data-ttu-id="01432-115">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="01432-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="01432-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="01432-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="01432-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01432-117">Attribute-Id</span></span>      | <span data-ttu-id="01432-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="01432-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="01432-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="01432-119">System-Id-Guid</span></span>    | <span data-ttu-id="01432-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="01432-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="01432-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01432-121">Syntax</span></span>            | [<span data-ttu-id="01432-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="01432-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="01432-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="01432-123">Implementations</span></span>

-   [<span data-ttu-id="01432-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="01432-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="01432-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01432-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01432-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="01432-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="01432-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01432-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01432-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01432-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01432-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01432-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01432-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01432-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="01432-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01432-131">Windows 2000 Server</span></span>



| <span data-ttu-id="01432-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-132">Entry</span></span> | <span data-ttu-id="01432-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-136">System-Only</span></span>            | <span data-ttu-id="01432-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-137">True</span></span>                            |
| <span data-ttu-id="01432-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-138">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-139">True</span></span>                            |
| <span data-ttu-id="01432-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-140">Is Indexed</span></span>             | <span data-ttu-id="01432-141">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-141">False</span></span>                           |
| <span data-ttu-id="01432-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-142">In Global Catalog</span></span>      | <span data-ttu-id="01432-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-143">True</span></span>                            |
| <span data-ttu-id="01432-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-148">Search-Flags</span></span>           | <span data-ttu-id="01432-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-149">0x00000000</span></span>                      |
| <span data-ttu-id="01432-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-150">System-Flags</span></span>           | <span data-ttu-id="01432-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-151">0x00000012</span></span>                      |
| <span data-ttu-id="01432-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-152">Classes used in</span></span>        | [<span data-ttu-id="01432-153">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="01432-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01432-154">Windows Server 2003</span></span>



| <span data-ttu-id="01432-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-155">Entry</span></span> | <span data-ttu-id="01432-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-159">System-Only</span></span>            | <span data-ttu-id="01432-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-160">True</span></span>                            |
| <span data-ttu-id="01432-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-161">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-162">True</span></span>                            |
| <span data-ttu-id="01432-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-163">Is Indexed</span></span>             | <span data-ttu-id="01432-164">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-164">False</span></span>                           |
| <span data-ttu-id="01432-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-165">In Global Catalog</span></span>      | <span data-ttu-id="01432-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-166">True</span></span>                            |
| <span data-ttu-id="01432-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-171">Search-Flags</span></span>           | <span data-ttu-id="01432-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-172">0x00000000</span></span>                      |
| <span data-ttu-id="01432-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-173">System-Flags</span></span>           | <span data-ttu-id="01432-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-174">0x00000012</span></span>                      |
| <span data-ttu-id="01432-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-175">Classes used in</span></span>        | [<span data-ttu-id="01432-176">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="01432-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="01432-177">ADAM</span></span>



| <span data-ttu-id="01432-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-178">Entry</span></span> | <span data-ttu-id="01432-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-182">System-Only</span></span>            | <span data-ttu-id="01432-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-183">True</span></span>                            |
| <span data-ttu-id="01432-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-184">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-185">True</span></span>                            |
| <span data-ttu-id="01432-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-186">Is Indexed</span></span>             | <span data-ttu-id="01432-187">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-187">False</span></span>                           |
| <span data-ttu-id="01432-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-188">In Global Catalog</span></span>      | <span data-ttu-id="01432-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-189">True</span></span>                            |
| <span data-ttu-id="01432-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-194">Search-Flags</span></span>           | <span data-ttu-id="01432-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-195">0x00000000</span></span>                      |
| <span data-ttu-id="01432-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-196">System-Flags</span></span>           | <span data-ttu-id="01432-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-197">0x00000012</span></span>                      |
| <span data-ttu-id="01432-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-198">Classes used in</span></span>        | [<span data-ttu-id="01432-199">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01432-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01432-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01432-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-201">Entry</span></span> | <span data-ttu-id="01432-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-205">System-Only</span></span>            | <span data-ttu-id="01432-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-206">True</span></span>                            |
| <span data-ttu-id="01432-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-207">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-208">True</span></span>                            |
| <span data-ttu-id="01432-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-209">Is Indexed</span></span>             | <span data-ttu-id="01432-210">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-210">False</span></span>                           |
| <span data-ttu-id="01432-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-211">In Global Catalog</span></span>      | <span data-ttu-id="01432-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-212">True</span></span>                            |
| <span data-ttu-id="01432-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-217">Search-Flags</span></span>           | <span data-ttu-id="01432-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-218">0x00000000</span></span>                      |
| <span data-ttu-id="01432-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-219">System-Flags</span></span>           | <span data-ttu-id="01432-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-220">0x00000012</span></span>                      |
| <span data-ttu-id="01432-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-221">Classes used in</span></span>        | [<span data-ttu-id="01432-222">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01432-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01432-223">Windows Server 2008</span></span>



| <span data-ttu-id="01432-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-224">Entry</span></span> | <span data-ttu-id="01432-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-228">System-Only</span></span>            | <span data-ttu-id="01432-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-229">True</span></span>                            |
| <span data-ttu-id="01432-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-230">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-231">True</span></span>                            |
| <span data-ttu-id="01432-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-232">Is Indexed</span></span>             | <span data-ttu-id="01432-233">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-233">False</span></span>                           |
| <span data-ttu-id="01432-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-234">In Global Catalog</span></span>      | <span data-ttu-id="01432-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-235">True</span></span>                            |
| <span data-ttu-id="01432-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-240">Search-Flags</span></span>           | <span data-ttu-id="01432-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-241">0x00000000</span></span>                      |
| <span data-ttu-id="01432-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-242">System-Flags</span></span>           | <span data-ttu-id="01432-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-243">0x00000012</span></span>                      |
| <span data-ttu-id="01432-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-244">Classes used in</span></span>        | [<span data-ttu-id="01432-245">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01432-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01432-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01432-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-247">Entry</span></span> | <span data-ttu-id="01432-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-251">System-Only</span></span>            | <span data-ttu-id="01432-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-252">True</span></span>                            |
| <span data-ttu-id="01432-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-253">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-254">True</span></span>                            |
| <span data-ttu-id="01432-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-255">Is Indexed</span></span>             | <span data-ttu-id="01432-256">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-256">False</span></span>                           |
| <span data-ttu-id="01432-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-257">In Global Catalog</span></span>      | <span data-ttu-id="01432-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-258">True</span></span>                            |
| <span data-ttu-id="01432-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-263">Search-Flags</span></span>           | <span data-ttu-id="01432-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-264">0x00000000</span></span>                      |
| <span data-ttu-id="01432-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-265">System-Flags</span></span>           | <span data-ttu-id="01432-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-266">0x00000012</span></span>                      |
| <span data-ttu-id="01432-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-267">Classes used in</span></span>        | [<span data-ttu-id="01432-268">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01432-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01432-269">Windows Server 2012</span></span>



| <span data-ttu-id="01432-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="01432-270">Entry</span></span> | <span data-ttu-id="01432-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="01432-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="01432-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="01432-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01432-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="01432-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="01432-274">System-Only</span></span>            | <span data-ttu-id="01432-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-275">True</span></span>                            |
| <span data-ttu-id="01432-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="01432-276">Is-Single-Valued</span></span>       | <span data-ttu-id="01432-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-277">True</span></span>                            |
| <span data-ttu-id="01432-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="01432-278">Is Indexed</span></span>             | <span data-ttu-id="01432-279">Faux</span><span class="sxs-lookup"><span data-stu-id="01432-279">False</span></span>                           |
| <span data-ttu-id="01432-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="01432-280">In Global Catalog</span></span>      | <span data-ttu-id="01432-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="01432-281">True</span></span>                            |
| <span data-ttu-id="01432-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="01432-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="01432-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="01432-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="01432-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01432-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="01432-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01432-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="01432-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-286">Search-Flags</span></span>           | <span data-ttu-id="01432-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01432-287">0x00000000</span></span>                      |
| <span data-ttu-id="01432-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01432-288">System-Flags</span></span>           | <span data-ttu-id="01432-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="01432-289">0x00000012</span></span>                      |
| <span data-ttu-id="01432-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="01432-290">Classes used in</span></span>        | [<span data-ttu-id="01432-291">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="01432-291">**Top**</span></span>](c-top.md)<br/> |



 

 





