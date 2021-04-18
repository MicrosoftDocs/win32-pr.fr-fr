---
description: Récupère les mesures de qualité sur l’annulation de l’écho acoustique (AEC) à partir du DSP de capture vocal.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533616"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="8176e-103">\_Propriété des \_ mesures de qualité MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="8176e-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="8176e-104">Récupère les mesures de qualité sur l’annulation de l’écho acoustique (AEC) à partir du DSP de capture vocal.</span><span class="sxs-lookup"><span data-stu-id="8176e-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8176e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8176e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8176e-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8176e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8176e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="8176e-107">Data Type</span></span>

<span data-ttu-id="8176e-108">\_objet BLOB VT</span><span class="sxs-lookup"><span data-stu-id="8176e-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="8176e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8176e-109">Remarks</span></span>

<span data-ttu-id="8176e-110">La valeur de cette propriété est une structure de [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) .</span><span class="sxs-lookup"><span data-stu-id="8176e-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="8176e-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8176e-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="8176e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8176e-112">Requirements</span></span>



| <span data-ttu-id="8176e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8176e-113">Requirement</span></span> | <span data-ttu-id="8176e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8176e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8176e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8176e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8176e-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8176e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8176e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8176e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8176e-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8176e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8176e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8176e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8176e-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8176e-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8176e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8176e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8176e-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8176e-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8176e-123">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="8176e-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
