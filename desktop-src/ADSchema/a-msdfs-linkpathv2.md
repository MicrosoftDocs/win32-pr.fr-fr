---
title: attribut ms-DFS-Link-Path-v2
description: Chemin de lien DFS relatif au partage cible racine DFS (autrement dit, sans les composants nom de l’espace de noms de serveur/domaine et de l’espace de noms DFS). Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DFS-Link-Path-v2
- Schéma AD de l’attribut msDFS-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108179"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="7ee11-106">attribut ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="7ee11-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="7ee11-107">Chemin de lien DFS relatif au partage cible racine DFS (autrement dit, sans les composants nom de l’espace de noms de serveur/domaine et de l’espace de noms DFS).</span><span class="sxs-lookup"><span data-stu-id="7ee11-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="7ee11-108">Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="7ee11-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="7ee11-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ee11-109">Entry</span></span> | <span data-ttu-id="7ee11-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee11-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7ee11-111">CN</span><span class="sxs-lookup"><span data-stu-id="7ee11-111">CN</span></span>                | <span data-ttu-id="7ee11-112">MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="7ee11-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="7ee11-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7ee11-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7ee11-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="7ee11-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="7ee11-115">Taille</span><span class="sxs-lookup"><span data-stu-id="7ee11-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="7ee11-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7ee11-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7ee11-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7ee11-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7ee11-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ee11-118">Attribute-Id</span></span>      | <span data-ttu-id="7ee11-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="7ee11-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="7ee11-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7ee11-120">System-Id-Guid</span></span>    | <span data-ttu-id="7ee11-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="7ee11-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="7ee11-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ee11-122">Syntax</span></span>            | [<span data-ttu-id="7ee11-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7ee11-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7ee11-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7ee11-124">Implementations</span></span>

-   [<span data-ttu-id="7ee11-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ee11-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ee11-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ee11-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ee11-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="7ee11-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ee11-128">Windows Server 2008</span></span>



| <span data-ttu-id="7ee11-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ee11-129">Entry</span></span> | <span data-ttu-id="7ee11-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee11-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee11-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ee11-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ee11-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ee11-133">System-Only</span></span>            | <span data-ttu-id="7ee11-134">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ee11-135">Is-Single-Valued</span></span>       | <span data-ttu-id="7ee11-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ee11-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="7ee11-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ee11-137">Is Indexed</span></span>             | <span data-ttu-id="7ee11-138">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ee11-139">In Global Catalog</span></span>      | <span data-ttu-id="7ee11-140">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ee11-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ee11-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ee11-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="7ee11-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ee11-143">Range-Lower</span></span>            | <span data-ttu-id="7ee11-144">0</span><span class="sxs-lookup"><span data-stu-id="7ee11-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="7ee11-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ee11-145">Range-Upper</span></span>            | <span data-ttu-id="7ee11-146">32766</span><span class="sxs-lookup"><span data-stu-id="7ee11-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-147">Search-Flags</span></span>           | <span data-ttu-id="7ee11-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ee11-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-149">System-Flags</span></span>           | <span data-ttu-id="7ee11-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ee11-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ee11-151">Classes used in</span></span>        | [<span data-ttu-id="7ee11-152">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="7ee11-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ee11-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ee11-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ee11-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ee11-155">Entry</span></span> | <span data-ttu-id="7ee11-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee11-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee11-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ee11-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ee11-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ee11-159">System-Only</span></span>            | <span data-ttu-id="7ee11-160">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ee11-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7ee11-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ee11-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="7ee11-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ee11-163">Is Indexed</span></span>             | <span data-ttu-id="7ee11-164">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ee11-165">In Global Catalog</span></span>      | <span data-ttu-id="7ee11-166">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ee11-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ee11-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ee11-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="7ee11-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ee11-169">Range-Lower</span></span>            | <span data-ttu-id="7ee11-170">0</span><span class="sxs-lookup"><span data-stu-id="7ee11-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="7ee11-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ee11-171">Range-Upper</span></span>            | <span data-ttu-id="7ee11-172">32766</span><span class="sxs-lookup"><span data-stu-id="7ee11-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-173">Search-Flags</span></span>           | <span data-ttu-id="7ee11-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ee11-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-175">System-Flags</span></span>           | <span data-ttu-id="7ee11-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ee11-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ee11-177">Classes used in</span></span>        | [<span data-ttu-id="7ee11-178">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="7ee11-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ee11-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ee11-180">Windows Server 2012</span></span>



| <span data-ttu-id="7ee11-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ee11-181">Entry</span></span> | <span data-ttu-id="7ee11-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee11-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee11-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ee11-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ee11-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="7ee11-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ee11-185">System-Only</span></span>            | <span data-ttu-id="7ee11-186">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ee11-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7ee11-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ee11-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="7ee11-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ee11-189">Is Indexed</span></span>             | <span data-ttu-id="7ee11-190">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ee11-191">In Global Catalog</span></span>      | <span data-ttu-id="7ee11-192">Faux</span><span class="sxs-lookup"><span data-stu-id="7ee11-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ee11-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ee11-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ee11-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="7ee11-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ee11-195">Range-Lower</span></span>            | <span data-ttu-id="7ee11-196">0</span><span class="sxs-lookup"><span data-stu-id="7ee11-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="7ee11-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ee11-197">Range-Upper</span></span>            | <span data-ttu-id="7ee11-198">32766</span><span class="sxs-lookup"><span data-stu-id="7ee11-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="7ee11-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-199">Search-Flags</span></span>           | <span data-ttu-id="7ee11-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ee11-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ee11-201">System-Flags</span></span>           | <span data-ttu-id="7ee11-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ee11-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="7ee11-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ee11-203">Classes used in</span></span>        | [<span data-ttu-id="7ee11-204">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="7ee11-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="7ee11-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





