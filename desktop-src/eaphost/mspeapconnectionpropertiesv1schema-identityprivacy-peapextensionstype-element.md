---
title: IdentityPrivacy (PeapExtensionsType), élément (v1)
description: Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. | Élément IdentityPrivacy (PeapExtensionsType)
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 748cf3ae8d5a4da4f8885332a72326bced45b398
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106523460"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="49aaa-105">Élément IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="49aaa-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="49aaa-106">L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="49aaa-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="49aaa-107">L’élément est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="49aaa-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="49aaa-108">Notes</span><span class="sxs-lookup"><span data-stu-id="49aaa-108">Remarks</span></span>

<span data-ttu-id="49aaa-109">L’élément **IdentityPrivacy** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="49aaa-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="49aaa-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49aaa-110">Requirements</span></span>



| <span data-ttu-id="49aaa-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49aaa-111">Requirement</span></span> | <span data-ttu-id="49aaa-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="49aaa-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="49aaa-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49aaa-113">Minimum supported client</span></span><br/> | <span data-ttu-id="49aaa-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49aaa-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="49aaa-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49aaa-115">Minimum supported server</span></span><br/> | <span data-ttu-id="49aaa-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49aaa-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49aaa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49aaa-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="49aaa-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="49aaa-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="49aaa-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="49aaa-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="49aaa-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="49aaa-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="49aaa-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="49aaa-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="49aaa-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="49aaa-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="49aaa-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="49aaa-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="49aaa-124">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="49aaa-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="49aaa-125">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="49aaa-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="49aaa-126">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="49aaa-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





