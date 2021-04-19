---
title: MS-auth-effective-attribut de stratégie de sécurité
description: Pour une règle d’accès centralisée, cet attribut définit l’autorisation qui s’applique aux ressources cibles sur la règle d’accès central.
ms.assetid: 0b7e14b7-9f5d-4437-a0a7-a6ec329c4f80
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-auth-effective-Security-Policy
- Schéma AD de l’attribut msAuthz-EffectiveSecurityPolicy
topic_type:
- apiref
api_name:
- ms-Authz-Effective-Security-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c78d6e3cb23c16f289fc280f07a3a4418d5383
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514670"
---
# <a name="ms-authz-effective-security-policy-attribute"></a><span data-ttu-id="cc2a5-105">MS-auth-effective-attribut de stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="cc2a5-105">ms-Authz-Effective-Security-Policy attribute</span></span>

<span data-ttu-id="cc2a5-106">Pour une règle d’accès centralisée, cet attribut définit l’autorisation qui s’applique aux ressources cibles sur la règle d’accès central.</span><span class="sxs-lookup"><span data-stu-id="cc2a5-106">For a central access rule, this attribute defines the permission that is applying to the target resources on the central access rule.</span></span>



| <span data-ttu-id="cc2a5-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc2a5-107">Entry</span></span> | <span data-ttu-id="cc2a5-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc2a5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cc2a5-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc2a5-109">CN</span></span>                | <span data-ttu-id="cc2a5-110">MS-auth-efficace-sécurité-stratégie</span><span class="sxs-lookup"><span data-stu-id="cc2a5-110">ms-Authz-Effective-Security-Policy</span></span>          |
| <span data-ttu-id="cc2a5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc2a5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc2a5-112">msAuthz-EffectiveSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="cc2a5-112">msAuthz-EffectiveSecurityPolicy</span></span>             |
| <span data-ttu-id="cc2a5-113">Taille</span><span class="sxs-lookup"><span data-stu-id="cc2a5-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="cc2a5-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cc2a5-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="cc2a5-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cc2a5-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cc2a5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc2a5-116">Attribute-Id</span></span>      | <span data-ttu-id="cc2a5-117">1.2.840.113556.1.4.2150</span><span class="sxs-lookup"><span data-stu-id="cc2a5-117">1.2.840.113556.1.4.2150</span></span>                     |
| <span data-ttu-id="cc2a5-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc2a5-118">System-Id-Guid</span></span>    | <span data-ttu-id="cc2a5-119">07831919-8f94-4fb6-8a42-91545dccdad3</span><span class="sxs-lookup"><span data-stu-id="cc2a5-119">07831919-8f94-4fb6-8a42-91545dccdad3</span></span>        |
| <span data-ttu-id="cc2a5-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc2a5-120">Syntax</span></span>            | [<span data-ttu-id="cc2a5-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cc2a5-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cc2a5-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cc2a5-122">Implementations</span></span>

-   [<span data-ttu-id="cc2a5-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc2a5-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="cc2a5-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc2a5-124">Windows Server 2012</span></span>



| <span data-ttu-id="cc2a5-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc2a5-125">Entry</span></span> | <span data-ttu-id="cc2a5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc2a5-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cc2a5-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc2a5-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="cc2a5-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2a5-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="cc2a5-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2a5-129">System-Only</span></span>            | <span data-ttu-id="cc2a5-130">Faux</span><span class="sxs-lookup"><span data-stu-id="cc2a5-130">False</span></span>                                                                          |
| <span data-ttu-id="cc2a5-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc2a5-131">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2a5-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="cc2a5-132">True</span></span>                                                                           |
| <span data-ttu-id="cc2a5-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc2a5-133">Is Indexed</span></span>             | <span data-ttu-id="cc2a5-134">Faux</span><span class="sxs-lookup"><span data-stu-id="cc2a5-134">False</span></span>                                                                          |
| <span data-ttu-id="cc2a5-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc2a5-135">In Global Catalog</span></span>      | <span data-ttu-id="cc2a5-136">Faux</span><span class="sxs-lookup"><span data-stu-id="cc2a5-136">False</span></span>                                                                          |
| <span data-ttu-id="cc2a5-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc2a5-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2a5-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc2a5-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="cc2a5-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2a5-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="cc2a5-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2a5-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="cc2a5-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2a5-141">Search-Flags</span></span>           | <span data-ttu-id="cc2a5-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2a5-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="cc2a5-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2a5-143">System-Flags</span></span>           | <span data-ttu-id="cc2a5-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2a5-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="cc2a5-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc2a5-145">Classes used in</span></span>        | [<span data-ttu-id="cc2a5-146">**MS-auth-central-Access-Rule**</span><span class="sxs-lookup"><span data-stu-id="cc2a5-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





