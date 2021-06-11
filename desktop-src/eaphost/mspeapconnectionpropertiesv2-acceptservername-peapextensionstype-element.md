---
title: Élément AcceptServerName (PeapExtensionsType)
description: L’élément AcceptServerName (PeapExtensionsType) indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans les nom_serveur dans le schéma mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Élément AcceptServerName EAPHost
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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989474"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="f1379-104">Élément AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="f1379-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="f1379-105">L’élément **AcceptServerName (PeapExtensionsType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1379-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="f1379-106">L’élément **AcceptServerName** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f1379-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1379-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1379-107">Remarks</span></span>

<span data-ttu-id="f1379-108">L’élément **AcceptServerName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f1379-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1379-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f1379-109">Requirements</span></span>



| <span data-ttu-id="f1379-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1379-110">Requirement</span></span> | <span data-ttu-id="f1379-111">Value</span><span class="sxs-lookup"><span data-stu-id="f1379-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f1379-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1379-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f1379-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1379-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f1379-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1379-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f1379-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1379-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1379-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1379-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1379-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f1379-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f1379-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="f1379-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f1379-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="f1379-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f1379-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="f1379-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f1379-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f1379-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f1379-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="f1379-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f1379-123">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f1379-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f1379-124">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f1379-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





