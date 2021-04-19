---
title: ms-DS-attribut-Encryption-types pris en charge
description: Algorithmes de chiffrement pris en charge par les comptes d’utilisateur, d’ordinateur ou de confiance. Notez que le KDC utilise ces informations lors de la génération d’un ticket de service pour ce compte.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs de types de chiffrement pris en charge par ms-DS
- Schéma Active Directory de l’attribut msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106513269"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="a3905-105">ms-DS-attribut-Encryption-types pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3905-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="a3905-106">Algorithmes de chiffrement pris en charge par les comptes d’utilisateur, d’ordinateur ou de confiance.</span><span class="sxs-lookup"><span data-stu-id="a3905-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="a3905-107">Le KDC utilise ces informations lors de la génération d’un ticket de service pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="a3905-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="a3905-108">Les services et les ordinateurs peuvent automatiquement mettre à jour cet attribut sur leurs comptes respectifs dans Active Directory et ont donc besoin d’un accès en écriture à cet attribut.</span><span class="sxs-lookup"><span data-stu-id="a3905-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="a3905-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3905-109">Entry</span></span> | <span data-ttu-id="a3905-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3905-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a3905-111">CN</span><span class="sxs-lookup"><span data-stu-id="a3905-111">CN</span></span>                | <span data-ttu-id="a3905-112">ms-DS-types de chiffrement pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3905-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="a3905-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a3905-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a3905-114">msDS-SupportedEncryptionTypes</span><span class="sxs-lookup"><span data-stu-id="a3905-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="a3905-115">Taille</span><span class="sxs-lookup"><span data-stu-id="a3905-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="a3905-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a3905-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a3905-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a3905-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a3905-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3905-118">Attribute-Id</span></span>      | <span data-ttu-id="a3905-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="a3905-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="a3905-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3905-120">System-Id-Guid</span></span>    | <span data-ttu-id="a3905-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="a3905-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="a3905-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3905-122">Syntax</span></span>            | [<span data-ttu-id="a3905-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a3905-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a3905-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a3905-124">Implementations</span></span>

-   [<span data-ttu-id="a3905-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3905-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3905-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3905-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3905-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3905-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="a3905-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3905-128">Windows Server 2008</span></span>



| <span data-ttu-id="a3905-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3905-129">Entry</span></span> | <span data-ttu-id="a3905-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3905-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3905-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3905-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3905-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3905-133">System-Only</span></span>            | <span data-ttu-id="a3905-134">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-134">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3905-135">Is-Single-Valued</span></span>       | <span data-ttu-id="a3905-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3905-136">True</span></span>                                                                                   |
| <span data-ttu-id="a3905-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3905-137">Is Indexed</span></span>             | <span data-ttu-id="a3905-138">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-138">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3905-139">In Global Catalog</span></span>      | <span data-ttu-id="a3905-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-140">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3905-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3905-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3905-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="a3905-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3905-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3905-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-145">Search-Flags</span></span>           | <span data-ttu-id="a3905-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3905-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="a3905-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-147">System-Flags</span></span>           | <span data-ttu-id="a3905-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3905-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="a3905-149">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3905-149">Classes used in</span></span>        | [<span data-ttu-id="a3905-150">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a3905-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="a3905-151">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3905-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3905-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3905-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3905-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3905-153">Entry</span></span> | <span data-ttu-id="a3905-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3905-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3905-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3905-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3905-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3905-157">System-Only</span></span>            | <span data-ttu-id="a3905-158">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-158">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3905-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a3905-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3905-160">True</span></span>                                                                                   |
| <span data-ttu-id="a3905-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3905-161">Is Indexed</span></span>             | <span data-ttu-id="a3905-162">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-162">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3905-163">In Global Catalog</span></span>      | <span data-ttu-id="a3905-164">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-164">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3905-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3905-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3905-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="a3905-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3905-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3905-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-169">Search-Flags</span></span>           | <span data-ttu-id="a3905-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3905-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="a3905-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-171">System-Flags</span></span>           | <span data-ttu-id="a3905-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3905-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="a3905-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3905-173">Classes used in</span></span>        | [<span data-ttu-id="a3905-174">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a3905-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="a3905-175">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3905-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3905-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3905-176">Windows Server 2012</span></span>



| <span data-ttu-id="a3905-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="a3905-177">Entry</span></span> | <span data-ttu-id="a3905-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3905-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3905-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a3905-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3905-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="a3905-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3905-181">System-Only</span></span>            | <span data-ttu-id="a3905-182">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-182">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a3905-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a3905-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="a3905-184">True</span></span>                                                                                   |
| <span data-ttu-id="a3905-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a3905-185">Is Indexed</span></span>             | <span data-ttu-id="a3905-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-186">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a3905-187">In Global Catalog</span></span>      | <span data-ttu-id="a3905-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a3905-188">False</span></span>                                                                                  |
| <span data-ttu-id="a3905-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a3905-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3905-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a3905-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="a3905-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3905-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3905-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="a3905-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-193">Search-Flags</span></span>           | <span data-ttu-id="a3905-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3905-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="a3905-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3905-195">System-Flags</span></span>           | <span data-ttu-id="a3905-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3905-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="a3905-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a3905-197">Classes used in</span></span>        | [<span data-ttu-id="a3905-198">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a3905-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="a3905-199">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a3905-199">**User**</span></span>](c-user.md)<br/> |



 

 





