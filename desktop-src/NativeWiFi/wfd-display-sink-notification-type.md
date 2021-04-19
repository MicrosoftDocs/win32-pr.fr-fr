---
description: Définit le type de la notification transmise à la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Énumération WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544835"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a>\_ \_ \_ Énumération des types de notification du récepteur d’affichage WFD \_

Le type d’énumération du **type de notification du \_ récepteur d’affichage \_ \_ \_ WFD** définit le type de la notification transmise à la fonction de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**
</dt> <dd>

La notification est une demande d’approvisionnement.

</dd> <dt>

<span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**
</dt> <dd>

La notification est une demande de reconnexion.

</dd> <dt>

<span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**
</dt> <dd>

La notification est une notification connectée.

</dd> <dt>

<span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**
</dt> <dd>

La notification est une notification déconnectée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




