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
ms.openlocfilehash: 841ba87b71f79d1f9dfbf85053d914315f89f592ec16a50bd9f6baf061b989a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035500"
---
# <a name="deviceinfotype-property"></a>DeviceInfo. type, propriété

récupère le type d’appareil matériel d’Acquisition d’images Windows (WIA). Les valeurs possibles sont les suivantes :

-   DigitalCamera
-   Scanneur
-   StreamingVideo
-   Par défaut

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui reçoit l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




