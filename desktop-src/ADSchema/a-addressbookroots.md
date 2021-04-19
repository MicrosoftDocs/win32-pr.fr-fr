---
title: Adresse-attribut de répertoire racines
description: Utilisé par Exchange. Exchange configure les arborescences des conteneurs de carnets d’adresses à afficher dans le carnet d’adresses MAPI. Cet attribut sur l’objet de configuration Exchange répertorie les racines des arborescences de conteneurs du carnet d’adresses. | Adresse-attribut de répertoire racines
ms.assetid: 7e6d2677-9818-4870-8429-50f73f9c8c1f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut adresse-livre-racines
- Schéma AD de l’attribut addressBookRoots
topic_type:
- apiref
api_name:
- Address-Book-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab195744bb7fb5029a9a48aeca55d703e6e05b62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527057"
---
# <a name="address-book-roots-attribute"></a><span data-ttu-id="2825d-108">Adresse-attribut de répertoire racines</span><span class="sxs-lookup"><span data-stu-id="2825d-108">Address-Book-Roots attribute</span></span>

<span data-ttu-id="2825d-109">Utilisé par Exchange.</span><span class="sxs-lookup"><span data-stu-id="2825d-109">Used by Exchange.</span></span> <span data-ttu-id="2825d-110">Exchange configure les arborescences des conteneurs de carnets d’adresses à afficher dans le carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="2825d-110">Exchange configures trees of address book containers to show up in the MAPI address book.</span></span> <span data-ttu-id="2825d-111">Cet attribut sur l’objet de configuration Exchange répertorie les racines des arborescences de conteneurs du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="2825d-111">This attribute on the Exchange Config object lists the roots of the address book container trees.</span></span>



| <span data-ttu-id="2825d-112">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-112">Entry</span></span> | <span data-ttu-id="2825d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-113">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2825d-114">CN</span><span class="sxs-lookup"><span data-stu-id="2825d-114">CN</span></span>                | <span data-ttu-id="2825d-115">Adresse-livres-racines</span><span class="sxs-lookup"><span data-stu-id="2825d-115">Address-Book-Roots</span></span>                      |
| <span data-ttu-id="2825d-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2825d-116">Ldap-Display-Name</span></span> | <span data-ttu-id="2825d-117">addressBookRoots</span><span class="sxs-lookup"><span data-stu-id="2825d-117">addressBookRoots</span></span>                        |
| <span data-ttu-id="2825d-118">Taille</span><span class="sxs-lookup"><span data-stu-id="2825d-118">Size</span></span>              | \-                                      |
| <span data-ttu-id="2825d-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2825d-119">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2825d-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2825d-120">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2825d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-121">Attribute-Id</span></span>      | <span data-ttu-id="2825d-122">1.2.840.113556.1.4.1244</span><span class="sxs-lookup"><span data-stu-id="2825d-122">1.2.840.113556.1.4.1244</span></span>                 |
| <span data-ttu-id="2825d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2825d-123">System-Id-Guid</span></span>    | <span data-ttu-id="2825d-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="2825d-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="2825d-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2825d-125">Syntax</span></span>            | [<span data-ttu-id="2825d-126">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2825d-126">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2825d-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2825d-127">Implementations</span></span>

-   [<span data-ttu-id="2825d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2825d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2825d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2825d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2825d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2825d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2825d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2825d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2825d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2825d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2825d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2825d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2825d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2825d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2825d-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-135">Entry</span></span> | <span data-ttu-id="2825d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-136">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-137">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-138">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-139">System-Only</span></span>            | <span data-ttu-id="2825d-140">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-140">False</span></span>                                                                                |
| <span data-ttu-id="2825d-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-142">False</span></span>                                                                                |
| <span data-ttu-id="2825d-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-143">Is Indexed</span></span>             | <span data-ttu-id="2825d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-144">False</span></span>                                                                                |
| <span data-ttu-id="2825d-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-145">In Global Catalog</span></span>      | <span data-ttu-id="2825d-146">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-146">False</span></span>                                                                                |
| <span data-ttu-id="2825d-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-148">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-149">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-150">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-151">Search-Flags</span></span>           | <span data-ttu-id="2825d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-152">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-153">System-Flags</span></span>           | <span data-ttu-id="2825d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-154">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-155">Classes used in</span></span>        | [<span data-ttu-id="2825d-156">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-156">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2825d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2825d-157">Windows Server 2003</span></span>



| <span data-ttu-id="2825d-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-158">Entry</span></span> | <span data-ttu-id="2825d-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-160">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-161">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-162">System-Only</span></span>            | <span data-ttu-id="2825d-163">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-163">False</span></span>                                                                                |
| <span data-ttu-id="2825d-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-165">False</span></span>                                                                                |
| <span data-ttu-id="2825d-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-166">Is Indexed</span></span>             | <span data-ttu-id="2825d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-167">False</span></span>                                                                                |
| <span data-ttu-id="2825d-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-168">In Global Catalog</span></span>      | <span data-ttu-id="2825d-169">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-169">False</span></span>                                                                                |
| <span data-ttu-id="2825d-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-171">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-172">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-173">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-174">Search-Flags</span></span>           | <span data-ttu-id="2825d-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-175">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-176">System-Flags</span></span>           | <span data-ttu-id="2825d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-177">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-178">Classes used in</span></span>        | [<span data-ttu-id="2825d-179">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-179">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2825d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2825d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2825d-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-181">Entry</span></span> | <span data-ttu-id="2825d-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-182">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-183">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-184">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-185">System-Only</span></span>            | <span data-ttu-id="2825d-186">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-186">False</span></span>                                                                                |
| <span data-ttu-id="2825d-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-188">False</span></span>                                                                                |
| <span data-ttu-id="2825d-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-189">Is Indexed</span></span>             | <span data-ttu-id="2825d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-190">False</span></span>                                                                                |
| <span data-ttu-id="2825d-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-191">In Global Catalog</span></span>      | <span data-ttu-id="2825d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-192">False</span></span>                                                                                |
| <span data-ttu-id="2825d-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-194">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-195">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-196">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-197">Search-Flags</span></span>           | <span data-ttu-id="2825d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-198">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-199">System-Flags</span></span>           | <span data-ttu-id="2825d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-200">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-201">Classes used in</span></span>        | [<span data-ttu-id="2825d-202">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-202">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2825d-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2825d-203">Windows Server 2008</span></span>



| <span data-ttu-id="2825d-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-204">Entry</span></span> | <span data-ttu-id="2825d-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-206">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-207">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-208">System-Only</span></span>            | <span data-ttu-id="2825d-209">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-209">False</span></span>                                                                                |
| <span data-ttu-id="2825d-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-211">False</span></span>                                                                                |
| <span data-ttu-id="2825d-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-212">Is Indexed</span></span>             | <span data-ttu-id="2825d-213">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-213">False</span></span>                                                                                |
| <span data-ttu-id="2825d-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-214">In Global Catalog</span></span>      | <span data-ttu-id="2825d-215">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-215">False</span></span>                                                                                |
| <span data-ttu-id="2825d-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-217">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-218">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-219">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-220">Search-Flags</span></span>           | <span data-ttu-id="2825d-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-221">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-222">System-Flags</span></span>           | <span data-ttu-id="2825d-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-223">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-224">Classes used in</span></span>        | [<span data-ttu-id="2825d-225">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-225">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2825d-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2825d-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2825d-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-227">Entry</span></span> | <span data-ttu-id="2825d-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-228">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-229">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-230">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-231">System-Only</span></span>            | <span data-ttu-id="2825d-232">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-232">False</span></span>                                                                                |
| <span data-ttu-id="2825d-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-234">False</span></span>                                                                                |
| <span data-ttu-id="2825d-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-235">Is Indexed</span></span>             | <span data-ttu-id="2825d-236">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-236">False</span></span>                                                                                |
| <span data-ttu-id="2825d-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-237">In Global Catalog</span></span>      | <span data-ttu-id="2825d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-238">False</span></span>                                                                                |
| <span data-ttu-id="2825d-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-240">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-241">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-242">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-243">Search-Flags</span></span>           | <span data-ttu-id="2825d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-244">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-245">System-Flags</span></span>           | <span data-ttu-id="2825d-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-246">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-247">Classes used in</span></span>        | [<span data-ttu-id="2825d-248">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-248">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2825d-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2825d-249">Windows Server 2012</span></span>



| <span data-ttu-id="2825d-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="2825d-250">Entry</span></span> | <span data-ttu-id="2825d-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="2825d-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2825d-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2825d-252">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2825d-253">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2825d-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="2825d-254">System-Only</span></span>            | <span data-ttu-id="2825d-255">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-255">False</span></span>                                                                                |
| <span data-ttu-id="2825d-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2825d-256">Is-Single-Valued</span></span>       | <span data-ttu-id="2825d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-257">False</span></span>                                                                                |
| <span data-ttu-id="2825d-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2825d-258">Is Indexed</span></span>             | <span data-ttu-id="2825d-259">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-259">False</span></span>                                                                                |
| <span data-ttu-id="2825d-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2825d-260">In Global Catalog</span></span>      | <span data-ttu-id="2825d-261">Faux</span><span class="sxs-lookup"><span data-stu-id="2825d-261">False</span></span>                                                                                |
| <span data-ttu-id="2825d-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2825d-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="2825d-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2825d-263">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2825d-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2825d-264">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2825d-265">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2825d-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-266">Search-Flags</span></span>           | <span data-ttu-id="2825d-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2825d-267">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2825d-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2825d-268">System-Flags</span></span>           | <span data-ttu-id="2825d-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2825d-269">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2825d-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2825d-270">Classes used in</span></span>        | [<span data-ttu-id="2825d-271">**ms-Exch-configuration-conteneur**</span><span class="sxs-lookup"><span data-stu-id="2825d-271">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





