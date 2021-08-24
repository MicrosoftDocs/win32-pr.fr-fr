---
description: Identifie l’emplacement d’enregistrement par défaut pour une bibliothèque pour les non-propriétaires de la bibliothèque.
ms.assetid: e6fe96de-4895-477e-a442-746fd34a7433
title: System. IsDefaultNonOwnerSaveLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e8ff6591f83364ec2c074cfd29d9ef5e1f76e9a039d988da51009735836c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716609"
---
# <a name="systemisdefaultnonownersavelocation"></a>System. IsDefaultNonOwnerSaveLocation

Identifie l’emplacement d’enregistrement par défaut pour une bibliothèque pour les non-propriétaires de la bibliothèque.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.IsDefaultNonOwnerSaveLocation
   shellPKey = PKEY_IsDefaultNonOwnerSaveLocation
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = DefaultPublicSave
            value = #TRUE#
            text = Public save location
            defineToken = ISDEFAULTPUBLICSAVE_YES
         enum
            name = NotDefaultPublicSave
            value = #FALSE#
            text
            defineToken = ISDEFAULTPUBLICSAVE_NO
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.IsDefaultNonOwnerSaveLocation
   shellPKey = PKEY_IsDefaultNonOwnerSaveLocation
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
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

 

 
