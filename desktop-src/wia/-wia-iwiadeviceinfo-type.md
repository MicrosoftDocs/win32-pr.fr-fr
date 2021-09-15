---
description: récupère le type d’appareil matériel d’Acquisition d’images Windows (WIA).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. type, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522196"
---
# <a name="deviceinfotype-property"></a>DeviceInfo. type, propriété

récupère le type d’appareil matériel d’Acquisition d’images Windows (WIA). Les valeurs possibles sont les suivantes :

-   DigitalCamera
-   Scanneur
-   StreamingVideo
-   Default

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui reçoit l’appareil.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




