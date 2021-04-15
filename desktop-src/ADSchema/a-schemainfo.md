---
title: Attribut Schema-Info
description: Valeur binaire interne utilisée pour détecter les modifications de schéma entre les contrôleurs de schéma et forcer un cycle de réplication NC de schéma avant la réplication d’un autre contexte de nommage. Utilisé pour résoudre les liens lorsque le FSMO de schéma est pris et qu’une modification est apportée sur plusieurs contrôleurs de périphérique.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Schema-Info
- Schéma AD de l’attribut schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520025"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="3d741-106">Attribut Schema-Info</span><span class="sxs-lookup"><span data-stu-id="3d741-106">Schema-Info attribute</span></span>

<span data-ttu-id="3d741-107">Valeur binaire interne utilisée pour détecter les modifications de schéma entre les contrôleurs de schéma et forcer un cycle de réplication NC de schéma avant la réplication d’un autre contexte de nommage.</span><span class="sxs-lookup"><span data-stu-id="3d741-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="3d741-108">Utilisé pour résoudre les liens lorsque le FSMO de schéma est pris et qu’une modification est apportée sur plusieurs contrôleurs de périphérique.</span><span class="sxs-lookup"><span data-stu-id="3d741-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="3d741-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-109">Entry</span></span> | <span data-ttu-id="3d741-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3d741-111">CN</span><span class="sxs-lookup"><span data-stu-id="3d741-111">CN</span></span>                | <span data-ttu-id="3d741-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="3d741-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="3d741-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3d741-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3d741-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="3d741-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="3d741-115">Taille</span><span class="sxs-lookup"><span data-stu-id="3d741-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3d741-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3d741-116">Update Privilege</span></span>  | <span data-ttu-id="3d741-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="3d741-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="3d741-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3d741-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3d741-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-119">Attribute-Id</span></span>      | <span data-ttu-id="3d741-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="3d741-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="3d741-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3d741-121">System-Id-Guid</span></span>    | <span data-ttu-id="3d741-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="3d741-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="3d741-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d741-123">Syntax</span></span>            | [<span data-ttu-id="3d741-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="3d741-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3d741-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3d741-125">Implementations</span></span>

-   [<span data-ttu-id="3d741-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d741-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d741-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d741-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d741-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3d741-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3d741-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d741-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d741-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d741-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d741-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d741-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d741-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d741-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d741-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d741-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3d741-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-134">Entry</span></span> | <span data-ttu-id="3d741-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-138">System-Only</span></span>            | <span data-ttu-id="3d741-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-139">True</span></span>                            |
| <span data-ttu-id="3d741-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-141">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-141">False</span></span>                           |
| <span data-ttu-id="3d741-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-142">Is Indexed</span></span>             | <span data-ttu-id="3d741-143">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-143">False</span></span>                           |
| <span data-ttu-id="3d741-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-144">In Global Catalog</span></span>      | <span data-ttu-id="3d741-145">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-145">False</span></span>                           |
| <span data-ttu-id="3d741-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-150">Search-Flags</span></span>           | <span data-ttu-id="3d741-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-151">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-152">System-Flags</span></span>           | <span data-ttu-id="3d741-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-153">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-154">Classes used in</span></span>        | [<span data-ttu-id="3d741-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d741-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d741-156">Windows Server 2003</span></span>



| <span data-ttu-id="3d741-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-157">Entry</span></span> | <span data-ttu-id="3d741-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-161">System-Only</span></span>            | <span data-ttu-id="3d741-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-162">True</span></span>                            |
| <span data-ttu-id="3d741-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-164">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-164">False</span></span>                           |
| <span data-ttu-id="3d741-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-165">Is Indexed</span></span>             | <span data-ttu-id="3d741-166">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-166">False</span></span>                           |
| <span data-ttu-id="3d741-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-167">In Global Catalog</span></span>      | <span data-ttu-id="3d741-168">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-168">False</span></span>                           |
| <span data-ttu-id="3d741-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-173">Search-Flags</span></span>           | <span data-ttu-id="3d741-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-174">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-175">System-Flags</span></span>           | <span data-ttu-id="3d741-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-176">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-177">Classes used in</span></span>        | [<span data-ttu-id="3d741-178">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3d741-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="3d741-179">ADAM</span></span>



| <span data-ttu-id="3d741-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-180">Entry</span></span> | <span data-ttu-id="3d741-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-184">System-Only</span></span>            | <span data-ttu-id="3d741-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-185">True</span></span>                            |
| <span data-ttu-id="3d741-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-187">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-187">False</span></span>                           |
| <span data-ttu-id="3d741-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-188">Is Indexed</span></span>             | <span data-ttu-id="3d741-189">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-189">False</span></span>                           |
| <span data-ttu-id="3d741-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-190">In Global Catalog</span></span>      | <span data-ttu-id="3d741-191">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-191">False</span></span>                           |
| <span data-ttu-id="3d741-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-196">Search-Flags</span></span>           | <span data-ttu-id="3d741-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-197">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-198">System-Flags</span></span>           | <span data-ttu-id="3d741-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-199">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-200">Classes used in</span></span>        | [<span data-ttu-id="3d741-201">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d741-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d741-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d741-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-203">Entry</span></span> | <span data-ttu-id="3d741-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-207">System-Only</span></span>            | <span data-ttu-id="3d741-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-208">True</span></span>                            |
| <span data-ttu-id="3d741-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-210">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-210">False</span></span>                           |
| <span data-ttu-id="3d741-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-211">Is Indexed</span></span>             | <span data-ttu-id="3d741-212">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-212">False</span></span>                           |
| <span data-ttu-id="3d741-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-213">In Global Catalog</span></span>      | <span data-ttu-id="3d741-214">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-214">False</span></span>                           |
| <span data-ttu-id="3d741-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-219">Search-Flags</span></span>           | <span data-ttu-id="3d741-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-220">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-221">System-Flags</span></span>           | <span data-ttu-id="3d741-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-222">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-223">Classes used in</span></span>        | [<span data-ttu-id="3d741-224">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d741-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d741-225">Windows Server 2008</span></span>



| <span data-ttu-id="3d741-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-226">Entry</span></span> | <span data-ttu-id="3d741-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-230">System-Only</span></span>            | <span data-ttu-id="3d741-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-231">True</span></span>                            |
| <span data-ttu-id="3d741-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-233">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-233">False</span></span>                           |
| <span data-ttu-id="3d741-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-234">Is Indexed</span></span>             | <span data-ttu-id="3d741-235">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-235">False</span></span>                           |
| <span data-ttu-id="3d741-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-236">In Global Catalog</span></span>      | <span data-ttu-id="3d741-237">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-237">False</span></span>                           |
| <span data-ttu-id="3d741-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-242">Search-Flags</span></span>           | <span data-ttu-id="3d741-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-243">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-244">System-Flags</span></span>           | <span data-ttu-id="3d741-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-245">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-246">Classes used in</span></span>        | [<span data-ttu-id="3d741-247">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d741-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d741-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d741-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-249">Entry</span></span> | <span data-ttu-id="3d741-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-253">System-Only</span></span>            | <span data-ttu-id="3d741-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-254">True</span></span>                            |
| <span data-ttu-id="3d741-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-255">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-256">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-256">False</span></span>                           |
| <span data-ttu-id="3d741-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-257">Is Indexed</span></span>             | <span data-ttu-id="3d741-258">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-258">False</span></span>                           |
| <span data-ttu-id="3d741-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-259">In Global Catalog</span></span>      | <span data-ttu-id="3d741-260">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-260">False</span></span>                           |
| <span data-ttu-id="3d741-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-265">Search-Flags</span></span>           | <span data-ttu-id="3d741-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-266">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-267">System-Flags</span></span>           | <span data-ttu-id="3d741-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-268">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-269">Classes used in</span></span>        | [<span data-ttu-id="3d741-270">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d741-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d741-271">Windows Server 2012</span></span>



| <span data-ttu-id="3d741-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d741-272">Entry</span></span> | <span data-ttu-id="3d741-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d741-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3d741-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3d741-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d741-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3d741-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d741-276">System-Only</span></span>            | <span data-ttu-id="3d741-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="3d741-277">True</span></span>                            |
| <span data-ttu-id="3d741-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3d741-278">Is-Single-Valued</span></span>       | <span data-ttu-id="3d741-279">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-279">False</span></span>                           |
| <span data-ttu-id="3d741-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3d741-280">Is Indexed</span></span>             | <span data-ttu-id="3d741-281">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-281">False</span></span>                           |
| <span data-ttu-id="3d741-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3d741-282">In Global Catalog</span></span>      | <span data-ttu-id="3d741-283">Faux</span><span class="sxs-lookup"><span data-stu-id="3d741-283">False</span></span>                           |
| <span data-ttu-id="3d741-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3d741-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d741-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3d741-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3d741-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d741-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3d741-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d741-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3d741-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-288">Search-Flags</span></span>           | <span data-ttu-id="3d741-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d741-289">0x00000000</span></span>                      |
| <span data-ttu-id="3d741-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d741-290">System-Flags</span></span>           | <span data-ttu-id="3d741-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d741-291">0x00000010</span></span>                      |
| <span data-ttu-id="3d741-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3d741-292">Classes used in</span></span>        | [<span data-ttu-id="3d741-293">**DMD**</span><span class="sxs-lookup"><span data-stu-id="3d741-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





