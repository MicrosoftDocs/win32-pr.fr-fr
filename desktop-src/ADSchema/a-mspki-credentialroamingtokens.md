---
title: MS-PKI-informations d’identification-attribut des jetons d’itinérance
description: Stockage des objets BLOB de jeton d’informations d’identification utilisateur chiffrés pour l’itinérance. | MS-PKI-informations d’identification-attribut des jetons d’itinérance
ms.assetid: 35500e2b-7922-47c9-a9dd-e76ea6fd4313
ms.tgt_platform: multiple
keywords:
- MS-PKI-Credential-profil itinérant-attribut des jetons-schéma Active Directory
- Schéma AD de l’attribut attribut mspki-CredentialRoamingTokens
topic_type:
- apiref
api_name:
- ms-PKI-Credential-Roaming-Tokens
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c35a0f949fd69aaad18db3b1cf965d808581c86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535767"
---
# <a name="ms-pki-credential-roaming-tokens-attribute"></a><span data-ttu-id="bdb51-106">MS-PKI-informations d’identification-attribut des jetons d’itinérance</span><span class="sxs-lookup"><span data-stu-id="bdb51-106">ms-PKI-Credential-Roaming-Tokens attribute</span></span>

<span data-ttu-id="bdb51-107">Stockage des objets BLOB de jeton d’informations d’identification utilisateur chiffrés pour l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="bdb51-107">Storage of encrypted user credential token BLOBs for roaming.</span></span>



| <span data-ttu-id="bdb51-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdb51-108">Entry</span></span> | <span data-ttu-id="bdb51-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb51-109">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="bdb51-110">CN</span><span class="sxs-lookup"><span data-stu-id="bdb51-110">CN</span></span>                | <span data-ttu-id="bdb51-111">MS-PKI-Credential-itinérance-jetons</span><span class="sxs-lookup"><span data-stu-id="bdb51-111">ms-PKI-Credential-Roaming-Tokens</span></span>                |
| <span data-ttu-id="bdb51-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bdb51-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bdb51-113">Attribut mspki-CredentialRoamingTokens</span><span class="sxs-lookup"><span data-stu-id="bdb51-113">msPKI-CredentialRoamingTokens</span></span>                   |
| <span data-ttu-id="bdb51-114">Taille</span><span class="sxs-lookup"><span data-stu-id="bdb51-114">Size</span></span>              | \-                                              |
| <span data-ttu-id="bdb51-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bdb51-115">Update Privilege</span></span>  | \-                                              |
| <span data-ttu-id="bdb51-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bdb51-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="bdb51-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bdb51-117">Attribute-Id</span></span>      | <span data-ttu-id="bdb51-118">1.2.840.113556.1.4.2050</span><span class="sxs-lookup"><span data-stu-id="bdb51-118">1.2.840.113556.1.4.2050</span></span>                         |
| <span data-ttu-id="bdb51-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bdb51-119">System-Id-Guid</span></span>    | <span data-ttu-id="bdb51-120">b7ff5a38-0818-42b0-8110-d3d154c97f24</span><span class="sxs-lookup"><span data-stu-id="bdb51-120">b7ff5a38-0818-42b0-8110-d3d154c97f24</span></span>            |
| <span data-ttu-id="bdb51-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb51-121">Syntax</span></span>            | [<span data-ttu-id="bdb51-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="bdb51-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="bdb51-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bdb51-123">Implementations</span></span>

-   [<span data-ttu-id="bdb51-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bdb51-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bdb51-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bdb51-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008-r2"></a><span data-ttu-id="bdb51-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdb51-126">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bdb51-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdb51-127">Entry</span></span> | <span data-ttu-id="bdb51-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb51-128">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdb51-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdb51-129">Link-Id</span></span>                | <span data-ttu-id="bdb51-130">2162</span><span class="sxs-lookup"><span data-stu-id="bdb51-130">2162</span></span>                              |
| <span data-ttu-id="bdb51-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdb51-131">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdb51-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdb51-132">System-Only</span></span>            | <span data-ttu-id="bdb51-133">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-133">False</span></span>                             |
| <span data-ttu-id="bdb51-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdb51-134">Is-Single-Valued</span></span>       | <span data-ttu-id="bdb51-135">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-135">False</span></span>                             |
| <span data-ttu-id="bdb51-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdb51-136">Is Indexed</span></span>             | <span data-ttu-id="bdb51-137">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-137">False</span></span>                             |
| <span data-ttu-id="bdb51-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdb51-138">In Global Catalog</span></span>      | <span data-ttu-id="bdb51-139">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-139">False</span></span>                             |
| <span data-ttu-id="bdb51-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdb51-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdb51-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdb51-141">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdb51-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdb51-142">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdb51-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdb51-143">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdb51-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdb51-144">Search-Flags</span></span>           | <span data-ttu-id="bdb51-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bdb51-145">0x00000080</span></span>                        |
| <span data-ttu-id="bdb51-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdb51-146">System-Flags</span></span>           | <span data-ttu-id="bdb51-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdb51-147">0x00000010</span></span>                        |
| <span data-ttu-id="bdb51-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdb51-148">Classes used in</span></span>        | [<span data-ttu-id="bdb51-149">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdb51-149">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bdb51-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdb51-150">Windows Server 2012</span></span>



| <span data-ttu-id="bdb51-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="bdb51-151">Entry</span></span> | <span data-ttu-id="bdb51-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb51-152">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bdb51-153">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bdb51-153">Link-Id</span></span>                | <span data-ttu-id="bdb51-154">2162</span><span class="sxs-lookup"><span data-stu-id="bdb51-154">2162</span></span>                              |
| <span data-ttu-id="bdb51-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdb51-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bdb51-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdb51-156">System-Only</span></span>            | <span data-ttu-id="bdb51-157">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-157">False</span></span>                             |
| <span data-ttu-id="bdb51-158">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bdb51-158">Is-Single-Valued</span></span>       | <span data-ttu-id="bdb51-159">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-159">False</span></span>                             |
| <span data-ttu-id="bdb51-160">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bdb51-160">Is Indexed</span></span>             | <span data-ttu-id="bdb51-161">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-161">False</span></span>                             |
| <span data-ttu-id="bdb51-162">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bdb51-162">In Global Catalog</span></span>      | <span data-ttu-id="bdb51-163">Faux</span><span class="sxs-lookup"><span data-stu-id="bdb51-163">False</span></span>                             |
| <span data-ttu-id="bdb51-164">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bdb51-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdb51-165">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bdb51-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bdb51-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdb51-166">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bdb51-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdb51-167">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bdb51-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdb51-168">Search-Flags</span></span>           | <span data-ttu-id="bdb51-169">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bdb51-169">0x00000080</span></span>                        |
| <span data-ttu-id="bdb51-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdb51-170">System-Flags</span></span>           | <span data-ttu-id="bdb51-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdb51-171">0x00000010</span></span>                        |
| <span data-ttu-id="bdb51-172">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bdb51-172">Classes used in</span></span>        | [<span data-ttu-id="bdb51-173">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bdb51-173">**User**</span></span>](c-user.md)<br/> |



 

 





