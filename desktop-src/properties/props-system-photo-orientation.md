---
description: L’orientation de la photo lorsqu’elle a été prise, comme spécifié dans les informations EXIF (Exchangeable Image File) et en termes de lignes et de colonnes.
ms.assetid: d6186248-8944-4bd6-8f04-bab5ea15b169
title: System. photo. orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac8cec8e199bd8eff52a92c7518a998d805d18d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412674"
---
# <a name="systemphotoorientation"></a>System. photo. orientation

L’orientation de la photo lorsqu’elle a été prise, comme spécifié dans les informations EXIF (Exchangeable Image File) et en termes de lignes et de colonnes. Cela permet aux applications et au shell d’orienter correctement l’image, au lieu d’orienter les pixels et de conserver l’image dans l’orientation d’affichage demandée, ce qui peut entraîner une perte de fidélité. Cette propriété n’est pas destinée à être affichée dans l’interface utilisateur.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PHOTO_ORIENTATION_NORMAL
         enum
            name = FlipHorizontal
            value = 2
            text = Flip horizontal
            defineToken = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            name = Rotate180
            value = 3
            text = Rotate 180 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE180
         enum
            name = FlipVertical
            value = 4
            text = Flip vertical
            defineToken = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            name = Transpose
            value = 5
            text = Transpose
            defineToken = PHOTO_ORIENTATION_TRANSPOSE
         enum
            name = Rotate270
            value = 6
            text = Rotate 270 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE270
         enum
            name = Transverse
            value = 7
            text = Transverse
            defineToken = PHOTO_ORIENTATION_TRANSVERSE
         enum
            name = Rotate90
            value = 8
            text = Rotate 90 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE90
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Normal
            defineName = PHOTO_ORIENTATION_NORMAL
         enum
            value = 2
            text = Flip horizontal
            defineName = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            value = 3
            text = Rotate 180 degrees
            defineName = PHOTO_ORIENTATION_ROTATE180
         enum
            value = 4
            text = Flip vertical
            defineName = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            value = 5
            text = Transpose
            defineName = PHOTO_ORIENTATION_TRANSPOSE
         enum
            value = 6
            text = Rotate 270 degrees
            defineName = PHOTO_ORIENTATION_ROTATE270
         enum
            value = 7
            text = Transverse
            defineName = PHOTO_ORIENTATION_TRANSVERSE
         enum
            value = 8
            text = Rotate 90 degrees
            defineName = PHOTO_ORIENTATION_ROTATE90
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

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

 

 
