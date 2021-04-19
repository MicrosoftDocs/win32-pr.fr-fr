---
description: Le \_ \_ \_ type d’énumération des paramètres de l’équilibre blanc wpd indique comment un appareil vidéo ou d’image poids des canaux de couleur pour obtenir une balance des blancs appropriée.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Énumération WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537472"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="c1b39-103">\_ \_ Énumération des paramètres de l’équilibre blanc wpd \_</span><span class="sxs-lookup"><span data-stu-id="c1b39-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="c1b39-104">Le type d’énumération des paramètres de l' **\_ \_ équilibre \_ blanc wpd** indique comment un appareil vidéo ou d’image poids des canaux de couleur pour obtenir une balance des blancs appropriée.</span><span class="sxs-lookup"><span data-stu-id="c1b39-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1b39-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="c1b39-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c1b39-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1b39-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_équilibre blanc \_ wpd \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="c1b39-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-108">Cette valeur n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="c1b39-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_Manuel d' \_ équilibre des blancs wpd \_**</span><span class="sxs-lookup"><span data-stu-id="c1b39-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-110">L’équilibre des blancs est défini explicitement à l’aide de la propriété d' [ \_ obtention d’image wpd continue \_ image \_ RGB \_ ](still-image-properties.md) et ne change pas par lui-même.</span><span class="sxs-lookup"><span data-stu-id="c1b39-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_équilibrer les blancs wpd \_ \_ automatique**</span><span class="sxs-lookup"><span data-stu-id="c1b39-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-112">L’appareil définit l’équilibre des blancs.</span><span class="sxs-lookup"><span data-stu-id="c1b39-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_équilibrer les blancs wpd sur \_ \_ un \_ Push \_ automatique**</span><span class="sxs-lookup"><span data-stu-id="c1b39-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-114">L’appareil définit l’équilibre des blancs, mais uniquement lorsque l’utilisateur pousse le bouton de capture de l’appareil tout en le recherchant dans un champ blanc.</span><span class="sxs-lookup"><span data-stu-id="c1b39-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**heure d’été de l' \_ équilibre blanc wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1b39-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-116">L’appareil utilise les nombres d’équilibres blancs appropriés pour une utilisation dans la plupart des paramètres d’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="c1b39-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**espace blanc de l’WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1b39-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-118">L’appareil utilise des chiffres de balance blancs appropriés pour une utilisation dans la plupart des paramètres d’éclairage lumineux.</span><span class="sxs-lookup"><span data-stu-id="c1b39-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="c1b39-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_Flash d' \_ équilibre des blancs wpd \_**</span><span class="sxs-lookup"><span data-stu-id="c1b39-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="c1b39-120">L’appareil utilise des nombres d’équilibres blancs appropriés pour une utilisation avec un flash.</span><span class="sxs-lookup"><span data-stu-id="c1b39-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b39-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c1b39-121">Remarks</span></span>

<span data-ttu-id="c1b39-122">Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ \_ équilibreur d’image de l’image wpd](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b39-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b39-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1b39-123">Requirements</span></span>



| <span data-ttu-id="c1b39-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1b39-124">Requirement</span></span> | <span data-ttu-id="c1b39-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1b39-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b39-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1b39-126">Header</span></span><br/> | <dl> <span data-ttu-id="c1b39-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b39-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b39-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b39-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b39-129">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="c1b39-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




