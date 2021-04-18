---
description: Le \_ \_ type d’énumération des modes de capture wpd décrit le mode de temporisation de capture d’une capture d’image continue.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Énumération WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533009"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="f4811-103">\_Énumération des modes de capture wpd \_</span><span class="sxs-lookup"><span data-stu-id="f4811-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="f4811-104">Le type d’énumération des **\_ \_ modes de capture wpd** décrit le mode de temporisation de capture d’une capture d’image continue.</span><span class="sxs-lookup"><span data-stu-id="f4811-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4811-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4811-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="f4811-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f4811-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4811-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_mode de capture wpd \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="f4811-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="f4811-108">Le mode de capture n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="f4811-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="f4811-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_mode de capture wpd \_ \_ normal**</span><span class="sxs-lookup"><span data-stu-id="f4811-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="f4811-110">Aucun mode de délai ou de rafale ne doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="f4811-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f4811-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_ \_ rafale en mode de capture wpd \_**</span><span class="sxs-lookup"><span data-stu-id="f4811-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="f4811-112">Spécifie qu’un nombre défini d’images doit être capturé avec un intervalle défini entre eux.</span><span class="sxs-lookup"><span data-stu-id="f4811-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="f4811-113">Le nombre d’images à capturer et le délai entre elles sont spécifiés par les propriétés de l’intervalle de [ \_ \_ \_ rafales \_ d’images fixes wpd](still-image-properties.md) et de l' [ \_ \_ \_ \_ intervalle de rafales d’images fixes](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f4811-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="f4811-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_mode de capture wpd \_ \_ TIMELAPSE**</span><span class="sxs-lookup"><span data-stu-id="f4811-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="f4811-115">La capture d’images doit utiliser la photographie temporelle.</span><span class="sxs-lookup"><span data-stu-id="f4811-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="f4811-116">Le nombre d’images et l’intervalle entre eux sont décrits par les propriétés de l' [ \_ image wpd toujours \_ image \_ TIMELAPSE \_ Number](still-image-properties.md) et [wpd \_ Still \_ image \_ TIMELAPSE \_ Interval](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f4811-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4811-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f4811-117">Remarks</span></span>

<span data-ttu-id="f4811-118">Cette énumération est utilisée par la propriété du [ \_ mode de \_ \_ capture \_ d’image](still-image-properties.md) de l’wpd.</span><span class="sxs-lookup"><span data-stu-id="f4811-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4811-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4811-119">Requirements</span></span>



| <span data-ttu-id="f4811-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4811-120">Requirement</span></span> | <span data-ttu-id="f4811-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4811-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4811-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4811-122">Header</span></span><br/> | <dl> <span data-ttu-id="f4811-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4811-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4811-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4811-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4811-125">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="f4811-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4811-126">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="f4811-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




