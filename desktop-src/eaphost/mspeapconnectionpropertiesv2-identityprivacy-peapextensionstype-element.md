---
title: Élément IdentityPrivacy (PeapExtensionsType)
description: Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. | Élément IdentityPrivacy (PeapExtensionsType)
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Élément IdentityPrivacy EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530645"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="59da5-105">Élément IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="59da5-105">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="59da5-106">L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="59da5-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="59da5-107">L’élément **IdentityPrivacy** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="59da5-107">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="59da5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="59da5-108">Remarks</span></span>

<span data-ttu-id="59da5-109">L’élément **IdentityPrivacy** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59da5-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="59da5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59da5-110">Requirements</span></span>



| <span data-ttu-id="59da5-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59da5-111">Requirement</span></span> | <span data-ttu-id="59da5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="59da5-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="59da5-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59da5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="59da5-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59da5-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="59da5-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59da5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="59da5-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59da5-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59da5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59da5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="59da5-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="59da5-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="59da5-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="59da5-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="59da5-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="59da5-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="59da5-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="59da5-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="59da5-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="59da5-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="59da5-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="59da5-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="59da5-124">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="59da5-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="59da5-125">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="59da5-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





