---
description: événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Événement WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209546"
---
# <a name="wiaondeviceconnected-event"></a>Événement WIA. OnDeviceConnected

événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.

## <a name="syntax"></a>Syntaxe


```JScript
Wia.OnDeviceConnected(
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

WIA notifie le script ou l’application chaque fois qu’un nouveau périphérique matériel est connecté à l’ordinateur. Implémentez la sous-routine **objWia** \_ **OnDeviceConnected ()** pour permettre au script ou à l’application de répondre à la connexion de l’appareil.

Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un nouveau périphérique est installé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




