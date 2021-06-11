---
title: AcceptServerName (PeapExtensionsType), élément (EAPHost)
description: L’élément AcceptServerName (PeapExtensionsType) indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans les nom_serveur dans le schéma mspeapconnectionpropertiesv1.
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989094"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="6bb9c-104">AcceptServerName (PeapExtensionsType), élément (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="6bb9c-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="6bb9c-105">L’élément **AcceptServerName (PeapExtensionsType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb9c-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="6bb9c-106">L’élément est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb9c-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb9c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bb9c-107">Remarks</span></span>

<span data-ttu-id="6bb9c-108">L’élément **AcceptServerName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb9c-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6bb9c-109">Requirements</span></span>



| <span data-ttu-id="6bb9c-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bb9c-110">Requirement</span></span> | <span data-ttu-id="6bb9c-111">Value</span><span class="sxs-lookup"><span data-stu-id="6bb9c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6bb9c-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bb9c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb9c-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bb9c-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6bb9c-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bb9c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb9c-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bb9c-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bb9c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bb9c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bb9c-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6bb9c-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="6bb9c-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6bb9c-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="6bb9c-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6bb9c-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6bb9c-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="6bb9c-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6bb9c-123">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6bb9c-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6bb9c-124">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6bb9c-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6bb9c-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





