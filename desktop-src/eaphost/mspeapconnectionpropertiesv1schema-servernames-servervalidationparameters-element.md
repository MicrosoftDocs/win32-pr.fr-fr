---
title: ServerNames (ServerValidationParameters), élément (PEAP)
description: En savoir plus sur l’élément ServerNames (ServerValidationParameters). Cet élément représente une liste de noms de serveurs délimités par des points-virgules. | ServerNames (ServerValidationParameters), élément (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522527"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="bf0de-106">ServerNames (ServerValidationParameters), élément (PEAP)</span><span class="sxs-lookup"><span data-stu-id="bf0de-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="bf0de-107">L’élément **serverNames (ServerValidationParameters)** représente une liste de noms de serveurs délimités par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="bf0de-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="bf0de-108">L’élément **serverNames** est défini par le type complexe [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bf0de-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0de-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bf0de-109">Remarks</span></span>

<span data-ttu-id="bf0de-110">Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="bf0de-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="bf0de-111">L’élément **serverNames** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bf0de-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0de-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf0de-112">Requirements</span></span>



| <span data-ttu-id="bf0de-113">Role</span><span class="sxs-lookup"><span data-stu-id="bf0de-113">Role</span></span> | <span data-ttu-id="bf0de-114">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="bf0de-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="bf0de-115">Client</span><span class="sxs-lookup"><span data-stu-id="bf0de-115">Client</span></span><br/> | <span data-ttu-id="bf0de-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0de-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf0de-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="bf0de-117">Server</span></span><br/> | <span data-ttu-id="bf0de-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0de-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf0de-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf0de-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf0de-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bf0de-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bf0de-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="bf0de-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="bf0de-122">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bf0de-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bf0de-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="bf0de-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="bf0de-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf0de-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bf0de-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="bf0de-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bf0de-126">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bf0de-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bf0de-127">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bf0de-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





