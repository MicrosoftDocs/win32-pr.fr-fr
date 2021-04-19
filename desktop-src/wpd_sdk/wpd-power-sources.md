---
description: Le \_ type d' \_ énumération des sources d’alimentation wpd décrit la source d’alimentation utilisée par un appareil.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Énumération WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542260"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="0b829-103">\_Énumération des sources d’alimentation wpd \_</span><span class="sxs-lookup"><span data-stu-id="0b829-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="0b829-104">Le type d’énumération des **\_ \_ sources d’alimentation wpd** décrit la source d’alimentation utilisée par un appareil.</span><span class="sxs-lookup"><span data-stu-id="0b829-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b829-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b829-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="0b829-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0b829-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b829-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batterie de \_ source d’alimentation wpd \_**</span><span class="sxs-lookup"><span data-stu-id="0b829-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="0b829-108">La source d’alimentation de l’appareil est une batterie.</span><span class="sxs-lookup"><span data-stu-id="0b829-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="0b829-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_source d’alimentation wpd \_ \_ externe**</span><span class="sxs-lookup"><span data-stu-id="0b829-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="0b829-110">L’appareil utilise une source d’alimentation externe.</span><span class="sxs-lookup"><span data-stu-id="0b829-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b829-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0b829-111">Remarks</span></span>

<span data-ttu-id="0b829-112">Cette énumération est utilisée par la propriété de la [ \_ \_ \_ source d’alimentation de l’appareil wpd](device-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0b829-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b829-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b829-113">Requirements</span></span>



| <span data-ttu-id="0b829-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b829-114">Requirement</span></span> | <span data-ttu-id="0b829-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b829-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b829-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b829-116">Header</span></span><br/> | <dl> <span data-ttu-id="0b829-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b829-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b829-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b829-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b829-119">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="0b829-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




