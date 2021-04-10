---
title: Élément EnableQuarantineChecks (EapType)
description: En savoir plus sur l’élément EnableQuarantineChecks (EapType). Cet élément indique s’il faut effectuer des vérifications de la protection d’accès réseau (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Élément EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941383"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="dc478-105">Élément EnableQuarantineChecks (EapType)</span><span class="sxs-lookup"><span data-stu-id="dc478-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="dc478-106">L’élément **EnableQuarantineChecks (EapType)** indique s’il faut effectuer des vérifications de la protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="dc478-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="dc478-107">L’élément **EnableQuarantineChecks** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dc478-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc478-108">Notes</span><span class="sxs-lookup"><span data-stu-id="dc478-108">Remarks</span></span>

<span data-ttu-id="dc478-109">Si l’élément **EnableQuarantineChecks** a la valeur true, PEAP effectue des vérifications NAP. Si la valeur est FALSe, PEAP n’effectue pas de vérifications NAP.</span><span class="sxs-lookup"><span data-stu-id="dc478-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="dc478-110">L’élément **EnableQuarantineChecks** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="dc478-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc478-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc478-111">Requirements</span></span>



| <span data-ttu-id="dc478-112">Role</span><span class="sxs-lookup"><span data-stu-id="dc478-112">Role</span></span> | <span data-ttu-id="dc478-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="dc478-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="dc478-114">Client</span><span class="sxs-lookup"><span data-stu-id="dc478-114">Client</span></span><br/> | <span data-ttu-id="dc478-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc478-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc478-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="dc478-116">Server</span></span><br/> | <span data-ttu-id="dc478-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc478-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc478-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc478-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc478-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="dc478-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dc478-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="dc478-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="dc478-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="dc478-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dc478-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="dc478-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="dc478-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="dc478-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="dc478-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="dc478-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="dc478-125">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="dc478-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="dc478-126">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="dc478-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





