---
title: attribut ms-DS-Sortss-claims-transformation-Policy
description: Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de stratégie de sortie ms-DS-Sortss-claims-transformation-Policy
- Schéma Active Directory de l’attribut msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943176"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="f9033-105">attribut ms-DS-Sortss-claims-transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="f9033-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="f9033-106">Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="f9033-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="f9033-107">Cela s’applique uniquement à une approbation inter-forêts entrante ou bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="f9033-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="f9033-108">Lorsque ce lien n’est pas présent, toutes les revendications sont autorisées à sortie en l’absence de.</span><span class="sxs-lookup"><span data-stu-id="f9033-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="f9033-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9033-109">Entry</span></span> | <span data-ttu-id="f9033-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9033-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="f9033-111">CN</span><span class="sxs-lookup"><span data-stu-id="f9033-111">CN</span></span>                | <span data-ttu-id="f9033-112">ms-DS-sortie-revendications-transformation-stratégie</span><span class="sxs-lookup"><span data-stu-id="f9033-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="f9033-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f9033-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f9033-114">msDS-EgressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="f9033-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="f9033-115">Taille</span><span class="sxs-lookup"><span data-stu-id="f9033-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="f9033-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f9033-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="f9033-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f9033-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="f9033-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9033-118">Attribute-Id</span></span>      | <span data-ttu-id="f9033-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="f9033-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="f9033-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9033-120">System-Id-Guid</span></span>    | <span data-ttu-id="f9033-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="f9033-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="f9033-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9033-122">Syntax</span></span>            | [<span data-ttu-id="f9033-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f9033-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="f9033-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f9033-124">Implementations</span></span>

-   [<span data-ttu-id="f9033-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9033-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="f9033-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9033-126">Windows Server 2012</span></span>



| <span data-ttu-id="f9033-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9033-127">Entry</span></span> | <span data-ttu-id="f9033-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9033-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f9033-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9033-129">Link-Id</span></span>                | <span data-ttu-id="f9033-130">2192</span><span class="sxs-lookup"><span data-stu-id="f9033-130">2192</span></span>                                                 |
| <span data-ttu-id="f9033-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9033-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f9033-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9033-132">System-Only</span></span>            | <span data-ttu-id="f9033-133">Faux</span><span class="sxs-lookup"><span data-stu-id="f9033-133">False</span></span>                                                |
| <span data-ttu-id="f9033-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9033-134">Is-Single-Valued</span></span>       | <span data-ttu-id="f9033-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9033-135">True</span></span>                                                 |
| <span data-ttu-id="f9033-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9033-136">Is Indexed</span></span>             | <span data-ttu-id="f9033-137">Faux</span><span class="sxs-lookup"><span data-stu-id="f9033-137">False</span></span>                                                |
| <span data-ttu-id="f9033-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9033-138">In Global Catalog</span></span>      | <span data-ttu-id="f9033-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f9033-139">False</span></span>                                                |
| <span data-ttu-id="f9033-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9033-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9033-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9033-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f9033-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9033-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f9033-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9033-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f9033-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9033-144">Search-Flags</span></span>           | <span data-ttu-id="f9033-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9033-145">0x00000000</span></span>                                           |
| <span data-ttu-id="f9033-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9033-146">System-Flags</span></span>           | <span data-ttu-id="f9033-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9033-147">0x00000010</span></span>                                           |
| <span data-ttu-id="f9033-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9033-148">Classes used in</span></span>        | [<span data-ttu-id="f9033-149">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f9033-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





