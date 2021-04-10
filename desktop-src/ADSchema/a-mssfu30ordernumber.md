---
title: attribut msSFU-30-Order-Number
description: Contient une valeur utilisée par NIS pour vérifier si le mappage a changé.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory msSFU-30-Order-Number
- Schéma AD de l’attribut msSFU30OrderNumber
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107704"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="6db1a-105">attribut msSFU-30-Order-Number</span><span class="sxs-lookup"><span data-stu-id="6db1a-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="6db1a-106">Contient une valeur utilisée par NIS pour vérifier si le mappage a changé.</span><span class="sxs-lookup"><span data-stu-id="6db1a-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="6db1a-107">Chaque fois que les données stockées dans l’objet [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md) changent, cette valeur est incrémentée.</span><span class="sxs-lookup"><span data-stu-id="6db1a-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="6db1a-108">Cette valeur est utilisée pour suivre les modifications de données entre les appels **ypxfer** .</span><span class="sxs-lookup"><span data-stu-id="6db1a-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="6db1a-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="6db1a-109">Entry</span></span> | <span data-ttu-id="6db1a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db1a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6db1a-111">CN</span><span class="sxs-lookup"><span data-stu-id="6db1a-111">CN</span></span>                | <span data-ttu-id="6db1a-112">msSFU-30-Order-Number</span><span class="sxs-lookup"><span data-stu-id="6db1a-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="6db1a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6db1a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6db1a-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="6db1a-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="6db1a-115">Taille</span><span class="sxs-lookup"><span data-stu-id="6db1a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6db1a-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6db1a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6db1a-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6db1a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6db1a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6db1a-118">Attribute-Id</span></span>      | <span data-ttu-id="6db1a-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="6db1a-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="6db1a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6db1a-120">System-Id-Guid</span></span>    | <span data-ttu-id="6db1a-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="6db1a-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="6db1a-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6db1a-122">Syntax</span></span>            | [<span data-ttu-id="6db1a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6db1a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6db1a-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6db1a-124">Implementations</span></span>

-   [<span data-ttu-id="6db1a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6db1a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6db1a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6db1a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6db1a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6db1a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6db1a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6db1a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="6db1a-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6db1a-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6db1a-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="6db1a-130">Entry</span></span> | <span data-ttu-id="6db1a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db1a-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6db1a-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6db1a-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db1a-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db1a-134">System-Only</span></span>            | <span data-ttu-id="6db1a-135">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-135">False</span></span>                                                          |
| <span data-ttu-id="6db1a-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6db1a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6db1a-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-137">True</span></span>                                                           |
| <span data-ttu-id="6db1a-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6db1a-138">Is Indexed</span></span>             | <span data-ttu-id="6db1a-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-139">True</span></span>                                                           |
| <span data-ttu-id="6db1a-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6db1a-140">In Global Catalog</span></span>      | <span data-ttu-id="6db1a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-141">False</span></span>                                                          |
| <span data-ttu-id="6db1a-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6db1a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db1a-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6db1a-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6db1a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db1a-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db1a-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-146">Search-Flags</span></span>           | <span data-ttu-id="6db1a-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db1a-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="6db1a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-148">System-Flags</span></span>           | <span data-ttu-id="6db1a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6db1a-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="6db1a-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6db1a-150">Classes used in</span></span>        | [<span data-ttu-id="6db1a-151">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6db1a-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6db1a-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6db1a-152">Windows Server 2008</span></span>



| <span data-ttu-id="6db1a-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="6db1a-153">Entry</span></span> | <span data-ttu-id="6db1a-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db1a-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6db1a-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6db1a-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db1a-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db1a-157">System-Only</span></span>            | <span data-ttu-id="6db1a-158">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-158">False</span></span>                                                          |
| <span data-ttu-id="6db1a-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6db1a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6db1a-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-160">True</span></span>                                                           |
| <span data-ttu-id="6db1a-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6db1a-161">Is Indexed</span></span>             | <span data-ttu-id="6db1a-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-162">True</span></span>                                                           |
| <span data-ttu-id="6db1a-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6db1a-163">In Global Catalog</span></span>      | <span data-ttu-id="6db1a-164">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-164">False</span></span>                                                          |
| <span data-ttu-id="6db1a-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6db1a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db1a-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6db1a-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6db1a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db1a-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db1a-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-169">Search-Flags</span></span>           | <span data-ttu-id="6db1a-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db1a-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="6db1a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-171">System-Flags</span></span>           | <span data-ttu-id="6db1a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6db1a-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="6db1a-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6db1a-173">Classes used in</span></span>        | [<span data-ttu-id="6db1a-174">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6db1a-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6db1a-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6db1a-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6db1a-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="6db1a-176">Entry</span></span> | <span data-ttu-id="6db1a-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db1a-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6db1a-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6db1a-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db1a-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db1a-180">System-Only</span></span>            | <span data-ttu-id="6db1a-181">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-181">False</span></span>                                                          |
| <span data-ttu-id="6db1a-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6db1a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6db1a-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-183">True</span></span>                                                           |
| <span data-ttu-id="6db1a-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6db1a-184">Is Indexed</span></span>             | <span data-ttu-id="6db1a-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-185">True</span></span>                                                           |
| <span data-ttu-id="6db1a-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6db1a-186">In Global Catalog</span></span>      | <span data-ttu-id="6db1a-187">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-187">False</span></span>                                                          |
| <span data-ttu-id="6db1a-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6db1a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db1a-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6db1a-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6db1a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db1a-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db1a-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-192">Search-Flags</span></span>           | <span data-ttu-id="6db1a-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db1a-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="6db1a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-194">System-Flags</span></span>           | <span data-ttu-id="6db1a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6db1a-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="6db1a-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6db1a-196">Classes used in</span></span>        | [<span data-ttu-id="6db1a-197">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6db1a-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6db1a-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6db1a-198">Windows Server 2012</span></span>



| <span data-ttu-id="6db1a-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="6db1a-199">Entry</span></span> | <span data-ttu-id="6db1a-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db1a-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6db1a-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6db1a-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db1a-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6db1a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db1a-203">System-Only</span></span>            | <span data-ttu-id="6db1a-204">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-204">False</span></span>                                                          |
| <span data-ttu-id="6db1a-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6db1a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6db1a-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-206">True</span></span>                                                           |
| <span data-ttu-id="6db1a-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6db1a-207">Is Indexed</span></span>             | <span data-ttu-id="6db1a-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="6db1a-208">True</span></span>                                                           |
| <span data-ttu-id="6db1a-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6db1a-209">In Global Catalog</span></span>      | <span data-ttu-id="6db1a-210">Faux</span><span class="sxs-lookup"><span data-stu-id="6db1a-210">False</span></span>                                                          |
| <span data-ttu-id="6db1a-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6db1a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db1a-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6db1a-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6db1a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db1a-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db1a-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6db1a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-215">Search-Flags</span></span>           | <span data-ttu-id="6db1a-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db1a-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="6db1a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db1a-217">System-Flags</span></span>           | <span data-ttu-id="6db1a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6db1a-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="6db1a-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6db1a-219">Classes used in</span></span>        | [<span data-ttu-id="6db1a-220">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6db1a-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





