---
title: TrustedRootCA (ServerValidationParameters), élément (v1)
description: Capture l’impression Thumb des autorités de certification racines approuvées par le client. | Élément TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- Élément TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106525699"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="5dd7d-105">Élément TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="5dd7d-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="5dd7d-106">L’élément **TrustedRootCA (ServerValidationParameters)** capture l’impression Thumb des autorités de certification (ca) racine approuvées par le client.</span><span class="sxs-lookup"><span data-stu-id="5dd7d-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="5dd7d-107">L’élément **TrustedRootCA** est défini par le type complexe [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd7d-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd7d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5dd7d-108">Remarks</span></span>

<span data-ttu-id="5dd7d-109">Le curseur d’impression est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.</span><span class="sxs-lookup"><span data-stu-id="5dd7d-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="5dd7d-110">L’élément **TrustedRootCA** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5dd7d-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd7d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dd7d-111">Requirements</span></span>



| <span data-ttu-id="5dd7d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dd7d-112">Requirement</span></span> | <span data-ttu-id="5dd7d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dd7d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5dd7d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dd7d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd7d-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dd7d-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5dd7d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dd7d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd7d-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dd7d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5dd7d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dd7d-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dd7d-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="5dd7d-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5dd7d-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="5dd7d-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="5dd7d-121">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="5dd7d-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5dd7d-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="5dd7d-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="5dd7d-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5dd7d-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5dd7d-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="5dd7d-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5dd7d-125">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5dd7d-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5dd7d-126">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5dd7d-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





