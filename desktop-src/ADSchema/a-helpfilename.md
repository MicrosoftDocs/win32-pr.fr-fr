---
title: Aide-attribut de nom de fichier
description: Cet attribut a été utilisé pour Exchange 4,0. Il contenait le nom à utiliser pour le fichier lorsque le fournisseur a téléchargé les données d’aide sur un ordinateur client. Elle n’est pas utilisée pour les autres versions d’Exchange.
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- Attribut de nom de fichier d’aide-schéma Active Directory
- Schéma AD de l’attribut helpFileName
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845242"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="ac2c9-107">Aide-attribut de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="ac2c9-107">Help-File-Name attribute</span></span>

<span data-ttu-id="ac2c9-108">Cet attribut a été utilisé pour Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="ac2c9-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="ac2c9-109">Il contenait le nom à utiliser pour le fichier lorsque le fournisseur a téléchargé les données d’aide sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="ac2c9-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="ac2c9-110">Elle n’est pas utilisée pour les autres versions d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac2c9-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="ac2c9-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-111">Entry</span></span> | <span data-ttu-id="ac2c9-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ac2c9-113">CN</span><span class="sxs-lookup"><span data-stu-id="ac2c9-113">CN</span></span>                | <span data-ttu-id="ac2c9-114">Help-nom-fichier</span><span class="sxs-lookup"><span data-stu-id="ac2c9-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="ac2c9-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ac2c9-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ac2c9-116">helpFileName</span><span class="sxs-lookup"><span data-stu-id="ac2c9-116">helpFileName</span></span>                                |
| <span data-ttu-id="ac2c9-117">Taille</span><span class="sxs-lookup"><span data-stu-id="ac2c9-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="ac2c9-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ac2c9-118">Update Privilege</span></span>  | <span data-ttu-id="ac2c9-119">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="ac2c9-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="ac2c9-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ac2c9-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ac2c9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-121">Attribute-Id</span></span>      | <span data-ttu-id="ac2c9-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="ac2c9-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="ac2c9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac2c9-123">System-Id-Guid</span></span>    | <span data-ttu-id="ac2c9-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ac2c9-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="ac2c9-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac2c9-125">Syntax</span></span>            | [<span data-ttu-id="ac2c9-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ac2c9-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ac2c9-127">Implementations</span></span>

-   [<span data-ttu-id="ac2c9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac2c9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac2c9-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac2c9-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac2c9-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac2c9-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac2c9-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac2c9-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ac2c9-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-135">Entry</span></span> | <span data-ttu-id="ac2c9-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-138">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-139">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-140">System-Only</span></span>            | <span data-ttu-id="ac2c9-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-141">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-143">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-144">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-145">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-145">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-146">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-147">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-147">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-150">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-151">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-151">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-152">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-153">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-153">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-154">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-155">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-156">System-Flags</span></span>           | <span data-ttu-id="ac2c9-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-157">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-158">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-159">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac2c9-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac2c9-160">Windows Server 2003</span></span>



| <span data-ttu-id="ac2c9-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-161">Entry</span></span> | <span data-ttu-id="ac2c9-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-164">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-165">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-166">System-Only</span></span>            | <span data-ttu-id="ac2c9-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-167">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-168">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-169">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-170">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-171">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-171">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-172">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-173">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-173">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-176">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-177">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-177">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-178">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-179">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-179">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-180">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-181">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-182">System-Flags</span></span>           | <span data-ttu-id="ac2c9-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-183">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-184">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-185">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac2c9-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac2c9-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac2c9-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-187">Entry</span></span> | <span data-ttu-id="ac2c9-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-190">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-191">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-192">System-Only</span></span>            | <span data-ttu-id="ac2c9-193">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-193">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-194">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-195">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-196">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-197">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-197">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-198">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-199">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-199">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-202">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-203">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-203">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-204">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-205">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-205">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-206">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-207">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-208">System-Flags</span></span>           | <span data-ttu-id="ac2c9-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-209">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-210">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-210">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-211">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac2c9-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac2c9-212">Windows Server 2008</span></span>



| <span data-ttu-id="ac2c9-213">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-213">Entry</span></span> | <span data-ttu-id="ac2c9-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-215">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-216">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-217">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-218">System-Only</span></span>            | <span data-ttu-id="ac2c9-219">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-219">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-220">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-220">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-221">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-221">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-222">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-222">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-223">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-223">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-224">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-224">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-225">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-225">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-226">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-227">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-228">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-229">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-229">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-230">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-231">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-231">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-232">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-233">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-234">System-Flags</span></span>           | <span data-ttu-id="ac2c9-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-235">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-236">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-236">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-237">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac2c9-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac2c9-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac2c9-239">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-239">Entry</span></span> | <span data-ttu-id="ac2c9-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-241">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-242">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-243">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-244">System-Only</span></span>            | <span data-ttu-id="ac2c9-245">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-245">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-246">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-247">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-247">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-248">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-249">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-249">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-250">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-251">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-251">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-254">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-255">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-255">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-256">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-257">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-257">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-258">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-259">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-260">System-Flags</span></span>           | <span data-ttu-id="ac2c9-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-261">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-262">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-262">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-263">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac2c9-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac2c9-264">Windows Server 2012</span></span>



| <span data-ttu-id="ac2c9-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="ac2c9-265">Entry</span></span> | <span data-ttu-id="ac2c9-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2c9-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac2c9-267">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ac2c9-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ac2c9-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac2c9-268">MAPI-Id</span></span>                | <span data-ttu-id="ac2c9-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="ac2c9-269">0x803B</span></span>                                                   |
| <span data-ttu-id="ac2c9-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac2c9-270">System-Only</span></span>            | <span data-ttu-id="ac2c9-271">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-271">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-272">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ac2c9-272">Is-Single-Valued</span></span>       | <span data-ttu-id="ac2c9-273">Vrai</span><span class="sxs-lookup"><span data-stu-id="ac2c9-273">True</span></span>                                                     |
| <span data-ttu-id="ac2c9-274">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ac2c9-274">Is Indexed</span></span>             | <span data-ttu-id="ac2c9-275">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-275">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-276">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ac2c9-276">In Global Catalog</span></span>      | <span data-ttu-id="ac2c9-277">Faux</span><span class="sxs-lookup"><span data-stu-id="ac2c9-277">False</span></span>                                                    |
| <span data-ttu-id="ac2c9-278">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ac2c9-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac2c9-279">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ac2c9-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ac2c9-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac2c9-280">Range-Lower</span></span>            | <span data-ttu-id="ac2c9-281">1</span><span class="sxs-lookup"><span data-stu-id="ac2c9-281">1</span></span>                                                        |
| <span data-ttu-id="ac2c9-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac2c9-282">Range-Upper</span></span>            | <span data-ttu-id="ac2c9-283">13</span><span class="sxs-lookup"><span data-stu-id="ac2c9-283">13</span></span>                                                       |
| <span data-ttu-id="ac2c9-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-284">Search-Flags</span></span>           | <span data-ttu-id="ac2c9-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac2c9-285">0x00000000</span></span>                                               |
| <span data-ttu-id="ac2c9-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac2c9-286">System-Flags</span></span>           | <span data-ttu-id="ac2c9-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac2c9-287">0x00000010</span></span>                                               |
| <span data-ttu-id="ac2c9-288">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ac2c9-288">Classes used in</span></span>        | [<span data-ttu-id="ac2c9-289">**Modèle d’affichage**</span><span class="sxs-lookup"><span data-stu-id="ac2c9-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





