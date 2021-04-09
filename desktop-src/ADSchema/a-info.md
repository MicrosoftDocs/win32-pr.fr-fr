---
title: Attribut comment
description: Commentaires de l’utilisateur. Cette chaîne peut être une chaîne NULL.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut comment
- Schéma AD des attributs d’informations
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744212"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="dfcb2-106">Attribut comment (schéma Active Directory)</span><span class="sxs-lookup"><span data-stu-id="dfcb2-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="dfcb2-107">Commentaires de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfcb2-107">The user's comments.</span></span> <span data-ttu-id="dfcb2-108">Cette chaîne peut être une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="dfcb2-108">This string can be a null string.</span></span>



| <span data-ttu-id="dfcb2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-109">Entry</span></span> | <span data-ttu-id="dfcb2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="dfcb2-111">CN</span><span class="sxs-lookup"><span data-stu-id="dfcb2-111">CN</span></span>                | <span data-ttu-id="dfcb2-112">Commentaire</span><span class="sxs-lookup"><span data-stu-id="dfcb2-112">Comment</span></span>                                                                  |
| <span data-ttu-id="dfcb2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dfcb2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dfcb2-114">info</span><span class="sxs-lookup"><span data-stu-id="dfcb2-114">info</span></span>                                                                     |
| <span data-ttu-id="dfcb2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="dfcb2-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="dfcb2-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="dfcb2-116">Update Privilege</span></span>  | <span data-ttu-id="dfcb2-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="dfcb2-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="dfcb2-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="dfcb2-118">Update Frequency</span></span>  | <span data-ttu-id="dfcb2-119">Chaque fois que l’utilisateur ou l’administrateur doit ajouter des commentaires sur le compte.</span><span class="sxs-lookup"><span data-stu-id="dfcb2-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="dfcb2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-120">Attribute-Id</span></span>      | <span data-ttu-id="dfcb2-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="dfcb2-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="dfcb2-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dfcb2-122">System-Id-Guid</span></span>    | <span data-ttu-id="dfcb2-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dfcb2-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="dfcb2-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfcb2-124">Syntax</span></span>            | [<span data-ttu-id="dfcb2-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="dfcb2-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="dfcb2-126">Implementations</span></span>

-   [<span data-ttu-id="dfcb2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dfcb2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dfcb2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dfcb2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfcb2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfcb2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dfcb2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfcb2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="dfcb2-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-134">Entry</span></span> | <span data-ttu-id="dfcb2-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-137">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-138">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-139">System-Only</span></span>            | <span data-ttu-id="dfcb2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-140">False</span></span>                                                |
| <span data-ttu-id="dfcb2-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-142">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-143">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-144">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-144">False</span></span>                                                |
| <span data-ttu-id="dfcb2-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-145">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-146">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-146">False</span></span>                                                |
| <span data-ttu-id="dfcb2-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-149">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-150">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-150">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-151">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-152">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-152">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-153">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-154">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-155">System-Flags</span></span>           | <span data-ttu-id="dfcb2-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-156">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-157">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-158">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dfcb2-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfcb2-159">Windows Server 2003</span></span>



| <span data-ttu-id="dfcb2-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-160">Entry</span></span> | <span data-ttu-id="dfcb2-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-163">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-164">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-165">System-Only</span></span>            | <span data-ttu-id="dfcb2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-166">False</span></span>                                                |
| <span data-ttu-id="dfcb2-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-167">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-168">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-169">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-170">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-170">False</span></span>                                                |
| <span data-ttu-id="dfcb2-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-171">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-172">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-172">False</span></span>                                                |
| <span data-ttu-id="dfcb2-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-175">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-176">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-176">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-177">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-178">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-178">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-179">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-180">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-181">System-Flags</span></span>           | <span data-ttu-id="dfcb2-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-182">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-183">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-183">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-184">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dfcb2-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dfcb2-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dfcb2-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-186">Entry</span></span> | <span data-ttu-id="dfcb2-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-189">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-190">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-191">System-Only</span></span>            | <span data-ttu-id="dfcb2-192">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-192">False</span></span>                                                |
| <span data-ttu-id="dfcb2-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-193">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-194">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-195">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-196">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-196">False</span></span>                                                |
| <span data-ttu-id="dfcb2-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-197">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-198">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-198">False</span></span>                                                |
| <span data-ttu-id="dfcb2-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-201">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-202">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-202">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-203">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-204">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-204">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-205">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-206">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-207">System-Flags</span></span>           | <span data-ttu-id="dfcb2-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-208">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-209">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-210">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dfcb2-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfcb2-211">Windows Server 2008</span></span>



| <span data-ttu-id="dfcb2-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-212">Entry</span></span> | <span data-ttu-id="dfcb2-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-215">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-216">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-217">System-Only</span></span>            | <span data-ttu-id="dfcb2-218">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-218">False</span></span>                                                |
| <span data-ttu-id="dfcb2-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-219">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-220">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-221">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-222">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-222">False</span></span>                                                |
| <span data-ttu-id="dfcb2-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-223">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-224">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-224">False</span></span>                                                |
| <span data-ttu-id="dfcb2-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-227">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-228">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-228">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-229">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-230">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-230">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-231">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-232">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-233">System-Flags</span></span>           | <span data-ttu-id="dfcb2-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-234">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-235">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-235">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-236">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfcb2-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfcb2-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfcb2-238">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-238">Entry</span></span> | <span data-ttu-id="dfcb2-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-240">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-241">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-242">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-243">System-Only</span></span>            | <span data-ttu-id="dfcb2-244">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-244">False</span></span>                                                |
| <span data-ttu-id="dfcb2-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-245">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-246">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-247">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-248">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-248">False</span></span>                                                |
| <span data-ttu-id="dfcb2-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-249">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-250">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-250">False</span></span>                                                |
| <span data-ttu-id="dfcb2-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-253">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-254">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-254">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-255">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-256">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-256">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-257">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-258">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-259">System-Flags</span></span>           | <span data-ttu-id="dfcb2-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-260">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-261">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-261">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-262">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfcb2-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfcb2-263">Windows Server 2012</span></span>



| <span data-ttu-id="dfcb2-264">Entrée</span><span class="sxs-lookup"><span data-stu-id="dfcb2-264">Entry</span></span> | <span data-ttu-id="dfcb2-265">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb2-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dfcb2-266">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dfcb2-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="dfcb2-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfcb2-267">MAPI-Id</span></span>                | <span data-ttu-id="dfcb2-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="dfcb2-268">0x3004</span></span>                                               |
| <span data-ttu-id="dfcb2-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfcb2-269">System-Only</span></span>            | <span data-ttu-id="dfcb2-270">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-270">False</span></span>                                                |
| <span data-ttu-id="dfcb2-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dfcb2-271">Is-Single-Valued</span></span>       | <span data-ttu-id="dfcb2-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="dfcb2-272">True</span></span>                                                 |
| <span data-ttu-id="dfcb2-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dfcb2-273">Is Indexed</span></span>             | <span data-ttu-id="dfcb2-274">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-274">False</span></span>                                                |
| <span data-ttu-id="dfcb2-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dfcb2-275">In Global Catalog</span></span>      | <span data-ttu-id="dfcb2-276">Faux</span><span class="sxs-lookup"><span data-stu-id="dfcb2-276">False</span></span>                                                |
| <span data-ttu-id="dfcb2-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dfcb2-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfcb2-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dfcb2-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="dfcb2-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfcb2-279">Range-Lower</span></span>            | <span data-ttu-id="dfcb2-280">1</span><span class="sxs-lookup"><span data-stu-id="dfcb2-280">1</span></span>                                                    |
| <span data-ttu-id="dfcb2-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfcb2-281">Range-Upper</span></span>            | <span data-ttu-id="dfcb2-282">1 024</span><span class="sxs-lookup"><span data-stu-id="dfcb2-282">1024</span></span>                                                 |
| <span data-ttu-id="dfcb2-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-283">Search-Flags</span></span>           | <span data-ttu-id="dfcb2-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfcb2-284">0x00000000</span></span>                                           |
| <span data-ttu-id="dfcb2-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfcb2-285">System-Flags</span></span>           | <span data-ttu-id="dfcb2-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfcb2-286">0x00000010</span></span>                                           |
| <span data-ttu-id="dfcb2-287">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dfcb2-287">Classes used in</span></span>        | [<span data-ttu-id="dfcb2-288">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="dfcb2-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





