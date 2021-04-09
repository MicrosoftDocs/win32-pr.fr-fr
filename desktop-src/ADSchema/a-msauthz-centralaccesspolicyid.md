---
title: MS-auth-central-Access-Policy-ID (attribut)
description: Pour une stratégie d’accès centralisée, cet attribut définit un GUID qui peut être utilisé pour identifier le jeu de stratégies lorsqu’il est appliqué à une ressource.
ms.assetid: db1fe49b-f737-4202-bd6f-7bab64187c82
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-auth-central-Access-Policy-ID
- Schéma AD de l’attribut msAuthz-CentralAccessPolicyID
topic_type:
- apiref
api_name:
- ms-Authz-Central-Access-Policy-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bda6a6d8b28ac43f984034c63a259e74d49712e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108190"
---
# <a name="ms-authz-central-access-policy-id-attribute"></a><span data-ttu-id="4f45a-105">MS-auth-central-Access-Policy-ID (attribut)</span><span class="sxs-lookup"><span data-stu-id="4f45a-105">ms-Authz-Central-Access-Policy-ID attribute</span></span>

<span data-ttu-id="4f45a-106">Pour une stratégie d’accès centralisée, cet attribut définit un GUID qui peut être utilisé pour identifier le jeu de stratégies lorsqu’il est appliqué à une ressource.</span><span class="sxs-lookup"><span data-stu-id="4f45a-106">For a Central Access Policy, this attribute defines a GUID that can be used to identify the set of policies when applied to a resource.</span></span>



| <span data-ttu-id="4f45a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f45a-107">Entry</span></span> | <span data-ttu-id="4f45a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f45a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4f45a-109">CN</span><span class="sxs-lookup"><span data-stu-id="4f45a-109">CN</span></span>                | <span data-ttu-id="4f45a-110">MS-auth-central-Access-Policy-ID</span><span class="sxs-lookup"><span data-stu-id="4f45a-110">ms-Authz-Central-Access-Policy-ID</span></span>    |
| <span data-ttu-id="4f45a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f45a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4f45a-112">msAuthz-CentralAccessPolicyID</span><span class="sxs-lookup"><span data-stu-id="4f45a-112">msAuthz-CentralAccessPolicyID</span></span>        |
| <span data-ttu-id="4f45a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4f45a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="4f45a-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4f45a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4f45a-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4f45a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4f45a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f45a-116">Attribute-Id</span></span>      | <span data-ttu-id="4f45a-117">1.2.840.113556.1.4.2154</span><span class="sxs-lookup"><span data-stu-id="4f45a-117">1.2.840.113556.1.4.2154</span></span>              |
| <span data-ttu-id="4f45a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f45a-118">System-Id-Guid</span></span>    | <span data-ttu-id="4f45a-119">62f29b60-be74-4630-9456-2f6691993a86</span><span class="sxs-lookup"><span data-stu-id="4f45a-119">62f29b60-be74-4630-9456-2f6691993a86</span></span> |
| <span data-ttu-id="4f45a-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f45a-120">Syntax</span></span>            | [<span data-ttu-id="4f45a-121">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="4f45a-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="4f45a-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4f45a-122">Implementations</span></span>

-   [<span data-ttu-id="4f45a-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f45a-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="4f45a-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f45a-124">Windows Server 2012</span></span>



| <span data-ttu-id="4f45a-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f45a-125">Entry</span></span> | <span data-ttu-id="4f45a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f45a-126">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f45a-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f45a-127">Link-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="4f45a-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f45a-128">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="4f45a-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f45a-129">System-Only</span></span>            | <span data-ttu-id="4f45a-130">Faux</span><span class="sxs-lookup"><span data-stu-id="4f45a-130">False</span></span>                                                                              |
| <span data-ttu-id="4f45a-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f45a-131">Is-Single-Valued</span></span>       | <span data-ttu-id="4f45a-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f45a-132">True</span></span>                                                                               |
| <span data-ttu-id="4f45a-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f45a-133">Is Indexed</span></span>             | <span data-ttu-id="4f45a-134">Faux</span><span class="sxs-lookup"><span data-stu-id="4f45a-134">False</span></span>                                                                              |
| <span data-ttu-id="4f45a-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f45a-135">In Global Catalog</span></span>      | <span data-ttu-id="4f45a-136">Faux</span><span class="sxs-lookup"><span data-stu-id="4f45a-136">False</span></span>                                                                              |
| <span data-ttu-id="4f45a-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f45a-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f45a-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f45a-138">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="4f45a-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f45a-139">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="4f45a-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f45a-140">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="4f45a-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f45a-141">Search-Flags</span></span>           | <span data-ttu-id="4f45a-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f45a-142">0x00000000</span></span>                                                                         |
| <span data-ttu-id="4f45a-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f45a-143">System-Flags</span></span>           | <span data-ttu-id="4f45a-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f45a-144">0x00000010</span></span>                                                                         |
| <span data-ttu-id="4f45a-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f45a-145">Classes used in</span></span>        | [<span data-ttu-id="4f45a-146">**MS-auth-central-Access-Policy**</span><span class="sxs-lookup"><span data-stu-id="4f45a-146">**ms-Authz-Central-Access-Policy**</span></span>](c-msauthz-centralaccesspolicy.md)<br/> |



 

 





