---
description: événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.
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
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442155"
---
# <a name="wiaondevicedisconnected-event"></a>Événement WIA. OnDeviceDisconnected

événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.

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

## <a name="remarks"></a>Remarques

WIA notifie le script ou l’application chaque fois qu’un périphérique matériel est déconnecté de l’ordinateur. Implémentez la sous-routine **objWia** \_ **OnDeviceDisconnected ()** pour permettre au script ou à l’application de répondre à la déconnexion de l’appareil.

Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un appareil est supprimé de l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




