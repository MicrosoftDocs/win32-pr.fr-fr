---
description: Décrit le résultat que vous pouvez éventuellement définir après le traitement d’un récepteur d’affichage notification par dans la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Structure WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
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
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780079"
---
# <a name="wfd_display_sink_notification_result-structure"></a>Structure du résultat de la notification du récepteur d' \_ affichage WFD \_ \_ \_

La structure du résultat de la **\_ notification du récepteur d’affichage \_ \_ \_ WFD** décrit le résultat que vous pouvez éventuellement définir après le traitement d’un récepteur d’affichage notification par dans la fonction de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**En-tête**
</dt> <dd>

[**\_ \_ \_ \_ En-tête d’objet récepteur WFD**](wfd-display-sink-object-header.md) qui décrit les données incluses dans le résultat de la notification.

</dd> <dt>

**type**
</dt> <dd>

Valeur [**du \_ \_ type de \_ notification \_ du récepteur d’affichage WFD**](wfd-display-sink-notification-type.md) qui indique le type du résultat de la notification. Ce paramètre détermine également les informations à utiliser dans l’Union ci-dessous.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Informations sur le résultat d’une demande d’approvisionnement. Utilisez cette valeur si le *type* a la valeur **ProvisioningRequestNotification**.

<dl> <dt>

**ConfigMethod**
</dt> <dd>

Méthode pour l’indication de l’interface utilisateur pour l’acceptation interactive.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Nombre de caractères larges dans la *clé de clé*, sans compter les terminateurs null.

</dd> <dt>

**Partout**
</dt> <dd>

Contient la clé de passe sous la forme d’un tableau de caractères larges. \_ \_ \_ \_ \_ La longueur maximale de la clé de clé du récepteur WFD \_ est définie sur la valeur (8).

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Informations sur le résultat d’une demande de reconnexion. Utilisez cette valeur si le *type* a la valeur **ReconnectRequestNotification**.

<dl> <dt>

**strProfile**
</dt> <dd>

Pointeur vers une chaîne se terminant par NULL et décrivant le profil.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




