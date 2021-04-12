---
title: AcceptServerName
description: Indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément ServerNames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211512"
---
# <a name="acceptservername"></a><span data-ttu-id="6ad3d-105">AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="6ad3d-105">AcceptServerName</span></span>

<span data-ttu-id="6ad3d-106">L’élément **AcceptServerName (EapType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad3d-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="6ad3d-107">L’élément est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad3d-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad3d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6ad3d-108">Remarks</span></span>

<span data-ttu-id="6ad3d-109">L’élément **AcceptServerName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6ad3d-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad3d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ad3d-110">Requirements</span></span>



| <span data-ttu-id="6ad3d-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ad3d-111">Requirement</span></span> | <span data-ttu-id="6ad3d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ad3d-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6ad3d-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad3d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad3d-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ad3d-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6ad3d-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad3d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad3d-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ad3d-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ad3d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad3d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ad3d-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6ad3d-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6ad3d-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6ad3d-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="6ad3d-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6ad3d-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6ad3d-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6ad3d-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="6ad3d-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6ad3d-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6ad3d-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="6ad3d-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6ad3d-124">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6ad3d-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6ad3d-125">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6ad3d-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6ad3d-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="6ad3d-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





