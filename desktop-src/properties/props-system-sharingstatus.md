---
description: 'Indique l’état de partage d’un élément : non partagé, partagé, tout le monde (groupe résidentiel ou tout le monde) ou privé.'
ms.assetid: 61d8a4fc-d9ad-467f-aa79-b0c208d0e905
title: System. SharingStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3c930309435c14e53cfc29d0fd068be6697c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320157"
---
# <a name="systemsharingstatus"></a>System. SharingStatus

Indique l’état de partage d’un élément : non partagé, partagé, tout le monde (groupe résidentiel ou tout le monde) ou privé.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.SharingStatus
   shellPKey = PKEY_SharingStatus
   formatID = EF884C5B-2BFE-41BB-AAE5-76EEDF4F9902
   propID = 300
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text = Not shared
            defineToken = SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text = Private
            defineToken = SHARINGSTATUS_PRIVATE
```

## <a name="remarks"></a>Notes

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

 

 
