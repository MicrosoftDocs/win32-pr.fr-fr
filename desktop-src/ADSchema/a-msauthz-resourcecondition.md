---
title: attribut ms-auth-Resource-condition
description: Pour une règle d’accès centralisée, cet attribut est une expression qui identifie l’étendue de la ressource cible à laquelle la stratégie s’applique.
ms.assetid: d3c1815e-3fa1-4106-82a1-74403f07fcde
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-auth-Resource-condition
- Schéma AD de l’attribut msAuthz-ResourceCondition
topic_type:
- apiref
api_name:
- ms-Authz-Resource-Condition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3891e75763fd52d14d4ceaac560b33c824d06449
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108186"
---
# <a name="ms-authz-resource-condition-attribute"></a><span data-ttu-id="598eb-105">attribut ms-auth-Resource-condition</span><span class="sxs-lookup"><span data-stu-id="598eb-105">ms-Authz-Resource-Condition attribute</span></span>

<span data-ttu-id="598eb-106">Pour une règle d’accès centralisée, cet attribut est une expression qui identifie l’étendue de la ressource cible à laquelle la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="598eb-106">For a central access rule, this attribute is an expression that identifies the scope of the target resource to which the policy applies.</span></span>



| <span data-ttu-id="598eb-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="598eb-107">Entry</span></span> | <span data-ttu-id="598eb-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="598eb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="598eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="598eb-109">CN</span></span>                | <span data-ttu-id="598eb-110">MS-auth-Resource-condition</span><span class="sxs-lookup"><span data-stu-id="598eb-110">ms-Authz-Resource-Condition</span></span>                 |
| <span data-ttu-id="598eb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="598eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="598eb-112">msAuthz-ResourceCondition</span><span class="sxs-lookup"><span data-stu-id="598eb-112">msAuthz-ResourceCondition</span></span>                   |
| <span data-ttu-id="598eb-113">Taille</span><span class="sxs-lookup"><span data-stu-id="598eb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="598eb-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="598eb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="598eb-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="598eb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="598eb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="598eb-116">Attribute-Id</span></span>      | <span data-ttu-id="598eb-117">1.2.840.113556.1.4.2153</span><span class="sxs-lookup"><span data-stu-id="598eb-117">1.2.840.113556.1.4.2153</span></span>                     |
| <span data-ttu-id="598eb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="598eb-118">System-Id-Guid</span></span>    | <span data-ttu-id="598eb-119">80997877-f874-4C68-864D-6e508a83bdbd</span><span class="sxs-lookup"><span data-stu-id="598eb-119">80997877-f874-4c68-864d-6e508a83bdbd</span></span>        |
| <span data-ttu-id="598eb-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="598eb-120">Syntax</span></span>            | [<span data-ttu-id="598eb-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="598eb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="598eb-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="598eb-122">Implementations</span></span>

-   [<span data-ttu-id="598eb-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="598eb-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="598eb-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="598eb-124">Windows Server 2012</span></span>



| <span data-ttu-id="598eb-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="598eb-125">Entry</span></span> | <span data-ttu-id="598eb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="598eb-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="598eb-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="598eb-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="598eb-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="598eb-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="598eb-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="598eb-129">System-Only</span></span>            | <span data-ttu-id="598eb-130">Faux</span><span class="sxs-lookup"><span data-stu-id="598eb-130">False</span></span>                                                                          |
| <span data-ttu-id="598eb-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="598eb-131">Is-Single-Valued</span></span>       | <span data-ttu-id="598eb-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="598eb-132">True</span></span>                                                                           |
| <span data-ttu-id="598eb-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="598eb-133">Is Indexed</span></span>             | <span data-ttu-id="598eb-134">Faux</span><span class="sxs-lookup"><span data-stu-id="598eb-134">False</span></span>                                                                          |
| <span data-ttu-id="598eb-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="598eb-135">In Global Catalog</span></span>      | <span data-ttu-id="598eb-136">Faux</span><span class="sxs-lookup"><span data-stu-id="598eb-136">False</span></span>                                                                          |
| <span data-ttu-id="598eb-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="598eb-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="598eb-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="598eb-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="598eb-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="598eb-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="598eb-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="598eb-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="598eb-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="598eb-141">Search-Flags</span></span>           | <span data-ttu-id="598eb-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="598eb-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="598eb-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="598eb-143">System-Flags</span></span>           | <span data-ttu-id="598eb-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="598eb-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="598eb-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="598eb-145">Classes used in</span></span>        | [<span data-ttu-id="598eb-146">**MS-auth-central-Access-Rule**</span><span class="sxs-lookup"><span data-stu-id="598eb-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





