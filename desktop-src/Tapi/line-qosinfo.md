---
description: Le message QOSINFO de la ligne TSPI \_ force l’interface TAPI à déclencher un événement QoS. Pour plus d’informations, consultez ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Message LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545511"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="f14b5-104">\_Message QOSINFO de ligne</span><span class="sxs-lookup"><span data-stu-id="f14b5-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="f14b5-105">Le message **\_ QOSINFO** de la ligne TSPI force l’interface TAPI à déclencher un événement QoS.</span><span class="sxs-lookup"><span data-stu-id="f14b5-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="f14b5-106">Pour plus d’informations, consultez [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .</span><span class="sxs-lookup"><span data-stu-id="f14b5-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="f14b5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f14b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14b5-108">*htLine*</span><span class="sxs-lookup"><span data-stu-id="f14b5-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-109">Handle TAPI pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="f14b5-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="f14b5-110">*htCall*</span><span class="sxs-lookup"><span data-stu-id="f14b5-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-111">Handle TAPI pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="f14b5-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="f14b5-112">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="f14b5-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-113">La ligne de valeur \_ QOSINFO.</span><span class="sxs-lookup"><span data-stu-id="f14b5-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="f14b5-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f14b5-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-115">Membre de l’énumérateur [**d' \_ événements QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) qui identifie le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="f14b5-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="f14b5-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f14b5-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-117">Constante de [type de média](./tapiprotocol--constants.md) qui identifie le média de l’appel associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="f14b5-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="f14b5-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f14b5-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f14b5-119">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="f14b5-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f14b5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f14b5-120">Requirements</span></span>



| <span data-ttu-id="f14b5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f14b5-121">Requirement</span></span> | <span data-ttu-id="f14b5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14b5-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f14b5-123">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f14b5-123">TAPI version</span></span><br/> | <span data-ttu-id="f14b5-124">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="f14b5-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="f14b5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f14b5-125">Header</span></span><br/>       | <dl> <span data-ttu-id="f14b5-126"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f14b5-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14b5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14b5-128">**\_événement QoS**</span><span class="sxs-lookup"><span data-stu-id="f14b5-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="f14b5-129">**ITQOSEvent**</span><span class="sxs-lookup"><span data-stu-id="f14b5-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

