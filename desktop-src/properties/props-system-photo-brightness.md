---
description: Valeur de luminosité de l’image, en unités APEX, généralement comprise entre-99,99 et 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530525"
---
# <a name="systemphotobrightness"></a>System. photo. Brightness

Valeur de luminosité de l’image, en unités APEX, généralement comprise entre-99,99 et 99,99.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Consultez la spécification EXIF 2,2, annexe C, pour obtenir une comparaison des chiffres [System. photo. Brightness]() et des mesures de Foot-Lambert. Cette propriété est calculée à partir de [System. photo. BrightnessNumerator](./props-system-photo-brightnessnumerator.md) et de [System. photo. BrightnessDenominator](./props-system-photo-brightnessdenominator.md). Si le numérateur de la valeur enregistrée est FFFFFFFF. H, « Unknown » doit être indiqué.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exchangeable Image File Format pour les appareils photo numériques : EXIF version 2,2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
