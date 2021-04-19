---
title: PerformServerValidation (PeapExtensionsType), élément (schéma v1)
description: En savoir plus sur l’élément PerformServerValidation (PeapExtensionsType). Cet élément indique si la validation du serveur est effectuée. | PerformServerValidation (PeapExtensionsType), élément (schéma v1)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539819"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="af579-106">PerformServerValidation (PeapExtensionsType), élément (schéma v1)</span><span class="sxs-lookup"><span data-stu-id="af579-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="af579-107">L’élément **PerformServerValidation (PeapExtensionsType)** indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="af579-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="af579-108">L’élément est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="af579-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="af579-109">Notes</span><span class="sxs-lookup"><span data-stu-id="af579-109">Remarks</span></span>

<span data-ttu-id="af579-110">L’élément **PerformServerValidation** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="af579-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="af579-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af579-111">Requirements</span></span>



| <span data-ttu-id="af579-112">Role</span><span class="sxs-lookup"><span data-stu-id="af579-112">Role</span></span> | <span data-ttu-id="af579-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="af579-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="af579-114">Client</span><span class="sxs-lookup"><span data-stu-id="af579-114">Client</span></span><br/> | <span data-ttu-id="af579-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af579-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="af579-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="af579-116">Server</span></span><br/> | <span data-ttu-id="af579-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af579-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af579-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af579-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="af579-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="af579-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="af579-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="af579-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="af579-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="af579-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="af579-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="af579-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="af579-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="af579-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="af579-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="af579-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="af579-125">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="af579-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="af579-126">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="af579-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="af579-127">**PerformServerValidation(PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="af579-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





