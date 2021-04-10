---
description: Le AudioEndpoint de la valeur de la propriété du jeu de la \_ \_ valeur prend en charge le \_ \_ mode EventDriven.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950784"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>Le AudioEndpoint de la- \_ \_ prend en charge le \_ \_ mode EventDriven

Le AudioEndpoint de la valeur de la propriété du jeu de la valeur **\_ \_ prend en charge le \_ \_ mode EventDriven** .

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** est une **valeur DWORD** qui indique si le point de terminaison prend en charge le mode piloté par les événements.

## <a name="remarks"></a>Notes

Cette valeur de propriété est remplie par un OEM audio dans un fichier. inf pour indiquer que le matériel HDAudio prend en charge le mode piloté par les événements conformément aux exigences du WHQL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




