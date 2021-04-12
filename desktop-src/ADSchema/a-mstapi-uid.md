---
title: attribut ms-TAPI-unique-identifier
description: Fournit le nom d’une conférence de multidiffusion TAPI. Il s’agit de l’attribut de nom de la classe Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut d’identificateur unique MS-TAPI
- Schéma AD msTAPI-Uid Attribute
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385383"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="35cd8-106">attribut ms-TAPI-unique-identifier</span><span class="sxs-lookup"><span data-stu-id="35cd8-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="35cd8-107">Fournit le nom d’une conférence de multidiffusion TAPI.</span><span class="sxs-lookup"><span data-stu-id="35cd8-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="35cd8-108">Il s’agit de l’attribut de nom de la classe Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="35cd8-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="35cd8-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-109">Entry</span></span> | <span data-ttu-id="35cd8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="35cd8-111">CN</span><span class="sxs-lookup"><span data-stu-id="35cd8-111">CN</span></span>                | <span data-ttu-id="35cd8-112">MS-TAPI-unique-identifier</span><span class="sxs-lookup"><span data-stu-id="35cd8-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="35cd8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="35cd8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="35cd8-114">msTAPI-UID</span><span class="sxs-lookup"><span data-stu-id="35cd8-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="35cd8-115">Taille</span><span class="sxs-lookup"><span data-stu-id="35cd8-115">Size</span></span>              | <span data-ttu-id="35cd8-116">Peut être une chaîne arbitraire, généralement inférieure à 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="35cd8-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="35cd8-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="35cd8-117">Update Privilege</span></span>  | <span data-ttu-id="35cd8-118">Aucun privilège spécial n’est requis.</span><span class="sxs-lookup"><span data-stu-id="35cd8-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="35cd8-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="35cd8-119">Update Frequency</span></span>  | <span data-ttu-id="35cd8-120">Défini une fois au moment de la création de l’objet Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="35cd8-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="35cd8-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-121">Attribute-Id</span></span>      | <span data-ttu-id="35cd8-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="35cd8-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="35cd8-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="35cd8-123">System-Id-Guid</span></span>    | <span data-ttu-id="35cd8-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="35cd8-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="35cd8-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35cd8-125">Syntax</span></span>            | [<span data-ttu-id="35cd8-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="35cd8-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="35cd8-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="35cd8-127">Implementations</span></span>

-   [<span data-ttu-id="35cd8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="35cd8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="35cd8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="35cd8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="35cd8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="35cd8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="35cd8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="35cd8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="35cd8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="35cd8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="35cd8-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35cd8-133">Windows Server 2003</span></span>



| <span data-ttu-id="35cd8-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-134">Entry</span></span> | <span data-ttu-id="35cd8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd8-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35cd8-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="35cd8-138">System-Only</span></span>            | <span data-ttu-id="35cd8-139">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35cd8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="35cd8-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="35cd8-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="35cd8-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35cd8-142">Is Indexed</span></span>             | <span data-ttu-id="35cd8-143">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35cd8-144">In Global Catalog</span></span>      | <span data-ttu-id="35cd8-145">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35cd8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="35cd8-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35cd8-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="35cd8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35cd8-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35cd8-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-150">Search-Flags</span></span>           | <span data-ttu-id="35cd8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35cd8-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-152">System-Flags</span></span>           | <span data-ttu-id="35cd8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35cd8-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35cd8-154">Classes used in</span></span>        | [<span data-ttu-id="35cd8-155">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="35cd8-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="35cd8-156">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="35cd8-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="35cd8-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="35cd8-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="35cd8-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-158">Entry</span></span> | <span data-ttu-id="35cd8-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd8-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35cd8-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="35cd8-162">System-Only</span></span>            | <span data-ttu-id="35cd8-163">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35cd8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="35cd8-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="35cd8-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="35cd8-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35cd8-166">Is Indexed</span></span>             | <span data-ttu-id="35cd8-167">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35cd8-168">In Global Catalog</span></span>      | <span data-ttu-id="35cd8-169">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35cd8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="35cd8-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35cd8-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="35cd8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35cd8-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35cd8-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-174">Search-Flags</span></span>           | <span data-ttu-id="35cd8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35cd8-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-176">System-Flags</span></span>           | <span data-ttu-id="35cd8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35cd8-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35cd8-178">Classes used in</span></span>        | [<span data-ttu-id="35cd8-179">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="35cd8-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="35cd8-180">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="35cd8-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="35cd8-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35cd8-181">Windows Server 2008</span></span>



| <span data-ttu-id="35cd8-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-182">Entry</span></span> | <span data-ttu-id="35cd8-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd8-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35cd8-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="35cd8-186">System-Only</span></span>            | <span data-ttu-id="35cd8-187">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35cd8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="35cd8-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="35cd8-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="35cd8-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35cd8-190">Is Indexed</span></span>             | <span data-ttu-id="35cd8-191">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35cd8-192">In Global Catalog</span></span>      | <span data-ttu-id="35cd8-193">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35cd8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="35cd8-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35cd8-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="35cd8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35cd8-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35cd8-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-198">Search-Flags</span></span>           | <span data-ttu-id="35cd8-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35cd8-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-200">System-Flags</span></span>           | <span data-ttu-id="35cd8-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35cd8-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35cd8-202">Classes used in</span></span>        | [<span data-ttu-id="35cd8-203">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="35cd8-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="35cd8-204">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="35cd8-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="35cd8-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35cd8-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="35cd8-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-206">Entry</span></span> | <span data-ttu-id="35cd8-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd8-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35cd8-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="35cd8-210">System-Only</span></span>            | <span data-ttu-id="35cd8-211">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35cd8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="35cd8-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="35cd8-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="35cd8-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35cd8-214">Is Indexed</span></span>             | <span data-ttu-id="35cd8-215">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35cd8-216">In Global Catalog</span></span>      | <span data-ttu-id="35cd8-217">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35cd8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="35cd8-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35cd8-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="35cd8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35cd8-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35cd8-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-222">Search-Flags</span></span>           | <span data-ttu-id="35cd8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35cd8-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-224">System-Flags</span></span>           | <span data-ttu-id="35cd8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35cd8-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35cd8-226">Classes used in</span></span>        | [<span data-ttu-id="35cd8-227">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="35cd8-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="35cd8-228">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="35cd8-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="35cd8-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35cd8-229">Windows Server 2012</span></span>



| <span data-ttu-id="35cd8-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="35cd8-230">Entry</span></span> | <span data-ttu-id="35cd8-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="35cd8-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd8-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35cd8-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35cd8-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="35cd8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="35cd8-234">System-Only</span></span>            | <span data-ttu-id="35cd8-235">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35cd8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="35cd8-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="35cd8-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="35cd8-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35cd8-238">Is Indexed</span></span>             | <span data-ttu-id="35cd8-239">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35cd8-240">In Global Catalog</span></span>      | <span data-ttu-id="35cd8-241">Faux</span><span class="sxs-lookup"><span data-stu-id="35cd8-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="35cd8-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35cd8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="35cd8-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35cd8-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="35cd8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35cd8-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35cd8-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="35cd8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-246">Search-Flags</span></span>           | <span data-ttu-id="35cd8-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35cd8-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35cd8-248">System-Flags</span></span>           | <span data-ttu-id="35cd8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35cd8-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="35cd8-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35cd8-250">Classes used in</span></span>        | [<span data-ttu-id="35cd8-251">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="35cd8-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="35cd8-252">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="35cd8-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





