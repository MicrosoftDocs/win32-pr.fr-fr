---
title: Énumération WMDMMessage
description: Le type d’énumération WMDMMessage définit les types de messages et les États.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Gestionnaire de périphériques Windows Media WMDMMessage, énumération
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523893"
---
# <a name="wmdmmessage-enumeration"></a>Énumération WMDMMessage

Le type d’énumération **WMDMMessage** définit les types de messages et les États.

## <a name="syntax"></a>Syntaxe


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**arrivée de l' \_ appareil WMDM MSG \_ \_**
</dt> <dd>

Un appareil Windows Media Gestionnaire de périphériques a été branché.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**suppression de l' \_ appareil WMDM MSG \_ \_**
</dt> <dd>

Un appareil Windows Media Gestionnaire de périphériques a été supprimé.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_arrivée du \_ support \_ MSG WMDM**
</dt> <dd>

Le média a été inséré sur un appareil Windows Media Gestionnaire de périphériques.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_suppression du \_ support \_ MSG WMDM**
</dt> <dd>

Le média a été supprimé d’un appareil Windows Media Gestionnaire de périphériques.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





