---
description: Le \_ type d' \_ énumération des modes d’effet wpd décrit différents effets visuels qui peuvent être appliqués à une image.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Énumération WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522414"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="93155-103">\_Énumération des modes d’effet wpd \_</span><span class="sxs-lookup"><span data-stu-id="93155-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="93155-104">Le type d’énumération des **\_ \_ modes d’effet wpd** décrit différents effets visuels qui peuvent être appliqués à une image.</span><span class="sxs-lookup"><span data-stu-id="93155-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="93155-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93155-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="93155-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="93155-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93155-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_mode effet wpd non \_ \_ défini**</span><span class="sxs-lookup"><span data-stu-id="93155-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="93155-108">Aucun effet n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="93155-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="93155-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_couleur du \_ mode d’effet wpd \_**</span><span class="sxs-lookup"><span data-stu-id="93155-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="93155-110">L’image doit être de couleur.</span><span class="sxs-lookup"><span data-stu-id="93155-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="93155-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_mode d’effet wpd \_ \_ noir \_ et \_ blanc**</span><span class="sxs-lookup"><span data-stu-id="93155-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="93155-112">L’image doit être en noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="93155-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="93155-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_mode effet \_ wpd \_ sépia**</span><span class="sxs-lookup"><span data-stu-id="93155-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="93155-114">L’image doit être sépia.</span><span class="sxs-lookup"><span data-stu-id="93155-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93155-115">Notes</span><span class="sxs-lookup"><span data-stu-id="93155-115">Remarks</span></span>

<span data-ttu-id="93155-116">Cette énumération est utilisée par la propriété du [ \_ mode d' \_ \_ effet \_ d’image toujours wpd](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="93155-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="93155-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93155-117">Requirements</span></span>



| <span data-ttu-id="93155-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93155-118">Requirement</span></span> | <span data-ttu-id="93155-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="93155-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93155-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="93155-120">Header</span></span><br/> | <dl> <span data-ttu-id="93155-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="93155-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93155-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93155-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93155-123">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="93155-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




