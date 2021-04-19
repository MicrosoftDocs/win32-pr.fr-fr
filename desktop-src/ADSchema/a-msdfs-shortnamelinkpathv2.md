---
title: attribut ms-DFS-Short-Name-Link-Path-v2
description: Chemin d’accès de lien DFS de nom abrégé relatif au partage cible racine DFS (autrement dit, sans les composants de nom de serveur/domaine et d’espace de noms DFS). Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DFS-Short-Name-Link-Path-v2
- Schéma AD de l’attribut msDFS-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514696"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="3fae2-106">attribut ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3fae2-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="3fae2-107">Chemin d’accès de lien DFS de nom abrégé relatif au partage cible racine DFS (autrement dit, sans les composants de nom de serveur/domaine et d’espace de noms DFS).</span><span class="sxs-lookup"><span data-stu-id="3fae2-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="3fae2-108">Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="3fae2-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="3fae2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="3fae2-109">Entry</span></span> | <span data-ttu-id="3fae2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fae2-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3fae2-111">CN</span><span class="sxs-lookup"><span data-stu-id="3fae2-111">CN</span></span>                | <span data-ttu-id="3fae2-112">MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3fae2-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="3fae2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3fae2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3fae2-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="3fae2-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="3fae2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="3fae2-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3fae2-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3fae2-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3fae2-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3fae2-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3fae2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3fae2-118">Attribute-Id</span></span>      | <span data-ttu-id="3fae2-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="3fae2-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="3fae2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3fae2-120">System-Id-Guid</span></span>    | <span data-ttu-id="3fae2-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="3fae2-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="3fae2-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fae2-122">Syntax</span></span>            | [<span data-ttu-id="3fae2-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3fae2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3fae2-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3fae2-124">Implementations</span></span>

-   [<span data-ttu-id="3fae2-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3fae2-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3fae2-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3fae2-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3fae2-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3fae2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fae2-128">Windows Server 2008</span></span>



| <span data-ttu-id="3fae2-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="3fae2-129">Entry</span></span> | <span data-ttu-id="3fae2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fae2-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fae2-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3fae2-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3fae2-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="3fae2-133">System-Only</span></span>            | <span data-ttu-id="3fae2-134">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3fae2-135">Is-Single-Valued</span></span>       | <span data-ttu-id="3fae2-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="3fae2-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="3fae2-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3fae2-137">Is Indexed</span></span>             | <span data-ttu-id="3fae2-138">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3fae2-139">In Global Catalog</span></span>      | <span data-ttu-id="3fae2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3fae2-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="3fae2-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3fae2-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3fae2-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3fae2-143">Range-Lower</span></span>            | <span data-ttu-id="3fae2-144">0</span><span class="sxs-lookup"><span data-stu-id="3fae2-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="3fae2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3fae2-145">Range-Upper</span></span>            | <span data-ttu-id="3fae2-146">32766</span><span class="sxs-lookup"><span data-stu-id="3fae2-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-147">Search-Flags</span></span>           | <span data-ttu-id="3fae2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3fae2-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-149">System-Flags</span></span>           | <span data-ttu-id="3fae2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3fae2-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3fae2-151">Classes used in</span></span>        | [<span data-ttu-id="3fae2-152">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3fae2-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3fae2-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3fae2-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3fae2-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="3fae2-155">Entry</span></span> | <span data-ttu-id="3fae2-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fae2-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fae2-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3fae2-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3fae2-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3fae2-159">System-Only</span></span>            | <span data-ttu-id="3fae2-160">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3fae2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3fae2-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="3fae2-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="3fae2-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3fae2-163">Is Indexed</span></span>             | <span data-ttu-id="3fae2-164">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3fae2-165">In Global Catalog</span></span>      | <span data-ttu-id="3fae2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3fae2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3fae2-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3fae2-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3fae2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3fae2-169">Range-Lower</span></span>            | <span data-ttu-id="3fae2-170">0</span><span class="sxs-lookup"><span data-stu-id="3fae2-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="3fae2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3fae2-171">Range-Upper</span></span>            | <span data-ttu-id="3fae2-172">32766</span><span class="sxs-lookup"><span data-stu-id="3fae2-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-173">Search-Flags</span></span>           | <span data-ttu-id="3fae2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3fae2-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-175">System-Flags</span></span>           | <span data-ttu-id="3fae2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3fae2-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3fae2-177">Classes used in</span></span>        | [<span data-ttu-id="3fae2-178">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3fae2-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3fae2-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3fae2-180">Windows Server 2012</span></span>



| <span data-ttu-id="3fae2-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="3fae2-181">Entry</span></span> | <span data-ttu-id="3fae2-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fae2-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fae2-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3fae2-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3fae2-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3fae2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3fae2-185">System-Only</span></span>            | <span data-ttu-id="3fae2-186">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3fae2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3fae2-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="3fae2-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="3fae2-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3fae2-189">Is Indexed</span></span>             | <span data-ttu-id="3fae2-190">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3fae2-191">In Global Catalog</span></span>      | <span data-ttu-id="3fae2-192">Faux</span><span class="sxs-lookup"><span data-stu-id="3fae2-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3fae2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3fae2-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3fae2-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3fae2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3fae2-195">Range-Lower</span></span>            | <span data-ttu-id="3fae2-196">0</span><span class="sxs-lookup"><span data-stu-id="3fae2-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="3fae2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3fae2-197">Range-Upper</span></span>            | <span data-ttu-id="3fae2-198">32766</span><span class="sxs-lookup"><span data-stu-id="3fae2-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3fae2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-199">Search-Flags</span></span>           | <span data-ttu-id="3fae2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3fae2-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3fae2-201">System-Flags</span></span>           | <span data-ttu-id="3fae2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3fae2-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3fae2-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3fae2-203">Classes used in</span></span>        | [<span data-ttu-id="3fae2-204">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3fae2-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3fae2-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





