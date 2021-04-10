---
title: Attribut Other-Name
description: Noms supplémentaires pour un utilisateur. Par exemple, Middle Name, patronymic, matronymic, etc.
ms.assetid: 539de593-e879-4b4a-bf75-c022f53e80de
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Other-Name
- Schéma Active Directory de l’attribut middleName
topic_type:
- apiref
api_name:
- Other-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e62a9555d77d95d5e30ebacaec5950a19c318b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107875"
---
# <a name="other-name-attribute"></a><span data-ttu-id="e8125-106">Attribut Other-Name</span><span class="sxs-lookup"><span data-stu-id="e8125-106">Other-Name attribute</span></span>

<span data-ttu-id="e8125-107">Noms supplémentaires pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8125-107">Additional names for a user.</span></span> <span data-ttu-id="e8125-108">Par exemple, Middle Name, patronymic, matronymic, etc.</span><span class="sxs-lookup"><span data-stu-id="e8125-108">For example, middle name, patronymic, matronymic, or others.</span></span>



| <span data-ttu-id="e8125-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-109">Entry</span></span> | <span data-ttu-id="e8125-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e8125-111">CN</span><span class="sxs-lookup"><span data-stu-id="e8125-111">CN</span></span>                | <span data-ttu-id="e8125-112">Other-Name</span><span class="sxs-lookup"><span data-stu-id="e8125-112">Other-Name</span></span>                                  |
| <span data-ttu-id="e8125-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e8125-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e8125-114">middleName</span><span class="sxs-lookup"><span data-stu-id="e8125-114">middleName</span></span>                                  |
| <span data-ttu-id="e8125-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e8125-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="e8125-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e8125-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e8125-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e8125-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e8125-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-118">Attribute-Id</span></span>      | <span data-ttu-id="e8125-119">2.16.840.1.113730.3.1.34</span><span class="sxs-lookup"><span data-stu-id="e8125-119">2.16.840.1.113730.3.1.34</span></span>                    |
| <span data-ttu-id="e8125-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8125-120">System-Id-Guid</span></span>    | <span data-ttu-id="e8125-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e8125-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="e8125-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8125-122">Syntax</span></span>            | [<span data-ttu-id="e8125-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e8125-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e8125-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e8125-124">Implementations</span></span>

-   [<span data-ttu-id="e8125-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8125-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8125-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8125-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8125-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8125-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8125-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8125-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8125-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8125-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8125-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8125-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8125-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8125-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e8125-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-132">Entry</span></span> | <span data-ttu-id="e8125-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-136">System-Only</span></span>            | <span data-ttu-id="e8125-137">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-137">False</span></span>                                                              |
| <span data-ttu-id="e8125-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-139">True</span></span>                                                               |
| <span data-ttu-id="e8125-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-140">Is Indexed</span></span>             | <span data-ttu-id="e8125-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-141">False</span></span>                                                              |
| <span data-ttu-id="e8125-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-142">In Global Catalog</span></span>      | <span data-ttu-id="e8125-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-143">False</span></span>                                                              |
| <span data-ttu-id="e8125-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-146">Range-Lower</span></span>            | <span data-ttu-id="e8125-147">0</span><span class="sxs-lookup"><span data-stu-id="e8125-147">0</span></span>                                                                  |
| <span data-ttu-id="e8125-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-148">Range-Upper</span></span>            | <span data-ttu-id="e8125-149">64</span><span class="sxs-lookup"><span data-stu-id="e8125-149">64</span></span>                                                                 |
| <span data-ttu-id="e8125-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-150">Search-Flags</span></span>           | <span data-ttu-id="e8125-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-152">System-Flags</span></span>           | <span data-ttu-id="e8125-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-154">Classes used in</span></span>        | [<span data-ttu-id="e8125-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8125-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8125-156">Windows Server 2003</span></span>



| <span data-ttu-id="e8125-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-157">Entry</span></span> | <span data-ttu-id="e8125-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-161">System-Only</span></span>            | <span data-ttu-id="e8125-162">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-162">False</span></span>                                                              |
| <span data-ttu-id="e8125-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-164">True</span></span>                                                               |
| <span data-ttu-id="e8125-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-165">Is Indexed</span></span>             | <span data-ttu-id="e8125-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-166">False</span></span>                                                              |
| <span data-ttu-id="e8125-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-167">In Global Catalog</span></span>      | <span data-ttu-id="e8125-168">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-168">False</span></span>                                                              |
| <span data-ttu-id="e8125-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-171">Range-Lower</span></span>            | <span data-ttu-id="e8125-172">0</span><span class="sxs-lookup"><span data-stu-id="e8125-172">0</span></span>                                                                  |
| <span data-ttu-id="e8125-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-173">Range-Upper</span></span>            | <span data-ttu-id="e8125-174">64</span><span class="sxs-lookup"><span data-stu-id="e8125-174">64</span></span>                                                                 |
| <span data-ttu-id="e8125-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-175">Search-Flags</span></span>           | <span data-ttu-id="e8125-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-177">System-Flags</span></span>           | <span data-ttu-id="e8125-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-179">Classes used in</span></span>        | [<span data-ttu-id="e8125-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8125-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8125-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8125-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-182">Entry</span></span> | <span data-ttu-id="e8125-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-186">System-Only</span></span>            | <span data-ttu-id="e8125-187">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-187">False</span></span>                                                              |
| <span data-ttu-id="e8125-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-189">True</span></span>                                                               |
| <span data-ttu-id="e8125-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-190">Is Indexed</span></span>             | <span data-ttu-id="e8125-191">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-191">False</span></span>                                                              |
| <span data-ttu-id="e8125-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-192">In Global Catalog</span></span>      | <span data-ttu-id="e8125-193">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-193">False</span></span>                                                              |
| <span data-ttu-id="e8125-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-196">Range-Lower</span></span>            | <span data-ttu-id="e8125-197">0</span><span class="sxs-lookup"><span data-stu-id="e8125-197">0</span></span>                                                                  |
| <span data-ttu-id="e8125-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-198">Range-Upper</span></span>            | <span data-ttu-id="e8125-199">64</span><span class="sxs-lookup"><span data-stu-id="e8125-199">64</span></span>                                                                 |
| <span data-ttu-id="e8125-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-200">Search-Flags</span></span>           | <span data-ttu-id="e8125-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-202">System-Flags</span></span>           | <span data-ttu-id="e8125-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-204">Classes used in</span></span>        | [<span data-ttu-id="e8125-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8125-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8125-206">Windows Server 2008</span></span>



| <span data-ttu-id="e8125-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-207">Entry</span></span> | <span data-ttu-id="e8125-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-211">System-Only</span></span>            | <span data-ttu-id="e8125-212">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-212">False</span></span>                                                              |
| <span data-ttu-id="e8125-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-213">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-214">True</span></span>                                                               |
| <span data-ttu-id="e8125-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-215">Is Indexed</span></span>             | <span data-ttu-id="e8125-216">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-216">False</span></span>                                                              |
| <span data-ttu-id="e8125-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-217">In Global Catalog</span></span>      | <span data-ttu-id="e8125-218">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-218">False</span></span>                                                              |
| <span data-ttu-id="e8125-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-221">Range-Lower</span></span>            | <span data-ttu-id="e8125-222">0</span><span class="sxs-lookup"><span data-stu-id="e8125-222">0</span></span>                                                                  |
| <span data-ttu-id="e8125-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-223">Range-Upper</span></span>            | <span data-ttu-id="e8125-224">64</span><span class="sxs-lookup"><span data-stu-id="e8125-224">64</span></span>                                                                 |
| <span data-ttu-id="e8125-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-225">Search-Flags</span></span>           | <span data-ttu-id="e8125-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-227">System-Flags</span></span>           | <span data-ttu-id="e8125-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-229">Classes used in</span></span>        | [<span data-ttu-id="e8125-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8125-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8125-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8125-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-232">Entry</span></span> | <span data-ttu-id="e8125-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-236">System-Only</span></span>            | <span data-ttu-id="e8125-237">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-237">False</span></span>                                                              |
| <span data-ttu-id="e8125-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-238">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-239">True</span></span>                                                               |
| <span data-ttu-id="e8125-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-240">Is Indexed</span></span>             | <span data-ttu-id="e8125-241">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-241">False</span></span>                                                              |
| <span data-ttu-id="e8125-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-242">In Global Catalog</span></span>      | <span data-ttu-id="e8125-243">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-243">False</span></span>                                                              |
| <span data-ttu-id="e8125-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-246">Range-Lower</span></span>            | <span data-ttu-id="e8125-247">0</span><span class="sxs-lookup"><span data-stu-id="e8125-247">0</span></span>                                                                  |
| <span data-ttu-id="e8125-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-248">Range-Upper</span></span>            | <span data-ttu-id="e8125-249">64</span><span class="sxs-lookup"><span data-stu-id="e8125-249">64</span></span>                                                                 |
| <span data-ttu-id="e8125-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-250">Search-Flags</span></span>           | <span data-ttu-id="e8125-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-252">System-Flags</span></span>           | <span data-ttu-id="e8125-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-254">Classes used in</span></span>        | [<span data-ttu-id="e8125-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8125-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8125-256">Windows Server 2012</span></span>



| <span data-ttu-id="e8125-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8125-257">Entry</span></span> | <span data-ttu-id="e8125-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8125-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e8125-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8125-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8125-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e8125-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8125-261">System-Only</span></span>            | <span data-ttu-id="e8125-262">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-262">False</span></span>                                                              |
| <span data-ttu-id="e8125-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8125-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e8125-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="e8125-264">True</span></span>                                                               |
| <span data-ttu-id="e8125-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8125-265">Is Indexed</span></span>             | <span data-ttu-id="e8125-266">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-266">False</span></span>                                                              |
| <span data-ttu-id="e8125-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8125-267">In Global Catalog</span></span>      | <span data-ttu-id="e8125-268">Faux</span><span class="sxs-lookup"><span data-stu-id="e8125-268">False</span></span>                                                              |
| <span data-ttu-id="e8125-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8125-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8125-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8125-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e8125-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8125-271">Range-Lower</span></span>            | <span data-ttu-id="e8125-272">0</span><span class="sxs-lookup"><span data-stu-id="e8125-272">0</span></span>                                                                  |
| <span data-ttu-id="e8125-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8125-273">Range-Upper</span></span>            | <span data-ttu-id="e8125-274">64</span><span class="sxs-lookup"><span data-stu-id="e8125-274">64</span></span>                                                                 |
| <span data-ttu-id="e8125-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-275">Search-Flags</span></span>           | <span data-ttu-id="e8125-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8125-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="e8125-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8125-277">System-Flags</span></span>           | <span data-ttu-id="e8125-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8125-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="e8125-279">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8125-279">Classes used in</span></span>        | [<span data-ttu-id="e8125-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e8125-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





