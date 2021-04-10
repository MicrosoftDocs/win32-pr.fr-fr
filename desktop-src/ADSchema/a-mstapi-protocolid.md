---
title: attribut ms-TAPI-Protocol-ID
description: Cet attribut indique le type de conférence TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-TAPI-Protocol-ID
- Schéma AD de l’attribut msTAPI-ProtocolId
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108058"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="6a8b2-105">attribut ms-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="6a8b2-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="6a8b2-106">Cet attribut indique le type de conférence TAPI.</span><span class="sxs-lookup"><span data-stu-id="6a8b2-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="6a8b2-107">Cet attribut est utilisé pour déterminer comment l’objet BLOB binaire de l’attribut [**MS-TAPI-Conference-BLOB**](a-mstapi-conferenceblob.md) doit être interprété.</span><span class="sxs-lookup"><span data-stu-id="6a8b2-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="6a8b2-108">Cet attribut est une chaîne arbitraire, dont la longueur est généralement inférieure à 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="6a8b2-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="6a8b2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-109">Entry</span></span> | <span data-ttu-id="6a8b2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="6a8b2-111">CN</span><span class="sxs-lookup"><span data-stu-id="6a8b2-111">CN</span></span>                | <span data-ttu-id="6a8b2-112">MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="6a8b2-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="6a8b2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6a8b2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6a8b2-114">msTAPI-ProtocolId</span><span class="sxs-lookup"><span data-stu-id="6a8b2-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="6a8b2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="6a8b2-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="6a8b2-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6a8b2-116">Update Privilege</span></span>  | <span data-ttu-id="6a8b2-117">Aucun privilège spécial n’est requis.</span><span class="sxs-lookup"><span data-stu-id="6a8b2-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="6a8b2-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6a8b2-118">Update Frequency</span></span>  | <span data-ttu-id="6a8b2-119">Défini une fois au moment de la création de l’objet Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="6a8b2-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="6a8b2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-120">Attribute-Id</span></span>      | <span data-ttu-id="6a8b2-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="6a8b2-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="6a8b2-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6a8b2-122">System-Id-Guid</span></span>    | <span data-ttu-id="6a8b2-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="6a8b2-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="6a8b2-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a8b2-124">Syntax</span></span>            | [<span data-ttu-id="6a8b2-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="6a8b2-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6a8b2-126">Implementations</span></span>

-   [<span data-ttu-id="6a8b2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a8b2-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a8b2-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a8b2-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a8b2-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6a8b2-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a8b2-132">Windows Server 2003</span></span>



| <span data-ttu-id="6a8b2-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-133">Entry</span></span> | <span data-ttu-id="6a8b2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a8b2-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6a8b2-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a8b2-137">System-Only</span></span>            | <span data-ttu-id="6a8b2-138">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-138">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6a8b2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6a8b2-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="6a8b2-140">True</span></span>                                                              |
| <span data-ttu-id="6a8b2-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6a8b2-141">Is Indexed</span></span>             | <span data-ttu-id="6a8b2-142">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-142">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6a8b2-143">In Global Catalog</span></span>      | <span data-ttu-id="6a8b2-144">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-144">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6a8b2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a8b2-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6a8b2-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a8b2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a8b2-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a8b2-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-149">Search-Flags</span></span>           | <span data-ttu-id="6a8b2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a8b2-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a8b2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-151">System-Flags</span></span>           | <span data-ttu-id="6a8b2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a8b2-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="6a8b2-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6a8b2-153">Classes used in</span></span>        | [<span data-ttu-id="6a8b2-154">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a8b2-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a8b2-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a8b2-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-156">Entry</span></span> | <span data-ttu-id="6a8b2-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a8b2-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6a8b2-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a8b2-160">System-Only</span></span>            | <span data-ttu-id="6a8b2-161">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-161">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6a8b2-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6a8b2-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="6a8b2-163">True</span></span>                                                              |
| <span data-ttu-id="6a8b2-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6a8b2-164">Is Indexed</span></span>             | <span data-ttu-id="6a8b2-165">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-165">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6a8b2-166">In Global Catalog</span></span>      | <span data-ttu-id="6a8b2-167">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-167">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6a8b2-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a8b2-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6a8b2-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a8b2-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a8b2-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a8b2-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-172">Search-Flags</span></span>           | <span data-ttu-id="6a8b2-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a8b2-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a8b2-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-174">System-Flags</span></span>           | <span data-ttu-id="6a8b2-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a8b2-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="6a8b2-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6a8b2-176">Classes used in</span></span>        | [<span data-ttu-id="6a8b2-177">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a8b2-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a8b2-178">Windows Server 2008</span></span>



| <span data-ttu-id="6a8b2-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-179">Entry</span></span> | <span data-ttu-id="6a8b2-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a8b2-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6a8b2-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a8b2-183">System-Only</span></span>            | <span data-ttu-id="6a8b2-184">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-184">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6a8b2-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6a8b2-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="6a8b2-186">True</span></span>                                                              |
| <span data-ttu-id="6a8b2-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6a8b2-187">Is Indexed</span></span>             | <span data-ttu-id="6a8b2-188">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-188">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6a8b2-189">In Global Catalog</span></span>      | <span data-ttu-id="6a8b2-190">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-190">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6a8b2-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a8b2-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6a8b2-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a8b2-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a8b2-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a8b2-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-195">Search-Flags</span></span>           | <span data-ttu-id="6a8b2-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a8b2-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a8b2-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-197">System-Flags</span></span>           | <span data-ttu-id="6a8b2-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a8b2-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="6a8b2-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6a8b2-199">Classes used in</span></span>        | [<span data-ttu-id="6a8b2-200">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a8b2-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a8b2-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a8b2-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-202">Entry</span></span> | <span data-ttu-id="6a8b2-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a8b2-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6a8b2-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a8b2-206">System-Only</span></span>            | <span data-ttu-id="6a8b2-207">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-207">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6a8b2-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6a8b2-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="6a8b2-209">True</span></span>                                                              |
| <span data-ttu-id="6a8b2-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6a8b2-210">Is Indexed</span></span>             | <span data-ttu-id="6a8b2-211">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-211">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6a8b2-212">In Global Catalog</span></span>      | <span data-ttu-id="6a8b2-213">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-213">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6a8b2-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a8b2-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6a8b2-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a8b2-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a8b2-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a8b2-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-218">Search-Flags</span></span>           | <span data-ttu-id="6a8b2-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a8b2-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a8b2-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-220">System-Flags</span></span>           | <span data-ttu-id="6a8b2-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a8b2-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="6a8b2-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6a8b2-222">Classes used in</span></span>        | [<span data-ttu-id="6a8b2-223">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a8b2-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a8b2-224">Windows Server 2012</span></span>



| <span data-ttu-id="6a8b2-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="6a8b2-225">Entry</span></span> | <span data-ttu-id="6a8b2-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8b2-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a8b2-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6a8b2-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a8b2-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a8b2-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a8b2-229">System-Only</span></span>            | <span data-ttu-id="6a8b2-230">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-230">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6a8b2-231">Is-Single-Valued</span></span>       | <span data-ttu-id="6a8b2-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="6a8b2-232">True</span></span>                                                              |
| <span data-ttu-id="6a8b2-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6a8b2-233">Is Indexed</span></span>             | <span data-ttu-id="6a8b2-234">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-234">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6a8b2-235">In Global Catalog</span></span>      | <span data-ttu-id="6a8b2-236">Faux</span><span class="sxs-lookup"><span data-stu-id="6a8b2-236">False</span></span>                                                             |
| <span data-ttu-id="6a8b2-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6a8b2-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a8b2-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6a8b2-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a8b2-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a8b2-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a8b2-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a8b2-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-241">Search-Flags</span></span>           | <span data-ttu-id="6a8b2-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a8b2-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a8b2-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a8b2-243">System-Flags</span></span>           | <span data-ttu-id="6a8b2-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a8b2-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="6a8b2-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6a8b2-245">Classes used in</span></span>        | [<span data-ttu-id="6a8b2-246">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="6a8b2-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





