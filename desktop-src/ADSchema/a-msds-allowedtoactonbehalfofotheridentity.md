---
title: ms-DS-allowed-to-Act-on-nom-autre-Identity (attribut)
description: Cet attribut est utilisé pour les vérifications d’accès afin de déterminer si un demandeur est autorisé à agir au nom d’autres identités pour les services qui s’exécutent en tant que ce compte.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-allowed-on-action-on-on-of-Identity
- Schéma Active Directory de l’attribut msDS-AllowedToActOnBehalfOfOtherIdentity
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dacd532b1d8a55b3656dc1d65fc1ebd940476c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845506"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a><span data-ttu-id="e218d-105">ms-DS-allowed-to-Act-on-nom-autre-Identity (attribut)</span><span class="sxs-lookup"><span data-stu-id="e218d-105">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity attribute</span></span>

<span data-ttu-id="e218d-106">Cet attribut est utilisé pour les vérifications d’accès afin de déterminer si un demandeur est autorisé à agir au nom d’autres identités pour les services qui s’exécutent en tant que ce compte.</span><span class="sxs-lookup"><span data-stu-id="e218d-106">This attribute is used for access checks to determine if a requestor has permission to act on the behalf of other identities to services running as this account.</span></span>



| <span data-ttu-id="e218d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e218d-107">Entry</span></span> | <span data-ttu-id="e218d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e218d-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="e218d-109">CN</span><span class="sxs-lookup"><span data-stu-id="e218d-109">CN</span></span>                | <span data-ttu-id="e218d-110">ms-DS-allowed-to-Act-on-on-of-other-Identity</span><span class="sxs-lookup"><span data-stu-id="e218d-110">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity</span></span>    |
| <span data-ttu-id="e218d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e218d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e218d-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span><span class="sxs-lookup"><span data-stu-id="e218d-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span></span>            |
| <span data-ttu-id="e218d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e218d-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="e218d-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e218d-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="e218d-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e218d-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="e218d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e218d-116">Attribute-Id</span></span>      | <span data-ttu-id="e218d-117">1.2.840.113556.1.4.2182</span><span class="sxs-lookup"><span data-stu-id="e218d-117">1.2.840.113556.1.4.2182</span></span>                             |
| <span data-ttu-id="e218d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e218d-118">System-Id-Guid</span></span>    | <span data-ttu-id="e218d-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span><span class="sxs-lookup"><span data-stu-id="e218d-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span></span>                |
| <span data-ttu-id="e218d-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e218d-120">Syntax</span></span>            | [<span data-ttu-id="e218d-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="e218d-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="e218d-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e218d-122">Implementations</span></span>

-   [<span data-ttu-id="e218d-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e218d-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="e218d-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e218d-124">Windows Server 2012</span></span>



| <span data-ttu-id="e218d-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="e218d-125">Entry</span></span> | <span data-ttu-id="e218d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e218d-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e218d-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e218d-127">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e218d-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e218d-128">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e218d-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="e218d-129">System-Only</span></span>            | <span data-ttu-id="e218d-130">Vrai</span><span class="sxs-lookup"><span data-stu-id="e218d-130">True</span></span>                                                               |
| <span data-ttu-id="e218d-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e218d-131">Is-Single-Valued</span></span>       | <span data-ttu-id="e218d-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="e218d-132">True</span></span>                                                               |
| <span data-ttu-id="e218d-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e218d-133">Is Indexed</span></span>             | <span data-ttu-id="e218d-134">Faux</span><span class="sxs-lookup"><span data-stu-id="e218d-134">False</span></span>                                                              |
| <span data-ttu-id="e218d-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e218d-135">In Global Catalog</span></span>      | <span data-ttu-id="e218d-136">Faux</span><span class="sxs-lookup"><span data-stu-id="e218d-136">False</span></span>                                                              |
| <span data-ttu-id="e218d-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e218d-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="e218d-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e218d-138">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e218d-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e218d-139">Range-Lower</span></span>            | <span data-ttu-id="e218d-140">0</span><span class="sxs-lookup"><span data-stu-id="e218d-140">0</span></span>                                                                  |
| <span data-ttu-id="e218d-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e218d-141">Range-Upper</span></span>            | <span data-ttu-id="e218d-142">132096</span><span class="sxs-lookup"><span data-stu-id="e218d-142">132096</span></span>                                                             |
| <span data-ttu-id="e218d-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e218d-143">Search-Flags</span></span>           | <span data-ttu-id="e218d-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e218d-144">0x00000000</span></span>                                                         |
| <span data-ttu-id="e218d-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e218d-145">System-Flags</span></span>           | <span data-ttu-id="e218d-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e218d-146">0x00000010</span></span>                                                         |
| <span data-ttu-id="e218d-147">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e218d-147">Classes used in</span></span>        | [<span data-ttu-id="e218d-148">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e218d-148">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





