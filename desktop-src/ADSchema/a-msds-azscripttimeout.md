---
title: ms-DS-AZ-script-Timeout (attribut)
description: Durée d’attente maximale, en millisecondes, d’un script pour terminer l’audit d’une stratégie spécifique.
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-AZ-script-Timeout
- Schéma Active Directory de l’attribut msDS-AzScriptTimeout
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385460"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="e3a9c-105">ms-DS-AZ-script-Timeout (attribut)</span><span class="sxs-lookup"><span data-stu-id="e3a9c-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="e3a9c-106">Durée d’attente maximale, en millisecondes, d’un script pour terminer l’audit d’une stratégie spécifique.</span><span class="sxs-lookup"><span data-stu-id="e3a9c-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="e3a9c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-107">Entry</span></span> | <span data-ttu-id="e3a9c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e3a9c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e3a9c-109">CN</span></span>                | <span data-ttu-id="e3a9c-110">ms-DS-AZ-script-Timeout</span><span class="sxs-lookup"><span data-stu-id="e3a9c-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="e3a9c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3a9c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e3a9c-112">msDS-AzScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="e3a9c-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="e3a9c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e3a9c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e3a9c-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e3a9c-114">Update Privilege</span></span>  | <span data-ttu-id="e3a9c-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="e3a9c-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="e3a9c-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e3a9c-116">Update Frequency</span></span>  | <span data-ttu-id="e3a9c-117">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e3a9c-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="e3a9c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-118">Attribute-Id</span></span>      | <span data-ttu-id="e3a9c-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="e3a9c-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="e3a9c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3a9c-120">System-Id-Guid</span></span>    | <span data-ttu-id="e3a9c-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span><span class="sxs-lookup"><span data-stu-id="e3a9c-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="e3a9c-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3a9c-122">Syntax</span></span>            | [<span data-ttu-id="e3a9c-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="e3a9c-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e3a9c-124">Implementations</span></span>

-   [<span data-ttu-id="e3a9c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3a9c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3a9c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3a9c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3a9c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e3a9c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3a9c-130">Windows Server 2003</span></span>



| <span data-ttu-id="e3a9c-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-131">Entry</span></span> | <span data-ttu-id="e3a9c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e3a9c-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3a9c-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3a9c-135">System-Only</span></span>            | <span data-ttu-id="e3a9c-136">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-136">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3a9c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e3a9c-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3a9c-138">True</span></span>                                                               |
| <span data-ttu-id="e3a9c-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3a9c-139">Is Indexed</span></span>             | <span data-ttu-id="e3a9c-140">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-140">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3a9c-141">In Global Catalog</span></span>      | <span data-ttu-id="e3a9c-142">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-142">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3a9c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3a9c-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3a9c-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e3a9c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3a9c-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3a9c-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-147">Search-Flags</span></span>           | <span data-ttu-id="e3a9c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3a9c-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="e3a9c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-149">System-Flags</span></span>           | <span data-ttu-id="e3a9c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3a9c-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="e3a9c-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3a9c-151">Classes used in</span></span>        | [<span data-ttu-id="e3a9c-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3a9c-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3a9c-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3a9c-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-154">Entry</span></span> | <span data-ttu-id="e3a9c-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e3a9c-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3a9c-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3a9c-158">System-Only</span></span>            | <span data-ttu-id="e3a9c-159">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-159">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3a9c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e3a9c-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3a9c-161">True</span></span>                                                               |
| <span data-ttu-id="e3a9c-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3a9c-162">Is Indexed</span></span>             | <span data-ttu-id="e3a9c-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-163">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3a9c-164">In Global Catalog</span></span>      | <span data-ttu-id="e3a9c-165">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-165">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3a9c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3a9c-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3a9c-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e3a9c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3a9c-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3a9c-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-170">Search-Flags</span></span>           | <span data-ttu-id="e3a9c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3a9c-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="e3a9c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-172">System-Flags</span></span>           | <span data-ttu-id="e3a9c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3a9c-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="e3a9c-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3a9c-174">Classes used in</span></span>        | [<span data-ttu-id="e3a9c-175">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3a9c-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3a9c-176">Windows Server 2008</span></span>



| <span data-ttu-id="e3a9c-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-177">Entry</span></span> | <span data-ttu-id="e3a9c-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e3a9c-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3a9c-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3a9c-181">System-Only</span></span>            | <span data-ttu-id="e3a9c-182">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-182">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3a9c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e3a9c-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3a9c-184">True</span></span>                                                               |
| <span data-ttu-id="e3a9c-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3a9c-185">Is Indexed</span></span>             | <span data-ttu-id="e3a9c-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-186">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3a9c-187">In Global Catalog</span></span>      | <span data-ttu-id="e3a9c-188">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-188">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3a9c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3a9c-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3a9c-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e3a9c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3a9c-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3a9c-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-193">Search-Flags</span></span>           | <span data-ttu-id="e3a9c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3a9c-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="e3a9c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-195">System-Flags</span></span>           | <span data-ttu-id="e3a9c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3a9c-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="e3a9c-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3a9c-197">Classes used in</span></span>        | [<span data-ttu-id="e3a9c-198">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3a9c-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3a9c-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3a9c-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-200">Entry</span></span> | <span data-ttu-id="e3a9c-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e3a9c-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3a9c-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3a9c-204">System-Only</span></span>            | <span data-ttu-id="e3a9c-205">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-205">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3a9c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e3a9c-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3a9c-207">True</span></span>                                                               |
| <span data-ttu-id="e3a9c-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3a9c-208">Is Indexed</span></span>             | <span data-ttu-id="e3a9c-209">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-209">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3a9c-210">In Global Catalog</span></span>      | <span data-ttu-id="e3a9c-211">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-211">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3a9c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3a9c-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3a9c-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e3a9c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3a9c-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3a9c-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-216">Search-Flags</span></span>           | <span data-ttu-id="e3a9c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3a9c-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="e3a9c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-218">System-Flags</span></span>           | <span data-ttu-id="e3a9c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3a9c-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="e3a9c-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3a9c-220">Classes used in</span></span>        | [<span data-ttu-id="e3a9c-221">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3a9c-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3a9c-222">Windows Server 2012</span></span>



| <span data-ttu-id="e3a9c-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3a9c-223">Entry</span></span> | <span data-ttu-id="e3a9c-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3a9c-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e3a9c-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3a9c-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3a9c-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e3a9c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3a9c-227">System-Only</span></span>            | <span data-ttu-id="e3a9c-228">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-228">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3a9c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e3a9c-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3a9c-230">True</span></span>                                                               |
| <span data-ttu-id="e3a9c-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3a9c-231">Is Indexed</span></span>             | <span data-ttu-id="e3a9c-232">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-232">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3a9c-233">In Global Catalog</span></span>      | <span data-ttu-id="e3a9c-234">Faux</span><span class="sxs-lookup"><span data-stu-id="e3a9c-234">False</span></span>                                                              |
| <span data-ttu-id="e3a9c-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3a9c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3a9c-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3a9c-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e3a9c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3a9c-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3a9c-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="e3a9c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-239">Search-Flags</span></span>           | <span data-ttu-id="e3a9c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3a9c-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="e3a9c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3a9c-241">System-Flags</span></span>           | <span data-ttu-id="e3a9c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3a9c-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="e3a9c-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3a9c-243">Classes used in</span></span>        | [<span data-ttu-id="e3a9c-244">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e3a9c-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





