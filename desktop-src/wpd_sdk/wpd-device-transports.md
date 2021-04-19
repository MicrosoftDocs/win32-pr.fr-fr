---
description: Le \_ \_ type d’énumération des transports d’appareils wpd spécifie la relation d’héritage pour un service. Cette énumération est utilisée par la \_ propriété de transport de l’appareil wpd \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Énumération WPD_DEVICE_TRANSPORTS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525121"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="0add9-104">\_Énumération des transports d’appareils wpd \_</span><span class="sxs-lookup"><span data-stu-id="0add9-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="0add9-105">Le type d’énumération des [**\_ \_ transports d’appareils wpd**](/windows/desktop/wpd_sdk/wpd-device-transports) spécifie la relation d’héritage pour un service.</span><span class="sxs-lookup"><span data-stu-id="0add9-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="0add9-106">Cette énumération est utilisée par la propriété de **\_ \_ transport de l’appareil wpd** .</span><span class="sxs-lookup"><span data-stu-id="0add9-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0add9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0add9-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="0add9-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0add9-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0add9-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_transport d’appareil wpd \_ \_ non spécifié**</span><span class="sxs-lookup"><span data-stu-id="0add9-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="0add9-110">Le type de transport n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="0add9-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="0add9-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_transport d’appareil wpd \_ \_ USB**</span><span class="sxs-lookup"><span data-stu-id="0add9-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="0add9-112">L’appareil est connecté via USB.</span><span class="sxs-lookup"><span data-stu-id="0add9-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="0add9-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**IP de transport de l' \_ appareil wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0add9-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="0add9-114">L’appareil est connecté via le protocole IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="0add9-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="0add9-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_transport d’appareil wpd \_ \_ Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="0add9-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="0add9-116">L’appareil est connecté via Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="0add9-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0add9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0add9-117">Requirements</span></span>



| <span data-ttu-id="0add9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0add9-118">Requirement</span></span> | <span data-ttu-id="0add9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0add9-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0add9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0add9-120">Header</span></span><br/> | <dl> <span data-ttu-id="0add9-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0add9-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

