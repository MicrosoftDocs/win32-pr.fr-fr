---
title: Élément ServerNames (ServerValidationParameters) (TLS)
description: En savoir plus sur l’élément ServerNames (ServerValidationParameters). Cet élément représente une liste de noms de serveurs délimités par des points-virgules. | Élément ServerNames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Élément ServerNames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523155"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="d866c-106">Élément ServerNames (ServerValidationParameters) (TLS)</span><span class="sxs-lookup"><span data-stu-id="d866c-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="d866c-107">L’élément **serverNames (ServerValidationParameters)** représente une liste de noms de serveurs délimités par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="d866c-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="d866c-108">L’élément **serverNames** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d866c-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d866c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d866c-109">Remarks</span></span>

<span data-ttu-id="d866c-110">Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="d866c-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="d866c-111">L’élément **serverNames** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d866c-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d866c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d866c-112">Requirements</span></span>



| <span data-ttu-id="d866c-113">Role</span><span class="sxs-lookup"><span data-stu-id="d866c-113">Role</span></span> | <span data-ttu-id="d866c-114">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="d866c-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d866c-115">Client</span><span class="sxs-lookup"><span data-stu-id="d866c-115">Client</span></span><br/> | <span data-ttu-id="d866c-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d866c-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d866c-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="d866c-117">Server</span></span><br/> | <span data-ttu-id="d866c-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d866c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d866c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d866c-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d866c-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="d866c-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d866c-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="d866c-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="d866c-122">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="d866c-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d866c-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="d866c-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="d866c-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d866c-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d866c-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="d866c-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d866c-126">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d866c-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d866c-127">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d866c-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





