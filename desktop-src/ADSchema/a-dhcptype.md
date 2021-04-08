---
title: attribut de type DHCP
description: Type de serveur DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de type DHCP
- Schéma AD de l’attribut dhcpType
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943011"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="cd64c-105">attribut de type DHCP</span><span class="sxs-lookup"><span data-stu-id="cd64c-105">dhcp-Type attribute</span></span>

<span data-ttu-id="cd64c-106">Type de serveur DHCP.</span><span class="sxs-lookup"><span data-stu-id="cd64c-106">The type of DHCP server.</span></span> <span data-ttu-id="cd64c-107">Cet attribut est défini sur tous les objets de objectClass [**dHCPClass**](c-dhcpclass.md).</span><span class="sxs-lookup"><span data-stu-id="cd64c-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="cd64c-108">Sa valeur définit le type de l’objet :</span><span class="sxs-lookup"><span data-stu-id="cd64c-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="cd64c-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-109">Entry</span></span> | <span data-ttu-id="cd64c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="cd64c-111">CN</span><span class="sxs-lookup"><span data-stu-id="cd64c-111">CN</span></span>                | <span data-ttu-id="cd64c-112">Type DHCP</span><span class="sxs-lookup"><span data-stu-id="cd64c-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="cd64c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cd64c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cd64c-114">dhcpType</span><span class="sxs-lookup"><span data-stu-id="cd64c-114">dhcpType</span></span>                                               |
| <span data-ttu-id="cd64c-115">Taille</span><span class="sxs-lookup"><span data-stu-id="cd64c-115">Size</span></span>              | <span data-ttu-id="cd64c-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="cd64c-116">4 bytes</span></span>                                                |
| <span data-ttu-id="cd64c-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cd64c-117">Update Privilege</span></span>  | <span data-ttu-id="cd64c-118">Administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="cd64c-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="cd64c-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cd64c-119">Update Frequency</span></span>  | <span data-ttu-id="cd64c-120">Lorsqu’un nouveau serveur est ajouté ou supprimé de la forêt.</span><span class="sxs-lookup"><span data-stu-id="cd64c-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="cd64c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-121">Attribute-Id</span></span>      | <span data-ttu-id="cd64c-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="cd64c-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="cd64c-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd64c-123">System-Id-Guid</span></span>    | <span data-ttu-id="cd64c-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="cd64c-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="cd64c-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd64c-125">Syntax</span></span>            | [<span data-ttu-id="cd64c-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="cd64c-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="cd64c-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cd64c-127">Implementations</span></span>

-   [<span data-ttu-id="cd64c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cd64c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cd64c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd64c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd64c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd64c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd64c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd64c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd64c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd64c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd64c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd64c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cd64c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd64c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="cd64c-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-135">Entry</span></span> | <span data-ttu-id="cd64c-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-139">System-Only</span></span>            | <span data-ttu-id="cd64c-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-140">False</span></span>                                        |
| <span data-ttu-id="cd64c-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-142">True</span></span>                                         |
| <span data-ttu-id="cd64c-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-143">Is Indexed</span></span>             | <span data-ttu-id="cd64c-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-144">True</span></span>                                         |
| <span data-ttu-id="cd64c-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-145">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-146">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-146">False</span></span>                                        |
| <span data-ttu-id="cd64c-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-151">Search-Flags</span></span>           | <span data-ttu-id="cd64c-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-152">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-153">System-Flags</span></span>           | <span data-ttu-id="cd64c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-154">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-155">Classes used in</span></span>        | [<span data-ttu-id="cd64c-156">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cd64c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd64c-157">Windows Server 2003</span></span>



| <span data-ttu-id="cd64c-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-158">Entry</span></span> | <span data-ttu-id="cd64c-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-162">System-Only</span></span>            | <span data-ttu-id="cd64c-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-163">False</span></span>                                        |
| <span data-ttu-id="cd64c-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-165">True</span></span>                                         |
| <span data-ttu-id="cd64c-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-166">Is Indexed</span></span>             | <span data-ttu-id="cd64c-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-167">True</span></span>                                         |
| <span data-ttu-id="cd64c-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-168">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-169">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-169">False</span></span>                                        |
| <span data-ttu-id="cd64c-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-174">Search-Flags</span></span>           | <span data-ttu-id="cd64c-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-175">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-176">System-Flags</span></span>           | <span data-ttu-id="cd64c-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-177">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-178">Classes used in</span></span>        | [<span data-ttu-id="cd64c-179">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd64c-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd64c-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd64c-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-181">Entry</span></span> | <span data-ttu-id="cd64c-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-185">System-Only</span></span>            | <span data-ttu-id="cd64c-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-186">False</span></span>                                        |
| <span data-ttu-id="cd64c-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-188">True</span></span>                                         |
| <span data-ttu-id="cd64c-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-189">Is Indexed</span></span>             | <span data-ttu-id="cd64c-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-190">True</span></span>                                         |
| <span data-ttu-id="cd64c-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-191">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-192">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-192">False</span></span>                                        |
| <span data-ttu-id="cd64c-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-197">Search-Flags</span></span>           | <span data-ttu-id="cd64c-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-198">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-199">System-Flags</span></span>           | <span data-ttu-id="cd64c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-200">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-201">Classes used in</span></span>        | [<span data-ttu-id="cd64c-202">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd64c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd64c-203">Windows Server 2008</span></span>



| <span data-ttu-id="cd64c-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-204">Entry</span></span> | <span data-ttu-id="cd64c-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-208">System-Only</span></span>            | <span data-ttu-id="cd64c-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-209">False</span></span>                                        |
| <span data-ttu-id="cd64c-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-211">True</span></span>                                         |
| <span data-ttu-id="cd64c-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-212">Is Indexed</span></span>             | <span data-ttu-id="cd64c-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-213">True</span></span>                                         |
| <span data-ttu-id="cd64c-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-214">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-215">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-215">False</span></span>                                        |
| <span data-ttu-id="cd64c-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-220">Search-Flags</span></span>           | <span data-ttu-id="cd64c-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-221">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-222">System-Flags</span></span>           | <span data-ttu-id="cd64c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-223">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-224">Classes used in</span></span>        | [<span data-ttu-id="cd64c-225">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd64c-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd64c-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd64c-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-227">Entry</span></span> | <span data-ttu-id="cd64c-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-231">System-Only</span></span>            | <span data-ttu-id="cd64c-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-232">False</span></span>                                        |
| <span data-ttu-id="cd64c-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-233">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-234">True</span></span>                                         |
| <span data-ttu-id="cd64c-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-235">Is Indexed</span></span>             | <span data-ttu-id="cd64c-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-236">True</span></span>                                         |
| <span data-ttu-id="cd64c-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-237">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-238">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-238">False</span></span>                                        |
| <span data-ttu-id="cd64c-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-243">Search-Flags</span></span>           | <span data-ttu-id="cd64c-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-244">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-245">System-Flags</span></span>           | <span data-ttu-id="cd64c-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-246">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-247">Classes used in</span></span>        | [<span data-ttu-id="cd64c-248">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd64c-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd64c-249">Windows Server 2012</span></span>



| <span data-ttu-id="cd64c-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="cd64c-250">Entry</span></span> | <span data-ttu-id="cd64c-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd64c-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cd64c-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cd64c-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd64c-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cd64c-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd64c-254">System-Only</span></span>            | <span data-ttu-id="cd64c-255">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-255">False</span></span>                                        |
| <span data-ttu-id="cd64c-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cd64c-256">Is-Single-Valued</span></span>       | <span data-ttu-id="cd64c-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-257">True</span></span>                                         |
| <span data-ttu-id="cd64c-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cd64c-258">Is Indexed</span></span>             | <span data-ttu-id="cd64c-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="cd64c-259">True</span></span>                                         |
| <span data-ttu-id="cd64c-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cd64c-260">In Global Catalog</span></span>      | <span data-ttu-id="cd64c-261">Faux</span><span class="sxs-lookup"><span data-stu-id="cd64c-261">False</span></span>                                        |
| <span data-ttu-id="cd64c-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cd64c-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd64c-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cd64c-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cd64c-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd64c-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd64c-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cd64c-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-266">Search-Flags</span></span>           | <span data-ttu-id="cd64c-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd64c-267">0x00000001</span></span>                                   |
| <span data-ttu-id="cd64c-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd64c-268">System-Flags</span></span>           | <span data-ttu-id="cd64c-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd64c-269">0x00000010</span></span>                                   |
| <span data-ttu-id="cd64c-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cd64c-270">Classes used in</span></span>        | [<span data-ttu-id="cd64c-271">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd64c-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





