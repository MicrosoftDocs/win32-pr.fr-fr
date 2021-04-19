---
description: Le \_ \_ type d’énumération de modes de focus wpd décrit le mode Focus utilisé par un appareil de capture d’image continue.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Énumération WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520967"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="2f3d4-103">\_Énumération des modes de focus wpd \_</span><span class="sxs-lookup"><span data-stu-id="2f3d4-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="2f3d4-104">Le type d’énumération de **\_ \_ modes de focus wpd** décrit le mode Focus utilisé par un appareil de capture d’image continue.</span><span class="sxs-lookup"><span data-stu-id="2f3d4-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f3d4-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="2f3d4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2f3d4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f3d4-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**\_focus wpd \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="2f3d4-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2f3d4-108">Le mode focus n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f3d4-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="2f3d4-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_Manuel de focus wpd \_**</span><span class="sxs-lookup"><span data-stu-id="2f3d4-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="2f3d4-110">Spécifie le focus manuel.</span><span class="sxs-lookup"><span data-stu-id="2f3d4-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="2f3d4-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_focus wpd \_ automatique**</span><span class="sxs-lookup"><span data-stu-id="2f3d4-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="2f3d4-112">Spécifie le focus automatique, contrôlé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2f3d4-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="2f3d4-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automatique Focus \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="2f3d4-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="2f3d4-114">Spécifie que l’appareil doit basculer automatiquement entre la macro et le focus normal, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="2f3d4-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f3d4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2f3d4-115">Remarks</span></span>

<span data-ttu-id="2f3d4-116">Cette énumération est utilisée par la propriété de [ \_ \_ \_ \_ mode focus d’image toujours wpd](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="2f3d4-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3d4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f3d4-117">Requirements</span></span>



| <span data-ttu-id="2f3d4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f3d4-118">Requirement</span></span> | <span data-ttu-id="2f3d4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f3d4-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3d4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f3d4-120">Header</span></span><br/> | <dl> <span data-ttu-id="2f3d4-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3d4-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f3d4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f3d4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3d4-123">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="2f3d4-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




