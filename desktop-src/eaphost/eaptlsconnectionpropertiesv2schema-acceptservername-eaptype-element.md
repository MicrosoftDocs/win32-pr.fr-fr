---
title: Élément AcceptServerName
description: Indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément ServerNames (ServerValidationParameters). | Élément AcceptServerName
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Élément AcceptServerName EAPHost
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539405"
---
# <a name="acceptservername-element"></a><span data-ttu-id="b37bd-105">Élément AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="b37bd-105">AcceptServerName element</span></span>

<span data-ttu-id="b37bd-106">L’élément **AcceptServerName (EapType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b37bd-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="b37bd-107">L’élément **AcceptServerName** est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b37bd-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b37bd-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b37bd-108">Remarks</span></span>

<span data-ttu-id="b37bd-109">L’élément **AcceptServerName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b37bd-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37bd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b37bd-110">Requirements</span></span>



| <span data-ttu-id="b37bd-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b37bd-111">Requirement</span></span> | <span data-ttu-id="b37bd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b37bd-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b37bd-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b37bd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b37bd-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b37bd-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b37bd-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b37bd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b37bd-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b37bd-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b37bd-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b37bd-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="b37bd-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="b37bd-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b37bd-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="b37bd-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="b37bd-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="b37bd-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b37bd-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="b37bd-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="b37bd-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b37bd-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b37bd-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="b37bd-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b37bd-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b37bd-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b37bd-125">Éléments de schéma eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b37bd-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b37bd-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="b37bd-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





