---
title: MS-auth-Last-effective-attribut de stratégie de sécurité
description: Pour une règle d’accès centralisée, cet attribut définit l’autorisation qui a été appliquée en dernier aux objets auxquels la règle d’accès centralisée est appliquée.
ms.assetid: bf3aed36-61ff-426d-848e-8993e784bd9f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-auth-Last-effectif-Security-Policy
- Schéma AD de l’attribut msAuthz-LastEffectiveSecurityPolicy
topic_type:
- apiref
api_name:
- ms-Authz-Last-Effective-Security-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a310048e6ab8576be742ece790ada0f3ebd218f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949903"
---
# <a name="ms-authz-last-effective-security-policy-attribute"></a><span data-ttu-id="50a8f-105">MS-auth-Last-effective-attribut de stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="50a8f-105">ms-Authz-Last-Effective-Security-Policy attribute</span></span>

<span data-ttu-id="50a8f-106">Pour une règle d’accès centralisée, cet attribut définit l’autorisation qui a été appliquée en dernier aux objets auxquels la règle d’accès centralisée est appliquée.</span><span class="sxs-lookup"><span data-stu-id="50a8f-106">For a central access rule, this attribute defines the permission that was last applied to the objects the Central Access Rule is applied to.</span></span>



| <span data-ttu-id="50a8f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="50a8f-107">Entry</span></span> | <span data-ttu-id="50a8f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="50a8f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="50a8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="50a8f-109">CN</span></span>                | <span data-ttu-id="50a8f-110">MS-auth-dernier-effectif-stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="50a8f-110">ms-Authz-Last-Effective-Security-Policy</span></span>     |
| <span data-ttu-id="50a8f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="50a8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50a8f-112">msAuthz-LastEffectiveSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="50a8f-112">msAuthz-LastEffectiveSecurityPolicy</span></span>         |
| <span data-ttu-id="50a8f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="50a8f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="50a8f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="50a8f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="50a8f-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="50a8f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="50a8f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50a8f-116">Attribute-Id</span></span>      | <span data-ttu-id="50a8f-117">1.2.840.113556.1.4.2152</span><span class="sxs-lookup"><span data-stu-id="50a8f-117">1.2.840.113556.1.4.2152</span></span>                     |
| <span data-ttu-id="50a8f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="50a8f-118">System-Id-Guid</span></span>    | <span data-ttu-id="50a8f-119">8e1685c6-3e2f-48a2-a58d-5af0ea789fa0</span><span class="sxs-lookup"><span data-stu-id="50a8f-119">8e1685c6-3e2f-48a2-a58d-5af0ea789fa0</span></span>        |
| <span data-ttu-id="50a8f-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50a8f-120">Syntax</span></span>            | [<span data-ttu-id="50a8f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="50a8f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="50a8f-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="50a8f-122">Implementations</span></span>

-   [<span data-ttu-id="50a8f-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50a8f-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="50a8f-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50a8f-124">Windows Server 2012</span></span>



| <span data-ttu-id="50a8f-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="50a8f-125">Entry</span></span> | <span data-ttu-id="50a8f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="50a8f-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="50a8f-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="50a8f-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="50a8f-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a8f-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="50a8f-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a8f-129">System-Only</span></span>            | <span data-ttu-id="50a8f-130">Faux</span><span class="sxs-lookup"><span data-stu-id="50a8f-130">False</span></span>                                                                          |
| <span data-ttu-id="50a8f-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="50a8f-131">Is-Single-Valued</span></span>       | <span data-ttu-id="50a8f-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="50a8f-132">True</span></span>                                                                           |
| <span data-ttu-id="50a8f-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="50a8f-133">Is Indexed</span></span>             | <span data-ttu-id="50a8f-134">Faux</span><span class="sxs-lookup"><span data-stu-id="50a8f-134">False</span></span>                                                                          |
| <span data-ttu-id="50a8f-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="50a8f-135">In Global Catalog</span></span>      | <span data-ttu-id="50a8f-136">Faux</span><span class="sxs-lookup"><span data-stu-id="50a8f-136">False</span></span>                                                                          |
| <span data-ttu-id="50a8f-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="50a8f-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a8f-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="50a8f-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="50a8f-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a8f-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="50a8f-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a8f-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="50a8f-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a8f-141">Search-Flags</span></span>           | <span data-ttu-id="50a8f-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a8f-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="50a8f-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a8f-143">System-Flags</span></span>           | <span data-ttu-id="50a8f-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a8f-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="50a8f-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="50a8f-145">Classes used in</span></span>        | [<span data-ttu-id="50a8f-146">**MS-auth-central-Access-Rule**</span><span class="sxs-lookup"><span data-stu-id="50a8f-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





