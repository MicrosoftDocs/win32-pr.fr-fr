---
title: Élément InnerEapOptional (EapType)
description: En savoir plus sur l’élément InnerEapOptional (EapType). Cet élément indique s’il faut effectuer l’accès invité.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Élément InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102333"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="bb4f1-105">Élément InnerEapOptional (EapType)</span><span class="sxs-lookup"><span data-stu-id="bb4f1-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="bb4f1-106">L’élément **InnerEapOptional (EapType)** indique s’il faut effectuer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="bb4f1-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="bb4f1-107">L’élément **InnerEapOptional** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4f1-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb4f1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="bb4f1-108">Remarks</span></span>

<span data-ttu-id="bb4f1-109">Si l’élément **InnerEapOptional** a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent et décrire la méthode interne et sa configuration. Si la valeur est FALSe, PEAP effectue un accès invité.</span><span class="sxs-lookup"><span data-stu-id="bb4f1-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="bb4f1-110">L’élément **InnerEapOptional** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bb4f1-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4f1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb4f1-111">Requirements</span></span>



| <span data-ttu-id="bb4f1-112">Role</span><span class="sxs-lookup"><span data-stu-id="bb4f1-112">Role</span></span> | <span data-ttu-id="bb4f1-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="bb4f1-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="bb4f1-114">Client</span><span class="sxs-lookup"><span data-stu-id="bb4f1-114">Client</span></span><br/> | <span data-ttu-id="bb4f1-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb4f1-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb4f1-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="bb4f1-116">Server</span></span><br/> | <span data-ttu-id="bb4f1-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb4f1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb4f1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb4f1-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb4f1-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bb4f1-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb4f1-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="bb4f1-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="bb4f1-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bb4f1-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb4f1-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="bb4f1-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="bb4f1-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bb4f1-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bb4f1-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="bb4f1-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bb4f1-125">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bb4f1-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bb4f1-126">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bb4f1-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





