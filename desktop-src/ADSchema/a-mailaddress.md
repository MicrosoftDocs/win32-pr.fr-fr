---
title: Attribut adresse de messagerie SMTP
description: Attribut d’adresse de messagerie générique. Utilisé dans la zone comme un attribut facultatif des objets serveur, où ils sont utilisés par la réplication de service d’annuaire par courrier (si les ordinateurs sont configurés).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut adresse de messagerie SMTP
- Schéma AD de l’attribut mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107227"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="2f1bf-106">Attribut adresse de messagerie SMTP</span><span class="sxs-lookup"><span data-stu-id="2f1bf-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="2f1bf-107">Attribut d’adresse de messagerie générique.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-107">Generic mail address attribute.</span></span> <span data-ttu-id="2f1bf-108">Utilisé dans la zone comme un attribut facultatif des objets serveur, où ils sont utilisés par la réplication de service d’annuaire par courrier (si les ordinateurs sont configurés).</span><span class="sxs-lookup"><span data-stu-id="2f1bf-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="2f1bf-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-109">Entry</span></span> | <span data-ttu-id="2f1bf-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2f1bf-111">CN</span><span class="sxs-lookup"><span data-stu-id="2f1bf-111">CN</span></span>                | <span data-ttu-id="2f1bf-112">Adresse de messagerie SMTP</span><span class="sxs-lookup"><span data-stu-id="2f1bf-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="2f1bf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2f1bf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2f1bf-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="2f1bf-114">mailAddress</span></span>                                 |
| <span data-ttu-id="2f1bf-115">Taille</span><span class="sxs-lookup"><span data-stu-id="2f1bf-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="2f1bf-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2f1bf-116">Update Privilege</span></span>  | <span data-ttu-id="2f1bf-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="2f1bf-117">Domain administrator</span></span>                        |
| <span data-ttu-id="2f1bf-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2f1bf-118">Update Frequency</span></span>  | <span data-ttu-id="2f1bf-119">Presque jamais</span><span class="sxs-lookup"><span data-stu-id="2f1bf-119">Almost never</span></span>                                |
| <span data-ttu-id="2f1bf-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-120">Attribute-Id</span></span>      | <span data-ttu-id="2f1bf-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="2f1bf-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="2f1bf-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2f1bf-122">System-Id-Guid</span></span>    | <span data-ttu-id="2f1bf-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2f1bf-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="2f1bf-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f1bf-124">Syntax</span></span>            | [<span data-ttu-id="2f1bf-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2f1bf-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2f1bf-126">Implementations</span></span>

-   [<span data-ttu-id="2f1bf-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2f1bf-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f1bf-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2f1bf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f1bf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f1bf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f1bf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2f1bf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f1bf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2f1bf-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-135">Entry</span></span> | <span data-ttu-id="2f1bf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-139">System-Only</span></span>            | <span data-ttu-id="2f1bf-140">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-140">False</span></span>                                 |
| <span data-ttu-id="2f1bf-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-142">True</span></span>                                  |
| <span data-ttu-id="2f1bf-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-143">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-144">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-144">False</span></span>                                 |
| <span data-ttu-id="2f1bf-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-145">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-146">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-146">False</span></span>                                 |
| <span data-ttu-id="2f1bf-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-151">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-152">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-153">System-Flags</span></span>           | <span data-ttu-id="2f1bf-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-154">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-155">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-156">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2f1bf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f1bf-157">Windows Server 2003</span></span>



| <span data-ttu-id="2f1bf-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-158">Entry</span></span> | <span data-ttu-id="2f1bf-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-162">System-Only</span></span>            | <span data-ttu-id="2f1bf-163">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-163">False</span></span>                                 |
| <span data-ttu-id="2f1bf-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-165">True</span></span>                                  |
| <span data-ttu-id="2f1bf-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-166">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-167">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-167">False</span></span>                                 |
| <span data-ttu-id="2f1bf-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-168">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-169">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-169">False</span></span>                                 |
| <span data-ttu-id="2f1bf-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-174">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-175">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-176">System-Flags</span></span>           | <span data-ttu-id="2f1bf-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-177">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-178">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-179">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2f1bf-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="2f1bf-180">ADAM</span></span>



| <span data-ttu-id="2f1bf-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-181">Entry</span></span> | <span data-ttu-id="2f1bf-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-185">System-Only</span></span>            | <span data-ttu-id="2f1bf-186">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-186">False</span></span>                                 |
| <span data-ttu-id="2f1bf-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-188">True</span></span>                                  |
| <span data-ttu-id="2f1bf-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-189">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-190">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-190">False</span></span>                                 |
| <span data-ttu-id="2f1bf-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-191">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-192">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-192">False</span></span>                                 |
| <span data-ttu-id="2f1bf-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-197">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-198">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-199">System-Flags</span></span>           | <span data-ttu-id="2f1bf-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-200">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-201">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-202">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f1bf-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f1bf-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f1bf-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-204">Entry</span></span> | <span data-ttu-id="2f1bf-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-208">System-Only</span></span>            | <span data-ttu-id="2f1bf-209">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-209">False</span></span>                                 |
| <span data-ttu-id="2f1bf-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-211">True</span></span>                                  |
| <span data-ttu-id="2f1bf-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-212">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-213">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-213">False</span></span>                                 |
| <span data-ttu-id="2f1bf-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-214">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-215">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-215">False</span></span>                                 |
| <span data-ttu-id="2f1bf-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-220">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-221">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-222">System-Flags</span></span>           | <span data-ttu-id="2f1bf-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-223">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-224">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-225">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f1bf-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f1bf-226">Windows Server 2008</span></span>



| <span data-ttu-id="2f1bf-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-227">Entry</span></span> | <span data-ttu-id="2f1bf-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-231">System-Only</span></span>            | <span data-ttu-id="2f1bf-232">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-232">False</span></span>                                 |
| <span data-ttu-id="2f1bf-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-234">True</span></span>                                  |
| <span data-ttu-id="2f1bf-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-235">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-236">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-236">False</span></span>                                 |
| <span data-ttu-id="2f1bf-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-237">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-238">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-238">False</span></span>                                 |
| <span data-ttu-id="2f1bf-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-243">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-244">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-245">System-Flags</span></span>           | <span data-ttu-id="2f1bf-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-246">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-247">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-248">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f1bf-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f1bf-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f1bf-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-250">Entry</span></span> | <span data-ttu-id="2f1bf-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-254">System-Only</span></span>            | <span data-ttu-id="2f1bf-255">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-255">False</span></span>                                 |
| <span data-ttu-id="2f1bf-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-257">True</span></span>                                  |
| <span data-ttu-id="2f1bf-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-258">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-259">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-259">False</span></span>                                 |
| <span data-ttu-id="2f1bf-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-260">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-261">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-261">False</span></span>                                 |
| <span data-ttu-id="2f1bf-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-266">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-267">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-268">System-Flags</span></span>           | <span data-ttu-id="2f1bf-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-269">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-270">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-271">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f1bf-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f1bf-272">Windows Server 2012</span></span>



| <span data-ttu-id="2f1bf-273">Entrée</span><span class="sxs-lookup"><span data-stu-id="2f1bf-273">Entry</span></span> | <span data-ttu-id="2f1bf-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1bf-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="2f1bf-275">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2f1bf-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f1bf-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="2f1bf-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f1bf-277">System-Only</span></span>            | <span data-ttu-id="2f1bf-278">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-278">False</span></span>                                 |
| <span data-ttu-id="2f1bf-279">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2f1bf-279">Is-Single-Valued</span></span>       | <span data-ttu-id="2f1bf-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="2f1bf-280">True</span></span>                                  |
| <span data-ttu-id="2f1bf-281">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2f1bf-281">Is Indexed</span></span>             | <span data-ttu-id="2f1bf-282">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-282">False</span></span>                                 |
| <span data-ttu-id="2f1bf-283">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2f1bf-283">In Global Catalog</span></span>      | <span data-ttu-id="2f1bf-284">Faux</span><span class="sxs-lookup"><span data-stu-id="2f1bf-284">False</span></span>                                 |
| <span data-ttu-id="2f1bf-285">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2f1bf-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f1bf-286">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2f1bf-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="2f1bf-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f1bf-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f1bf-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="2f1bf-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-289">Search-Flags</span></span>           | <span data-ttu-id="2f1bf-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f1bf-290">0x00000000</span></span>                            |
| <span data-ttu-id="2f1bf-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f1bf-291">System-Flags</span></span>           | <span data-ttu-id="2f1bf-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f1bf-292">0x00000010</span></span>                            |
| <span data-ttu-id="2f1bf-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2f1bf-293">Classes used in</span></span>        | [<span data-ttu-id="2f1bf-294">**Serveurs**</span><span class="sxs-lookup"><span data-stu-id="2f1bf-294">**Server**</span></span>](c-server.md)<br/> |



 

 





