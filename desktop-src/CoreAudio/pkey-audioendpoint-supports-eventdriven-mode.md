---
description: Le AudioEndpoint de la valeur de la propriété du jeu de la \_ \_ valeur prend en charge le \_ \_ mode EventDriven.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 280be65d4ae8e0b557bd96320ea31f67ba75657ecb5b685608bd2c314e10836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758919"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>Le AudioEndpoint de la- \_ \_ prend en charge le \_ \_ mode EventDriven

Le AudioEndpoint de la valeur de la propriété du jeu de la valeur **\_ \_ prend en charge le \_ \_ mode EventDriven** .

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** est une **valeur DWORD** qui indique si le point de terminaison prend en charge le mode piloté par les événements.

## <a name="remarks"></a>Remarques

Cette valeur de propriété est remplie par un OEM audio dans un fichier. inf pour indiquer que le matériel HDAudio prend en charge le mode piloté par les événements conformément aux exigences du WHQL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




