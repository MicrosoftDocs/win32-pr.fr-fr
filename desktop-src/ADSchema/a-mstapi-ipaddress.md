---
title: attribut ms-TAPI-IP-address
description: Adresses IP d’un ordinateur client TAPI auquel un utilisateur est connecté. Cet attribut peut être utilisé comme attribut générique pour contenir des adresses IP d’ordinateur.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-TAPI-IP-address
- Schéma AD de l’attribut msTAPI-IpAddress
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943143"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="f6cf9-106">attribut ms-TAPI-IP-address</span><span class="sxs-lookup"><span data-stu-id="f6cf9-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="f6cf9-107">Adresses IP d’un ordinateur client TAPI auquel un utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="f6cf9-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="f6cf9-108">Cet attribut peut être utilisé comme attribut générique pour contenir des adresses IP d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6cf9-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="f6cf9-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-109">Entry</span></span> | <span data-ttu-id="f6cf9-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="f6cf9-111">CN</span><span class="sxs-lookup"><span data-stu-id="f6cf9-111">CN</span></span>                | <span data-ttu-id="f6cf9-112">MS-TAPI-IP-adresse</span><span class="sxs-lookup"><span data-stu-id="f6cf9-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="f6cf9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f6cf9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f6cf9-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f6cf9-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="f6cf9-115">Taille</span><span class="sxs-lookup"><span data-stu-id="f6cf9-115">Size</span></span>              | <span data-ttu-id="f6cf9-116">Chaque adresse IP est stockée sous forme de chaîne dans une notation. B. C. D.</span><span class="sxs-lookup"><span data-stu-id="f6cf9-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="f6cf9-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f6cf9-117">Update Privilege</span></span>  | <span data-ttu-id="f6cf9-118">Aucun privilège spécial n’est requis.</span><span class="sxs-lookup"><span data-stu-id="f6cf9-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="f6cf9-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f6cf9-119">Update Frequency</span></span>  | <span data-ttu-id="f6cf9-120">Généralement très faible.</span><span class="sxs-lookup"><span data-stu-id="f6cf9-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="f6cf9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-121">Attribute-Id</span></span>      | <span data-ttu-id="f6cf9-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="f6cf9-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="f6cf9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f6cf9-123">System-Id-Guid</span></span>    | <span data-ttu-id="f6cf9-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="f6cf9-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="f6cf9-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6cf9-125">Syntax</span></span>            | [<span data-ttu-id="f6cf9-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="f6cf9-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f6cf9-127">Implementations</span></span>

-   [<span data-ttu-id="f6cf9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6cf9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6cf9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6cf9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6cf9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f6cf9-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6cf9-133">Windows Server 2003</span></span>



| <span data-ttu-id="f6cf9-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-134">Entry</span></span> | <span data-ttu-id="f6cf9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f6cf9-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6cf9-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6cf9-138">System-Only</span></span>            | <span data-ttu-id="f6cf9-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-139">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6cf9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f6cf9-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-141">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6cf9-142">Is Indexed</span></span>             | <span data-ttu-id="f6cf9-143">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-143">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6cf9-144">In Global Catalog</span></span>      | <span data-ttu-id="f6cf9-145">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-145">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6cf9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6cf9-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6cf9-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f6cf9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6cf9-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6cf9-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-150">Search-Flags</span></span>           | <span data-ttu-id="f6cf9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6cf9-151">0x00000000</span></span>                                                |
| <span data-ttu-id="f6cf9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-152">System-Flags</span></span>           | <span data-ttu-id="f6cf9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6cf9-153">0x00000010</span></span>                                                |
| <span data-ttu-id="f6cf9-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6cf9-154">Classes used in</span></span>        | [<span data-ttu-id="f6cf9-155">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6cf9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6cf9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6cf9-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-157">Entry</span></span> | <span data-ttu-id="f6cf9-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f6cf9-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6cf9-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6cf9-161">System-Only</span></span>            | <span data-ttu-id="f6cf9-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-162">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6cf9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f6cf9-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-164">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6cf9-165">Is Indexed</span></span>             | <span data-ttu-id="f6cf9-166">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-166">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6cf9-167">In Global Catalog</span></span>      | <span data-ttu-id="f6cf9-168">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-168">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6cf9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6cf9-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6cf9-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f6cf9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6cf9-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6cf9-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-173">Search-Flags</span></span>           | <span data-ttu-id="f6cf9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6cf9-174">0x00000000</span></span>                                                |
| <span data-ttu-id="f6cf9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-175">System-Flags</span></span>           | <span data-ttu-id="f6cf9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6cf9-176">0x00000010</span></span>                                                |
| <span data-ttu-id="f6cf9-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6cf9-177">Classes used in</span></span>        | [<span data-ttu-id="f6cf9-178">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6cf9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6cf9-179">Windows Server 2008</span></span>



| <span data-ttu-id="f6cf9-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-180">Entry</span></span> | <span data-ttu-id="f6cf9-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f6cf9-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6cf9-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6cf9-184">System-Only</span></span>            | <span data-ttu-id="f6cf9-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-185">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6cf9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f6cf9-187">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-187">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6cf9-188">Is Indexed</span></span>             | <span data-ttu-id="f6cf9-189">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-189">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6cf9-190">In Global Catalog</span></span>      | <span data-ttu-id="f6cf9-191">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-191">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6cf9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6cf9-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6cf9-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f6cf9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6cf9-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6cf9-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-196">Search-Flags</span></span>           | <span data-ttu-id="f6cf9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6cf9-197">0x00000000</span></span>                                                |
| <span data-ttu-id="f6cf9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-198">System-Flags</span></span>           | <span data-ttu-id="f6cf9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6cf9-199">0x00000010</span></span>                                                |
| <span data-ttu-id="f6cf9-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6cf9-200">Classes used in</span></span>        | [<span data-ttu-id="f6cf9-201">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6cf9-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6cf9-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6cf9-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-203">Entry</span></span> | <span data-ttu-id="f6cf9-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f6cf9-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6cf9-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6cf9-207">System-Only</span></span>            | <span data-ttu-id="f6cf9-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-208">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6cf9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f6cf9-210">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-210">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6cf9-211">Is Indexed</span></span>             | <span data-ttu-id="f6cf9-212">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-212">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6cf9-213">In Global Catalog</span></span>      | <span data-ttu-id="f6cf9-214">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-214">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6cf9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6cf9-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6cf9-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f6cf9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6cf9-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6cf9-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-219">Search-Flags</span></span>           | <span data-ttu-id="f6cf9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6cf9-220">0x00000000</span></span>                                                |
| <span data-ttu-id="f6cf9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-221">System-Flags</span></span>           | <span data-ttu-id="f6cf9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6cf9-222">0x00000010</span></span>                                                |
| <span data-ttu-id="f6cf9-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6cf9-223">Classes used in</span></span>        | [<span data-ttu-id="f6cf9-224">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6cf9-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6cf9-225">Windows Server 2012</span></span>



| <span data-ttu-id="f6cf9-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6cf9-226">Entry</span></span> | <span data-ttu-id="f6cf9-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6cf9-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f6cf9-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6cf9-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6cf9-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f6cf9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6cf9-230">System-Only</span></span>            | <span data-ttu-id="f6cf9-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-231">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6cf9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f6cf9-233">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-233">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6cf9-234">Is Indexed</span></span>             | <span data-ttu-id="f6cf9-235">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-235">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6cf9-236">In Global Catalog</span></span>      | <span data-ttu-id="f6cf9-237">Faux</span><span class="sxs-lookup"><span data-stu-id="f6cf9-237">False</span></span>                                                     |
| <span data-ttu-id="f6cf9-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6cf9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6cf9-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6cf9-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f6cf9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6cf9-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6cf9-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f6cf9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-242">Search-Flags</span></span>           | <span data-ttu-id="f6cf9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6cf9-243">0x00000000</span></span>                                                |
| <span data-ttu-id="f6cf9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6cf9-244">System-Flags</span></span>           | <span data-ttu-id="f6cf9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6cf9-245">0x00000010</span></span>                                                |
| <span data-ttu-id="f6cf9-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6cf9-246">Classes used in</span></span>        | [<span data-ttu-id="f6cf9-247">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="f6cf9-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





