---
title: ms-DS-attribut paramètres
description: Utilisé pour stocker les paramètres d’un objet. Son utilisation est déterminée uniquement par le propriétaire de l’objet. Nous vous recommandons de l’utiliser pour stocker les paires nom/valeur. Par exemple, couleur bleue.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Settings
- Schéma Active Directory de l’attribut msDS-Settings
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845121"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="f7f82-108">ms-DS-attribut paramètres</span><span class="sxs-lookup"><span data-stu-id="f7f82-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="f7f82-109">Utilisé pour stocker les paramètres d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f7f82-109">Used to store settings for an object.</span></span> <span data-ttu-id="f7f82-110">Son utilisation est déterminée uniquement par le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7f82-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="f7f82-111">Nous vous recommandons de l’utiliser pour stocker les paires nom/valeur.</span><span class="sxs-lookup"><span data-stu-id="f7f82-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="f7f82-112">Par exemple, Color = Blue.</span><span class="sxs-lookup"><span data-stu-id="f7f82-112">For example, color=blue.</span></span>



| <span data-ttu-id="f7f82-113">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-113">Entry</span></span> | <span data-ttu-id="f7f82-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f7f82-115">CN</span><span class="sxs-lookup"><span data-stu-id="f7f82-115">CN</span></span>                | <span data-ttu-id="f7f82-116">ms-DS-paramètres</span><span class="sxs-lookup"><span data-stu-id="f7f82-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="f7f82-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f7f82-117">Ldap-Display-Name</span></span> | <span data-ttu-id="f7f82-118">msDS-Settings</span><span class="sxs-lookup"><span data-stu-id="f7f82-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="f7f82-119">Taille</span><span class="sxs-lookup"><span data-stu-id="f7f82-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="f7f82-120">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f7f82-120">Update Privilege</span></span>  | <span data-ttu-id="f7f82-121">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="f7f82-121">Domain administrator</span></span>                        |
| <span data-ttu-id="f7f82-122">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f7f82-122">Update Frequency</span></span>  | <span data-ttu-id="f7f82-123">Chaque fois que les valeurs des paramètres changent.</span><span class="sxs-lookup"><span data-stu-id="f7f82-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="f7f82-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-124">Attribute-Id</span></span>      | <span data-ttu-id="f7f82-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="f7f82-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="f7f82-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7f82-126">System-Id-Guid</span></span>    | <span data-ttu-id="f7f82-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="f7f82-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="f7f82-128">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7f82-128">Syntax</span></span>            | [<span data-ttu-id="f7f82-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f7f82-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f7f82-130">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f7f82-130">Implementations</span></span>

-   [<span data-ttu-id="f7f82-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7f82-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7f82-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f7f82-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f7f82-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f82-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7f82-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7f82-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7f82-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f82-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7f82-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7f82-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f7f82-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7f82-137">Windows Server 2003</span></span>



| <span data-ttu-id="f7f82-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-138">Entry</span></span> | <span data-ttu-id="f7f82-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f82-140">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-142">System-Only</span></span>            | <span data-ttu-id="f7f82-143">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-144">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-144">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-145">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-146">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-146">Is Indexed</span></span>             | <span data-ttu-id="f7f82-147">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-148">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-148">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-149">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-150">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-151">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f7f82-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-154">Search-Flags</span></span>           | <span data-ttu-id="f7f82-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-156">System-Flags</span></span>           | <span data-ttu-id="f7f82-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-158">Classes used in</span></span>        | [<span data-ttu-id="f7f82-159">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f7f82-160">**Point de connexion**</span><span class="sxs-lookup"><span data-stu-id="f7f82-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f7f82-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="f7f82-161">ADAM</span></span>



| <span data-ttu-id="f7f82-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-162">Entry</span></span> | <span data-ttu-id="f7f82-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f7f82-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f7f82-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f7f82-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-166">System-Only</span></span>            | <span data-ttu-id="f7f82-167">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-167">False</span></span>                                                            |
| <span data-ttu-id="f7f82-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-168">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-169">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-169">False</span></span>                                                            |
| <span data-ttu-id="f7f82-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-170">Is Indexed</span></span>             | <span data-ttu-id="f7f82-171">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-171">False</span></span>                                                            |
| <span data-ttu-id="f7f82-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-172">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-173">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-173">False</span></span>                                                            |
| <span data-ttu-id="f7f82-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f7f82-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f7f82-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f7f82-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-178">Search-Flags</span></span>           | <span data-ttu-id="f7f82-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="f7f82-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-180">System-Flags</span></span>           | <span data-ttu-id="f7f82-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="f7f82-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-182">Classes used in</span></span>        | [<span data-ttu-id="f7f82-183">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7f82-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7f82-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7f82-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-185">Entry</span></span> | <span data-ttu-id="f7f82-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f82-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-189">System-Only</span></span>            | <span data-ttu-id="f7f82-190">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-192">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-193">Is Indexed</span></span>             | <span data-ttu-id="f7f82-194">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-195">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-196">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f7f82-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-201">Search-Flags</span></span>           | <span data-ttu-id="f7f82-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-203">System-Flags</span></span>           | <span data-ttu-id="f7f82-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-205">Classes used in</span></span>        | [<span data-ttu-id="f7f82-206">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f7f82-207">**Point de connexion**</span><span class="sxs-lookup"><span data-stu-id="f7f82-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7f82-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7f82-208">Windows Server 2008</span></span>



| <span data-ttu-id="f7f82-209">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-209">Entry</span></span> | <span data-ttu-id="f7f82-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f82-211">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-213">System-Only</span></span>            | <span data-ttu-id="f7f82-214">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-215">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-215">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-216">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-217">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-217">Is Indexed</span></span>             | <span data-ttu-id="f7f82-218">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-219">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-219">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-220">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-221">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-222">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f7f82-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-225">Search-Flags</span></span>           | <span data-ttu-id="f7f82-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-227">System-Flags</span></span>           | <span data-ttu-id="f7f82-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-229">Classes used in</span></span>        | [<span data-ttu-id="f7f82-230">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f7f82-231">**Point de connexion**</span><span class="sxs-lookup"><span data-stu-id="f7f82-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7f82-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7f82-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7f82-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-233">Entry</span></span> | <span data-ttu-id="f7f82-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f82-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-237">System-Only</span></span>            | <span data-ttu-id="f7f82-238">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-240">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-241">Is Indexed</span></span>             | <span data-ttu-id="f7f82-242">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-243">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-244">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f7f82-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-249">Search-Flags</span></span>           | <span data-ttu-id="f7f82-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-251">System-Flags</span></span>           | <span data-ttu-id="f7f82-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-253">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-253">Classes used in</span></span>        | [<span data-ttu-id="f7f82-254">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f7f82-255">**Point de connexion**</span><span class="sxs-lookup"><span data-stu-id="f7f82-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7f82-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7f82-256">Windows Server 2012</span></span>



| <span data-ttu-id="f7f82-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="f7f82-257">Entry</span></span> | <span data-ttu-id="f7f82-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f82-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f82-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f7f82-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f82-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f7f82-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f82-261">System-Only</span></span>            | <span data-ttu-id="f7f82-262">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f7f82-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f82-264">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f7f82-265">Is Indexed</span></span>             | <span data-ttu-id="f7f82-266">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f7f82-267">In Global Catalog</span></span>      | <span data-ttu-id="f7f82-268">Faux</span><span class="sxs-lookup"><span data-stu-id="f7f82-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="f7f82-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f7f82-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f82-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f7f82-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f7f82-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f82-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f82-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f7f82-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-273">Search-Flags</span></span>           | <span data-ttu-id="f7f82-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f82-275">System-Flags</span></span>           | <span data-ttu-id="f7f82-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f82-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f7f82-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f7f82-277">Classes used in</span></span>        | [<span data-ttu-id="f7f82-278">**Paramètres de l’application**</span><span class="sxs-lookup"><span data-stu-id="f7f82-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f7f82-279">**Point de connexion**</span><span class="sxs-lookup"><span data-stu-id="f7f82-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





