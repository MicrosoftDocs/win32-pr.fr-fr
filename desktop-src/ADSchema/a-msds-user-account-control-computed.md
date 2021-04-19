---
title: attribut calculé ms-DS-User-Account-Control
description: msDS-User-Account-Control-controled s’apparente à userAccountControl, mais la valeur de l’attribut peut contenir des bits supplémentaires qui ne sont pas persistants.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut calculé ms-DS-User-Account-Control
- Schéma Active Directory msDS-User-Account-Control-attribut calculé
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514680"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="bdca2-105">attribut calculé ms-DS-User-Account-Control</span><span class="sxs-lookup"><span data-stu-id="bdca2-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="bdca2-106">**MSDS-User-Account-Control-controled** s’apparente à [**UserAccountControl**](a-useraccountcontrol.md), mais la valeur de l’attribut peut contenir des bits supplémentaires qui ne sont pas persistants.</span><span class="sxs-lookup"><span data-stu-id="bdca2-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="bdca2-107">Les bits calculés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="bdca2-107">The computed bits include the following.</span></span>



| <span data-ttu-id="bdca2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-108">Value</span></span>                | <span data-ttu-id="bdca2-109">Name (défini dans IADs. h)</span><span class="sxs-lookup"><span data-stu-id="bdca2-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="bdca2-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="bdca2-110">0x0010</span></span><br/>    | <span data-ttu-id="bdca2-111">**\_verrouillage uf**</span><span class="sxs-lookup"><span data-stu-id="bdca2-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="bdca2-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="bdca2-112">0x800000</span></span><br/>  | <span data-ttu-id="bdca2-113">**\_mot de passe UF \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="bdca2-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="bdca2-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-114">0x4000000</span></span><br/> | <span data-ttu-id="bdca2-115">**\_compte de \_ secrets PARTIELs UF \_**</span><span class="sxs-lookup"><span data-stu-id="bdca2-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="bdca2-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-116">0x8000000</span></span><br/> | <span data-ttu-id="bdca2-117">**UF \_ utiliser \_ des \_ clés AES**</span><span class="sxs-lookup"><span data-stu-id="bdca2-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="bdca2-118">La liste complète des bits utilisés par le contrôle de [**compte**](a-useraccountcontrol.md) d’utilisateur et, par conséquent, le contrôle de compte d' **utilisateur MSDS** peut également être trouvée dans la page de référence de **contrôle de compte d’utilisateur** (mappée via l’FlagSet [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) ou sur les pages de référence de gestion de réseau pour la structure [**\_ informations utilisateur \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .</span><span class="sxs-lookup"><span data-stu-id="bdca2-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="bdca2-119">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-119">Entry</span></span> | <span data-ttu-id="bdca2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bdca2-121">CN</span><span class="sxs-lookup"><span data-stu-id="bdca2-121">CN</span></span>                | <span data-ttu-id="bdca2-122">ms-DS-utilisateur-compte-contrôle-calculé</span><span class="sxs-lookup"><span data-stu-id="bdca2-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="bdca2-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bdca2-123">Ldap-Display-Name</span></span> | <span data-ttu-id="bdca2-124">msDS-User-Account-Control-calculé</span><span class="sxs-lookup"><span data-stu-id="bdca2-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="bdca2-125">Taille</span><span class="sxs-lookup"><span data-stu-id="bdca2-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="bdca2-126">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bdca2-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bdca2-127">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bdca2-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bdca2-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-128">Attribute-Id</span></span>      | <span data-ttu-id="bdca2-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="bdca2-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="bdca2-130">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bdca2-130">System-Id-Guid</span></span>    | <span data-ttu-id="bdca2-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="bdca2-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="bdca2-132">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdca2-132">Syntax</span></span>            | [<span data-ttu-id="bdca2-133">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="bdca2-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bdca2-134">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bdca2-134">Implementations</span></span>

-   [<span data-ttu-id="bdca2-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bdca2-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bdca2-136">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bdca2-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bdca2-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bdca2-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bdca2-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bdca2-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bdca2-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bdca2-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bdca2-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bdca2-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bdca2-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdca2-141">Windows Server 2003</span></span>



| <span data-ttu-id="bdca2-142">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-142">Entry</span></span> | <span data-ttu-id="bdca2-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdca2-144">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-146">System-Only</span></span>            | <span data-ttu-id="bdca2-147">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-147">False</span></span>                             |
| <span data-ttu-id="bdca2-148">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-148">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-149">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-149">True</span></span>                              |
| <span data-ttu-id="bdca2-150">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-150">Is Indexed</span></span>             | <span data-ttu-id="bdca2-151">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-151">False</span></span>                             |
| <span data-ttu-id="bdca2-152">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-152">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-153">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-153">False</span></span>                             |
| <span data-ttu-id="bdca2-154">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-155">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdca2-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdca2-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdca2-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-158">Search-Flags</span></span>           | <span data-ttu-id="bdca2-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-159">0x00000000</span></span>                        |
| <span data-ttu-id="bdca2-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-160">System-Flags</span></span>           | <span data-ttu-id="bdca2-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-161">0x00000014</span></span>                        |
| <span data-ttu-id="bdca2-162">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-162">Classes used in</span></span>        | [<span data-ttu-id="bdca2-163">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdca2-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bdca2-164">ADAM</span><span class="sxs-lookup"><span data-stu-id="bdca2-164">ADAM</span></span>



| <span data-ttu-id="bdca2-165">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-165">Entry</span></span> | <span data-ttu-id="bdca2-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdca2-167">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdca2-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdca2-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-169">System-Only</span></span>            | <span data-ttu-id="bdca2-170">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-170">False</span></span>                                                             |
| <span data-ttu-id="bdca2-171">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-171">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-172">True</span></span>                                                              |
| <span data-ttu-id="bdca2-173">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-173">Is Indexed</span></span>             | <span data-ttu-id="bdca2-174">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-174">False</span></span>                                                             |
| <span data-ttu-id="bdca2-175">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-175">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-176">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-176">False</span></span>                                                             |
| <span data-ttu-id="bdca2-177">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-178">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdca2-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdca2-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdca2-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-181">Search-Flags</span></span>           | <span data-ttu-id="bdca2-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdca2-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-183">System-Flags</span></span>           | <span data-ttu-id="bdca2-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="bdca2-185">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-185">Classes used in</span></span>        | [<span data-ttu-id="bdca2-186">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="bdca2-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bdca2-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bdca2-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bdca2-188">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-188">Entry</span></span> | <span data-ttu-id="bdca2-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdca2-190">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-192">System-Only</span></span>            | <span data-ttu-id="bdca2-193">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-193">False</span></span>                             |
| <span data-ttu-id="bdca2-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-194">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-195">True</span></span>                              |
| <span data-ttu-id="bdca2-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-196">Is Indexed</span></span>             | <span data-ttu-id="bdca2-197">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-197">False</span></span>                             |
| <span data-ttu-id="bdca2-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-198">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-199">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-199">False</span></span>                             |
| <span data-ttu-id="bdca2-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdca2-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdca2-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdca2-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-204">Search-Flags</span></span>           | <span data-ttu-id="bdca2-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-205">0x00000000</span></span>                        |
| <span data-ttu-id="bdca2-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-206">System-Flags</span></span>           | <span data-ttu-id="bdca2-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-207">0x00000014</span></span>                        |
| <span data-ttu-id="bdca2-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-208">Classes used in</span></span>        | [<span data-ttu-id="bdca2-209">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdca2-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bdca2-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdca2-210">Windows Server 2008</span></span>



| <span data-ttu-id="bdca2-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-211">Entry</span></span> | <span data-ttu-id="bdca2-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdca2-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-215">System-Only</span></span>            | <span data-ttu-id="bdca2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-216">False</span></span>                             |
| <span data-ttu-id="bdca2-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-218">True</span></span>                              |
| <span data-ttu-id="bdca2-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-219">Is Indexed</span></span>             | <span data-ttu-id="bdca2-220">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-220">False</span></span>                             |
| <span data-ttu-id="bdca2-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-221">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-222">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-222">False</span></span>                             |
| <span data-ttu-id="bdca2-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdca2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdca2-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdca2-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-227">Search-Flags</span></span>           | <span data-ttu-id="bdca2-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-228">0x00000000</span></span>                        |
| <span data-ttu-id="bdca2-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-229">System-Flags</span></span>           | <span data-ttu-id="bdca2-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-230">0x00000014</span></span>                        |
| <span data-ttu-id="bdca2-231">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-231">Classes used in</span></span>        | [<span data-ttu-id="bdca2-232">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdca2-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bdca2-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdca2-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bdca2-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-234">Entry</span></span> | <span data-ttu-id="bdca2-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdca2-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-238">System-Only</span></span>            | <span data-ttu-id="bdca2-239">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-239">False</span></span>                             |
| <span data-ttu-id="bdca2-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-240">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-241">True</span></span>                              |
| <span data-ttu-id="bdca2-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-242">Is Indexed</span></span>             | <span data-ttu-id="bdca2-243">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-243">False</span></span>                             |
| <span data-ttu-id="bdca2-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-244">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-245">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-245">False</span></span>                             |
| <span data-ttu-id="bdca2-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdca2-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdca2-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdca2-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-250">Search-Flags</span></span>           | <span data-ttu-id="bdca2-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-251">0x00000000</span></span>                        |
| <span data-ttu-id="bdca2-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-252">System-Flags</span></span>           | <span data-ttu-id="bdca2-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-253">0x00000014</span></span>                        |
| <span data-ttu-id="bdca2-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-254">Classes used in</span></span>        | [<span data-ttu-id="bdca2-255">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdca2-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bdca2-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdca2-256">Windows Server 2012</span></span>



| <span data-ttu-id="bdca2-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdca2-257">Entry</span></span> | <span data-ttu-id="bdca2-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdca2-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdca2-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdca2-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdca2-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdca2-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdca2-261">System-Only</span></span>            | <span data-ttu-id="bdca2-262">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-262">False</span></span>                             |
| <span data-ttu-id="bdca2-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdca2-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bdca2-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="bdca2-264">True</span></span>                              |
| <span data-ttu-id="bdca2-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdca2-265">Is Indexed</span></span>             | <span data-ttu-id="bdca2-266">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-266">False</span></span>                             |
| <span data-ttu-id="bdca2-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdca2-267">In Global Catalog</span></span>      | <span data-ttu-id="bdca2-268">Faux</span><span class="sxs-lookup"><span data-stu-id="bdca2-268">False</span></span>                             |
| <span data-ttu-id="bdca2-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdca2-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdca2-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdca2-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdca2-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdca2-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdca2-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdca2-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdca2-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-273">Search-Flags</span></span>           | <span data-ttu-id="bdca2-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdca2-274">0x00000000</span></span>                        |
| <span data-ttu-id="bdca2-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdca2-275">System-Flags</span></span>           | <span data-ttu-id="bdca2-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bdca2-276">0x00000014</span></span>                        |
| <span data-ttu-id="bdca2-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdca2-277">Classes used in</span></span>        | [<span data-ttu-id="bdca2-278">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdca2-278">**User**</span></span>](c-user.md)<br/> |



 

