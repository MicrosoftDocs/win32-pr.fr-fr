---
title: Élément FastReconnect (EapType)
description: En savoir plus sur l’élément FastReconnect (EapType). Cet élément indique s’il faut effectuer une reconnexion rapide.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Élément FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513554"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="60936-105">Élément FastReconnect (EapType)</span><span class="sxs-lookup"><span data-stu-id="60936-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="60936-106">L’élément **FastReconnect (EapType)** indique s’il faut effectuer une reconnexion rapide.</span><span class="sxs-lookup"><span data-stu-id="60936-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="60936-107">L’élément **FastReconnect** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="60936-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="60936-108">Notes</span><span class="sxs-lookup"><span data-stu-id="60936-108">Remarks</span></span>

<span data-ttu-id="60936-109">Si l’élément **FastReconnect** a la valeur true, PEAP tente d’effectuer une reconnexion rapide ; Si la valeur est FALSe, PEAP effectue l’authentification complète.</span><span class="sxs-lookup"><span data-stu-id="60936-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="60936-110">L’élément **FastReconnect** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="60936-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="60936-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60936-111">Requirements</span></span>



| <span data-ttu-id="60936-112">Role</span><span class="sxs-lookup"><span data-stu-id="60936-112">Role</span></span> | <span data-ttu-id="60936-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="60936-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="60936-114">Client</span><span class="sxs-lookup"><span data-stu-id="60936-114">Client</span></span><br/> | <span data-ttu-id="60936-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60936-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60936-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="60936-116">Server</span></span><br/> | <span data-ttu-id="60936-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60936-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60936-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60936-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="60936-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="60936-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="60936-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="60936-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="60936-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="60936-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="60936-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="60936-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="60936-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="60936-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="60936-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="60936-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="60936-125">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="60936-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="60936-126">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="60936-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





