---
description: Récupère le type d’appareil matériel WIA (Windows Image Acquisition).
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520383"
---
# <a name="deviceinfotype-property"></a>DeviceInfo. type, propriété

Récupère le type d’appareil matériel WIA (Windows Image Acquisition). Les valeurs possibles sont les suivantes :

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




