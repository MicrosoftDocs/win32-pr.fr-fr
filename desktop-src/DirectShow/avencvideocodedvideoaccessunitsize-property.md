---
description: Spécifie la taille des unités d’accès vidéo, en octets. Cette propriété s’applique uniquement aux modes de contrôle VBR (variable bit rate).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propriété AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949980"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="21a5e-104">Propriété AVEncVideoCodedVideoAccessUnitSize</span><span class="sxs-lookup"><span data-stu-id="21a5e-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="21a5e-105">Spécifie la taille des unités d’accès vidéo, en octets.</span><span class="sxs-lookup"><span data-stu-id="21a5e-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="21a5e-106">Cette propriété s’applique uniquement aux modes de contrôle VBR (variable bit rate).</span><span class="sxs-lookup"><span data-stu-id="21a5e-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="21a5e-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="21a5e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="21a5e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="21a5e-108">Data type</span></span>

<span data-ttu-id="21a5e-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="21a5e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="21a5e-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="21a5e-110">Property GUID</span></span>

<span data-ttu-id="21a5e-111">**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**</span><span class="sxs-lookup"><span data-stu-id="21a5e-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="21a5e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="21a5e-112">Property value</span></span>

<span data-ttu-id="21a5e-113">Cette propriété est retournée sous la forme d’une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="21a5e-113">This property is returned as a range of values.</span></span> <span data-ttu-id="21a5e-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="21a5e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="21a5e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21a5e-115">Requirements</span></span>



| <span data-ttu-id="21a5e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21a5e-116">Requirement</span></span> | <span data-ttu-id="21a5e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="21a5e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21a5e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21a5e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21a5e-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="21a5e-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="21a5e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21a5e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21a5e-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="21a5e-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="21a5e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="21a5e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21a5e-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="21a5e-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a5e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21a5e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a5e-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="21a5e-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="21a5e-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="21a5e-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




