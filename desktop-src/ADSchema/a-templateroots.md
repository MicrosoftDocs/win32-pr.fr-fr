---
title: Attribut Template-Roots
description: Cet attribut est utilisé sur le conteneur de configuration Exchange pour indiquer l’emplacement de stockage des conteneurs de modèles. Ces informations sont utilisées par le fournisseur MAPI Active Directory.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Template-Roots
- Schéma AD de l’attribut templateRoots
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744900"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="fd9cb-106">Attribut Template-Roots</span><span class="sxs-lookup"><span data-stu-id="fd9cb-106">Template-Roots attribute</span></span>

<span data-ttu-id="fd9cb-107">Cet attribut est utilisé sur le conteneur de configuration Exchange pour indiquer l’emplacement de stockage des conteneurs de modèles.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="fd9cb-108">Ces informations sont utilisées par le fournisseur MAPI Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="fd9cb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-109">Entry</span></span> | <span data-ttu-id="fd9cb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="fd9cb-111">CN</span><span class="sxs-lookup"><span data-stu-id="fd9cb-111">CN</span></span>                | <span data-ttu-id="fd9cb-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="fd9cb-112">Template-Roots</span></span>                          |
| <span data-ttu-id="fd9cb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fd9cb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fd9cb-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="fd9cb-114">templateRoots</span></span>                           |
| <span data-ttu-id="fd9cb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="fd9cb-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="fd9cb-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="fd9cb-116">Update Privilege</span></span>  | <span data-ttu-id="fd9cb-117">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="fd9cb-117">This is used by the system.</span></span>             |
| <span data-ttu-id="fd9cb-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="fd9cb-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="fd9cb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-119">Attribute-Id</span></span>      | <span data-ttu-id="fd9cb-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="fd9cb-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="fd9cb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fd9cb-121">System-Id-Guid</span></span>    | <span data-ttu-id="fd9cb-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="fd9cb-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="fd9cb-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd9cb-123">Syntax</span></span>            | [<span data-ttu-id="fd9cb-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="fd9cb-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="fd9cb-125">Implementations</span></span>

-   [<span data-ttu-id="fd9cb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fd9cb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fd9cb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fd9cb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fd9cb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fd9cb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fd9cb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd9cb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fd9cb-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-133">Entry</span></span> | <span data-ttu-id="fd9cb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-137">System-Only</span></span>            | <span data-ttu-id="fd9cb-138">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-138">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-140">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-141">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-142">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-142">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-143">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-144">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-144">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-149">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-151">System-Flags</span></span>           | <span data-ttu-id="fd9cb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-153">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-154">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fd9cb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd9cb-155">Windows Server 2003</span></span>



| <span data-ttu-id="fd9cb-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-156">Entry</span></span> | <span data-ttu-id="fd9cb-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-160">System-Only</span></span>            | <span data-ttu-id="fd9cb-161">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-161">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-163">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-164">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-165">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-165">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-166">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-167">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-172">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-174">System-Flags</span></span>           | <span data-ttu-id="fd9cb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-176">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-177">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fd9cb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fd9cb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fd9cb-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-179">Entry</span></span> | <span data-ttu-id="fd9cb-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-183">System-Only</span></span>            | <span data-ttu-id="fd9cb-184">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-184">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-186">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-186">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-187">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-188">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-188">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-189">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-190">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-195">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-197">System-Flags</span></span>           | <span data-ttu-id="fd9cb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-199">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-200">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fd9cb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd9cb-201">Windows Server 2008</span></span>



| <span data-ttu-id="fd9cb-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-202">Entry</span></span> | <span data-ttu-id="fd9cb-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-206">System-Only</span></span>            | <span data-ttu-id="fd9cb-207">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-207">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-209">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-209">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-210">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-211">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-211">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-212">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-213">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-213">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-218">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-220">System-Flags</span></span>           | <span data-ttu-id="fd9cb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-222">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-223">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fd9cb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd9cb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fd9cb-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-225">Entry</span></span> | <span data-ttu-id="fd9cb-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-229">System-Only</span></span>            | <span data-ttu-id="fd9cb-230">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-230">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-232">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-233">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-234">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-234">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-235">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-236">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-241">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-243">System-Flags</span></span>           | <span data-ttu-id="fd9cb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-245">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-246">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fd9cb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd9cb-247">Windows Server 2012</span></span>



| <span data-ttu-id="fd9cb-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="fd9cb-248">Entry</span></span> | <span data-ttu-id="fd9cb-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9cb-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9cb-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fd9cb-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd9cb-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fd9cb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd9cb-252">System-Only</span></span>            | <span data-ttu-id="fd9cb-253">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-253">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fd9cb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fd9cb-255">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-255">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fd9cb-256">Is Indexed</span></span>             | <span data-ttu-id="fd9cb-257">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-257">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fd9cb-258">In Global Catalog</span></span>      | <span data-ttu-id="fd9cb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="fd9cb-259">False</span></span>                                                                                |
| <span data-ttu-id="fd9cb-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fd9cb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd9cb-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fd9cb-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fd9cb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd9cb-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd9cb-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fd9cb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-264">Search-Flags</span></span>           | <span data-ttu-id="fd9cb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd9cb-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fd9cb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd9cb-266">System-Flags</span></span>           | <span data-ttu-id="fd9cb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd9cb-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fd9cb-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fd9cb-268">Classes used in</span></span>        | [<span data-ttu-id="fd9cb-269">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="fd9cb-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





