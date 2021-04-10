---
title: Téléphone-IP-attribut principal
description: Adresse TCP/IP du téléphone. Utilisé par la téléphonie.
ms.assetid: b51f28e4-4677-4798-87f1-2bd952a528ea
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory-IP-Primary Attribute
- Schéma AD de l’attribut ipPhone
topic_type:
- apiref
api_name:
- Phone-Ip-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4f16d29f6b3f45c5a229d76ec30c0dd7efdea2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107023"
---
# <a name="phone-ip-primary-attribute"></a><span data-ttu-id="28793-106">Téléphone-IP-attribut principal</span><span class="sxs-lookup"><span data-stu-id="28793-106">Phone-Ip-Primary attribute</span></span>

<span data-ttu-id="28793-107">Adresse TCP/IP du téléphone.</span><span class="sxs-lookup"><span data-stu-id="28793-107">The TCP/IP address for the phone.</span></span> <span data-ttu-id="28793-108">Utilisé par la téléphonie.</span><span class="sxs-lookup"><span data-stu-id="28793-108">Used by Telephony.</span></span>



| <span data-ttu-id="28793-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-109">Entry</span></span> | <span data-ttu-id="28793-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28793-111">CN</span><span class="sxs-lookup"><span data-stu-id="28793-111">CN</span></span>                | <span data-ttu-id="28793-112">Téléphone-IP-principal</span><span class="sxs-lookup"><span data-stu-id="28793-112">Phone-Ip-Primary</span></span>                                                                 |
| <span data-ttu-id="28793-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="28793-113">Ldap-Display-Name</span></span> | <span data-ttu-id="28793-114">ipPhone</span><span class="sxs-lookup"><span data-stu-id="28793-114">ipPhone</span></span>                                                                          |
| <span data-ttu-id="28793-115">Taille</span><span class="sxs-lookup"><span data-stu-id="28793-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="28793-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="28793-116">Update Privilege</span></span>  | <span data-ttu-id="28793-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="28793-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="28793-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="28793-118">Update Frequency</span></span>  | <span data-ttu-id="28793-119">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le numéro de téléphone doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="28793-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="28793-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28793-120">Attribute-Id</span></span>      | <span data-ttu-id="28793-121">1.2.840.113556.1.4.721</span><span class="sxs-lookup"><span data-stu-id="28793-121">1.2.840.113556.1.4.721</span></span>                                                           |
| <span data-ttu-id="28793-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="28793-122">System-Id-Guid</span></span>    | <span data-ttu-id="28793-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="28793-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="28793-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28793-124">Syntax</span></span>            | [<span data-ttu-id="28793-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="28793-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="28793-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="28793-126">Implementations</span></span>

-   [<span data-ttu-id="28793-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28793-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28793-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28793-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28793-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28793-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28793-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28793-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28793-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28793-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28793-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28793-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28793-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28793-133">Windows 2000 Server</span></span>



| <span data-ttu-id="28793-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-134">Entry</span></span> | <span data-ttu-id="28793-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-138">System-Only</span></span>            | <span data-ttu-id="28793-139">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-139">False</span></span>                                                              |
| <span data-ttu-id="28793-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-140">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-141">True</span></span>                                                               |
| <span data-ttu-id="28793-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-142">Is Indexed</span></span>             | <span data-ttu-id="28793-143">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-143">False</span></span>                                                              |
| <span data-ttu-id="28793-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-144">In Global Catalog</span></span>      | <span data-ttu-id="28793-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-145">True</span></span>                                                               |
| <span data-ttu-id="28793-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-150">Search-Flags</span></span>           | <span data-ttu-id="28793-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-152">System-Flags</span></span>           | <span data-ttu-id="28793-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-154">Classes used in</span></span>        | [<span data-ttu-id="28793-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28793-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28793-156">Windows Server 2003</span></span>



| <span data-ttu-id="28793-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-157">Entry</span></span> | <span data-ttu-id="28793-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-161">System-Only</span></span>            | <span data-ttu-id="28793-162">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-162">False</span></span>                                                              |
| <span data-ttu-id="28793-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-163">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-164">True</span></span>                                                               |
| <span data-ttu-id="28793-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-165">Is Indexed</span></span>             | <span data-ttu-id="28793-166">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-166">False</span></span>                                                              |
| <span data-ttu-id="28793-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-167">In Global Catalog</span></span>      | <span data-ttu-id="28793-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-168">True</span></span>                                                               |
| <span data-ttu-id="28793-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-173">Search-Flags</span></span>           | <span data-ttu-id="28793-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-175">System-Flags</span></span>           | <span data-ttu-id="28793-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-177">Classes used in</span></span>        | [<span data-ttu-id="28793-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28793-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28793-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28793-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-180">Entry</span></span> | <span data-ttu-id="28793-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-184">System-Only</span></span>            | <span data-ttu-id="28793-185">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-185">False</span></span>                                                              |
| <span data-ttu-id="28793-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-186">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-187">True</span></span>                                                               |
| <span data-ttu-id="28793-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-188">Is Indexed</span></span>             | <span data-ttu-id="28793-189">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-189">False</span></span>                                                              |
| <span data-ttu-id="28793-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-190">In Global Catalog</span></span>      | <span data-ttu-id="28793-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-191">True</span></span>                                                               |
| <span data-ttu-id="28793-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-196">Search-Flags</span></span>           | <span data-ttu-id="28793-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-198">System-Flags</span></span>           | <span data-ttu-id="28793-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-200">Classes used in</span></span>        | [<span data-ttu-id="28793-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28793-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28793-202">Windows Server 2008</span></span>



| <span data-ttu-id="28793-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-203">Entry</span></span> | <span data-ttu-id="28793-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-207">System-Only</span></span>            | <span data-ttu-id="28793-208">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-208">False</span></span>                                                              |
| <span data-ttu-id="28793-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-209">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-210">True</span></span>                                                               |
| <span data-ttu-id="28793-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-211">Is Indexed</span></span>             | <span data-ttu-id="28793-212">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-212">False</span></span>                                                              |
| <span data-ttu-id="28793-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-213">In Global Catalog</span></span>      | <span data-ttu-id="28793-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-214">True</span></span>                                                               |
| <span data-ttu-id="28793-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-219">Search-Flags</span></span>           | <span data-ttu-id="28793-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-221">System-Flags</span></span>           | <span data-ttu-id="28793-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-223">Classes used in</span></span>        | [<span data-ttu-id="28793-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28793-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28793-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28793-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-226">Entry</span></span> | <span data-ttu-id="28793-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-230">System-Only</span></span>            | <span data-ttu-id="28793-231">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-231">False</span></span>                                                              |
| <span data-ttu-id="28793-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-232">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-233">True</span></span>                                                               |
| <span data-ttu-id="28793-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-234">Is Indexed</span></span>             | <span data-ttu-id="28793-235">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-235">False</span></span>                                                              |
| <span data-ttu-id="28793-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-236">In Global Catalog</span></span>      | <span data-ttu-id="28793-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-237">True</span></span>                                                               |
| <span data-ttu-id="28793-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-242">Search-Flags</span></span>           | <span data-ttu-id="28793-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-244">System-Flags</span></span>           | <span data-ttu-id="28793-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-246">Classes used in</span></span>        | [<span data-ttu-id="28793-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28793-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28793-248">Windows Server 2012</span></span>



| <span data-ttu-id="28793-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="28793-249">Entry</span></span> | <span data-ttu-id="28793-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="28793-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28793-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="28793-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28793-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28793-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="28793-253">System-Only</span></span>            | <span data-ttu-id="28793-254">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-254">False</span></span>                                                              |
| <span data-ttu-id="28793-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="28793-255">Is-Single-Valued</span></span>       | <span data-ttu-id="28793-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-256">True</span></span>                                                               |
| <span data-ttu-id="28793-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="28793-257">Is Indexed</span></span>             | <span data-ttu-id="28793-258">Faux</span><span class="sxs-lookup"><span data-stu-id="28793-258">False</span></span>                                                              |
| <span data-ttu-id="28793-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="28793-259">In Global Catalog</span></span>      | <span data-ttu-id="28793-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="28793-260">True</span></span>                                                               |
| <span data-ttu-id="28793-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="28793-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="28793-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="28793-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28793-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28793-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28793-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28793-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-265">Search-Flags</span></span>           | <span data-ttu-id="28793-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28793-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="28793-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28793-267">System-Flags</span></span>           | <span data-ttu-id="28793-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28793-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="28793-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="28793-269">Classes used in</span></span>        | [<span data-ttu-id="28793-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="28793-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





