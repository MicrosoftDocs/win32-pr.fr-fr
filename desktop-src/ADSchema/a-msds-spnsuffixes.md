---
title: attribut ms-DS-SPN-suffixes
description: Cet attribut décrit les suffixes des noms d’hôtes DNS utilisés par les serveurs de la forêt. Ces suffixes DNS seront partagés avec d’autres forêts qui ont une approbation inter-forêts avec cette forêt.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-SPN-suffixes
- Schéma Active Directory de l’attribut msDS-SPNSuffixes
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943168"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="b7e9b-106">attribut ms-DS-SPN-suffixes</span><span class="sxs-lookup"><span data-stu-id="b7e9b-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="b7e9b-107">Cet attribut décrit les suffixes des noms d’hôtes DNS utilisés par les serveurs de la forêt.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="b7e9b-108">Ces suffixes DNS seront partagés avec d’autres forêts qui ont une approbation inter-forêts avec cette forêt.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="b7e9b-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-109">Entry</span></span> | <span data-ttu-id="b7e9b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="b7e9b-111">CN</span><span class="sxs-lookup"><span data-stu-id="b7e9b-111">CN</span></span>                | <span data-ttu-id="b7e9b-112">ms-DS-SPN-suffixes</span><span class="sxs-lookup"><span data-stu-id="b7e9b-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="b7e9b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7e9b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b7e9b-114">msDS-SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="b7e9b-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="b7e9b-115">Taille</span><span class="sxs-lookup"><span data-stu-id="b7e9b-115">Size</span></span>              | <span data-ttu-id="b7e9b-116">255 octets</span><span class="sxs-lookup"><span data-stu-id="b7e9b-116">255 bytes</span></span>                                    |
| <span data-ttu-id="b7e9b-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b7e9b-117">Update Privilege</span></span>  | <span data-ttu-id="b7e9b-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="b7e9b-118">Domain administrator</span></span>                         |
| <span data-ttu-id="b7e9b-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b7e9b-119">Update Frequency</span></span>  | <span data-ttu-id="b7e9b-120">Lorsque les serveurs de la forêt obtiennent un nouveau suffixe.</span><span class="sxs-lookup"><span data-stu-id="b7e9b-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="b7e9b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-121">Attribute-Id</span></span>      | <span data-ttu-id="b7e9b-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="b7e9b-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="b7e9b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7e9b-123">System-Id-Guid</span></span>    | <span data-ttu-id="b7e9b-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="b7e9b-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="b7e9b-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7e9b-125">Syntax</span></span>            | [<span data-ttu-id="b7e9b-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="b7e9b-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b7e9b-127">Implementations</span></span>

-   [<span data-ttu-id="b7e9b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7e9b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7e9b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7e9b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7e9b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b7e9b-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7e9b-133">Windows Server 2003</span></span>



| <span data-ttu-id="b7e9b-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-134">Entry</span></span> | <span data-ttu-id="b7e9b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e9b-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b7e9b-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7e9b-138">System-Only</span></span>            | <span data-ttu-id="b7e9b-139">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-139">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b7e9b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b7e9b-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-141">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b7e9b-142">Is Indexed</span></span>             | <span data-ttu-id="b7e9b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-143">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b7e9b-144">In Global Catalog</span></span>      | <span data-ttu-id="b7e9b-145">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-145">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b7e9b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7e9b-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b7e9b-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b7e9b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7e9b-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7e9b-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-150">Search-Flags</span></span>           | <span data-ttu-id="b7e9b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7e9b-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="b7e9b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-152">System-Flags</span></span>           | <span data-ttu-id="b7e9b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7e9b-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="b7e9b-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b7e9b-154">Classes used in</span></span>        | [<span data-ttu-id="b7e9b-155">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7e9b-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7e9b-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7e9b-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-157">Entry</span></span> | <span data-ttu-id="b7e9b-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e9b-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b7e9b-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7e9b-161">System-Only</span></span>            | <span data-ttu-id="b7e9b-162">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-162">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b7e9b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b7e9b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-164">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b7e9b-165">Is Indexed</span></span>             | <span data-ttu-id="b7e9b-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-166">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b7e9b-167">In Global Catalog</span></span>      | <span data-ttu-id="b7e9b-168">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-168">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b7e9b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7e9b-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b7e9b-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b7e9b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7e9b-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7e9b-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-173">Search-Flags</span></span>           | <span data-ttu-id="b7e9b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7e9b-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="b7e9b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-175">System-Flags</span></span>           | <span data-ttu-id="b7e9b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7e9b-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="b7e9b-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b7e9b-177">Classes used in</span></span>        | [<span data-ttu-id="b7e9b-178">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7e9b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e9b-179">Windows Server 2008</span></span>



| <span data-ttu-id="b7e9b-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-180">Entry</span></span> | <span data-ttu-id="b7e9b-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e9b-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b7e9b-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7e9b-184">System-Only</span></span>            | <span data-ttu-id="b7e9b-185">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-185">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b7e9b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b7e9b-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-187">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b7e9b-188">Is Indexed</span></span>             | <span data-ttu-id="b7e9b-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-189">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b7e9b-190">In Global Catalog</span></span>      | <span data-ttu-id="b7e9b-191">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-191">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b7e9b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7e9b-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b7e9b-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b7e9b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7e9b-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7e9b-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-196">Search-Flags</span></span>           | <span data-ttu-id="b7e9b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7e9b-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="b7e9b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-198">System-Flags</span></span>           | <span data-ttu-id="b7e9b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7e9b-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="b7e9b-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b7e9b-200">Classes used in</span></span>        | [<span data-ttu-id="b7e9b-201">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7e9b-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7e9b-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7e9b-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-203">Entry</span></span> | <span data-ttu-id="b7e9b-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e9b-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b7e9b-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7e9b-207">System-Only</span></span>            | <span data-ttu-id="b7e9b-208">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-208">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b7e9b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b7e9b-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-210">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b7e9b-211">Is Indexed</span></span>             | <span data-ttu-id="b7e9b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-212">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b7e9b-213">In Global Catalog</span></span>      | <span data-ttu-id="b7e9b-214">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-214">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b7e9b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7e9b-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b7e9b-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b7e9b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7e9b-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7e9b-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-219">Search-Flags</span></span>           | <span data-ttu-id="b7e9b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7e9b-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="b7e9b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-221">System-Flags</span></span>           | <span data-ttu-id="b7e9b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7e9b-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="b7e9b-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b7e9b-223">Classes used in</span></span>        | [<span data-ttu-id="b7e9b-224">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7e9b-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7e9b-225">Windows Server 2012</span></span>



| <span data-ttu-id="b7e9b-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="b7e9b-226">Entry</span></span> | <span data-ttu-id="b7e9b-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e9b-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e9b-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b7e9b-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7e9b-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b7e9b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7e9b-230">System-Only</span></span>            | <span data-ttu-id="b7e9b-231">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-231">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b7e9b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b7e9b-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-233">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b7e9b-234">Is Indexed</span></span>             | <span data-ttu-id="b7e9b-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-235">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b7e9b-236">In Global Catalog</span></span>      | <span data-ttu-id="b7e9b-237">Faux</span><span class="sxs-lookup"><span data-stu-id="b7e9b-237">False</span></span>                                                         |
| <span data-ttu-id="b7e9b-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b7e9b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7e9b-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b7e9b-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b7e9b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7e9b-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7e9b-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b7e9b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-242">Search-Flags</span></span>           | <span data-ttu-id="b7e9b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7e9b-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="b7e9b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7e9b-244">System-Flags</span></span>           | <span data-ttu-id="b7e9b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7e9b-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="b7e9b-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b7e9b-246">Classes used in</span></span>        | [<span data-ttu-id="b7e9b-247">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="b7e9b-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





