---
title: attribut ms-TAPI-Conference-BLOB
description: BLOB de données binaire qui décrit les différentes propriétés d’une conférence de multidiffusion TAPI. Son format et son contenu sont déterminés par la valeur de l’attribut Protocol-Id dans le même objet. En règle générale, les données de cet objet BLOB sont conformes à RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-TAPI-Conference-BLOB Attribute
- Schéma AD de l’attribut msTAPI-ConferenceBlob
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516527"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="ead23-107">attribut ms-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="ead23-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="ead23-108">BLOB de données binaire qui décrit les différentes propriétés d’une conférence de multidiffusion TAPI.</span><span class="sxs-lookup"><span data-stu-id="ead23-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="ead23-109">Son format et son contenu sont déterminés par la valeur de l’attribut Protocol-Id dans le même objet.</span><span class="sxs-lookup"><span data-stu-id="ead23-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="ead23-110">En règle générale, les données de cet objet BLOB sont conformes à RFC2327.</span><span class="sxs-lookup"><span data-stu-id="ead23-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="ead23-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-111">Entry</span></span> | <span data-ttu-id="ead23-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead23-113">CN</span><span class="sxs-lookup"><span data-stu-id="ead23-113">CN</span></span>                | <span data-ttu-id="ead23-114">MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="ead23-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="ead23-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ead23-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ead23-116">msTAPI-ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="ead23-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="ead23-117">Taille</span><span class="sxs-lookup"><span data-stu-id="ead23-117">Size</span></span>              | <span data-ttu-id="ead23-118">Peut être de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ead23-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="ead23-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ead23-119">Update Privilege</span></span>  | <span data-ttu-id="ead23-120">Aucun privilège spécial n’est requis.</span><span class="sxs-lookup"><span data-stu-id="ead23-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="ead23-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ead23-121">Update Frequency</span></span>  | <span data-ttu-id="ead23-122">Peut changer à la discrétion d’un propriétaire de conférence TAPI lorsque certaines données relatives à la conférence doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="ead23-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="ead23-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-123">Attribute-Id</span></span>      | <span data-ttu-id="ead23-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="ead23-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="ead23-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ead23-125">System-Id-Guid</span></span>    | <span data-ttu-id="ead23-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="ead23-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="ead23-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ead23-127">Syntax</span></span>            | [<span data-ttu-id="ead23-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ead23-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="ead23-129">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ead23-129">Implementations</span></span>

-   [<span data-ttu-id="ead23-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ead23-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ead23-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ead23-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ead23-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ead23-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ead23-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ead23-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ead23-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ead23-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ead23-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ead23-135">Windows Server 2003</span></span>



| <span data-ttu-id="ead23-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-136">Entry</span></span> | <span data-ttu-id="ead23-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ead23-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ead23-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead23-140">System-Only</span></span>            | <span data-ttu-id="ead23-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-141">False</span></span>                                                             |
| <span data-ttu-id="ead23-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ead23-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ead23-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="ead23-143">True</span></span>                                                              |
| <span data-ttu-id="ead23-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ead23-144">Is Indexed</span></span>             | <span data-ttu-id="ead23-145">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-145">False</span></span>                                                             |
| <span data-ttu-id="ead23-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ead23-146">In Global Catalog</span></span>      | <span data-ttu-id="ead23-147">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-147">False</span></span>                                                             |
| <span data-ttu-id="ead23-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ead23-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead23-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ead23-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ead23-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead23-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead23-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-152">Search-Flags</span></span>           | <span data-ttu-id="ead23-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead23-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="ead23-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-154">System-Flags</span></span>           | <span data-ttu-id="ead23-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead23-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="ead23-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ead23-156">Classes used in</span></span>        | [<span data-ttu-id="ead23-157">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="ead23-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ead23-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ead23-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ead23-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-159">Entry</span></span> | <span data-ttu-id="ead23-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ead23-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ead23-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead23-163">System-Only</span></span>            | <span data-ttu-id="ead23-164">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-164">False</span></span>                                                             |
| <span data-ttu-id="ead23-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ead23-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ead23-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="ead23-166">True</span></span>                                                              |
| <span data-ttu-id="ead23-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ead23-167">Is Indexed</span></span>             | <span data-ttu-id="ead23-168">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-168">False</span></span>                                                             |
| <span data-ttu-id="ead23-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ead23-169">In Global Catalog</span></span>      | <span data-ttu-id="ead23-170">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-170">False</span></span>                                                             |
| <span data-ttu-id="ead23-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ead23-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead23-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ead23-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ead23-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead23-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead23-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-175">Search-Flags</span></span>           | <span data-ttu-id="ead23-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead23-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="ead23-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-177">System-Flags</span></span>           | <span data-ttu-id="ead23-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead23-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="ead23-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ead23-179">Classes used in</span></span>        | [<span data-ttu-id="ead23-180">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="ead23-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ead23-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ead23-181">Windows Server 2008</span></span>



| <span data-ttu-id="ead23-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-182">Entry</span></span> | <span data-ttu-id="ead23-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ead23-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ead23-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead23-186">System-Only</span></span>            | <span data-ttu-id="ead23-187">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-187">False</span></span>                                                             |
| <span data-ttu-id="ead23-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ead23-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ead23-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="ead23-189">True</span></span>                                                              |
| <span data-ttu-id="ead23-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ead23-190">Is Indexed</span></span>             | <span data-ttu-id="ead23-191">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-191">False</span></span>                                                             |
| <span data-ttu-id="ead23-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ead23-192">In Global Catalog</span></span>      | <span data-ttu-id="ead23-193">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-193">False</span></span>                                                             |
| <span data-ttu-id="ead23-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ead23-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead23-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ead23-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ead23-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead23-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead23-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-198">Search-Flags</span></span>           | <span data-ttu-id="ead23-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead23-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="ead23-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-200">System-Flags</span></span>           | <span data-ttu-id="ead23-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead23-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="ead23-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ead23-202">Classes used in</span></span>        | [<span data-ttu-id="ead23-203">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="ead23-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ead23-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ead23-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ead23-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-205">Entry</span></span> | <span data-ttu-id="ead23-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ead23-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ead23-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead23-209">System-Only</span></span>            | <span data-ttu-id="ead23-210">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-210">False</span></span>                                                             |
| <span data-ttu-id="ead23-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ead23-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ead23-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="ead23-212">True</span></span>                                                              |
| <span data-ttu-id="ead23-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ead23-213">Is Indexed</span></span>             | <span data-ttu-id="ead23-214">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-214">False</span></span>                                                             |
| <span data-ttu-id="ead23-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ead23-215">In Global Catalog</span></span>      | <span data-ttu-id="ead23-216">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-216">False</span></span>                                                             |
| <span data-ttu-id="ead23-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ead23-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead23-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ead23-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ead23-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead23-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead23-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-221">Search-Flags</span></span>           | <span data-ttu-id="ead23-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead23-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="ead23-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-223">System-Flags</span></span>           | <span data-ttu-id="ead23-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead23-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="ead23-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ead23-225">Classes used in</span></span>        | [<span data-ttu-id="ead23-226">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="ead23-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ead23-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ead23-227">Windows Server 2012</span></span>



| <span data-ttu-id="ead23-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="ead23-228">Entry</span></span> | <span data-ttu-id="ead23-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead23-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ead23-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ead23-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead23-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ead23-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead23-232">System-Only</span></span>            | <span data-ttu-id="ead23-233">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-233">False</span></span>                                                             |
| <span data-ttu-id="ead23-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ead23-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ead23-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="ead23-235">True</span></span>                                                              |
| <span data-ttu-id="ead23-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ead23-236">Is Indexed</span></span>             | <span data-ttu-id="ead23-237">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-237">False</span></span>                                                             |
| <span data-ttu-id="ead23-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ead23-238">In Global Catalog</span></span>      | <span data-ttu-id="ead23-239">Faux</span><span class="sxs-lookup"><span data-stu-id="ead23-239">False</span></span>                                                             |
| <span data-ttu-id="ead23-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ead23-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead23-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ead23-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ead23-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead23-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead23-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ead23-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-244">Search-Flags</span></span>           | <span data-ttu-id="ead23-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead23-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="ead23-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead23-246">System-Flags</span></span>           | <span data-ttu-id="ead23-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead23-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="ead23-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ead23-248">Classes used in</span></span>        | [<span data-ttu-id="ead23-249">**MS-TAPI-RT-Conférence**</span><span class="sxs-lookup"><span data-stu-id="ead23-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





