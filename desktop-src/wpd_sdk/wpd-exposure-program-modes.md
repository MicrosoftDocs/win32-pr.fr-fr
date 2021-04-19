---
description: Le \_ \_ type d’énumération des modes de programme d’exposition wpd \_ décrit un mode d’exposition à utiliser lors de la capture d’images avec un appareil.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Énumération WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545514"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="03376-103">\_ \_ Énumération des modes du programme d’exposition wpd \_</span><span class="sxs-lookup"><span data-stu-id="03376-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="03376-104">Le type d’énumération des **\_ modes de \_ programme \_ d’exposition wpd** décrit un mode d’exposition à utiliser lors de la capture d’images avec un appareil.</span><span class="sxs-lookup"><span data-stu-id="03376-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="03376-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03376-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="03376-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="03376-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="03376-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_mode de programme d’exposition wpd \_ \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="03376-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="03376-108">Le mode d’exposition n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="03376-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="03376-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_Manuel du \_ mode de programme d’exposition wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03376-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="03376-110">L’application doit spécifier tous les paramètres d’exposition.</span><span class="sxs-lookup"><span data-stu-id="03376-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="03376-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_mode de programme d’exposition wpd \_ \_ \_ automatique**</span><span class="sxs-lookup"><span data-stu-id="03376-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="03376-112">Utilisez un mode d’exposition automatique défini par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="03376-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="03376-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**exposition de l' \_ ouverture du mode de programme d’exposition wpd \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03376-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="03376-114">Mode d’exposition automatisé qui indique que la valeur de l’ouverture de l’objectif doit rester fixe, mais la vitesse d’obturation doit être déterminée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="03376-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="03376-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_priorité d' \_ obturation du mode de programme d’exposition wpd \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03376-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="03376-116">Mode d’exposition automatisé qui indique que la vitesse d’obturation doit rester fixe, mais que l’ouverture de l’objectif doit être déterminée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="03376-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="03376-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_ \_ \_ élément créatif du mode de programme exposition wpd \_**</span><span class="sxs-lookup"><span data-stu-id="03376-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="03376-118">Mode d’exposition automatisé qui tente d’optimiser la profondeur du champ.</span><span class="sxs-lookup"><span data-stu-id="03376-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="03376-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_action du \_ mode de programme d’exposition wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03376-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="03376-120">Mode d’exposition automatisé qui tente d’optimiser la vitesse d’obturation.</span><span class="sxs-lookup"><span data-stu-id="03376-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="03376-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_mode de \_ programme exposition wpd \_ \_ portrait**</span><span class="sxs-lookup"><span data-stu-id="03376-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="03376-122">Mode d’exposition automatisé qui spécifie une profondeur relativement faible de champ.</span><span class="sxs-lookup"><span data-stu-id="03376-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03376-123">Notes</span><span class="sxs-lookup"><span data-stu-id="03376-123">Remarks</span></span>

<span data-ttu-id="03376-124">Indique le mode de programme d’exposition de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="03376-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="03376-125">Cette énumération est utilisée par la propriété du [mode de programme d' \_ \_ exposition d’image \_ \_ \_ toujours wpd](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="03376-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="03376-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03376-126">Requirements</span></span>



| <span data-ttu-id="03376-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03376-127">Requirement</span></span> | <span data-ttu-id="03376-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="03376-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="03376-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="03376-129">Header</span></span><br/> | <dl> <span data-ttu-id="03376-130"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="03376-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03376-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03376-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03376-132">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="03376-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




