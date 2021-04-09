---
title: Attribut MSMQ-Recipient-FormatName
description: Utilisé comme nom de format de destinataire dans la classe MSMQ-Custom-Recipient.
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MSMQ-Recipient-FormatName
- Schéma AD de l’attribut msMQ-Recipient-FormatName
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108099"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="26405-105">Attribut MSMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="26405-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="26405-106">Utilisé comme nom de format de destinataire dans la classe MSMQ-Custom-Recipient.</span><span class="sxs-lookup"><span data-stu-id="26405-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="26405-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-107">Entry</span></span> | <span data-ttu-id="26405-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="26405-109">CN</span><span class="sxs-lookup"><span data-stu-id="26405-109">CN</span></span>                | <span data-ttu-id="26405-110">MSMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="26405-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="26405-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="26405-111">Ldap-Display-Name</span></span> | <span data-ttu-id="26405-112">msMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="26405-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="26405-113">Taille</span><span class="sxs-lookup"><span data-stu-id="26405-113">Size</span></span>              | <span data-ttu-id="26405-114">1 à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="26405-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="26405-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="26405-115">Update Privilege</span></span>  | <span data-ttu-id="26405-116">Propriétaire de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="26405-116">The queue owner.</span></span>                            |
| <span data-ttu-id="26405-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="26405-117">Update Frequency</span></span>  | <span data-ttu-id="26405-118">Uniquement après le déplacement de la file d’attente externe.</span><span class="sxs-lookup"><span data-stu-id="26405-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="26405-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26405-119">Attribute-Id</span></span>      | <span data-ttu-id="26405-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="26405-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="26405-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="26405-121">System-Id-Guid</span></span>    | <span data-ttu-id="26405-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="26405-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="26405-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26405-123">Syntax</span></span>            | [<span data-ttu-id="26405-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="26405-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="26405-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="26405-125">Implementations</span></span>

-   [<span data-ttu-id="26405-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26405-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26405-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26405-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26405-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26405-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26405-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26405-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26405-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26405-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="26405-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26405-131">Windows Server 2003</span></span>



| <span data-ttu-id="26405-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-132">Entry</span></span> | <span data-ttu-id="26405-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26405-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="26405-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26405-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="26405-136">System-Only</span></span>            | <span data-ttu-id="26405-137">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-137">False</span></span>                                                               |
| <span data-ttu-id="26405-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="26405-138">Is-Single-Valued</span></span>       | <span data-ttu-id="26405-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="26405-139">True</span></span>                                                                |
| <span data-ttu-id="26405-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="26405-140">Is Indexed</span></span>             | <span data-ttu-id="26405-141">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-141">False</span></span>                                                               |
| <span data-ttu-id="26405-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="26405-142">In Global Catalog</span></span>      | <span data-ttu-id="26405-143">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-143">False</span></span>                                                               |
| <span data-ttu-id="26405-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="26405-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="26405-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="26405-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="26405-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26405-146">Range-Lower</span></span>            | <span data-ttu-id="26405-147">1</span><span class="sxs-lookup"><span data-stu-id="26405-147">1</span></span>                                                                   |
| <span data-ttu-id="26405-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26405-148">Range-Upper</span></span>            | <span data-ttu-id="26405-149">255</span><span class="sxs-lookup"><span data-stu-id="26405-149">255</span></span>                                                                 |
| <span data-ttu-id="26405-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-150">Search-Flags</span></span>           | <span data-ttu-id="26405-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26405-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="26405-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-152">System-Flags</span></span>           | <span data-ttu-id="26405-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26405-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="26405-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="26405-154">Classes used in</span></span>        | [<span data-ttu-id="26405-155">**MSMQ-personnalisé-destinataire**</span><span class="sxs-lookup"><span data-stu-id="26405-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26405-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26405-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26405-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-157">Entry</span></span> | <span data-ttu-id="26405-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26405-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="26405-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26405-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="26405-161">System-Only</span></span>            | <span data-ttu-id="26405-162">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-162">False</span></span>                                                               |
| <span data-ttu-id="26405-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="26405-163">Is-Single-Valued</span></span>       | <span data-ttu-id="26405-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="26405-164">True</span></span>                                                                |
| <span data-ttu-id="26405-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="26405-165">Is Indexed</span></span>             | <span data-ttu-id="26405-166">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-166">False</span></span>                                                               |
| <span data-ttu-id="26405-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="26405-167">In Global Catalog</span></span>      | <span data-ttu-id="26405-168">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-168">False</span></span>                                                               |
| <span data-ttu-id="26405-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="26405-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="26405-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="26405-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="26405-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26405-171">Range-Lower</span></span>            | <span data-ttu-id="26405-172">1</span><span class="sxs-lookup"><span data-stu-id="26405-172">1</span></span>                                                                   |
| <span data-ttu-id="26405-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26405-173">Range-Upper</span></span>            | <span data-ttu-id="26405-174">255</span><span class="sxs-lookup"><span data-stu-id="26405-174">255</span></span>                                                                 |
| <span data-ttu-id="26405-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-175">Search-Flags</span></span>           | <span data-ttu-id="26405-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26405-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="26405-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-177">System-Flags</span></span>           | <span data-ttu-id="26405-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26405-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="26405-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="26405-179">Classes used in</span></span>        | [<span data-ttu-id="26405-180">**MSMQ-personnalisé-destinataire**</span><span class="sxs-lookup"><span data-stu-id="26405-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="26405-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26405-181">Windows Server 2008</span></span>



| <span data-ttu-id="26405-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-182">Entry</span></span> | <span data-ttu-id="26405-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26405-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="26405-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26405-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="26405-186">System-Only</span></span>            | <span data-ttu-id="26405-187">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-187">False</span></span>                                                               |
| <span data-ttu-id="26405-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="26405-188">Is-Single-Valued</span></span>       | <span data-ttu-id="26405-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="26405-189">True</span></span>                                                                |
| <span data-ttu-id="26405-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="26405-190">Is Indexed</span></span>             | <span data-ttu-id="26405-191">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-191">False</span></span>                                                               |
| <span data-ttu-id="26405-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="26405-192">In Global Catalog</span></span>      | <span data-ttu-id="26405-193">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-193">False</span></span>                                                               |
| <span data-ttu-id="26405-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="26405-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="26405-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="26405-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="26405-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26405-196">Range-Lower</span></span>            | <span data-ttu-id="26405-197">1</span><span class="sxs-lookup"><span data-stu-id="26405-197">1</span></span>                                                                   |
| <span data-ttu-id="26405-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26405-198">Range-Upper</span></span>            | <span data-ttu-id="26405-199">255</span><span class="sxs-lookup"><span data-stu-id="26405-199">255</span></span>                                                                 |
| <span data-ttu-id="26405-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-200">Search-Flags</span></span>           | <span data-ttu-id="26405-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26405-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="26405-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-202">System-Flags</span></span>           | <span data-ttu-id="26405-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26405-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="26405-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="26405-204">Classes used in</span></span>        | [<span data-ttu-id="26405-205">**MSMQ-personnalisé-destinataire**</span><span class="sxs-lookup"><span data-stu-id="26405-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26405-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26405-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26405-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-207">Entry</span></span> | <span data-ttu-id="26405-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26405-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="26405-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26405-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="26405-211">System-Only</span></span>            | <span data-ttu-id="26405-212">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-212">False</span></span>                                                               |
| <span data-ttu-id="26405-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="26405-213">Is-Single-Valued</span></span>       | <span data-ttu-id="26405-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="26405-214">True</span></span>                                                                |
| <span data-ttu-id="26405-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="26405-215">Is Indexed</span></span>             | <span data-ttu-id="26405-216">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-216">False</span></span>                                                               |
| <span data-ttu-id="26405-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="26405-217">In Global Catalog</span></span>      | <span data-ttu-id="26405-218">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-218">False</span></span>                                                               |
| <span data-ttu-id="26405-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="26405-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="26405-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="26405-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="26405-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26405-221">Range-Lower</span></span>            | <span data-ttu-id="26405-222">1</span><span class="sxs-lookup"><span data-stu-id="26405-222">1</span></span>                                                                   |
| <span data-ttu-id="26405-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26405-223">Range-Upper</span></span>            | <span data-ttu-id="26405-224">255</span><span class="sxs-lookup"><span data-stu-id="26405-224">255</span></span>                                                                 |
| <span data-ttu-id="26405-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-225">Search-Flags</span></span>           | <span data-ttu-id="26405-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26405-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="26405-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-227">System-Flags</span></span>           | <span data-ttu-id="26405-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26405-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="26405-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="26405-229">Classes used in</span></span>        | [<span data-ttu-id="26405-230">**MSMQ-personnalisé-destinataire**</span><span class="sxs-lookup"><span data-stu-id="26405-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="26405-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26405-231">Windows Server 2012</span></span>



| <span data-ttu-id="26405-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="26405-232">Entry</span></span> | <span data-ttu-id="26405-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="26405-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26405-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="26405-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26405-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="26405-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="26405-236">System-Only</span></span>            | <span data-ttu-id="26405-237">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-237">False</span></span>                                                               |
| <span data-ttu-id="26405-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="26405-238">Is-Single-Valued</span></span>       | <span data-ttu-id="26405-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="26405-239">True</span></span>                                                                |
| <span data-ttu-id="26405-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="26405-240">Is Indexed</span></span>             | <span data-ttu-id="26405-241">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-241">False</span></span>                                                               |
| <span data-ttu-id="26405-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="26405-242">In Global Catalog</span></span>      | <span data-ttu-id="26405-243">Faux</span><span class="sxs-lookup"><span data-stu-id="26405-243">False</span></span>                                                               |
| <span data-ttu-id="26405-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="26405-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="26405-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="26405-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="26405-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26405-246">Range-Lower</span></span>            | <span data-ttu-id="26405-247">1</span><span class="sxs-lookup"><span data-stu-id="26405-247">1</span></span>                                                                   |
| <span data-ttu-id="26405-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26405-248">Range-Upper</span></span>            | <span data-ttu-id="26405-249">255</span><span class="sxs-lookup"><span data-stu-id="26405-249">255</span></span>                                                                 |
| <span data-ttu-id="26405-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-250">Search-Flags</span></span>           | <span data-ttu-id="26405-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26405-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="26405-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26405-252">System-Flags</span></span>           | <span data-ttu-id="26405-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26405-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="26405-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="26405-254">Classes used in</span></span>        | [<span data-ttu-id="26405-255">**MSMQ-personnalisé-destinataire**</span><span class="sxs-lookup"><span data-stu-id="26405-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 





