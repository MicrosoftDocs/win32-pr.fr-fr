---
description: Spécifie le niveau d’économie d’énergie d’un décodeur vidéo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propriété AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514092"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="6ed74-103">Propriété AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="6ed74-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="6ed74-104">Spécifie le niveau d’économie d’énergie d’un décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="6ed74-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="6ed74-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6ed74-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ed74-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="6ed74-106">Data type</span></span>

<span data-ttu-id="6ed74-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6ed74-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6ed74-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="6ed74-108">Property GUID</span></span>

<span data-ttu-id="6ed74-109">**CODECAPI \_ AVDecVideoSWPowerLevel**</span><span class="sxs-lookup"><span data-stu-id="6ed74-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="6ed74-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6ed74-110">Property value</span></span>

<span data-ttu-id="6ed74-111">La plage des valeurs possibles est \[ 0.. 100 \] , inclusive, avec la signification suivante.</span><span class="sxs-lookup"><span data-stu-id="6ed74-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="6ed74-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ed74-112">Value</span></span> | <span data-ttu-id="6ed74-113">Description</span><span class="sxs-lookup"><span data-stu-id="6ed74-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="6ed74-114">0</span><span class="sxs-lookup"><span data-stu-id="6ed74-114">0</span></span>     | <span data-ttu-id="6ed74-115">Optimiser la durée de vie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="6ed74-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="6ed74-116">100</span><span class="sxs-lookup"><span data-stu-id="6ed74-116">100</span></span>   | <span data-ttu-id="6ed74-117">Optimisez la qualité vidéo.</span><span class="sxs-lookup"><span data-stu-id="6ed74-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="6ed74-118">L’énumération [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) définit des constantes spécifiques dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="6ed74-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed74-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6ed74-119">Remarks</span></span>

<span data-ttu-id="6ed74-120">Vous pouvez définir cette propriété lors de la lecture pour modifier le niveau d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6ed74-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed74-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ed74-121">Requirements</span></span>



| <span data-ttu-id="6ed74-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ed74-122">Requirement</span></span> | <span data-ttu-id="6ed74-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ed74-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed74-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ed74-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed74-125">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="6ed74-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6ed74-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ed74-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed74-127">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="6ed74-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6ed74-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ed74-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed74-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed74-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed74-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ed74-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed74-131">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="6ed74-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6ed74-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6ed74-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




