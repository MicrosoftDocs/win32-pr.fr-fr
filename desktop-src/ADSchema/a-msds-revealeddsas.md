---
title: attribut ms-DS-Reveal-DSA
description: Lien vers l’arrière pour ms-DS-Revealed-Users. Identifie le RODC qui détient le secret de l’utilisateur.
ms.assetid: cd84db75-d961-4290-8aa7-2805febbd842
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut DSA de ms-DS-Reveal
- Schéma Active Directory de l’attribut msDS-RevealedDSAs
topic_type:
- apiref
api_name:
- ms-DS-Revealed-DSAs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77dfd69fafffc3286f0ff9419965d7ae9daaa0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480069"
---
# <a name="ms-ds-revealed-dsas-attribute"></a><span data-ttu-id="00031-106">attribut ms-DS-Reveal-DSA</span><span class="sxs-lookup"><span data-stu-id="00031-106">ms-DS-Revealed-DSAs attribute</span></span>

<span data-ttu-id="00031-107">Lien vers l’arrière pour [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span><span class="sxs-lookup"><span data-stu-id="00031-107">Backward link for [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span></span> <span data-ttu-id="00031-108">Identifie le contrôleur de domaine en lecture seule qui détient le secret de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00031-108">Identifies which RODC holds that user's secret.</span></span>



| <span data-ttu-id="00031-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="00031-109">Entry</span></span> | <span data-ttu-id="00031-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="00031-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="00031-111">CN</span><span class="sxs-lookup"><span data-stu-id="00031-111">CN</span></span>                | <span data-ttu-id="00031-112">ms-DS-dévoilé-DSA</span><span class="sxs-lookup"><span data-stu-id="00031-112">ms-DS-Revealed-DSAs</span></span>                     |
| <span data-ttu-id="00031-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="00031-113">Ldap-Display-Name</span></span> | <span data-ttu-id="00031-114">msDS-RevealedDSAs</span><span class="sxs-lookup"><span data-stu-id="00031-114">msDS-RevealedDSAs</span></span>                       |
| <span data-ttu-id="00031-115">Taille</span><span class="sxs-lookup"><span data-stu-id="00031-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="00031-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="00031-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="00031-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="00031-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="00031-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00031-118">Attribute-Id</span></span>      | <span data-ttu-id="00031-119">1.2.840.113556.1.4.1930</span><span class="sxs-lookup"><span data-stu-id="00031-119">1.2.840.113556.1.4.1930</span></span>                 |
| <span data-ttu-id="00031-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00031-120">System-Id-Guid</span></span>    | <span data-ttu-id="00031-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span><span class="sxs-lookup"><span data-stu-id="00031-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span></span>    |
| <span data-ttu-id="00031-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00031-122">Syntax</span></span>            | [<span data-ttu-id="00031-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="00031-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="00031-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="00031-124">Implementations</span></span>

-   [<span data-ttu-id="00031-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00031-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00031-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00031-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00031-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00031-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="00031-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00031-128">Windows Server 2008</span></span>



| <span data-ttu-id="00031-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="00031-129">Entry</span></span> | <span data-ttu-id="00031-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="00031-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00031-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00031-131">Link-Id</span></span>                | <span data-ttu-id="00031-132">2103</span><span class="sxs-lookup"><span data-stu-id="00031-132">2103</span></span>                            |
| <span data-ttu-id="00031-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00031-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00031-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="00031-134">System-Only</span></span>            | <span data-ttu-id="00031-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="00031-135">True</span></span>                            |
| <span data-ttu-id="00031-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00031-136">Is-Single-Valued</span></span>       | <span data-ttu-id="00031-137">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-137">False</span></span>                           |
| <span data-ttu-id="00031-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00031-138">Is Indexed</span></span>             | <span data-ttu-id="00031-139">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-139">False</span></span>                           |
| <span data-ttu-id="00031-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00031-140">In Global Catalog</span></span>      | <span data-ttu-id="00031-141">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-141">False</span></span>                           |
| <span data-ttu-id="00031-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00031-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="00031-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00031-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00031-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00031-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00031-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00031-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00031-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-146">Search-Flags</span></span>           | <span data-ttu-id="00031-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00031-147">0x00000000</span></span>                      |
| <span data-ttu-id="00031-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-148">System-Flags</span></span>           | <span data-ttu-id="00031-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="00031-149">0x00000011</span></span>                      |
| <span data-ttu-id="00031-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00031-150">Classes used in</span></span>        | [<span data-ttu-id="00031-151">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="00031-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00031-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00031-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00031-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="00031-153">Entry</span></span> | <span data-ttu-id="00031-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="00031-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00031-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00031-155">Link-Id</span></span>                | <span data-ttu-id="00031-156">2103</span><span class="sxs-lookup"><span data-stu-id="00031-156">2103</span></span>                            |
| <span data-ttu-id="00031-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00031-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00031-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="00031-158">System-Only</span></span>            | <span data-ttu-id="00031-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="00031-159">True</span></span>                            |
| <span data-ttu-id="00031-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00031-160">Is-Single-Valued</span></span>       | <span data-ttu-id="00031-161">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-161">False</span></span>                           |
| <span data-ttu-id="00031-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00031-162">Is Indexed</span></span>             | <span data-ttu-id="00031-163">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-163">False</span></span>                           |
| <span data-ttu-id="00031-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00031-164">In Global Catalog</span></span>      | <span data-ttu-id="00031-165">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-165">False</span></span>                           |
| <span data-ttu-id="00031-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00031-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="00031-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00031-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00031-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00031-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00031-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00031-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00031-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-170">Search-Flags</span></span>           | <span data-ttu-id="00031-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00031-171">0x00000000</span></span>                      |
| <span data-ttu-id="00031-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-172">System-Flags</span></span>           | <span data-ttu-id="00031-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="00031-173">0x00000011</span></span>                      |
| <span data-ttu-id="00031-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00031-174">Classes used in</span></span>        | [<span data-ttu-id="00031-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="00031-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00031-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00031-176">Windows Server 2012</span></span>



| <span data-ttu-id="00031-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="00031-177">Entry</span></span> | <span data-ttu-id="00031-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="00031-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00031-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="00031-179">Link-Id</span></span>                | <span data-ttu-id="00031-180">2103</span><span class="sxs-lookup"><span data-stu-id="00031-180">2103</span></span>                            |
| <span data-ttu-id="00031-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00031-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00031-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="00031-182">System-Only</span></span>            | <span data-ttu-id="00031-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="00031-183">True</span></span>                            |
| <span data-ttu-id="00031-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="00031-184">Is-Single-Valued</span></span>       | <span data-ttu-id="00031-185">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-185">False</span></span>                           |
| <span data-ttu-id="00031-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="00031-186">Is Indexed</span></span>             | <span data-ttu-id="00031-187">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-187">False</span></span>                           |
| <span data-ttu-id="00031-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="00031-188">In Global Catalog</span></span>      | <span data-ttu-id="00031-189">Faux</span><span class="sxs-lookup"><span data-stu-id="00031-189">False</span></span>                           |
| <span data-ttu-id="00031-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="00031-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="00031-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="00031-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00031-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00031-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00031-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00031-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00031-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-194">Search-Flags</span></span>           | <span data-ttu-id="00031-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00031-195">0x00000000</span></span>                      |
| <span data-ttu-id="00031-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00031-196">System-Flags</span></span>           | <span data-ttu-id="00031-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="00031-197">0x00000011</span></span>                      |
| <span data-ttu-id="00031-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="00031-198">Classes used in</span></span>        | [<span data-ttu-id="00031-199">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="00031-199">**Top**</span></span>](c-top.md)<br/> |



 

 





