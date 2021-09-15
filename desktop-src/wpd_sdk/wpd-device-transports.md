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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411333"
---
# <a name="wpd_device_transports-enumeration"></a>\_Énumération des transports d’appareils wpd \_

Le type d’énumération des [**\_ \_ transports d’appareils wpd**](/windows/desktop/wpd_sdk/wpd-device-transports) spécifie la relation d’héritage pour un service. Cette énumération est utilisée par la propriété de **\_ \_ transport de l’appareil wpd** .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_transport d’appareil wpd \_ \_ non spécifié**
</dt> <dd>

Le type de transport n’a pas été spécifié.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_transport d’appareil wpd \_ \_ USB**
</dt> <dd>

L’appareil est connecté via USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**IP de transport de l' \_ appareil wpd \_ \_**
</dt> <dd>

L’appareil est connecté via le protocole IP (Internet Protocol).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_transport d’appareil wpd \_ \_ Bluetooth**
</dt> <dd>

L’appareil est connecté via Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

