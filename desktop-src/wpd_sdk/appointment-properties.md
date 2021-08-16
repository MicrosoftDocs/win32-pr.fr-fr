---
description: Windows Appareils mobiles prend en charge les propriétés de rendez-vous suivantes.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Propriétés du rendez-vous (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2ba82c12dfffb0367ab61d355d6e256ab5d97bfbeef3e4a588f3a76a5651f9b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843589"
---
# <a name="appointment-properties"></a>Propriétés du rendez-vous

Windows Appareils mobiles prend en charge les propriétés de rendez-vous suivantes.



| Propriété                                   | VarType        | Description                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **participants à un \_ rendez-vous \_ accepté par wpd \_**  | **\_LPWStr VT** | Liste délimitée par des points-virgules des participants qui ont accepté le rendez-vous.             |
| **\_rendez-vous \_ refusé aux \_ participants**  | **\_LPWStr VT** | Liste délimitée par des points-virgules des participants ayant refusé le rendez-vous.             |
| **\_emplacement du rendez-vous wpd \_**             | \_LPWStr VT     | Emplacement convivial du lecteur du rendez-vous, par exemple, « bâtiment 5, salle 7 ».    |
| **\_ \_ participants facultatifs RENDus wpd \_**  | **\_LPWStr VT** | Liste délimitée par des points-virgules des participants facultatifs au rendez-vous.                  |
| **participants obligatoires à un \_ rendez-vous \_ \_**  | **\_LPWStr VT** | Liste délimitée par des points-virgules des participants obligatoires au rendez-vous.                  |
| **\_ressources de rendez-vous wpd \_**            | **\_LPWStr VT** | Liste délimitée par des points-virgules des ressources requises pour le rendez-vous.                  |
| **\_ \_ participants provisoires au rendez-vous pour wpd \_** | **\_LPWStr VT** | Liste délimitée par des points-virgules des participants qui ont provisoirement accepté le rendez-vous. |
| **\_type de rendez-vous wpd \_**                 | **\_LPWStr VT** | Type de rendez-vous, par exemple « personnel », « professionnel », etc.              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




