---
title: PerformServerValidation (PeapExtensionsType), élément (schéma v2)
description: En savoir plus sur l’élément PerformServerValidation (PeapExtensionsType). Cet élément indique si la validation du serveur est effectuée. | PerformServerValidation (PeapExtensionsType), élément (schéma v2)
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- Élément PerformServerValidation EAPHost
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
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211549"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a><span data-ttu-id="ec1be-106">PerformServerValidation (PeapExtensionsType), élément (schéma v2)</span><span class="sxs-lookup"><span data-stu-id="ec1be-106">PerformServerValidation (PeapExtensionsType) Element (V2 schema)</span></span>

<span data-ttu-id="ec1be-107">L’élément **PerformServerValidation (PeapExtensionsType)** indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="ec1be-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="ec1be-108">L’élément **PerformServerValidation** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ec1be-108">The **PerformServerValidation** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1be-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ec1be-109">Remarks</span></span>

<span data-ttu-id="ec1be-110">L’élément **PerformServerValidation** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ec1be-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1be-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec1be-111">Requirements</span></span>



| <span data-ttu-id="ec1be-112">Role</span><span class="sxs-lookup"><span data-stu-id="ec1be-112">Role</span></span> | <span data-ttu-id="ec1be-113">Version minimale du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ec1be-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="ec1be-114">Client</span><span class="sxs-lookup"><span data-stu-id="ec1be-114">Client</span></span><br/> | <span data-ttu-id="ec1be-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec1be-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ec1be-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="ec1be-116">Server</span></span><br/> | <span data-ttu-id="ec1be-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec1be-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec1be-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec1be-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec1be-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ec1be-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ec1be-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="ec1be-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="ec1be-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ec1be-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ec1be-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="ec1be-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="ec1be-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ec1be-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ec1be-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="ec1be-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ec1be-125">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="ec1be-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ec1be-126">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="ec1be-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





