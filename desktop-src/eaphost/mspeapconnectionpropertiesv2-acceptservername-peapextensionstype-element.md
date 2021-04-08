---
title: Élément AcceptServerName (PeapExtensionsType)
description: Indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément ServerNames (ServerValidationParameters). | Élément AcceptServerName (PeapExtensionsType)
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
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953726"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="bb7b9-105">Élément AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="bb7b9-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="bb7b9-106">L’élément **AcceptServerName (PeapExtensionsType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7b9-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="bb7b9-107">L’élément **AcceptServerName** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7b9-107">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7b9-108">Notes</span><span class="sxs-lookup"><span data-stu-id="bb7b9-108">Remarks</span></span>

<span data-ttu-id="bb7b9-109">L’élément **AcceptServerName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7b9-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb7b9-110">Requirements</span></span>



| <span data-ttu-id="bb7b9-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb7b9-111">Requirement</span></span> | <span data-ttu-id="bb7b9-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb7b9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bb7b9-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb7b9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7b9-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb7b9-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bb7b9-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb7b9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7b9-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb7b9-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb7b9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb7b9-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb7b9-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bb7b9-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7b9-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="bb7b9-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="bb7b9-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bb7b9-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7b9-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="bb7b9-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="bb7b9-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bb7b9-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bb7b9-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="bb7b9-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bb7b9-124">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bb7b9-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bb7b9-125">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bb7b9-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





