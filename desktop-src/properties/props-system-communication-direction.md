---
description: Indique si une communication a été entrante ou sortante.
ms.assetid: b41f185b-f8b3-433b-9aed-8e71d59e4602
title: System. communication. direction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee35e5f9dcf32e55e14196344ef0452288d520984e70c77e6a0d55f19911d4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554229"
---
# <a name="systemcommunicationdirection"></a>System. communication. direction

Indique si une communication était entrante ou sortante

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507

```
propertyDescription
   name = System.Communication.Direction
   shellPKey = PKEY_Communication_Direction
   formatID = 8E531030-B960-4346-AE0D-66BC9A86FB94
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = COMMUNICATION_DIRECTION_UNKNOWN
         enum
            name = Incoming
            value = 1
            text = Incoming
            defineToken = COMMUNICATION_DIRECTION_INCOMING
         enum
            name = Outgoing
            value = 2
            text = Outgoing
            defineToken = COMMUNICATION_DIRECTION_OUTGOING
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
