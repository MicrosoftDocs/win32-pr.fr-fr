---
title: attribut ms-DS-ExecuteScriptPassword
description: Utilisé lors du changement de nom de domaine. Cette valeur ne peut pas être écrite ou lue à l’aide de LDAP.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-ExecuteScriptPassword
- Schéma Active Directory de l’attribut msDS-ExecuteScriptPassword
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106511997"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="eb539-106">attribut ms-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="eb539-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="eb539-107">Utilisé lors du changement de nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="eb539-107">Used during domain rename.</span></span> <span data-ttu-id="eb539-108">Cette valeur ne peut pas être écrite ou lue à l’aide de LDAP.</span><span class="sxs-lookup"><span data-stu-id="eb539-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="eb539-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-109">Entry</span></span> | <span data-ttu-id="eb539-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="eb539-111">CN</span><span class="sxs-lookup"><span data-stu-id="eb539-111">CN</span></span>                | <span data-ttu-id="eb539-112">ms-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="eb539-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="eb539-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="eb539-113">Ldap-Display-Name</span></span> | <span data-ttu-id="eb539-114">msDS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="eb539-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="eb539-115">Taille</span><span class="sxs-lookup"><span data-stu-id="eb539-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="eb539-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="eb539-116">Update Privilege</span></span>  | <span data-ttu-id="eb539-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="eb539-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="eb539-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="eb539-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="eb539-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-119">Attribute-Id</span></span>      | <span data-ttu-id="eb539-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="eb539-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="eb539-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="eb539-121">System-Id-Guid</span></span>    | <span data-ttu-id="eb539-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="eb539-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="eb539-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb539-123">Syntax</span></span>            | [<span data-ttu-id="eb539-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="eb539-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="eb539-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="eb539-125">Implementations</span></span>

-   [<span data-ttu-id="eb539-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eb539-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eb539-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="eb539-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eb539-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eb539-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eb539-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eb539-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eb539-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eb539-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eb539-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eb539-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="eb539-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb539-132">Windows Server 2003</span></span>



| <span data-ttu-id="eb539-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-133">Entry</span></span> | <span data-ttu-id="eb539-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="eb539-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-137">System-Only</span></span>            | <span data-ttu-id="eb539-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-138">True</span></span>                                                          |
| <span data-ttu-id="eb539-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-139">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-140">True</span></span>                                                          |
| <span data-ttu-id="eb539-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-141">Is Indexed</span></span>             | <span data-ttu-id="eb539-142">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-142">False</span></span>                                                         |
| <span data-ttu-id="eb539-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-143">In Global Catalog</span></span>      | <span data-ttu-id="eb539-144">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-144">False</span></span>                                                         |
| <span data-ttu-id="eb539-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="eb539-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-147">Range-Lower</span></span>            | <span data-ttu-id="eb539-148">0</span><span class="sxs-lookup"><span data-stu-id="eb539-148">0</span></span>                                                             |
| <span data-ttu-id="eb539-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-149">Range-Upper</span></span>            | <span data-ttu-id="eb539-150">64</span><span class="sxs-lookup"><span data-stu-id="eb539-150">64</span></span>                                                            |
| <span data-ttu-id="eb539-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-151">Search-Flags</span></span>           | <span data-ttu-id="eb539-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="eb539-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-153">System-Flags</span></span>           | <span data-ttu-id="eb539-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="eb539-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-155">Classes used in</span></span>        | [<span data-ttu-id="eb539-156">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eb539-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="eb539-157">ADAM</span></span>



| <span data-ttu-id="eb539-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-158">Entry</span></span> | <span data-ttu-id="eb539-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="eb539-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-162">System-Only</span></span>            | <span data-ttu-id="eb539-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-163">True</span></span>                                                          |
| <span data-ttu-id="eb539-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-164">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-165">True</span></span>                                                          |
| <span data-ttu-id="eb539-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-166">Is Indexed</span></span>             | <span data-ttu-id="eb539-167">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-167">False</span></span>                                                         |
| <span data-ttu-id="eb539-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-168">In Global Catalog</span></span>      | <span data-ttu-id="eb539-169">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-169">False</span></span>                                                         |
| <span data-ttu-id="eb539-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="eb539-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-172">Range-Lower</span></span>            | <span data-ttu-id="eb539-173">0</span><span class="sxs-lookup"><span data-stu-id="eb539-173">0</span></span>                                                             |
| <span data-ttu-id="eb539-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-174">Range-Upper</span></span>            | <span data-ttu-id="eb539-175">64</span><span class="sxs-lookup"><span data-stu-id="eb539-175">64</span></span>                                                            |
| <span data-ttu-id="eb539-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-176">Search-Flags</span></span>           | <span data-ttu-id="eb539-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="eb539-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-178">System-Flags</span></span>           | <span data-ttu-id="eb539-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="eb539-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-180">Classes used in</span></span>        | [<span data-ttu-id="eb539-181">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eb539-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eb539-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eb539-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-183">Entry</span></span> | <span data-ttu-id="eb539-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="eb539-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="eb539-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-187">System-Only</span></span>            | <span data-ttu-id="eb539-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-188">True</span></span>                                                          |
| <span data-ttu-id="eb539-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-189">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-190">True</span></span>                                                          |
| <span data-ttu-id="eb539-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-191">Is Indexed</span></span>             | <span data-ttu-id="eb539-192">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-192">False</span></span>                                                         |
| <span data-ttu-id="eb539-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-193">In Global Catalog</span></span>      | <span data-ttu-id="eb539-194">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-194">False</span></span>                                                         |
| <span data-ttu-id="eb539-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="eb539-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-197">Range-Lower</span></span>            | <span data-ttu-id="eb539-198">0</span><span class="sxs-lookup"><span data-stu-id="eb539-198">0</span></span>                                                             |
| <span data-ttu-id="eb539-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-199">Range-Upper</span></span>            | <span data-ttu-id="eb539-200">64</span><span class="sxs-lookup"><span data-stu-id="eb539-200">64</span></span>                                                            |
| <span data-ttu-id="eb539-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-201">Search-Flags</span></span>           | <span data-ttu-id="eb539-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="eb539-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-203">System-Flags</span></span>           | <span data-ttu-id="eb539-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="eb539-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-205">Classes used in</span></span>        | [<span data-ttu-id="eb539-206">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eb539-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb539-207">Windows Server 2008</span></span>



| <span data-ttu-id="eb539-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-208">Entry</span></span> | <span data-ttu-id="eb539-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb539-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-212">System-Only</span></span>            | <span data-ttu-id="eb539-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-213">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-214">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-215">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-216">Is Indexed</span></span>             | <span data-ttu-id="eb539-217">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-217">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-218">In Global Catalog</span></span>      | <span data-ttu-id="eb539-219">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-219">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="eb539-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-222">Range-Lower</span></span>            | <span data-ttu-id="eb539-223">0</span><span class="sxs-lookup"><span data-stu-id="eb539-223">0</span></span>                                                                                                       |
| <span data-ttu-id="eb539-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-224">Range-Upper</span></span>            | <span data-ttu-id="eb539-225">64</span><span class="sxs-lookup"><span data-stu-id="eb539-225">64</span></span>                                                                                                      |
| <span data-ttu-id="eb539-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-226">Search-Flags</span></span>           | <span data-ttu-id="eb539-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="eb539-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-228">System-Flags</span></span>           | <span data-ttu-id="eb539-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="eb539-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-230">Classes used in</span></span>        | [<span data-ttu-id="eb539-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="eb539-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eb539-232">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eb539-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb539-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eb539-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-234">Entry</span></span> | <span data-ttu-id="eb539-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb539-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-238">System-Only</span></span>            | <span data-ttu-id="eb539-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-239">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-240">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-241">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-242">Is Indexed</span></span>             | <span data-ttu-id="eb539-243">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-243">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-244">In Global Catalog</span></span>      | <span data-ttu-id="eb539-245">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-245">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="eb539-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-248">Range-Lower</span></span>            | <span data-ttu-id="eb539-249">0</span><span class="sxs-lookup"><span data-stu-id="eb539-249">0</span></span>                                                                                                       |
| <span data-ttu-id="eb539-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-250">Range-Upper</span></span>            | <span data-ttu-id="eb539-251">64</span><span class="sxs-lookup"><span data-stu-id="eb539-251">64</span></span>                                                                                                      |
| <span data-ttu-id="eb539-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-252">Search-Flags</span></span>           | <span data-ttu-id="eb539-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="eb539-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-254">System-Flags</span></span>           | <span data-ttu-id="eb539-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="eb539-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-256">Classes used in</span></span>        | [<span data-ttu-id="eb539-257">**Computer**</span><span class="sxs-lookup"><span data-stu-id="eb539-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eb539-258">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eb539-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb539-259">Windows Server 2012</span></span>



| <span data-ttu-id="eb539-260">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb539-260">Entry</span></span> | <span data-ttu-id="eb539-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb539-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb539-262">ID de lien</span><span class="sxs-lookup"><span data-stu-id="eb539-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb539-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="eb539-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb539-264">System-Only</span></span>            | <span data-ttu-id="eb539-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-265">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-266">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="eb539-266">Is-Single-Valued</span></span>       | <span data-ttu-id="eb539-267">Vrai</span><span class="sxs-lookup"><span data-stu-id="eb539-267">True</span></span>                                                                                                    |
| <span data-ttu-id="eb539-268">Est indexé</span><span class="sxs-lookup"><span data-stu-id="eb539-268">Is Indexed</span></span>             | <span data-ttu-id="eb539-269">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-269">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-270">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="eb539-270">In Global Catalog</span></span>      | <span data-ttu-id="eb539-271">Faux</span><span class="sxs-lookup"><span data-stu-id="eb539-271">False</span></span>                                                                                                   |
| <span data-ttu-id="eb539-272">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="eb539-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb539-273">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="eb539-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="eb539-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb539-274">Range-Lower</span></span>            | <span data-ttu-id="eb539-275">0</span><span class="sxs-lookup"><span data-stu-id="eb539-275">0</span></span>                                                                                                       |
| <span data-ttu-id="eb539-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb539-276">Range-Upper</span></span>            | <span data-ttu-id="eb539-277">64</span><span class="sxs-lookup"><span data-stu-id="eb539-277">64</span></span>                                                                                                      |
| <span data-ttu-id="eb539-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-278">Search-Flags</span></span>           | <span data-ttu-id="eb539-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb539-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="eb539-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb539-280">System-Flags</span></span>           | <span data-ttu-id="eb539-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="eb539-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="eb539-282">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="eb539-282">Classes used in</span></span>        | [<span data-ttu-id="eb539-283">**Computer**</span><span class="sxs-lookup"><span data-stu-id="eb539-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eb539-284">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="eb539-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





