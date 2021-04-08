---
title: Attribut localization-Display-ID
description: Permet d’indexer dans le fichier Extrts.mc pour obtenir le displayName localisé pour les objets à des fins d’interface utilisateur.
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut localization-Display-ID
- Schéma AD de l’attribut localizationDisplayId
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744804"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="bda17-105">Attribut localization-Display-ID</span><span class="sxs-lookup"><span data-stu-id="bda17-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="bda17-106">Permet d’indexer dans le fichier Extrts.mc pour obtenir le displayName localisé pour les objets à des fins d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bda17-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="bda17-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-107">Entry</span></span> | <span data-ttu-id="bda17-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bda17-109">CN</span><span class="sxs-lookup"><span data-stu-id="bda17-109">CN</span></span>                | <span data-ttu-id="bda17-110">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="bda17-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="bda17-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bda17-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bda17-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="bda17-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="bda17-113">Taille</span><span class="sxs-lookup"><span data-stu-id="bda17-113">Size</span></span>              | <span data-ttu-id="bda17-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="bda17-114">4 bytes</span></span>                              |
| <span data-ttu-id="bda17-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bda17-115">Update Privilege</span></span>  | <span data-ttu-id="bda17-116">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="bda17-116">Schema administrator</span></span>                 |
| <span data-ttu-id="bda17-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bda17-117">Update Frequency</span></span>  | <span data-ttu-id="bda17-118">Un ID ne doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="bda17-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="bda17-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-119">Attribute-Id</span></span>      | <span data-ttu-id="bda17-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="bda17-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="bda17-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bda17-121">System-Id-Guid</span></span>    | <span data-ttu-id="bda17-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="bda17-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="bda17-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bda17-123">Syntax</span></span>            | [<span data-ttu-id="bda17-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="bda17-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bda17-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bda17-125">Implementations</span></span>

-   [<span data-ttu-id="bda17-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bda17-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bda17-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bda17-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bda17-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bda17-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bda17-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bda17-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bda17-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bda17-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bda17-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bda17-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bda17-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bda17-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bda17-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bda17-133">Windows 2000 Server</span></span>



| <span data-ttu-id="bda17-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-134">Entry</span></span> | <span data-ttu-id="bda17-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-138">System-Only</span></span>            | <span data-ttu-id="bda17-139">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-139">False</span></span>                                                           |
| <span data-ttu-id="bda17-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-140">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-141">True</span></span>                                                            |
| <span data-ttu-id="bda17-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-142">Is Indexed</span></span>             | <span data-ttu-id="bda17-143">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-143">False</span></span>                                                           |
| <span data-ttu-id="bda17-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-144">In Global Catalog</span></span>      | <span data-ttu-id="bda17-145">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-145">False</span></span>                                                           |
| <span data-ttu-id="bda17-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-150">Search-Flags</span></span>           | <span data-ttu-id="bda17-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-152">System-Flags</span></span>           | <span data-ttu-id="bda17-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-154">Classes used in</span></span>        | [<span data-ttu-id="bda17-155">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bda17-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bda17-156">Windows Server 2003</span></span>



| <span data-ttu-id="bda17-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-157">Entry</span></span> | <span data-ttu-id="bda17-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-161">System-Only</span></span>            | <span data-ttu-id="bda17-162">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-162">False</span></span>                                                           |
| <span data-ttu-id="bda17-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-164">True</span></span>                                                            |
| <span data-ttu-id="bda17-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-165">Is Indexed</span></span>             | <span data-ttu-id="bda17-166">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-166">False</span></span>                                                           |
| <span data-ttu-id="bda17-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-167">In Global Catalog</span></span>      | <span data-ttu-id="bda17-168">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-168">False</span></span>                                                           |
| <span data-ttu-id="bda17-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-173">Search-Flags</span></span>           | <span data-ttu-id="bda17-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-175">System-Flags</span></span>           | <span data-ttu-id="bda17-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-177">Classes used in</span></span>        | [<span data-ttu-id="bda17-178">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bda17-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="bda17-179">ADAM</span></span>



| <span data-ttu-id="bda17-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-180">Entry</span></span> | <span data-ttu-id="bda17-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-184">System-Only</span></span>            | <span data-ttu-id="bda17-185">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-185">False</span></span>                                                           |
| <span data-ttu-id="bda17-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-186">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-187">True</span></span>                                                            |
| <span data-ttu-id="bda17-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-188">Is Indexed</span></span>             | <span data-ttu-id="bda17-189">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-189">False</span></span>                                                           |
| <span data-ttu-id="bda17-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-190">In Global Catalog</span></span>      | <span data-ttu-id="bda17-191">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-191">False</span></span>                                                           |
| <span data-ttu-id="bda17-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-196">Search-Flags</span></span>           | <span data-ttu-id="bda17-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-198">System-Flags</span></span>           | <span data-ttu-id="bda17-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-200">Classes used in</span></span>        | [<span data-ttu-id="bda17-201">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bda17-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bda17-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bda17-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-203">Entry</span></span> | <span data-ttu-id="bda17-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-207">System-Only</span></span>            | <span data-ttu-id="bda17-208">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-208">False</span></span>                                                           |
| <span data-ttu-id="bda17-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-209">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-210">True</span></span>                                                            |
| <span data-ttu-id="bda17-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-211">Is Indexed</span></span>             | <span data-ttu-id="bda17-212">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-212">False</span></span>                                                           |
| <span data-ttu-id="bda17-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-213">In Global Catalog</span></span>      | <span data-ttu-id="bda17-214">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-214">False</span></span>                                                           |
| <span data-ttu-id="bda17-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-219">Search-Flags</span></span>           | <span data-ttu-id="bda17-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-221">System-Flags</span></span>           | <span data-ttu-id="bda17-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-223">Classes used in</span></span>        | [<span data-ttu-id="bda17-224">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bda17-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bda17-225">Windows Server 2008</span></span>



| <span data-ttu-id="bda17-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-226">Entry</span></span> | <span data-ttu-id="bda17-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-230">System-Only</span></span>            | <span data-ttu-id="bda17-231">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-231">False</span></span>                                                           |
| <span data-ttu-id="bda17-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-232">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-233">True</span></span>                                                            |
| <span data-ttu-id="bda17-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-234">Is Indexed</span></span>             | <span data-ttu-id="bda17-235">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-235">False</span></span>                                                           |
| <span data-ttu-id="bda17-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-236">In Global Catalog</span></span>      | <span data-ttu-id="bda17-237">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-237">False</span></span>                                                           |
| <span data-ttu-id="bda17-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-242">Search-Flags</span></span>           | <span data-ttu-id="bda17-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-244">System-Flags</span></span>           | <span data-ttu-id="bda17-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-246">Classes used in</span></span>        | [<span data-ttu-id="bda17-247">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bda17-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bda17-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bda17-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-249">Entry</span></span> | <span data-ttu-id="bda17-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-253">System-Only</span></span>            | <span data-ttu-id="bda17-254">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-254">False</span></span>                                                           |
| <span data-ttu-id="bda17-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-255">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-256">True</span></span>                                                            |
| <span data-ttu-id="bda17-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-257">Is Indexed</span></span>             | <span data-ttu-id="bda17-258">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-258">False</span></span>                                                           |
| <span data-ttu-id="bda17-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-259">In Global Catalog</span></span>      | <span data-ttu-id="bda17-260">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-260">False</span></span>                                                           |
| <span data-ttu-id="bda17-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-265">Search-Flags</span></span>           | <span data-ttu-id="bda17-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-267">System-Flags</span></span>           | <span data-ttu-id="bda17-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-269">Classes used in</span></span>        | [<span data-ttu-id="bda17-270">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bda17-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bda17-271">Windows Server 2012</span></span>



| <span data-ttu-id="bda17-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="bda17-272">Entry</span></span> | <span data-ttu-id="bda17-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda17-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bda17-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bda17-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda17-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bda17-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda17-276">System-Only</span></span>            | <span data-ttu-id="bda17-277">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-277">False</span></span>                                                           |
| <span data-ttu-id="bda17-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bda17-278">Is-Single-Valued</span></span>       | <span data-ttu-id="bda17-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="bda17-279">True</span></span>                                                            |
| <span data-ttu-id="bda17-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bda17-280">Is Indexed</span></span>             | <span data-ttu-id="bda17-281">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-281">False</span></span>                                                           |
| <span data-ttu-id="bda17-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bda17-282">In Global Catalog</span></span>      | <span data-ttu-id="bda17-283">Faux</span><span class="sxs-lookup"><span data-stu-id="bda17-283">False</span></span>                                                           |
| <span data-ttu-id="bda17-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bda17-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda17-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bda17-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bda17-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda17-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda17-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="bda17-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-288">Search-Flags</span></span>           | <span data-ttu-id="bda17-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda17-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="bda17-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda17-290">System-Flags</span></span>           | <span data-ttu-id="bda17-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bda17-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="bda17-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bda17-292">Classes used in</span></span>        | [<span data-ttu-id="bda17-293">**Accès au contrôle-droit**</span><span class="sxs-lookup"><span data-stu-id="bda17-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





