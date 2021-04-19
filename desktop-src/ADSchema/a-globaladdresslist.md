---
title: Attribut Global-Address-List
description: Cet attribut est utilisé sur un conteneur Microsoft Exchange pour stocker le nom unique d’une liste d’adresses globale (GAL) nouvellement créée.
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Global-Address-List
- Schéma AD de l’attribut globalAddressList
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106543431"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="d75e0-105">Attribut Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="d75e0-105">Global-Address-List attribute</span></span>

<span data-ttu-id="d75e0-106">Cet attribut est utilisé sur un conteneur Microsoft Exchange pour stocker le nom unique d’une liste d’adresses globale (GAL) nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="d75e0-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="d75e0-107">Cet attribut doit avoir une entrée pour que vous puissiez permettre aux clients MAPI (Messaging Application Programming Interface) d’utiliser une liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="d75e0-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="d75e0-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-108">Entry</span></span> | <span data-ttu-id="d75e0-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d75e0-110">CN</span><span class="sxs-lookup"><span data-stu-id="d75e0-110">CN</span></span>                | <span data-ttu-id="d75e0-111">Liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="d75e0-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="d75e0-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d75e0-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d75e0-113">globalAddressList</span><span class="sxs-lookup"><span data-stu-id="d75e0-113">globalAddressList</span></span>                       |
| <span data-ttu-id="d75e0-114">Taille</span><span class="sxs-lookup"><span data-stu-id="d75e0-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="d75e0-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d75e0-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d75e0-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d75e0-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d75e0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-117">Attribute-Id</span></span>      | <span data-ttu-id="d75e0-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="d75e0-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="d75e0-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d75e0-119">System-Id-Guid</span></span>    | <span data-ttu-id="d75e0-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="d75e0-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="d75e0-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d75e0-121">Syntax</span></span>            | [<span data-ttu-id="d75e0-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d75e0-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d75e0-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d75e0-123">Implementations</span></span>

-   [<span data-ttu-id="d75e0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d75e0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d75e0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d75e0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d75e0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d75e0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d75e0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d75e0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d75e0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d75e0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d75e0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d75e0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d75e0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d75e0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d75e0-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-131">Entry</span></span> | <span data-ttu-id="d75e0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-135">System-Only</span></span>            | <span data-ttu-id="d75e0-136">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-136">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-138">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-138">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-139">Is Indexed</span></span>             | <span data-ttu-id="d75e0-140">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-140">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-141">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-142">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-147">Search-Flags</span></span>           | <span data-ttu-id="d75e0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-149">System-Flags</span></span>           | <span data-ttu-id="d75e0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-151">Classes used in</span></span>        | [<span data-ttu-id="d75e0-152">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d75e0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d75e0-153">Windows Server 2003</span></span>



| <span data-ttu-id="d75e0-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-154">Entry</span></span> | <span data-ttu-id="d75e0-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-158">System-Only</span></span>            | <span data-ttu-id="d75e0-159">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-159">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-161">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-161">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-162">Is Indexed</span></span>             | <span data-ttu-id="d75e0-163">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-163">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-164">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-165">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-165">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-170">Search-Flags</span></span>           | <span data-ttu-id="d75e0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-172">System-Flags</span></span>           | <span data-ttu-id="d75e0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-174">Classes used in</span></span>        | [<span data-ttu-id="d75e0-175">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d75e0-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d75e0-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d75e0-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-177">Entry</span></span> | <span data-ttu-id="d75e0-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-181">System-Only</span></span>            | <span data-ttu-id="d75e0-182">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-182">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-184">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-184">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-185">Is Indexed</span></span>             | <span data-ttu-id="d75e0-186">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-186">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-187">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-188">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-193">Search-Flags</span></span>           | <span data-ttu-id="d75e0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-195">System-Flags</span></span>           | <span data-ttu-id="d75e0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-197">Classes used in</span></span>        | [<span data-ttu-id="d75e0-198">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d75e0-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d75e0-199">Windows Server 2008</span></span>



| <span data-ttu-id="d75e0-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-200">Entry</span></span> | <span data-ttu-id="d75e0-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-204">System-Only</span></span>            | <span data-ttu-id="d75e0-205">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-205">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-207">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-207">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-208">Is Indexed</span></span>             | <span data-ttu-id="d75e0-209">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-209">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-210">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-211">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-211">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-216">Search-Flags</span></span>           | <span data-ttu-id="d75e0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-218">System-Flags</span></span>           | <span data-ttu-id="d75e0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-220">Classes used in</span></span>        | [<span data-ttu-id="d75e0-221">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d75e0-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d75e0-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d75e0-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-223">Entry</span></span> | <span data-ttu-id="d75e0-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-227">System-Only</span></span>            | <span data-ttu-id="d75e0-228">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-228">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-230">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-230">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-231">Is Indexed</span></span>             | <span data-ttu-id="d75e0-232">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-232">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-233">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-234">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-234">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-239">Search-Flags</span></span>           | <span data-ttu-id="d75e0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-241">System-Flags</span></span>           | <span data-ttu-id="d75e0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-243">Classes used in</span></span>        | [<span data-ttu-id="d75e0-244">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d75e0-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d75e0-245">Windows Server 2012</span></span>



| <span data-ttu-id="d75e0-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="d75e0-246">Entry</span></span> | <span data-ttu-id="d75e0-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75e0-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e0-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d75e0-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d75e0-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="d75e0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d75e0-250">System-Only</span></span>            | <span data-ttu-id="d75e0-251">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-251">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d75e0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d75e0-253">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-253">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d75e0-254">Is Indexed</span></span>             | <span data-ttu-id="d75e0-255">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-255">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d75e0-256">In Global Catalog</span></span>      | <span data-ttu-id="d75e0-257">Faux</span><span class="sxs-lookup"><span data-stu-id="d75e0-257">False</span></span>                                                                                |
| <span data-ttu-id="d75e0-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d75e0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d75e0-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d75e0-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="d75e0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d75e0-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d75e0-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="d75e0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-262">Search-Flags</span></span>           | <span data-ttu-id="d75e0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d75e0-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="d75e0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d75e0-264">System-Flags</span></span>           | <span data-ttu-id="d75e0-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d75e0-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="d75e0-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d75e0-266">Classes used in</span></span>        | [<span data-ttu-id="d75e0-267">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="d75e0-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





