---
description: Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.
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
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202899"
---
# <a name="wiaondeviceconnected-event"></a>Événement WIA. OnDeviceConnected

Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.

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

## <a name="remarks"></a>Notes

WIA notifie le script ou l’application chaque fois qu’un nouveau périphérique matériel est connecté à l’ordinateur. Implémentez la sous-routine **objWia** \_ **OnDeviceConnected ()** pour permettre au script ou à l’application de répondre à la connexion de l’appareil.

Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un nouveau périphérique est installé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




