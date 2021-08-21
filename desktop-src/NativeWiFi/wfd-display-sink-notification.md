---
description: Décrit la notification transmise à la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Structure WFD_DISPLAY_SINK_NOTIFICATION (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 96d78be4942b9b1313f5b3f1f35aca0b2f3441e2c05a2c376092f01cbaf36c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064909"
---
# <a name="wfd_display_sink_notification-structure"></a>\_Structure de \_ notification du récepteur d’affichage WFD \_

La structure de **\_ notification du \_ récepteur \_ d’affichage WFD** décrit la notification transmise à la fonction de rappel de notification du [**récepteur d' \_ affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**En-tête**
</dt> <dd>

[**\_ \_ \_ \_ En-tête d’objet récepteur WFD**](wfd-display-sink-object-header.md) qui décrit les données incluses dans la notification.

</dd> <dt>

**type**
</dt> <dd>

Valeur [**du \_ \_ type de \_ notification \_ du récepteur d’affichage WFD**](wfd-display-sink-notification-type.md) qui indique le type de la notification. Ce paramètre détermine également les informations à utiliser dans l’Union ci-dessous.

</dd> <dt>

**strRemoteDeviceName**
</dt> <dd>

Contient une chaîne se terminant par un caractère NULL qui contient le nom de l’appareil distant. \_ \_ \_ \_ La longueur maximale du nom d’appareil du récepteur WFD \_ est définie en tant que valeur (32).

</dd> <dt>

**RemoteDeviceAddress**
</dt> <dd>

[**\_ \_ Adresse Mac DOT11**](dot11-mac-address-type.md) qui contient le BSSID du périphérique distant.

</dd> <dt>

**ProvisioningRequestInfo**
</dt> <dd>

Informations sur une demande d’approvisionnement. Utilisez cette valeur si le *type* a la valeur **ProvisioningRequestNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Handle de session.

</dd> <dt>

**PossibleConfigMethods**
</dt> <dd>

Méthodes possibles pour l’indication de l’interface utilisateur pour l’acceptation interactive.

</dd> </dl> </dd> <dt>

**ReconnectRequestInfo**
</dt> <dd>

Informations sur une demande de reconnexion. Utilisez cette valeur si le *type* a la valeur **ReconnectRequestNotification**.

<dl> <dt>

**GroupID**
</dt> <dd>

ID de groupe.

</dd> </dl> </dd> <dt>

**ConnectedInfo**
</dt> <dd>

Informations sur une notification connectée. Utilisez cette valeur si le *type* a la valeur **ConnectedNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Handle de session.

</dd> <dt>

**guidSessionInterface**
</dt> <dd>

GUID indiquant l’interface de la session.

</dd> <dt>

**GroupID**
</dt> <dd>

ID de groupe.

</dd> <dt>

**strProfile**
</dt> <dd>

Pointeur vers une chaîne se terminant par NULL et décrivant le profil.

</dd> <dt>

**LocalAddress**
</dt> <dd>

Adresse locale.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

Adresse distante.

</dd> <dt>

**uRTSPPort**
</dt> <dd>

Port RTSP.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




