---
title: Attribut de nom de la DLL de transport
description: Nom de la DLL qui gérera un transport.
ms.assetid: a6b078ec-8738-4c57-9d94-05a96dbc645b
ms.tgt_platform: multiple
keywords:
- Attribut de nom de la DLL de transport-schéma AD
- Schéma AD de l’attribut transportDLLName
topic_type:
- apiref
api_name:
- Transport-DLL-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c118a2f7553c86de4b3c36b2904a3b7d75518a2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516132"
---
# <a name="transport-dll-name-attribute"></a><span data-ttu-id="d7a83-105">Attribut de nom de la DLL de transport</span><span class="sxs-lookup"><span data-stu-id="d7a83-105">Transport-DLL-Name attribute</span></span>

<span data-ttu-id="d7a83-106">Nom de la DLL qui gérera un transport.</span><span class="sxs-lookup"><span data-stu-id="d7a83-106">The name of the DLL that will manage a transport.</span></span>



| <span data-ttu-id="d7a83-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-107">Entry</span></span> | <span data-ttu-id="d7a83-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d7a83-109">CN</span><span class="sxs-lookup"><span data-stu-id="d7a83-109">CN</span></span>                | <span data-ttu-id="d7a83-110">Transport-DLL-Name</span><span class="sxs-lookup"><span data-stu-id="d7a83-110">Transport-DLL-Name</span></span>                          |
| <span data-ttu-id="d7a83-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d7a83-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d7a83-112">transportDLLName</span><span class="sxs-lookup"><span data-stu-id="d7a83-112">transportDLLName</span></span>                            |
| <span data-ttu-id="d7a83-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d7a83-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d7a83-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d7a83-114">Update Privilege</span></span>  | <span data-ttu-id="d7a83-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="d7a83-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="d7a83-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d7a83-116">Update Frequency</span></span>  | <span data-ttu-id="d7a83-117">Lors de la connexion de sites.</span><span class="sxs-lookup"><span data-stu-id="d7a83-117">When connecting sites.</span></span>                      |
| <span data-ttu-id="d7a83-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-118">Attribute-Id</span></span>      | <span data-ttu-id="d7a83-119">1.2.840.113556.1.4.789</span><span class="sxs-lookup"><span data-stu-id="d7a83-119">1.2.840.113556.1.4.789</span></span>                      |
| <span data-ttu-id="d7a83-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d7a83-120">System-Id-Guid</span></span>    | <span data-ttu-id="d7a83-121">26d97372-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d7a83-121">26d97372-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="d7a83-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7a83-122">Syntax</span></span>            | [<span data-ttu-id="d7a83-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d7a83-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d7a83-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d7a83-124">Implementations</span></span>

-   [<span data-ttu-id="d7a83-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d7a83-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d7a83-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d7a83-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d7a83-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d7a83-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d7a83-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d7a83-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d7a83-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d7a83-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d7a83-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d7a83-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d7a83-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d7a83-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d7a83-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7a83-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d7a83-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-133">Entry</span></span> | <span data-ttu-id="d7a83-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-137">System-Only</span></span>            | <span data-ttu-id="d7a83-138">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-138">False</span></span>                                                           |
| <span data-ttu-id="d7a83-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-140">True</span></span>                                                            |
| <span data-ttu-id="d7a83-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-141">Is Indexed</span></span>             | <span data-ttu-id="d7a83-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-142">False</span></span>                                                           |
| <span data-ttu-id="d7a83-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-143">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-144">False</span></span>                                                           |
| <span data-ttu-id="d7a83-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-147">Range-Lower</span></span>            | <span data-ttu-id="d7a83-148">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-148">0</span></span>                                                               |
| <span data-ttu-id="d7a83-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-149">Range-Upper</span></span>            | <span data-ttu-id="d7a83-150">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-150">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-151">Search-Flags</span></span>           | <span data-ttu-id="d7a83-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-153">System-Flags</span></span>           | <span data-ttu-id="d7a83-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-155">Classes used in</span></span>        | [<span data-ttu-id="d7a83-156">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d7a83-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7a83-157">Windows Server 2003</span></span>



| <span data-ttu-id="d7a83-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-158">Entry</span></span> | <span data-ttu-id="d7a83-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-162">System-Only</span></span>            | <span data-ttu-id="d7a83-163">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-163">False</span></span>                                                           |
| <span data-ttu-id="d7a83-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-165">True</span></span>                                                            |
| <span data-ttu-id="d7a83-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-166">Is Indexed</span></span>             | <span data-ttu-id="d7a83-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-167">False</span></span>                                                           |
| <span data-ttu-id="d7a83-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-168">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-169">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-169">False</span></span>                                                           |
| <span data-ttu-id="d7a83-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-172">Range-Lower</span></span>            | <span data-ttu-id="d7a83-173">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-173">0</span></span>                                                               |
| <span data-ttu-id="d7a83-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-174">Range-Upper</span></span>            | <span data-ttu-id="d7a83-175">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-175">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-176">Search-Flags</span></span>           | <span data-ttu-id="d7a83-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-178">System-Flags</span></span>           | <span data-ttu-id="d7a83-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-180">Classes used in</span></span>        | [<span data-ttu-id="d7a83-181">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-181">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d7a83-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="d7a83-182">ADAM</span></span>



| <span data-ttu-id="d7a83-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-183">Entry</span></span> | <span data-ttu-id="d7a83-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-187">System-Only</span></span>            | <span data-ttu-id="d7a83-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-188">False</span></span>                                                           |
| <span data-ttu-id="d7a83-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-189">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-190">True</span></span>                                                            |
| <span data-ttu-id="d7a83-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-191">Is Indexed</span></span>             | <span data-ttu-id="d7a83-192">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-192">False</span></span>                                                           |
| <span data-ttu-id="d7a83-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-193">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-194">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-194">False</span></span>                                                           |
| <span data-ttu-id="d7a83-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-197">Range-Lower</span></span>            | <span data-ttu-id="d7a83-198">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-198">0</span></span>                                                               |
| <span data-ttu-id="d7a83-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-199">Range-Upper</span></span>            | <span data-ttu-id="d7a83-200">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-200">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-201">Search-Flags</span></span>           | <span data-ttu-id="d7a83-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-203">System-Flags</span></span>           | <span data-ttu-id="d7a83-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-205">Classes used in</span></span>        | [<span data-ttu-id="d7a83-206">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-206">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d7a83-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d7a83-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d7a83-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-208">Entry</span></span> | <span data-ttu-id="d7a83-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-212">System-Only</span></span>            | <span data-ttu-id="d7a83-213">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-213">False</span></span>                                                           |
| <span data-ttu-id="d7a83-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-214">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-215">True</span></span>                                                            |
| <span data-ttu-id="d7a83-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-216">Is Indexed</span></span>             | <span data-ttu-id="d7a83-217">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-217">False</span></span>                                                           |
| <span data-ttu-id="d7a83-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-218">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-219">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-219">False</span></span>                                                           |
| <span data-ttu-id="d7a83-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-222">Range-Lower</span></span>            | <span data-ttu-id="d7a83-223">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-223">0</span></span>                                                               |
| <span data-ttu-id="d7a83-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-224">Range-Upper</span></span>            | <span data-ttu-id="d7a83-225">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-225">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-226">Search-Flags</span></span>           | <span data-ttu-id="d7a83-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-228">System-Flags</span></span>           | <span data-ttu-id="d7a83-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-230">Classes used in</span></span>        | [<span data-ttu-id="d7a83-231">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-231">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d7a83-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7a83-232">Windows Server 2008</span></span>



| <span data-ttu-id="d7a83-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-233">Entry</span></span> | <span data-ttu-id="d7a83-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-237">System-Only</span></span>            | <span data-ttu-id="d7a83-238">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-238">False</span></span>                                                           |
| <span data-ttu-id="d7a83-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-239">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-240">True</span></span>                                                            |
| <span data-ttu-id="d7a83-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-241">Is Indexed</span></span>             | <span data-ttu-id="d7a83-242">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-242">False</span></span>                                                           |
| <span data-ttu-id="d7a83-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-243">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-244">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-244">False</span></span>                                                           |
| <span data-ttu-id="d7a83-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-247">Range-Lower</span></span>            | <span data-ttu-id="d7a83-248">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-248">0</span></span>                                                               |
| <span data-ttu-id="d7a83-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-249">Range-Upper</span></span>            | <span data-ttu-id="d7a83-250">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-250">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-251">Search-Flags</span></span>           | <span data-ttu-id="d7a83-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-253">System-Flags</span></span>           | <span data-ttu-id="d7a83-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-255">Classes used in</span></span>        | [<span data-ttu-id="d7a83-256">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-256">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d7a83-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7a83-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d7a83-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-258">Entry</span></span> | <span data-ttu-id="d7a83-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-262">System-Only</span></span>            | <span data-ttu-id="d7a83-263">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-263">False</span></span>                                                           |
| <span data-ttu-id="d7a83-264">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-264">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-265">True</span></span>                                                            |
| <span data-ttu-id="d7a83-266">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-266">Is Indexed</span></span>             | <span data-ttu-id="d7a83-267">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-267">False</span></span>                                                           |
| <span data-ttu-id="d7a83-268">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-268">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-269">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-269">False</span></span>                                                           |
| <span data-ttu-id="d7a83-270">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-271">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-272">Range-Lower</span></span>            | <span data-ttu-id="d7a83-273">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-273">0</span></span>                                                               |
| <span data-ttu-id="d7a83-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-274">Range-Upper</span></span>            | <span data-ttu-id="d7a83-275">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-275">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-276">Search-Flags</span></span>           | <span data-ttu-id="d7a83-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-278">System-Flags</span></span>           | <span data-ttu-id="d7a83-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-280">Classes used in</span></span>        | [<span data-ttu-id="d7a83-281">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-281">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d7a83-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7a83-282">Windows Server 2012</span></span>



| <span data-ttu-id="d7a83-283">Entrée</span><span class="sxs-lookup"><span data-stu-id="d7a83-283">Entry</span></span> | <span data-ttu-id="d7a83-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a83-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7a83-285">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d7a83-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7a83-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d7a83-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7a83-287">System-Only</span></span>            | <span data-ttu-id="d7a83-288">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-288">False</span></span>                                                           |
| <span data-ttu-id="d7a83-289">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d7a83-289">Is-Single-Valued</span></span>       | <span data-ttu-id="d7a83-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="d7a83-290">True</span></span>                                                            |
| <span data-ttu-id="d7a83-291">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d7a83-291">Is Indexed</span></span>             | <span data-ttu-id="d7a83-292">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-292">False</span></span>                                                           |
| <span data-ttu-id="d7a83-293">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d7a83-293">In Global Catalog</span></span>      | <span data-ttu-id="d7a83-294">Faux</span><span class="sxs-lookup"><span data-stu-id="d7a83-294">False</span></span>                                                           |
| <span data-ttu-id="d7a83-295">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d7a83-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7a83-296">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d7a83-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d7a83-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7a83-297">Range-Lower</span></span>            | <span data-ttu-id="d7a83-298">0</span><span class="sxs-lookup"><span data-stu-id="d7a83-298">0</span></span>                                                               |
| <span data-ttu-id="d7a83-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7a83-299">Range-Upper</span></span>            | <span data-ttu-id="d7a83-300">1 024</span><span class="sxs-lookup"><span data-stu-id="d7a83-300">1024</span></span>                                                            |
| <span data-ttu-id="d7a83-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-301">Search-Flags</span></span>           | <span data-ttu-id="d7a83-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7a83-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="d7a83-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7a83-303">System-Flags</span></span>           | <span data-ttu-id="d7a83-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7a83-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="d7a83-305">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d7a83-305">Classes used in</span></span>        | [<span data-ttu-id="d7a83-306">**Transport inter-sites**</span><span class="sxs-lookup"><span data-stu-id="d7a83-306">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



 

 





