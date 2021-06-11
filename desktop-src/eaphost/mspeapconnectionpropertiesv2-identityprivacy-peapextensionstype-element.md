---
title: Élément IdentityPrivacy (PeapExtensionsType)
description: L’élément IdentityPrivacy (PeapExtensionsType) indique si l’identité réelle d’un utilisateur est envoyée dans le schéma mspeapconnectionpropertiesv2.
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
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988945"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="bc57a-104">Élément IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="bc57a-104">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="bc57a-105">L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="bc57a-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="bc57a-106">L’élément **IdentityPrivacy** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc57a-106">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc57a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc57a-107">Remarks</span></span>

<span data-ttu-id="bc57a-108">L’élément **IdentityPrivacy** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bc57a-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc57a-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc57a-109">Requirements</span></span>



| <span data-ttu-id="bc57a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc57a-110">Requirement</span></span> | <span data-ttu-id="bc57a-111">Value</span><span class="sxs-lookup"><span data-stu-id="bc57a-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bc57a-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc57a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bc57a-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc57a-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bc57a-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc57a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bc57a-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc57a-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc57a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc57a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc57a-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bc57a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bc57a-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="bc57a-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="bc57a-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bc57a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bc57a-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="bc57a-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="bc57a-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bc57a-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bc57a-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="bc57a-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bc57a-123">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bc57a-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bc57a-124">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bc57a-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





