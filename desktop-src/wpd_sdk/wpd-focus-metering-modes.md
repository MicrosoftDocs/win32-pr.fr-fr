---
description: Le \_ \_ \_ type d’énumération des modes de contrôle de focus wpd décrit comment un appareil doit déterminer quelle partie d’un cadre utiliser pour définir le focus.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Énumération WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525284"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="1ab31-103">\_ \_ Énumération des modes de contrôle de focus wpd \_</span><span class="sxs-lookup"><span data-stu-id="1ab31-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="1ab31-104">Le type d’énumération des **\_ modes de \_ contrôle \_ de focus wpd** décrit comment un appareil doit déterminer quelle partie d’un cadre utiliser pour définir le focus.</span><span class="sxs-lookup"><span data-stu-id="1ab31-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab31-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="1ab31-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1ab31-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1ab31-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_mode de contrôle de focus wpd \_ \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="1ab31-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1ab31-108">Indique qu’aucun mode de focus n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ab31-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ab31-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_point \_ central du mode de contrôle du focus wpd \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ab31-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="1ab31-110">Se concentre sur le centre de la zone de trame.</span><span class="sxs-lookup"><span data-stu-id="1ab31-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="1ab31-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_mode de contrôle du focus wpd \_ \_ \_ \_ sur plusieurs points**</span><span class="sxs-lookup"><span data-stu-id="1ab31-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="1ab31-112">Déterminez le focus en analysant plusieurs parties de la zone encadrée.</span><span class="sxs-lookup"><span data-stu-id="1ab31-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ab31-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1ab31-113">Remarks</span></span>

<span data-ttu-id="1ab31-114">Cette énumération est spécifiée par la propriété du mode de contrôle de focus de l' [ \_ \_ image \_ \_ \_ wpd continue](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="1ab31-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab31-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ab31-115">Requirements</span></span>



| <span data-ttu-id="1ab31-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ab31-116">Requirement</span></span> | <span data-ttu-id="1ab31-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ab31-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab31-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ab31-118">Header</span></span><br/> | <dl> <span data-ttu-id="1ab31-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab31-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab31-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab31-121">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="1ab31-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




