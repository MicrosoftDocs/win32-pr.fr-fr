---
title: Netboot-machine-attribut-file-path
description: Cet attribut spécifie le serveur qui répond au client. Depuis le système d’exploitation Windows Server 2003, il peut indiquer le Startrom.com que le client obtient.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Netboot-machine-attribut de chemin d’accès de fichier-schéma AD
- Schéma AD de l’attribut netbootMachineFilePath
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516716"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="1cfdf-106">Netboot-machine-attribut-file-path</span><span class="sxs-lookup"><span data-stu-id="1cfdf-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="1cfdf-107">Cet attribut spécifie le serveur qui répond au client.</span><span class="sxs-lookup"><span data-stu-id="1cfdf-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="1cfdf-108">Depuis le système d’exploitation Windows Server 2003, il peut indiquer le Startrom.com que le client obtient.</span><span class="sxs-lookup"><span data-stu-id="1cfdf-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="1cfdf-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-109">Entry</span></span> | <span data-ttu-id="1cfdf-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1cfdf-111">CN</span><span class="sxs-lookup"><span data-stu-id="1cfdf-111">CN</span></span>                | <span data-ttu-id="1cfdf-112">Netboot-machine-file-path</span><span class="sxs-lookup"><span data-stu-id="1cfdf-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="1cfdf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1cfdf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1cfdf-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="1cfdf-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="1cfdf-115">Taille</span><span class="sxs-lookup"><span data-stu-id="1cfdf-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="1cfdf-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="1cfdf-116">Update Privilege</span></span>  | <span data-ttu-id="1cfdf-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="1cfdf-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="1cfdf-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="1cfdf-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1cfdf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-119">Attribute-Id</span></span>      | <span data-ttu-id="1cfdf-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="1cfdf-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="1cfdf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1cfdf-121">System-Id-Guid</span></span>    | <span data-ttu-id="1cfdf-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="1cfdf-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="1cfdf-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cfdf-123">Syntax</span></span>            | [<span data-ttu-id="1cfdf-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1cfdf-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="1cfdf-125">Implementations</span></span>

-   [<span data-ttu-id="1cfdf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1cfdf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1cfdf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1cfdf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1cfdf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1cfdf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1cfdf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cfdf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1cfdf-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-133">Entry</span></span> | <span data-ttu-id="1cfdf-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-137">System-Only</span></span>            | <span data-ttu-id="1cfdf-138">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-138">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-140">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-141">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-142">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-142">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-143">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-144">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-149">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-151">System-Flags</span></span>           | <span data-ttu-id="1cfdf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-153">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-155">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1cfdf-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cfdf-156">Windows Server 2003</span></span>



| <span data-ttu-id="1cfdf-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-157">Entry</span></span> | <span data-ttu-id="1cfdf-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-161">System-Only</span></span>            | <span data-ttu-id="1cfdf-162">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-162">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-163">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-164">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-165">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-166">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-166">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-167">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-168">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-173">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-175">System-Flags</span></span>           | <span data-ttu-id="1cfdf-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-177">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-178">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-179">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1cfdf-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1cfdf-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1cfdf-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-181">Entry</span></span> | <span data-ttu-id="1cfdf-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-185">System-Only</span></span>            | <span data-ttu-id="1cfdf-186">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-186">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-188">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-189">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-190">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-190">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-191">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-192">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-197">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-199">System-Flags</span></span>           | <span data-ttu-id="1cfdf-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-201">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-202">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-203">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1cfdf-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cfdf-204">Windows Server 2008</span></span>



| <span data-ttu-id="1cfdf-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-205">Entry</span></span> | <span data-ttu-id="1cfdf-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-209">System-Only</span></span>            | <span data-ttu-id="1cfdf-210">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-210">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-212">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-213">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-214">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-214">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-215">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-216">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-221">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-223">System-Flags</span></span>           | <span data-ttu-id="1cfdf-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-225">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-226">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-227">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1cfdf-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cfdf-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1cfdf-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-229">Entry</span></span> | <span data-ttu-id="1cfdf-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-233">System-Only</span></span>            | <span data-ttu-id="1cfdf-234">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-234">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-235">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-236">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-237">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-238">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-238">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-239">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-240">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-245">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-247">System-Flags</span></span>           | <span data-ttu-id="1cfdf-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-249">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-250">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-251">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1cfdf-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cfdf-252">Windows Server 2012</span></span>



| <span data-ttu-id="1cfdf-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cfdf-253">Entry</span></span> | <span data-ttu-id="1cfdf-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfdf-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfdf-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1cfdf-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cfdf-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="1cfdf-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cfdf-257">System-Only</span></span>            | <span data-ttu-id="1cfdf-258">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-258">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1cfdf-259">Is-Single-Valued</span></span>       | <span data-ttu-id="1cfdf-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-260">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1cfdf-261">Is Indexed</span></span>             | <span data-ttu-id="1cfdf-262">Faux</span><span class="sxs-lookup"><span data-stu-id="1cfdf-262">False</span></span>                                                                                                |
| <span data-ttu-id="1cfdf-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1cfdf-263">In Global Catalog</span></span>      | <span data-ttu-id="1cfdf-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="1cfdf-264">True</span></span>                                                                                                 |
| <span data-ttu-id="1cfdf-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1cfdf-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cfdf-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1cfdf-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="1cfdf-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cfdf-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cfdf-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="1cfdf-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-269">Search-Flags</span></span>           | <span data-ttu-id="1cfdf-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cfdf-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cfdf-271">System-Flags</span></span>           | <span data-ttu-id="1cfdf-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cfdf-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="1cfdf-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1cfdf-273">Classes used in</span></span>        | [<span data-ttu-id="1cfdf-274">**Computer**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="1cfdf-275">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="1cfdf-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





