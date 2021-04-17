---
title: ms-DS-entrée-revendications-transformation-stratégie (attribut)
description: Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications entrantes (revendications entrantes dans cette forêt) à partir du domaine approuvé.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-entrée-revendications-transformation-stratégie
- Schéma Active Directory de l’attribut msDS-IngressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519850"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="88427-105">ms-DS-entrée-revendications-transformation-stratégie (attribut)</span><span class="sxs-lookup"><span data-stu-id="88427-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="88427-106">Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications entrantes (revendications entrantes dans cette forêt) à partir du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="88427-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="88427-107">Cela s’applique uniquement à une approbation inter-forêts sortante ou bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="88427-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="88427-108">Si ce lien est absent, toutes les revendications entrantes sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="88427-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="88427-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="88427-109">Entry</span></span> | <span data-ttu-id="88427-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="88427-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="88427-111">CN</span><span class="sxs-lookup"><span data-stu-id="88427-111">CN</span></span>                | <span data-ttu-id="88427-112">ms-DS-entrée-revendications-transformation-stratégie</span><span class="sxs-lookup"><span data-stu-id="88427-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="88427-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88427-113">Ldap-Display-Name</span></span> | <span data-ttu-id="88427-114">msDS-IngressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="88427-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="88427-115">Taille</span><span class="sxs-lookup"><span data-stu-id="88427-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="88427-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="88427-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="88427-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="88427-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="88427-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88427-118">Attribute-Id</span></span>      | <span data-ttu-id="88427-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="88427-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="88427-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88427-120">System-Id-Guid</span></span>    | <span data-ttu-id="88427-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="88427-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="88427-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88427-122">Syntax</span></span>            | [<span data-ttu-id="88427-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="88427-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="88427-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="88427-124">Implementations</span></span>

-   [<span data-ttu-id="88427-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88427-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="88427-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88427-126">Windows Server 2012</span></span>



| <span data-ttu-id="88427-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="88427-127">Entry</span></span> | <span data-ttu-id="88427-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="88427-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="88427-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="88427-129">Link-Id</span></span>                | <span data-ttu-id="88427-130">2190</span><span class="sxs-lookup"><span data-stu-id="88427-130">2190</span></span>                                                 |
| <span data-ttu-id="88427-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88427-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="88427-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="88427-132">System-Only</span></span>            | <span data-ttu-id="88427-133">Faux</span><span class="sxs-lookup"><span data-stu-id="88427-133">False</span></span>                                                |
| <span data-ttu-id="88427-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="88427-134">Is-Single-Valued</span></span>       | <span data-ttu-id="88427-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="88427-135">True</span></span>                                                 |
| <span data-ttu-id="88427-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="88427-136">Is Indexed</span></span>             | <span data-ttu-id="88427-137">Faux</span><span class="sxs-lookup"><span data-stu-id="88427-137">False</span></span>                                                |
| <span data-ttu-id="88427-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="88427-138">In Global Catalog</span></span>      | <span data-ttu-id="88427-139">Faux</span><span class="sxs-lookup"><span data-stu-id="88427-139">False</span></span>                                                |
| <span data-ttu-id="88427-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="88427-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="88427-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="88427-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="88427-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88427-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="88427-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88427-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="88427-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88427-144">Search-Flags</span></span>           | <span data-ttu-id="88427-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88427-145">0x00000000</span></span>                                           |
| <span data-ttu-id="88427-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88427-146">System-Flags</span></span>           | <span data-ttu-id="88427-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88427-147">0x00000010</span></span>                                           |
| <span data-ttu-id="88427-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="88427-148">Classes used in</span></span>        | [<span data-ttu-id="88427-149">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="88427-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





