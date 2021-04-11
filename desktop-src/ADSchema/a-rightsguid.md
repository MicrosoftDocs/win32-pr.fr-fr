---
title: Attribut Rights-Guid
description: GUID utilisé pour représenter un droit étendu dans une entrée de contrôle d’accès.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Rights-Guid
- Schéma AD de l’attribut rightsGuid
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107962"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="aee7f-105">Attribut Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="aee7f-105">Rights-Guid attribute</span></span>

<span data-ttu-id="aee7f-106">GUID utilisé pour représenter un droit étendu dans une entrée de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="aee7f-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="aee7f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-107">Entry</span></span> | <span data-ttu-id="aee7f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="aee7f-109">CN</span><span class="sxs-lookup"><span data-stu-id="aee7f-109">CN</span></span>                | <span data-ttu-id="aee7f-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="aee7f-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="aee7f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aee7f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aee7f-112">rightsGuid</span><span class="sxs-lookup"><span data-stu-id="aee7f-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="aee7f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="aee7f-113">Size</span></span>              | <span data-ttu-id="aee7f-114">16 octets</span><span class="sxs-lookup"><span data-stu-id="aee7f-114">16 bytes</span></span>                                    |
| <span data-ttu-id="aee7f-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="aee7f-115">Update Privilege</span></span>  | <span data-ttu-id="aee7f-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="aee7f-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="aee7f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="aee7f-117">Update Frequency</span></span>  | <span data-ttu-id="aee7f-118">Lors de la création d’un nouveau droit étendu.</span><span class="sxs-lookup"><span data-stu-id="aee7f-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="aee7f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-119">Attribute-Id</span></span>      | <span data-ttu-id="aee7f-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="aee7f-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="aee7f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aee7f-121">System-Id-Guid</span></span>    | <span data-ttu-id="aee7f-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="aee7f-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="aee7f-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aee7f-123">Syntax</span></span>            | [<span data-ttu-id="aee7f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aee7f-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="aee7f-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="aee7f-125">Implementations</span></span>

-   [<span data-ttu-id="aee7f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aee7f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aee7f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aee7f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aee7f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="aee7f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="aee7f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aee7f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aee7f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aee7f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aee7f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aee7f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aee7f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aee7f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aee7f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aee7f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="aee7f-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-134">Entry</span></span> | <span data-ttu-id="aee7f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-138">System-Only</span></span>            | <span data-ttu-id="aee7f-139">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-139">False</span></span>                                                           |
| <span data-ttu-id="aee7f-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-141">True</span></span>                                                            |
| <span data-ttu-id="aee7f-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-142">Is Indexed</span></span>             | <span data-ttu-id="aee7f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-143">False</span></span>                                                           |
| <span data-ttu-id="aee7f-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-144">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-145">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-145">False</span></span>                                                           |
| <span data-ttu-id="aee7f-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-148">Range-Lower</span></span>            | <span data-ttu-id="aee7f-149">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-149">36</span></span>                                                              |
| <span data-ttu-id="aee7f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-150">Range-Upper</span></span>            | <span data-ttu-id="aee7f-151">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-151">36</span></span>                                                              |
| <span data-ttu-id="aee7f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-152">Search-Flags</span></span>           | <span data-ttu-id="aee7f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-154">System-Flags</span></span>           | <span data-ttu-id="aee7f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-156">Classes used in</span></span>        | [<span data-ttu-id="aee7f-157">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aee7f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aee7f-158">Windows Server 2003</span></span>



| <span data-ttu-id="aee7f-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-159">Entry</span></span> | <span data-ttu-id="aee7f-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-163">System-Only</span></span>            | <span data-ttu-id="aee7f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-164">False</span></span>                                                           |
| <span data-ttu-id="aee7f-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-166">True</span></span>                                                            |
| <span data-ttu-id="aee7f-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-167">Is Indexed</span></span>             | <span data-ttu-id="aee7f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-168">False</span></span>                                                           |
| <span data-ttu-id="aee7f-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-169">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-170">False</span></span>                                                           |
| <span data-ttu-id="aee7f-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-173">Range-Lower</span></span>            | <span data-ttu-id="aee7f-174">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-174">36</span></span>                                                              |
| <span data-ttu-id="aee7f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-175">Range-Upper</span></span>            | <span data-ttu-id="aee7f-176">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-176">36</span></span>                                                              |
| <span data-ttu-id="aee7f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-177">Search-Flags</span></span>           | <span data-ttu-id="aee7f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-179">System-Flags</span></span>           | <span data-ttu-id="aee7f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-181">Classes used in</span></span>        | [<span data-ttu-id="aee7f-182">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="aee7f-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="aee7f-183">ADAM</span></span>



| <span data-ttu-id="aee7f-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-184">Entry</span></span> | <span data-ttu-id="aee7f-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-188">System-Only</span></span>            | <span data-ttu-id="aee7f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-189">False</span></span>                                                           |
| <span data-ttu-id="aee7f-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-190">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-191">True</span></span>                                                            |
| <span data-ttu-id="aee7f-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-192">Is Indexed</span></span>             | <span data-ttu-id="aee7f-193">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-193">False</span></span>                                                           |
| <span data-ttu-id="aee7f-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-194">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-195">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-195">False</span></span>                                                           |
| <span data-ttu-id="aee7f-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-198">Range-Lower</span></span>            | <span data-ttu-id="aee7f-199">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-199">36</span></span>                                                              |
| <span data-ttu-id="aee7f-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-200">Range-Upper</span></span>            | <span data-ttu-id="aee7f-201">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-201">36</span></span>                                                              |
| <span data-ttu-id="aee7f-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-202">Search-Flags</span></span>           | <span data-ttu-id="aee7f-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-204">System-Flags</span></span>           | <span data-ttu-id="aee7f-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-206">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-206">Classes used in</span></span>        | [<span data-ttu-id="aee7f-207">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aee7f-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aee7f-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aee7f-209">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-209">Entry</span></span> | <span data-ttu-id="aee7f-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-211">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-213">System-Only</span></span>            | <span data-ttu-id="aee7f-214">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-214">False</span></span>                                                           |
| <span data-ttu-id="aee7f-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-215">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-216">True</span></span>                                                            |
| <span data-ttu-id="aee7f-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-217">Is Indexed</span></span>             | <span data-ttu-id="aee7f-218">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-218">False</span></span>                                                           |
| <span data-ttu-id="aee7f-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-219">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-220">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-220">False</span></span>                                                           |
| <span data-ttu-id="aee7f-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-223">Range-Lower</span></span>            | <span data-ttu-id="aee7f-224">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-224">36</span></span>                                                              |
| <span data-ttu-id="aee7f-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-225">Range-Upper</span></span>            | <span data-ttu-id="aee7f-226">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-226">36</span></span>                                                              |
| <span data-ttu-id="aee7f-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-227">Search-Flags</span></span>           | <span data-ttu-id="aee7f-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-229">System-Flags</span></span>           | <span data-ttu-id="aee7f-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-231">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-231">Classes used in</span></span>        | [<span data-ttu-id="aee7f-232">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aee7f-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee7f-233">Windows Server 2008</span></span>



| <span data-ttu-id="aee7f-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-234">Entry</span></span> | <span data-ttu-id="aee7f-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-238">System-Only</span></span>            | <span data-ttu-id="aee7f-239">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-239">False</span></span>                                                           |
| <span data-ttu-id="aee7f-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-240">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-241">True</span></span>                                                            |
| <span data-ttu-id="aee7f-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-242">Is Indexed</span></span>             | <span data-ttu-id="aee7f-243">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-243">False</span></span>                                                           |
| <span data-ttu-id="aee7f-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-244">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-245">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-245">False</span></span>                                                           |
| <span data-ttu-id="aee7f-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-248">Range-Lower</span></span>            | <span data-ttu-id="aee7f-249">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-249">36</span></span>                                                              |
| <span data-ttu-id="aee7f-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-250">Range-Upper</span></span>            | <span data-ttu-id="aee7f-251">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-251">36</span></span>                                                              |
| <span data-ttu-id="aee7f-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-252">Search-Flags</span></span>           | <span data-ttu-id="aee7f-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-254">System-Flags</span></span>           | <span data-ttu-id="aee7f-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-256">Classes used in</span></span>        | [<span data-ttu-id="aee7f-257">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aee7f-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aee7f-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aee7f-259">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-259">Entry</span></span> | <span data-ttu-id="aee7f-260">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-261">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-263">System-Only</span></span>            | <span data-ttu-id="aee7f-264">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-264">False</span></span>                                                           |
| <span data-ttu-id="aee7f-265">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-265">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-266">True</span></span>                                                            |
| <span data-ttu-id="aee7f-267">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-267">Is Indexed</span></span>             | <span data-ttu-id="aee7f-268">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-268">False</span></span>                                                           |
| <span data-ttu-id="aee7f-269">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-269">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-270">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-270">False</span></span>                                                           |
| <span data-ttu-id="aee7f-271">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-272">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-273">Range-Lower</span></span>            | <span data-ttu-id="aee7f-274">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-274">36</span></span>                                                              |
| <span data-ttu-id="aee7f-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-275">Range-Upper</span></span>            | <span data-ttu-id="aee7f-276">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-276">36</span></span>                                                              |
| <span data-ttu-id="aee7f-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-277">Search-Flags</span></span>           | <span data-ttu-id="aee7f-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-279">System-Flags</span></span>           | <span data-ttu-id="aee7f-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-281">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-281">Classes used in</span></span>        | [<span data-ttu-id="aee7f-282">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aee7f-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aee7f-283">Windows Server 2012</span></span>



| <span data-ttu-id="aee7f-284">Entrée</span><span class="sxs-lookup"><span data-stu-id="aee7f-284">Entry</span></span> | <span data-ttu-id="aee7f-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee7f-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aee7f-286">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aee7f-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aee7f-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="aee7f-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="aee7f-288">System-Only</span></span>            | <span data-ttu-id="aee7f-289">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-289">False</span></span>                                                           |
| <span data-ttu-id="aee7f-290">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aee7f-290">Is-Single-Valued</span></span>       | <span data-ttu-id="aee7f-291">Vrai</span><span class="sxs-lookup"><span data-stu-id="aee7f-291">True</span></span>                                                            |
| <span data-ttu-id="aee7f-292">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aee7f-292">Is Indexed</span></span>             | <span data-ttu-id="aee7f-293">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-293">False</span></span>                                                           |
| <span data-ttu-id="aee7f-294">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aee7f-294">In Global Catalog</span></span>      | <span data-ttu-id="aee7f-295">Faux</span><span class="sxs-lookup"><span data-stu-id="aee7f-295">False</span></span>                                                           |
| <span data-ttu-id="aee7f-296">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aee7f-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="aee7f-297">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aee7f-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="aee7f-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aee7f-298">Range-Lower</span></span>            | <span data-ttu-id="aee7f-299">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-299">36</span></span>                                                              |
| <span data-ttu-id="aee7f-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aee7f-300">Range-Upper</span></span>            | <span data-ttu-id="aee7f-301">36</span><span class="sxs-lookup"><span data-stu-id="aee7f-301">36</span></span>                                                              |
| <span data-ttu-id="aee7f-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-302">Search-Flags</span></span>           | <span data-ttu-id="aee7f-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aee7f-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="aee7f-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aee7f-304">System-Flags</span></span>           | <span data-ttu-id="aee7f-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aee7f-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="aee7f-306">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aee7f-306">Classes used in</span></span>        | [<span data-ttu-id="aee7f-307">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="aee7f-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





