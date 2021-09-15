---
description: Collection d’objets DeviceInfo qui représentent tous les périphériques installés sur l’ordinateur.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: WIA. Devices, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522236"
---
# <a name="wiadevices-property"></a>WIA. Devices, propriété

Collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) qui représentent tous les périphériques installés sur l’ordinateur. Lecture seule.

> [!Note]  
> Cette collection est de base 0.

 

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la collection **Devices** pour énumérer les périphériques sur un système.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




