---
description: Le \_ \_ type d’énumération des modes flash wpd décrit un mode flash à utiliser lors de la capture d’images avec un appareil.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Énumération WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536026"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="cccfa-103">\_ \_ Énumération des modes flash wpd</span><span class="sxs-lookup"><span data-stu-id="cccfa-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="cccfa-104">Le type d’énumération des **\_ \_ modes flash wpd** décrit un mode flash à utiliser lors de la capture d’images avec un appareil.</span><span class="sxs-lookup"><span data-stu-id="cccfa-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cccfa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cccfa-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="cccfa-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cccfa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cccfa-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_mode flash \_ wpd \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="cccfa-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-108">Aucun mode flash n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="cccfa-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_mode flash \_ wpd \_ automatique**</span><span class="sxs-lookup"><span data-stu-id="cccfa-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-110">Spécifie que le flash doit être utilisé en mode automatique, comme spécifié par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cccfa-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_mode flash \_ wpd \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="cccfa-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-112">Spécifie qu’aucun flash ne doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cccfa-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_remplissage du \_ mode \_ Flash wpd**</span><span class="sxs-lookup"><span data-stu-id="cccfa-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-114">Spécifie un flash de type de remplissage.</span><span class="sxs-lookup"><span data-stu-id="cccfa-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_mode flash wpd- \_ \_ \_ yeux rouges \_ auto**</span><span class="sxs-lookup"><span data-stu-id="cccfa-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-116">Spécifie que le flash de réduction des yeux rouges doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cccfa-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_ \_ couleur rouge du mode flash \_ \_ wpd \_**</span><span class="sxs-lookup"><span data-stu-id="cccfa-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-118">Spécifie que le flash de remplissage des yeux rouges doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cccfa-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cccfa-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ synchronisation externe en mode flash \_ wpd \_**</span><span class="sxs-lookup"><span data-stu-id="cccfa-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="cccfa-120">Spécifie que le flash doit être synchronisé avec d’autres périphériques flash externes.</span><span class="sxs-lookup"><span data-stu-id="cccfa-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cccfa-121">Notes</span><span class="sxs-lookup"><span data-stu-id="cccfa-121">Remarks</span></span>

<span data-ttu-id="cccfa-122">Cette énumération est utilisée par la propriété du [ \_ \_ \_ \_ mode flash de l’image wpd](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="cccfa-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cccfa-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cccfa-123">Requirements</span></span>



| <span data-ttu-id="cccfa-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cccfa-124">Requirement</span></span> | <span data-ttu-id="cccfa-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cccfa-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cccfa-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cccfa-126">Header</span></span><br/> | <dl> <span data-ttu-id="cccfa-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cccfa-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cccfa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cccfa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cccfa-129">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="cccfa-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




