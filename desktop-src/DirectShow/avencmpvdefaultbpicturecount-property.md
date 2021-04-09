---
description: Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propriété AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033521"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="71b00-103">Propriété AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="71b00-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="71b00-104">Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.</span><span class="sxs-lookup"><span data-stu-id="71b00-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="71b00-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="71b00-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="71b00-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="71b00-106">Data type</span></span>

<span data-ttu-id="71b00-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="71b00-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="71b00-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="71b00-108">Property GUID</span></span>

<span data-ttu-id="71b00-109">**CODECAPI \_ AVEncMPVDefaultBPictureCount**</span><span class="sxs-lookup"><span data-stu-id="71b00-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="71b00-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="71b00-110">Property value</span></span>

<span data-ttu-id="71b00-111">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="71b00-111">This property has a linear range of values.</span></span> <span data-ttu-id="71b00-112">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="71b00-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="71b00-113">Notes</span><span class="sxs-lookup"><span data-stu-id="71b00-113">Remarks</span></span>

<span data-ttu-id="71b00-114">Avant Windows 8, cette propriété s’applique aux encodeurs vidéo MPEG.</span><span class="sxs-lookup"><span data-stu-id="71b00-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="71b00-115">À compter de Windows 8, cette propriété est utilisée par les encodeurs vidéo MPEG, WMV et H. 264.</span><span class="sxs-lookup"><span data-stu-id="71b00-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="71b00-116">Si l’encodeur prend en charge cette propriété, il peut être utilisé pour contrôler la structure du groupe d’images (GOP).</span><span class="sxs-lookup"><span data-stu-id="71b00-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b00-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71b00-117">Requirements</span></span>



| <span data-ttu-id="71b00-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71b00-118">Requirement</span></span> | <span data-ttu-id="71b00-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="71b00-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b00-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71b00-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71b00-121">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="71b00-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="71b00-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71b00-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71b00-123">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="71b00-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="71b00-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="71b00-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b00-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b00-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b00-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b00-127">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="71b00-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="71b00-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="71b00-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




