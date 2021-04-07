---
description: Définit le seuil auquel l’encodeur considère un champ vidéo redondant.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriété AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745660"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="67f81-103">Propriété AVEncVideoInverseTelecineThreshold</span><span class="sxs-lookup"><span data-stu-id="67f81-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="67f81-104">Définit le seuil auquel l’encodeur considère un champ vidéo redondant.</span><span class="sxs-lookup"><span data-stu-id="67f81-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="67f81-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="67f81-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="67f81-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="67f81-106">Data type</span></span>

<span data-ttu-id="67f81-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="67f81-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="67f81-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="67f81-108">Property GUID</span></span>

<span data-ttu-id="67f81-109">**CODECAPI \_ AVEncVideoInverseTelecineThreshold**</span><span class="sxs-lookup"><span data-stu-id="67f81-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="67f81-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="67f81-110">Property value</span></span>

<span data-ttu-id="67f81-111">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="67f81-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="67f81-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f81-112">Value</span></span> | <span data-ttu-id="67f81-113">Description</span><span class="sxs-lookup"><span data-stu-id="67f81-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="67f81-114">0</span><span class="sxs-lookup"><span data-stu-id="67f81-114">0</span></span>     | <span data-ttu-id="67f81-115">L’encodeur est moins susceptible de considérer les champs vidéo comme redondants.</span><span class="sxs-lookup"><span data-stu-id="67f81-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="67f81-116">100</span><span class="sxs-lookup"><span data-stu-id="67f81-116">100</span></span>   | <span data-ttu-id="67f81-117">L’encodeur est plus susceptible de considérer les champs vidéo comme redondants.</span><span class="sxs-lookup"><span data-stu-id="67f81-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="67f81-118">Notes</span><span class="sxs-lookup"><span data-stu-id="67f81-118">Remarks</span></span>

<span data-ttu-id="67f81-119">Définissez cette propriété si l’encodeur effectue un télécinéma inverse avec une source vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="67f81-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f81-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67f81-120">Requirements</span></span>



| <span data-ttu-id="67f81-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67f81-121">Requirement</span></span> | <span data-ttu-id="67f81-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f81-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67f81-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f81-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67f81-124">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="67f81-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="67f81-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f81-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67f81-126">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="67f81-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="67f81-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="67f81-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f81-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67f81-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67f81-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67f81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f81-130">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="67f81-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="67f81-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="67f81-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




