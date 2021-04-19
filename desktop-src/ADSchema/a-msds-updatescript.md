---
title: attribut ms-DS-UpdateScript
description: Il est utilisé pour contenir le script avec les instructions de restructuration de domaine.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-UpdateScript
- Schéma Active Directory de l’attribut msDS-UpdateScript
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514482"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="d6bd4-105">attribut ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="d6bd4-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="d6bd4-106">Il est utilisé pour contenir le script avec les instructions de restructuration de domaine.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="d6bd4-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-107">Entry</span></span> | <span data-ttu-id="d6bd4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d6bd4-109">CN</span><span class="sxs-lookup"><span data-stu-id="d6bd4-109">CN</span></span>                | <span data-ttu-id="d6bd4-110">ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="d6bd4-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="d6bd4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d6bd4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d6bd4-112">msDS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="d6bd4-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="d6bd4-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d6bd4-113">Size</span></span>              | <span data-ttu-id="d6bd4-114">Taille maximale de 10 Ko.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="d6bd4-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d6bd4-115">Update Privilege</span></span>  | <span data-ttu-id="d6bd4-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="d6bd4-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d6bd4-117">Update Frequency</span></span>  | <span data-ttu-id="d6bd4-118">Uniquement pendant la restructuration de domaine.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="d6bd4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-119">Attribute-Id</span></span>      | <span data-ttu-id="d6bd4-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="d6bd4-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="d6bd4-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d6bd4-121">System-Id-Guid</span></span>    | <span data-ttu-id="d6bd4-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="d6bd4-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="d6bd4-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6bd4-123">Syntax</span></span>            | [<span data-ttu-id="d6bd4-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d6bd4-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d6bd4-125">Implementations</span></span>

-   [<span data-ttu-id="d6bd4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d6bd4-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d6bd4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d6bd4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d6bd4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d6bd4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d6bd4-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6bd4-132">Windows Server 2003</span></span>



| <span data-ttu-id="d6bd4-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-133">Entry</span></span> | <span data-ttu-id="d6bd4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-137">System-Only</span></span>            | <span data-ttu-id="d6bd4-138">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-138">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-140">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-141">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-142">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-143">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-144">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-149">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-151">System-Flags</span></span>           | <span data-ttu-id="d6bd4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-153">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-154">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d6bd4-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="d6bd4-155">ADAM</span></span>



| <span data-ttu-id="d6bd4-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-156">Entry</span></span> | <span data-ttu-id="d6bd4-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-160">System-Only</span></span>            | <span data-ttu-id="d6bd4-161">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-161">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-163">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-164">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-165">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-165">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-166">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-167">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-172">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-174">System-Flags</span></span>           | <span data-ttu-id="d6bd4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-176">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-177">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d6bd4-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d6bd4-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d6bd4-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-179">Entry</span></span> | <span data-ttu-id="d6bd4-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-183">System-Only</span></span>            | <span data-ttu-id="d6bd4-184">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-184">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-186">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-187">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-188">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-189">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-190">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-190">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-195">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-197">System-Flags</span></span>           | <span data-ttu-id="d6bd4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-199">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-200">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d6bd4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6bd4-201">Windows Server 2008</span></span>



| <span data-ttu-id="d6bd4-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-202">Entry</span></span> | <span data-ttu-id="d6bd4-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-206">System-Only</span></span>            | <span data-ttu-id="d6bd4-207">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-207">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-209">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-210">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-211">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-211">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-212">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-213">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-213">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-218">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-220">System-Flags</span></span>           | <span data-ttu-id="d6bd4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-222">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-223">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d6bd4-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6bd4-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d6bd4-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-225">Entry</span></span> | <span data-ttu-id="d6bd4-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-229">System-Only</span></span>            | <span data-ttu-id="d6bd4-230">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-230">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-232">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-233">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-234">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-234">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-235">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-236">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-236">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-241">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-243">System-Flags</span></span>           | <span data-ttu-id="d6bd4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-245">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-246">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d6bd4-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6bd4-247">Windows Server 2012</span></span>



| <span data-ttu-id="d6bd4-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="d6bd4-248">Entry</span></span> | <span data-ttu-id="d6bd4-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd4-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6bd4-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d6bd4-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6bd4-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d6bd4-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6bd4-252">System-Only</span></span>            | <span data-ttu-id="d6bd4-253">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-253">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d6bd4-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d6bd4-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="d6bd4-255">True</span></span>                                                          |
| <span data-ttu-id="d6bd4-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d6bd4-256">Is Indexed</span></span>             | <span data-ttu-id="d6bd4-257">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-257">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d6bd4-258">In Global Catalog</span></span>      | <span data-ttu-id="d6bd4-259">Faux</span><span class="sxs-lookup"><span data-stu-id="d6bd4-259">False</span></span>                                                         |
| <span data-ttu-id="d6bd4-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d6bd4-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6bd4-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d6bd4-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d6bd4-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6bd4-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6bd4-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="d6bd4-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-264">Search-Flags</span></span>           | <span data-ttu-id="d6bd4-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6bd4-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="d6bd4-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6bd4-266">System-Flags</span></span>           | <span data-ttu-id="d6bd4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6bd4-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="d6bd4-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d6bd4-268">Classes used in</span></span>        | [<span data-ttu-id="d6bd4-269">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="d6bd4-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





