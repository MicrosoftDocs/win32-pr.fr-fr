---
title: MS-WMI-attribut de classe
description: Nom d’un objet de classe WMI dans un encodage associé (par exemple, Win32 \_ ComputerSystem). L’encodage peut être une instance ou un objet de classe.
ms.assetid: a0a4284e-3b52-4597-8656-df2f3297060d
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de classe ms-WMI
- Schéma AD msWMI-attribut de classe
topic_type:
- apiref
api_name:
- ms-WMI-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e69cd36fa4242203f0b36b8598d22bf96783b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107686"
---
# <a name="ms-wmi-class-attribute"></a><span data-ttu-id="3889c-106">MS-WMI-attribut de classe</span><span class="sxs-lookup"><span data-stu-id="3889c-106">ms-WMI-Class attribute</span></span>

<span data-ttu-id="3889c-107">Nom d’un objet de classe WMI dans un encodage associé (par exemple, Win32 \_ ComputerSystem).</span><span class="sxs-lookup"><span data-stu-id="3889c-107">The name of a WMI Class object in an associated encoding (for example, Win32\_ComputerSystem).</span></span> <span data-ttu-id="3889c-108">L’encodage peut être une instance ou un objet de classe.</span><span class="sxs-lookup"><span data-stu-id="3889c-108">The encoding can be either an instance or class object.</span></span>



| <span data-ttu-id="3889c-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-109">Entry</span></span> | <span data-ttu-id="3889c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="3889c-111">CN</span><span class="sxs-lookup"><span data-stu-id="3889c-111">CN</span></span>                | <span data-ttu-id="3889c-112">MS-WMI-classe</span><span class="sxs-lookup"><span data-stu-id="3889c-112">ms-WMI-Class</span></span>                                                    |
| <span data-ttu-id="3889c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3889c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3889c-114">msWMI-classe</span><span class="sxs-lookup"><span data-stu-id="3889c-114">msWMI-Class</span></span>                                                     |
| <span data-ttu-id="3889c-115">Taille</span><span class="sxs-lookup"><span data-stu-id="3889c-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="3889c-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3889c-116">Update Privilege</span></span>  | <span data-ttu-id="3889c-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="3889c-117">Domain administrator</span></span>                                            |
| <span data-ttu-id="3889c-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3889c-118">Update Frequency</span></span>  | <span data-ttu-id="3889c-119">Chaque fois qu’une classe contenant l’attribut est ajoutée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="3889c-119">Whenever a class containing the attribute is added or modified.</span></span> |
| <span data-ttu-id="3889c-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-120">Attribute-Id</span></span>      | <span data-ttu-id="3889c-121">1.2.840.113556.1.4.1676</span><span class="sxs-lookup"><span data-stu-id="3889c-121">1.2.840.113556.1.4.1676</span></span>                                         |
| <span data-ttu-id="3889c-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3889c-122">System-Id-Guid</span></span>    | <span data-ttu-id="3889c-123">90c1925f-4a24-4b07-b202-be32eb3c8b74</span><span class="sxs-lookup"><span data-stu-id="3889c-123">90c1925f-4a24-4b07-b202-be32eb3c8b74</span></span>                            |
| <span data-ttu-id="3889c-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3889c-124">Syntax</span></span>            | [<span data-ttu-id="3889c-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3889c-125">**String(Unicode)**</span></span>](s-string-unicode.md)                     |



## <a name="implementations"></a><span data-ttu-id="3889c-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3889c-126">Implementations</span></span>

-   [<span data-ttu-id="3889c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3889c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3889c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3889c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3889c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3889c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3889c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3889c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3889c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3889c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3889c-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3889c-132">Windows Server 2003</span></span>



| <span data-ttu-id="3889c-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-133">Entry</span></span> | <span data-ttu-id="3889c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3889c-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3889c-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3889c-137">System-Only</span></span>            | <span data-ttu-id="3889c-138">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-138">False</span></span>                                                              |
| <span data-ttu-id="3889c-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3889c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3889c-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="3889c-140">True</span></span>                                                               |
| <span data-ttu-id="3889c-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3889c-141">Is Indexed</span></span>             | <span data-ttu-id="3889c-142">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-142">False</span></span>                                                              |
| <span data-ttu-id="3889c-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3889c-143">In Global Catalog</span></span>      | <span data-ttu-id="3889c-144">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-144">False</span></span>                                                              |
| <span data-ttu-id="3889c-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3889c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3889c-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3889c-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3889c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3889c-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3889c-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-149">Search-Flags</span></span>           | <span data-ttu-id="3889c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3889c-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="3889c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-151">System-Flags</span></span>           | <span data-ttu-id="3889c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3889c-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="3889c-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3889c-153">Classes used in</span></span>        | [<span data-ttu-id="3889c-154">**MS-WMI-ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="3889c-154">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3889c-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3889c-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3889c-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-156">Entry</span></span> | <span data-ttu-id="3889c-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3889c-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3889c-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3889c-160">System-Only</span></span>            | <span data-ttu-id="3889c-161">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-161">False</span></span>                                                              |
| <span data-ttu-id="3889c-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3889c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3889c-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="3889c-163">True</span></span>                                                               |
| <span data-ttu-id="3889c-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3889c-164">Is Indexed</span></span>             | <span data-ttu-id="3889c-165">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-165">False</span></span>                                                              |
| <span data-ttu-id="3889c-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3889c-166">In Global Catalog</span></span>      | <span data-ttu-id="3889c-167">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-167">False</span></span>                                                              |
| <span data-ttu-id="3889c-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3889c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3889c-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3889c-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3889c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3889c-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3889c-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-172">Search-Flags</span></span>           | <span data-ttu-id="3889c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3889c-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="3889c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-174">System-Flags</span></span>           | <span data-ttu-id="3889c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3889c-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="3889c-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3889c-176">Classes used in</span></span>        | [<span data-ttu-id="3889c-177">**MS-WMI-ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="3889c-177">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3889c-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3889c-178">Windows Server 2008</span></span>



| <span data-ttu-id="3889c-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-179">Entry</span></span> | <span data-ttu-id="3889c-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3889c-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3889c-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3889c-183">System-Only</span></span>            | <span data-ttu-id="3889c-184">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-184">False</span></span>                                                              |
| <span data-ttu-id="3889c-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3889c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3889c-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="3889c-186">True</span></span>                                                               |
| <span data-ttu-id="3889c-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3889c-187">Is Indexed</span></span>             | <span data-ttu-id="3889c-188">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-188">False</span></span>                                                              |
| <span data-ttu-id="3889c-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3889c-189">In Global Catalog</span></span>      | <span data-ttu-id="3889c-190">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-190">False</span></span>                                                              |
| <span data-ttu-id="3889c-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3889c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3889c-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3889c-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3889c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3889c-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3889c-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-195">Search-Flags</span></span>           | <span data-ttu-id="3889c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3889c-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="3889c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-197">System-Flags</span></span>           | <span data-ttu-id="3889c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3889c-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="3889c-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3889c-199">Classes used in</span></span>        | [<span data-ttu-id="3889c-200">**MS-WMI-ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="3889c-200">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3889c-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3889c-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3889c-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-202">Entry</span></span> | <span data-ttu-id="3889c-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3889c-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3889c-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="3889c-206">System-Only</span></span>            | <span data-ttu-id="3889c-207">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-207">False</span></span>                                                              |
| <span data-ttu-id="3889c-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3889c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="3889c-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="3889c-209">True</span></span>                                                               |
| <span data-ttu-id="3889c-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3889c-210">Is Indexed</span></span>             | <span data-ttu-id="3889c-211">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-211">False</span></span>                                                              |
| <span data-ttu-id="3889c-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3889c-212">In Global Catalog</span></span>      | <span data-ttu-id="3889c-213">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-213">False</span></span>                                                              |
| <span data-ttu-id="3889c-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3889c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="3889c-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3889c-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3889c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3889c-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3889c-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-218">Search-Flags</span></span>           | <span data-ttu-id="3889c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3889c-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="3889c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-220">System-Flags</span></span>           | <span data-ttu-id="3889c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3889c-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="3889c-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3889c-222">Classes used in</span></span>        | [<span data-ttu-id="3889c-223">**MS-WMI-ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="3889c-223">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3889c-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3889c-224">Windows Server 2012</span></span>



| <span data-ttu-id="3889c-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="3889c-225">Entry</span></span> | <span data-ttu-id="3889c-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="3889c-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3889c-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3889c-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3889c-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="3889c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="3889c-229">System-Only</span></span>            | <span data-ttu-id="3889c-230">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-230">False</span></span>                                                              |
| <span data-ttu-id="3889c-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3889c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="3889c-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="3889c-232">True</span></span>                                                               |
| <span data-ttu-id="3889c-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3889c-233">Is Indexed</span></span>             | <span data-ttu-id="3889c-234">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-234">False</span></span>                                                              |
| <span data-ttu-id="3889c-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3889c-235">In Global Catalog</span></span>      | <span data-ttu-id="3889c-236">Faux</span><span class="sxs-lookup"><span data-stu-id="3889c-236">False</span></span>                                                              |
| <span data-ttu-id="3889c-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3889c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="3889c-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3889c-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3889c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3889c-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3889c-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3889c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-241">Search-Flags</span></span>           | <span data-ttu-id="3889c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3889c-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="3889c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3889c-243">System-Flags</span></span>           | <span data-ttu-id="3889c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3889c-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="3889c-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3889c-245">Classes used in</span></span>        | [<span data-ttu-id="3889c-246">**MS-WMI-ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="3889c-246">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



 

 





