---
description: Le \_ \_ \_ type d’énumération des modes d’exposition wpd permet de décrire le mode de contrôle à utiliser lors de l’estimation de l’exposition pour la capture d’image continue par un appareil.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Énumération WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541287"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="21062-103">\_ \_ Énumération des modes de contrôle d’exposition wpd \_</span><span class="sxs-lookup"><span data-stu-id="21062-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="21062-104">Le type d’énumération des **\_ \_ \_ modes d’exposition wpd** permet de décrire le mode de contrôle à utiliser lors de l’estimation de l’exposition pour la capture d’image continue par un appareil.</span><span class="sxs-lookup"><span data-stu-id="21062-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="21062-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21062-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="21062-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="21062-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="21062-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_mode de contrôle d’exposition wpd \_ \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="21062-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="21062-108">Le mode de contrôle n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="21062-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="21062-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_moyenne du \_ mode de contrôle d’exposition wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21062-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="21062-110">Utilisez l’exposition moyenne sur l’intégralité de l’image.</span><span class="sxs-lookup"><span data-stu-id="21062-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="21062-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**Centre du mode de contrôle d’exposition WPD- \_ \_ \_ \_ \_ moyenne pondérée \_**</span><span class="sxs-lookup"><span data-stu-id="21062-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="21062-112">Utilisez une exposition moyenne, le centre de l’image étant donné un poids plus grand.</span><span class="sxs-lookup"><span data-stu-id="21062-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="21062-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODE de contrôle d’exposition WPD à \_ \_ \_ \_ plusieurs \_ points**</span><span class="sxs-lookup"><span data-stu-id="21062-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="21062-114">Utilisez une technique de calcul de la moyenne sur plusieurs points.</span><span class="sxs-lookup"><span data-stu-id="21062-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="21062-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**point \_ \_ central du mode de contrôle d’exposition wpd \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21062-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="21062-116">Utilisez une technique de la moyenne à la place.</span><span class="sxs-lookup"><span data-stu-id="21062-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21062-117">Notes</span><span class="sxs-lookup"><span data-stu-id="21062-117">Remarks</span></span>

<span data-ttu-id="21062-118">Indique le mode de mesure de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="21062-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="21062-119">Cette énumération est utilisée par la propriété du mode de mesure de l’exposition de l' [ \_ \_ image \_ \_ \_ wpd continue](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="21062-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21062-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21062-120">Requirements</span></span>



| <span data-ttu-id="21062-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21062-121">Requirement</span></span> | <span data-ttu-id="21062-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="21062-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="21062-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="21062-123">Header</span></span><br/> | <dl> <span data-ttu-id="21062-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="21062-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21062-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21062-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21062-126">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="21062-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




