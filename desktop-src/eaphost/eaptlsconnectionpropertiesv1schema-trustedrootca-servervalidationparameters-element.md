---
title: Élément TrustedRootCA (ServerValidationParameters)-connexion
description: Capture le curseur de l’impression des autorités de certification racines approuvées par le client. | Élément TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106522401"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="94ad1-105">Élément TrustedRootCA (ServerValidationParameters) pour les propriétés de connexion</span><span class="sxs-lookup"><span data-stu-id="94ad1-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="94ad1-106">L’élément **TrustedRootCA (ServerValidationParameters)** capture l’impression Thumb des autorités de certification racines approuvées par le client.</span><span class="sxs-lookup"><span data-stu-id="94ad1-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="94ad1-107">L’élément **TrustedRootCA** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="94ad1-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="94ad1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="94ad1-108">Remarks</span></span>

<span data-ttu-id="94ad1-109">Le curseur d’impression est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.</span><span class="sxs-lookup"><span data-stu-id="94ad1-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="94ad1-110">L’élément **TrustedRootCA** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="94ad1-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ad1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94ad1-111">Requirements</span></span>



| <span data-ttu-id="94ad1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94ad1-112">Requirement</span></span> | <span data-ttu-id="94ad1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="94ad1-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94ad1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94ad1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="94ad1-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ad1-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94ad1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94ad1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="94ad1-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ad1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94ad1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94ad1-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="94ad1-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="94ad1-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="94ad1-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="94ad1-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="94ad1-121">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="94ad1-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="94ad1-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="94ad1-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="94ad1-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="94ad1-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="94ad1-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="94ad1-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="94ad1-125">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="94ad1-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="94ad1-126">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="94ad1-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





