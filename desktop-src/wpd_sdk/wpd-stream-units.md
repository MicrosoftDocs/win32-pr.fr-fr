---
description: L' \_ \_ énumération d’unités de flux wpd spécifie les types d’unités à utiliser pour les opérations IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Énumération WPD_STREAM_UNITS (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758836"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="d5243-103">\_Énumération des unités de flux wpd \_</span><span class="sxs-lookup"><span data-stu-id="d5243-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="d5243-104">L’énumération d' **\_ \_ unités de flux wpd** spécifie les types d’unités à utiliser pour les opérations [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .</span><span class="sxs-lookup"><span data-stu-id="d5243-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5243-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5243-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="d5243-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d5243-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d5243-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_octets d' \_ unités de flux wpd \_**</span><span class="sxs-lookup"><span data-stu-id="d5243-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="d5243-108">Les unités de flux sont spécifiées en octets.</span><span class="sxs-lookup"><span data-stu-id="d5243-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d5243-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_ \_ frames d’unités de flux wpd \_**</span><span class="sxs-lookup"><span data-stu-id="d5243-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="d5243-110">Les unités de flux sont spécifiées dans des frames.</span><span class="sxs-lookup"><span data-stu-id="d5243-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="d5243-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_lignes d' \_ unités de flux wpd \_**</span><span class="sxs-lookup"><span data-stu-id="d5243-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="d5243-112">Les unités de flux sont spécifiées dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="d5243-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="d5243-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**unités de flux WPD en \_ \_ \_ millisecondes**</span><span class="sxs-lookup"><span data-stu-id="d5243-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="d5243-114">Les unités de flux sont spécifiées en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="d5243-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="d5243-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**microsecondes d' \_ unités de flux wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d5243-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="d5243-116">Les unités de flux de données sont spécifiées en microsecondes.</span><span class="sxs-lookup"><span data-stu-id="d5243-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5243-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5243-117">Requirements</span></span>



| <span data-ttu-id="d5243-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5243-118">Requirement</span></span> | <span data-ttu-id="d5243-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5243-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5243-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5243-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5243-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5243-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5243-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5243-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5243-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5243-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="d5243-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5243-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5243-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5243-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5243-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5243-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5243-127">**IPortableDeviceUnitsStream**</span><span class="sxs-lookup"><span data-stu-id="d5243-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="d5243-128">**IPortableDeviceUnitsStream::SeekInUnits**</span><span class="sxs-lookup"><span data-stu-id="d5243-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




