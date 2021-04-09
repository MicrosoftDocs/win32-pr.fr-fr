---
title: Attribut Canonical-Name
description: Nom de l’objet au format canonique.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Canonical-Name
- Schéma AD de l’attribut canonicalName
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845581"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="cdddf-105">Attribut Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="cdddf-105">Canonical-Name attribute</span></span>

<span data-ttu-id="cdddf-106">Nom de l’objet au format canonique.</span><span class="sxs-lookup"><span data-stu-id="cdddf-106">The name of the object in canonical format.</span></span> <span data-ttu-id="cdddf-107">myserver2.fabrikam.com/users/jeffsmith est un exemple de nom unique au format canonique.</span><span class="sxs-lookup"><span data-stu-id="cdddf-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="cdddf-108">Il s’agit d’un attribut construit.</span><span class="sxs-lookup"><span data-stu-id="cdddf-108">This is a constructed attribute.</span></span> <span data-ttu-id="cdddf-109">Les résultats retournés sont identiques à ceux retournés par la fonction Active Directory suivante : DsCrackNames (valeur NULL, identificateur de nom de service d’annuaire \_ \_ \_ syntaxique \_ uniquement, \_ nom de domaine complet DS \_ 1779 \_ , \_ nom canonique DS \_ ,...).</span><span class="sxs-lookup"><span data-stu-id="cdddf-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="cdddf-110">Pour plus d’informations sur les formats de noms, consultez [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="cdddf-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="cdddf-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-111">Entry</span></span> | <span data-ttu-id="cdddf-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cdddf-113">CN</span><span class="sxs-lookup"><span data-stu-id="cdddf-113">CN</span></span>                | <span data-ttu-id="cdddf-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="cdddf-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="cdddf-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cdddf-115">Ldap-Display-Name</span></span> | <span data-ttu-id="cdddf-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="cdddf-116">canonicalName</span></span>                               |
| <span data-ttu-id="cdddf-117">Taille</span><span class="sxs-lookup"><span data-stu-id="cdddf-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="cdddf-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cdddf-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="cdddf-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cdddf-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cdddf-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-120">Attribute-Id</span></span>      | <span data-ttu-id="cdddf-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="cdddf-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="cdddf-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cdddf-122">System-Id-Guid</span></span>    | <span data-ttu-id="cdddf-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="cdddf-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="cdddf-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdddf-124">Syntax</span></span>            | [<span data-ttu-id="cdddf-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cdddf-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cdddf-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cdddf-126">Implementations</span></span>

-   [<span data-ttu-id="cdddf-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cdddf-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cdddf-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cdddf-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cdddf-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cdddf-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cdddf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cdddf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cdddf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cdddf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cdddf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cdddf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cdddf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cdddf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cdddf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cdddf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="cdddf-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-135">Entry</span></span> | <span data-ttu-id="cdddf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-139">System-Only</span></span>            | <span data-ttu-id="cdddf-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-140">True</span></span>                            |
| <span data-ttu-id="cdddf-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-142">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-142">False</span></span>                           |
| <span data-ttu-id="cdddf-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-143">Is Indexed</span></span>             | <span data-ttu-id="cdddf-144">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-144">False</span></span>                           |
| <span data-ttu-id="cdddf-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-145">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-146">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-146">False</span></span>                           |
| <span data-ttu-id="cdddf-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-151">Search-Flags</span></span>           | <span data-ttu-id="cdddf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-152">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-153">System-Flags</span></span>           | <span data-ttu-id="cdddf-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-154">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-155">Classes used in</span></span>        | [<span data-ttu-id="cdddf-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cdddf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cdddf-157">Windows Server 2003</span></span>



| <span data-ttu-id="cdddf-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-158">Entry</span></span> | <span data-ttu-id="cdddf-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-162">System-Only</span></span>            | <span data-ttu-id="cdddf-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-163">True</span></span>                            |
| <span data-ttu-id="cdddf-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-165">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-165">False</span></span>                           |
| <span data-ttu-id="cdddf-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-166">Is Indexed</span></span>             | <span data-ttu-id="cdddf-167">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-167">False</span></span>                           |
| <span data-ttu-id="cdddf-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-168">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-169">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-169">False</span></span>                           |
| <span data-ttu-id="cdddf-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-174">Search-Flags</span></span>           | <span data-ttu-id="cdddf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-175">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-176">System-Flags</span></span>           | <span data-ttu-id="cdddf-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-177">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-178">Classes used in</span></span>        | [<span data-ttu-id="cdddf-179">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cdddf-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="cdddf-180">ADAM</span></span>



| <span data-ttu-id="cdddf-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-181">Entry</span></span> | <span data-ttu-id="cdddf-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-185">System-Only</span></span>            | <span data-ttu-id="cdddf-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-186">True</span></span>                            |
| <span data-ttu-id="cdddf-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-188">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-188">False</span></span>                           |
| <span data-ttu-id="cdddf-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-189">Is Indexed</span></span>             | <span data-ttu-id="cdddf-190">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-190">False</span></span>                           |
| <span data-ttu-id="cdddf-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-191">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-192">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-192">False</span></span>                           |
| <span data-ttu-id="cdddf-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-197">Search-Flags</span></span>           | <span data-ttu-id="cdddf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-198">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-199">System-Flags</span></span>           | <span data-ttu-id="cdddf-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-200">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-201">Classes used in</span></span>        | [<span data-ttu-id="cdddf-202">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cdddf-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cdddf-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cdddf-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-204">Entry</span></span> | <span data-ttu-id="cdddf-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-208">System-Only</span></span>            | <span data-ttu-id="cdddf-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-209">True</span></span>                            |
| <span data-ttu-id="cdddf-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-211">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-211">False</span></span>                           |
| <span data-ttu-id="cdddf-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-212">Is Indexed</span></span>             | <span data-ttu-id="cdddf-213">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-213">False</span></span>                           |
| <span data-ttu-id="cdddf-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-214">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-215">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-215">False</span></span>                           |
| <span data-ttu-id="cdddf-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-220">Search-Flags</span></span>           | <span data-ttu-id="cdddf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-221">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-222">System-Flags</span></span>           | <span data-ttu-id="cdddf-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-223">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-224">Classes used in</span></span>        | [<span data-ttu-id="cdddf-225">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cdddf-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdddf-226">Windows Server 2008</span></span>



| <span data-ttu-id="cdddf-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-227">Entry</span></span> | <span data-ttu-id="cdddf-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-231">System-Only</span></span>            | <span data-ttu-id="cdddf-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-232">True</span></span>                            |
| <span data-ttu-id="cdddf-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-234">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-234">False</span></span>                           |
| <span data-ttu-id="cdddf-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-235">Is Indexed</span></span>             | <span data-ttu-id="cdddf-236">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-236">False</span></span>                           |
| <span data-ttu-id="cdddf-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-237">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-238">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-238">False</span></span>                           |
| <span data-ttu-id="cdddf-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-243">Search-Flags</span></span>           | <span data-ttu-id="cdddf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-244">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-245">System-Flags</span></span>           | <span data-ttu-id="cdddf-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-246">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-247">Classes used in</span></span>        | [<span data-ttu-id="cdddf-248">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cdddf-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cdddf-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cdddf-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-250">Entry</span></span> | <span data-ttu-id="cdddf-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-254">System-Only</span></span>            | <span data-ttu-id="cdddf-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-255">True</span></span>                            |
| <span data-ttu-id="cdddf-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-257">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-257">False</span></span>                           |
| <span data-ttu-id="cdddf-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-258">Is Indexed</span></span>             | <span data-ttu-id="cdddf-259">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-259">False</span></span>                           |
| <span data-ttu-id="cdddf-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-260">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-261">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-261">False</span></span>                           |
| <span data-ttu-id="cdddf-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-266">Search-Flags</span></span>           | <span data-ttu-id="cdddf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-267">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-268">System-Flags</span></span>           | <span data-ttu-id="cdddf-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-269">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-270">Classes used in</span></span>        | [<span data-ttu-id="cdddf-271">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cdddf-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdddf-272">Windows Server 2012</span></span>



| <span data-ttu-id="cdddf-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="cdddf-273">Entry</span></span> | <span data-ttu-id="cdddf-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdddf-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdddf-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cdddf-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdddf-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdddf-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdddf-277">System-Only</span></span>            | <span data-ttu-id="cdddf-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="cdddf-278">True</span></span>                            |
| <span data-ttu-id="cdddf-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cdddf-279">Is-Single-Valued</span></span>       | <span data-ttu-id="cdddf-280">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-280">False</span></span>                           |
| <span data-ttu-id="cdddf-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cdddf-281">Is Indexed</span></span>             | <span data-ttu-id="cdddf-282">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-282">False</span></span>                           |
| <span data-ttu-id="cdddf-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cdddf-283">In Global Catalog</span></span>      | <span data-ttu-id="cdddf-284">Faux</span><span class="sxs-lookup"><span data-stu-id="cdddf-284">False</span></span>                           |
| <span data-ttu-id="cdddf-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cdddf-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdddf-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cdddf-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdddf-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdddf-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdddf-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdddf-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdddf-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-289">Search-Flags</span></span>           | <span data-ttu-id="cdddf-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdddf-290">0x00000000</span></span>                      |
| <span data-ttu-id="cdddf-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdddf-291">System-Flags</span></span>           | <span data-ttu-id="cdddf-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdddf-292">0x08000014</span></span>                      |
| <span data-ttu-id="cdddf-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cdddf-293">Classes used in</span></span>        | [<span data-ttu-id="cdddf-294">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cdddf-294">**Top**</span></span>](c-top.md)<br/> |



 

