---
title: IdentityPrivacy (PeapExtensionsType), élément (v1)
description: L’élément IdentityPrivacy (PeapExtensionsType) indique si l’identité réelle d’un utilisateur est envoyée dans le schéma mspeapconnectionpropertiesv1.
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
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989214"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="5f559-104">Élément IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="5f559-104">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="5f559-105">L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="5f559-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="5f559-106">L’élément est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5f559-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f559-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f559-107">Remarks</span></span>

<span data-ttu-id="5f559-108">L’élément **IdentityPrivacy** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f559-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f559-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5f559-109">Requirements</span></span>



| <span data-ttu-id="5f559-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f559-110">Requirement</span></span> | <span data-ttu-id="5f559-111">Value</span><span class="sxs-lookup"><span data-stu-id="5f559-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5f559-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f559-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5f559-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f559-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5f559-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f559-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5f559-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f559-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f559-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f559-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f559-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="5f559-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5f559-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="5f559-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="5f559-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="5f559-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5f559-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="5f559-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="5f559-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5f559-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5f559-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="5f559-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5f559-123">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5f559-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5f559-124">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5f559-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5f559-125">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="5f559-125">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





