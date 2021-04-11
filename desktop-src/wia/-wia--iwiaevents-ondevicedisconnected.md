---
description: Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Événement WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202898"
---
# <a name="wiaondevicedisconnected-event"></a>Événement WIA. OnDeviceDisconnected

Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.

## <a name="syntax"></a>Syntaxe


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Chaîne qui contient l’ID de l’appareil connecté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

WIA notifie le script ou l’application chaque fois qu’un périphérique matériel est déconnecté de l’ordinateur. Implémentez la sous-routine **objWia** \_ **OnDeviceDisconnected ()** pour permettre au script ou à l’application de répondre à la déconnexion de l’appareil.

Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un appareil est supprimé de l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




