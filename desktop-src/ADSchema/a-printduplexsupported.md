---
title: Print-attribut pris en charge en mode duplex
description: Indique le type de prise en charge duplex d’une imprimante.
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory d’attribut pris en charge en mode duplex
- Schéma AD de l’attribut printDuplexSupported
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516120"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="f1040-105">Print-attribut pris en charge en mode duplex</span><span class="sxs-lookup"><span data-stu-id="f1040-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="f1040-106">Indique le type de prise en charge duplex d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="f1040-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="f1040-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-107">Entry</span></span> | <span data-ttu-id="f1040-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f1040-109">CN</span><span class="sxs-lookup"><span data-stu-id="f1040-109">CN</span></span>                | <span data-ttu-id="f1040-110">Print-duplex-pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1040-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="f1040-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1040-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f1040-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="f1040-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="f1040-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f1040-113">Size</span></span>              | <span data-ttu-id="f1040-114">4 octets.</span><span class="sxs-lookup"><span data-stu-id="f1040-114">4 bytes.</span></span> <span data-ttu-id="f1040-115">Duplex pris en charge = 2.</span><span class="sxs-lookup"><span data-stu-id="f1040-115">Duplex supported = 2.</span></span> <span data-ttu-id="f1040-116">Simplex uniquement = 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="f1040-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="f1040-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f1040-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f1040-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f1040-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f1040-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-119">Attribute-Id</span></span>      | <span data-ttu-id="f1040-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="f1040-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="f1040-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1040-121">System-Id-Guid</span></span>    | <span data-ttu-id="f1040-122">281416cc-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f1040-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="f1040-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1040-123">Syntax</span></span>            | [<span data-ttu-id="f1040-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1040-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="f1040-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f1040-125">Implementations</span></span>

-   [<span data-ttu-id="f1040-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1040-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1040-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1040-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1040-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1040-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1040-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1040-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1040-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1040-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1040-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1040-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1040-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1040-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f1040-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-133">Entry</span></span> | <span data-ttu-id="f1040-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-137">System-Only</span></span>            | <span data-ttu-id="f1040-138">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-138">False</span></span>                                          |
| <span data-ttu-id="f1040-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-140">True</span></span>                                           |
| <span data-ttu-id="f1040-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-141">Is Indexed</span></span>             | <span data-ttu-id="f1040-142">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-142">False</span></span>                                          |
| <span data-ttu-id="f1040-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-143">In Global Catalog</span></span>      | <span data-ttu-id="f1040-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-144">True</span></span>                                           |
| <span data-ttu-id="f1040-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-149">Search-Flags</span></span>           | <span data-ttu-id="f1040-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-150">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-151">System-Flags</span></span>           | <span data-ttu-id="f1040-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-152">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-153">Classes used in</span></span>        | [<span data-ttu-id="f1040-154">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1040-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1040-155">Windows Server 2003</span></span>



| <span data-ttu-id="f1040-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-156">Entry</span></span> | <span data-ttu-id="f1040-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-160">System-Only</span></span>            | <span data-ttu-id="f1040-161">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-161">False</span></span>                                          |
| <span data-ttu-id="f1040-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-163">True</span></span>                                           |
| <span data-ttu-id="f1040-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-164">Is Indexed</span></span>             | <span data-ttu-id="f1040-165">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-165">False</span></span>                                          |
| <span data-ttu-id="f1040-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-166">In Global Catalog</span></span>      | <span data-ttu-id="f1040-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-167">True</span></span>                                           |
| <span data-ttu-id="f1040-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-172">Search-Flags</span></span>           | <span data-ttu-id="f1040-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-173">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-174">System-Flags</span></span>           | <span data-ttu-id="f1040-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-175">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-176">Classes used in</span></span>        | [<span data-ttu-id="f1040-177">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1040-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1040-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1040-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-179">Entry</span></span> | <span data-ttu-id="f1040-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-183">System-Only</span></span>            | <span data-ttu-id="f1040-184">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-184">False</span></span>                                          |
| <span data-ttu-id="f1040-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-186">True</span></span>                                           |
| <span data-ttu-id="f1040-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-187">Is Indexed</span></span>             | <span data-ttu-id="f1040-188">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-188">False</span></span>                                          |
| <span data-ttu-id="f1040-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-189">In Global Catalog</span></span>      | <span data-ttu-id="f1040-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-190">True</span></span>                                           |
| <span data-ttu-id="f1040-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-195">Search-Flags</span></span>           | <span data-ttu-id="f1040-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-196">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-197">System-Flags</span></span>           | <span data-ttu-id="f1040-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-198">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-199">Classes used in</span></span>        | [<span data-ttu-id="f1040-200">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1040-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1040-201">Windows Server 2008</span></span>



| <span data-ttu-id="f1040-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-202">Entry</span></span> | <span data-ttu-id="f1040-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-206">System-Only</span></span>            | <span data-ttu-id="f1040-207">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-207">False</span></span>                                          |
| <span data-ttu-id="f1040-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-209">True</span></span>                                           |
| <span data-ttu-id="f1040-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-210">Is Indexed</span></span>             | <span data-ttu-id="f1040-211">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-211">False</span></span>                                          |
| <span data-ttu-id="f1040-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-212">In Global Catalog</span></span>      | <span data-ttu-id="f1040-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-213">True</span></span>                                           |
| <span data-ttu-id="f1040-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-218">Search-Flags</span></span>           | <span data-ttu-id="f1040-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-219">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-220">System-Flags</span></span>           | <span data-ttu-id="f1040-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-221">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-222">Classes used in</span></span>        | [<span data-ttu-id="f1040-223">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1040-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1040-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1040-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-225">Entry</span></span> | <span data-ttu-id="f1040-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-229">System-Only</span></span>            | <span data-ttu-id="f1040-230">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-230">False</span></span>                                          |
| <span data-ttu-id="f1040-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-232">True</span></span>                                           |
| <span data-ttu-id="f1040-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-233">Is Indexed</span></span>             | <span data-ttu-id="f1040-234">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-234">False</span></span>                                          |
| <span data-ttu-id="f1040-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-235">In Global Catalog</span></span>      | <span data-ttu-id="f1040-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-236">True</span></span>                                           |
| <span data-ttu-id="f1040-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-241">Search-Flags</span></span>           | <span data-ttu-id="f1040-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-242">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-243">System-Flags</span></span>           | <span data-ttu-id="f1040-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-244">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-245">Classes used in</span></span>        | [<span data-ttu-id="f1040-246">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1040-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1040-247">Windows Server 2012</span></span>



| <span data-ttu-id="f1040-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1040-248">Entry</span></span> | <span data-ttu-id="f1040-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1040-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f1040-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1040-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f1040-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-252">System-Only</span></span>            | <span data-ttu-id="f1040-253">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-253">False</span></span>                                          |
| <span data-ttu-id="f1040-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1040-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-255">True</span></span>                                           |
| <span data-ttu-id="f1040-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1040-256">Is Indexed</span></span>             | <span data-ttu-id="f1040-257">Faux</span><span class="sxs-lookup"><span data-stu-id="f1040-257">False</span></span>                                          |
| <span data-ttu-id="f1040-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1040-258">In Global Catalog</span></span>      | <span data-ttu-id="f1040-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1040-259">True</span></span>                                           |
| <span data-ttu-id="f1040-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1040-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1040-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f1040-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f1040-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f1040-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-264">Search-Flags</span></span>           | <span data-ttu-id="f1040-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-265">0x00000000</span></span>                                     |
| <span data-ttu-id="f1040-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-266">System-Flags</span></span>           | <span data-ttu-id="f1040-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-267">0x00000010</span></span>                                     |
| <span data-ttu-id="f1040-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1040-268">Classes used in</span></span>        | [<span data-ttu-id="f1040-269">**File d’attente d’impression**</span><span class="sxs-lookup"><span data-stu-id="f1040-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





