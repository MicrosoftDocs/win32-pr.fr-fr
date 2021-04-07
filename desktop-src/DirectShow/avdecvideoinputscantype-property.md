---
description: Spécifie la façon dont le flux vidéo décodé est entrelacé.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propriété AVDecVideoInputScanType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846550"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="f0b42-103">Propriété AVDecVideoInputScanType</span><span class="sxs-lookup"><span data-stu-id="f0b42-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="f0b42-104">Spécifie la façon dont le flux vidéo décodé est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="f0b42-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="f0b42-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f0b42-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0b42-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="f0b42-106">Data type</span></span>

<span data-ttu-id="f0b42-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="f0b42-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f0b42-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="f0b42-108">Property GUID</span></span>

<span data-ttu-id="f0b42-109">**CODECAPI \_ AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="f0b42-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="f0b42-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f0b42-110">Property value</span></span>

<span data-ttu-id="f0b42-111">La valeur de cette propriété est un membre de l’énumération [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .</span><span class="sxs-lookup"><span data-stu-id="f0b42-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b42-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f0b42-112">Remarks</span></span>

<span data-ttu-id="f0b42-113">Les 16 bits supérieurs de la valeur contiennent la largeur, tandis que les 16 bits inférieurs contiennent la hauteur.</span><span class="sxs-lookup"><span data-stu-id="f0b42-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b42-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0b42-114">Requirements</span></span>



| <span data-ttu-id="f0b42-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0b42-115">Requirement</span></span> | <span data-ttu-id="f0b42-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0b42-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b42-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0b42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b42-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f0b42-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f0b42-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0b42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b42-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f0b42-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f0b42-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0b42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b42-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b42-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b42-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b42-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="f0b42-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f0b42-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f0b42-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

