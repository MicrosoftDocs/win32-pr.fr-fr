---
title: Attribut de nom d’utilisateur principal
description: Cet attribut contient l’UPN qui est un nom de connexion de style Internet pour un utilisateur basé sur la norme Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut User-Principal-Name
- Schéma AD de l’attribut userPrincipalName
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943092"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="93e6e-105">Attribut de nom d’utilisateur principal</span><span class="sxs-lookup"><span data-stu-id="93e6e-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="93e6e-106">Cet attribut contient l’UPN qui est un nom de connexion de style Internet pour un utilisateur basé sur la norme Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span><span class="sxs-lookup"><span data-stu-id="93e6e-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="93e6e-107">L’UPN est plus petit que le nom unique et il est plus facile à mémoriser.</span><span class="sxs-lookup"><span data-stu-id="93e6e-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="93e6e-108">Par Convention, cette valeur doit correspondre au nom de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93e6e-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="93e6e-109">La valeur définie pour cet attribut est égale à la longueur de l’ID de l’utilisateur et du nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="93e6e-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="93e6e-110">Pour plus d’informations sur cet attribut, consultez [User Naming Attributes](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="93e6e-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="93e6e-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-111">Entry</span></span> | <span data-ttu-id="93e6e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="93e6e-113">CN</span><span class="sxs-lookup"><span data-stu-id="93e6e-113">CN</span></span>                | <span data-ttu-id="93e6e-114">User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="93e6e-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="93e6e-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="93e6e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="93e6e-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="93e6e-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="93e6e-117">Taille</span><span class="sxs-lookup"><span data-stu-id="93e6e-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="93e6e-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="93e6e-118">Update Privilege</span></span>  | <span data-ttu-id="93e6e-119">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="93e6e-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="93e6e-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="93e6e-120">Update Frequency</span></span>  | <span data-ttu-id="93e6e-121">En théorie, cela ne doit jamais changer.</span><span class="sxs-lookup"><span data-stu-id="93e6e-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="93e6e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-122">Attribute-Id</span></span>      | <span data-ttu-id="93e6e-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="93e6e-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="93e6e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="93e6e-124">System-Id-Guid</span></span>    | <span data-ttu-id="93e6e-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="93e6e-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="93e6e-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93e6e-126">Syntax</span></span>            | [<span data-ttu-id="93e6e-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="93e6e-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="93e6e-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="93e6e-128">Implementations</span></span>

-   [<span data-ttu-id="93e6e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93e6e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93e6e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93e6e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93e6e-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="93e6e-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="93e6e-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93e6e-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93e6e-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93e6e-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93e6e-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93e6e-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93e6e-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93e6e-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93e6e-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93e6e-136">Windows 2000 Server</span></span>



| <span data-ttu-id="93e6e-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-137">Entry</span></span> | <span data-ttu-id="93e6e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-141">System-Only</span></span>            | <span data-ttu-id="93e6e-142">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-142">False</span></span>                             |
| <span data-ttu-id="93e6e-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-144">True</span></span>                              |
| <span data-ttu-id="93e6e-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-145">Is Indexed</span></span>             | <span data-ttu-id="93e6e-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-146">True</span></span>                              |
| <span data-ttu-id="93e6e-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-147">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-148">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-148">True</span></span>                              |
| <span data-ttu-id="93e6e-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-153">Search-Flags</span></span>           | <span data-ttu-id="93e6e-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-154">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-155">System-Flags</span></span>           | <span data-ttu-id="93e6e-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-156">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-157">Classes used in</span></span>        | [<span data-ttu-id="93e6e-158">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93e6e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93e6e-159">Windows Server 2003</span></span>



| <span data-ttu-id="93e6e-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-160">Entry</span></span> | <span data-ttu-id="93e6e-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-164">System-Only</span></span>            | <span data-ttu-id="93e6e-165">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-165">False</span></span>                             |
| <span data-ttu-id="93e6e-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-166">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-167">True</span></span>                              |
| <span data-ttu-id="93e6e-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-168">Is Indexed</span></span>             | <span data-ttu-id="93e6e-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-169">True</span></span>                              |
| <span data-ttu-id="93e6e-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-170">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-171">True</span></span>                              |
| <span data-ttu-id="93e6e-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-176">Search-Flags</span></span>           | <span data-ttu-id="93e6e-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-177">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-178">System-Flags</span></span>           | <span data-ttu-id="93e6e-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-179">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-180">Classes used in</span></span>        | [<span data-ttu-id="93e6e-181">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="93e6e-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="93e6e-182">ADAM</span></span>



| <span data-ttu-id="93e6e-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-183">Entry</span></span> | <span data-ttu-id="93e6e-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="93e6e-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="93e6e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="93e6e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-187">System-Only</span></span>            | <span data-ttu-id="93e6e-188">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-188">False</span></span>        |
| <span data-ttu-id="93e6e-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-190">True</span></span>         |
| <span data-ttu-id="93e6e-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-191">Is Indexed</span></span>             | <span data-ttu-id="93e6e-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-192">True</span></span>         |
| <span data-ttu-id="93e6e-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-193">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-194">True</span></span>         |
| <span data-ttu-id="93e6e-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="93e6e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="93e6e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="93e6e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-199">Search-Flags</span></span>           | <span data-ttu-id="93e6e-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-200">0x00000001</span></span>   |
| <span data-ttu-id="93e6e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-201">System-Flags</span></span>           | <span data-ttu-id="93e6e-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-202">0x00000012</span></span>   |
| <span data-ttu-id="93e6e-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93e6e-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93e6e-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93e6e-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-205">Entry</span></span> | <span data-ttu-id="93e6e-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-209">System-Only</span></span>            | <span data-ttu-id="93e6e-210">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-210">False</span></span>                             |
| <span data-ttu-id="93e6e-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-212">True</span></span>                              |
| <span data-ttu-id="93e6e-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-213">Is Indexed</span></span>             | <span data-ttu-id="93e6e-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-214">True</span></span>                              |
| <span data-ttu-id="93e6e-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-215">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-216">True</span></span>                              |
| <span data-ttu-id="93e6e-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-221">Search-Flags</span></span>           | <span data-ttu-id="93e6e-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-222">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-223">System-Flags</span></span>           | <span data-ttu-id="93e6e-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-224">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-225">Classes used in</span></span>        | [<span data-ttu-id="93e6e-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93e6e-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93e6e-227">Windows Server 2008</span></span>



| <span data-ttu-id="93e6e-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-228">Entry</span></span> | <span data-ttu-id="93e6e-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-232">System-Only</span></span>            | <span data-ttu-id="93e6e-233">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-233">False</span></span>                             |
| <span data-ttu-id="93e6e-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-235">True</span></span>                              |
| <span data-ttu-id="93e6e-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-236">Is Indexed</span></span>             | <span data-ttu-id="93e6e-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-237">True</span></span>                              |
| <span data-ttu-id="93e6e-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-238">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-239">True</span></span>                              |
| <span data-ttu-id="93e6e-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-244">Search-Flags</span></span>           | <span data-ttu-id="93e6e-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-245">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-246">System-Flags</span></span>           | <span data-ttu-id="93e6e-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-247">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-248">Classes used in</span></span>        | [<span data-ttu-id="93e6e-249">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93e6e-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93e6e-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93e6e-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-251">Entry</span></span> | <span data-ttu-id="93e6e-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-255">System-Only</span></span>            | <span data-ttu-id="93e6e-256">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-256">False</span></span>                             |
| <span data-ttu-id="93e6e-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-257">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-258">True</span></span>                              |
| <span data-ttu-id="93e6e-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-259">Is Indexed</span></span>             | <span data-ttu-id="93e6e-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-260">True</span></span>                              |
| <span data-ttu-id="93e6e-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-261">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-262">True</span></span>                              |
| <span data-ttu-id="93e6e-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-267">Search-Flags</span></span>           | <span data-ttu-id="93e6e-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-268">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-269">System-Flags</span></span>           | <span data-ttu-id="93e6e-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-270">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-271">Classes used in</span></span>        | [<span data-ttu-id="93e6e-272">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93e6e-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93e6e-273">Windows Server 2012</span></span>



| <span data-ttu-id="93e6e-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="93e6e-274">Entry</span></span> | <span data-ttu-id="93e6e-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e6e-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="93e6e-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="93e6e-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93e6e-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="93e6e-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="93e6e-278">System-Only</span></span>            | <span data-ttu-id="93e6e-279">Faux</span><span class="sxs-lookup"><span data-stu-id="93e6e-279">False</span></span>                             |
| <span data-ttu-id="93e6e-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="93e6e-280">Is-Single-Valued</span></span>       | <span data-ttu-id="93e6e-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-281">True</span></span>                              |
| <span data-ttu-id="93e6e-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="93e6e-282">Is Indexed</span></span>             | <span data-ttu-id="93e6e-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-283">True</span></span>                              |
| <span data-ttu-id="93e6e-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="93e6e-284">In Global Catalog</span></span>      | <span data-ttu-id="93e6e-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="93e6e-285">True</span></span>                              |
| <span data-ttu-id="93e6e-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="93e6e-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="93e6e-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="93e6e-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="93e6e-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93e6e-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="93e6e-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93e6e-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="93e6e-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-290">Search-Flags</span></span>           | <span data-ttu-id="93e6e-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93e6e-291">0x00000001</span></span>                        |
| <span data-ttu-id="93e6e-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93e6e-292">System-Flags</span></span>           | <span data-ttu-id="93e6e-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="93e6e-293">0x00000012</span></span>                        |
| <span data-ttu-id="93e6e-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="93e6e-294">Classes used in</span></span>        | [<span data-ttu-id="93e6e-295">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="93e6e-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="93e6e-296">Notes</span><span class="sxs-lookup"><span data-stu-id="93e6e-296">Remarks</span></span>

<span data-ttu-id="93e6e-297">Dans ADAM, cet attribut ne doit pas être au format standard Internet RFC 822. Il peut s’agir d’un nom simple.</span><span class="sxs-lookup"><span data-stu-id="93e6e-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

