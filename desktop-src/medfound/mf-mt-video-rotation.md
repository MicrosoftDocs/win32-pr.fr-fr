---
description: Spécifie la rotation d’une image vidéo dans le sens des aiguilles d’une montre.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Attribut MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868937"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="3b3cb-103">Attribut de rotation de la \_ vidéo MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b3cb-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="3b3cb-104">Spécifie la rotation d’une image vidéo dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="3b3cb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3b3cb-105">Data type</span></span>

<span data-ttu-id="3b3cb-106">**MFVideoRotationFormat** stocké en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b3cb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3b3cb-107">Remarks</span></span>

<span data-ttu-id="3b3cb-108">La vidéo à partir d’un périphérique de poche, tel qu’un téléphone mobile, est souvent pivotée par 90, 180 ou 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="3b3cb-109">Si l’appareil photo stocke l’orientation en tant que métadonnées dans le fichier vidéo, l’image peut être ajustée au moment de la lecture.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="3b3cb-110">Si cet attribut a la valeur **MFVideoRotationFormat \_ 90**, cela signifie que le contenu a été pivoté de 90 degrés dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="3b3cb-111">Si le contenu a pivoté de 90 degrés dans le sens des aiguilles d’une montre, la valeur de l’attribut serait **MFVideoRotationFormat \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="3b3cb-112">Les valeurs prises en charge pour cet attribut sont énumérées dans [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span><span class="sxs-lookup"><span data-stu-id="3b3cb-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="3b3cb-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b3cb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b3cb-114">Requirements</span></span>



| <span data-ttu-id="3b3cb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b3cb-115">Requirement</span></span> | <span data-ttu-id="3b3cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b3cb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3cb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b3cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3b3cb-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3b3cb-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3b3cb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b3cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3b3cb-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="3b3cb-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3b3cb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b3cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b3cb-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b3cb-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b3cb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b3cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b3cb-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b3cb-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3b3cb-125">Types de médias</span><span class="sxs-lookup"><span data-stu-id="3b3cb-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




