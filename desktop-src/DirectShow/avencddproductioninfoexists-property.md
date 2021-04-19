---
description: Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propriété AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514505"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="bdb54-104">Propriété AVEncDDProductionInfoExists</span><span class="sxs-lookup"><span data-stu-id="bdb54-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="bdb54-105">Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="bdb54-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="bdb54-106">Cette propriété s’applique aux encodeurs audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="bdb54-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="bdb54-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bdb54-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bdb54-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="bdb54-108">Data type</span></span>

<span data-ttu-id="bdb54-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="bdb54-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bdb54-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="bdb54-110">Property GUID</span></span>

<span data-ttu-id="bdb54-111">**CODECAPI \_ AVEncDDProductionInfoExists**</span><span class="sxs-lookup"><span data-stu-id="bdb54-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb54-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb54-112">Remarks</span></span>

<span data-ttu-id="bdb54-113">Si la valeur est **\_ true**, le niveau de mélange et les paramètres de type d’espace sont valides.</span><span class="sxs-lookup"><span data-stu-id="bdb54-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="bdb54-114">Spécifiez ces paramètres avec les propriétés [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) et [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb54-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb54-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdb54-115">Requirements</span></span>



| <span data-ttu-id="bdb54-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdb54-116">Requirement</span></span> | <span data-ttu-id="bdb54-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb54-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdb54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb54-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bdb54-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bdb54-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdb54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb54-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bdb54-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bdb54-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdb54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb54-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb54-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb54-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb54-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb54-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="bdb54-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bdb54-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bdb54-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




