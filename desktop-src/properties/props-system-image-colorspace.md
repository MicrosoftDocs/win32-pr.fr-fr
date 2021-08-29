---
description: Colorspace incorporé dans l’image. Extrait des informations EXIF (Exchangeable Image File).
ms.assetid: 2375e132-e400-419f-a0f9-cbb6f9acdf45
title: System. image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17ef7d2ca0d2843a6297a135df6105b96edd5c4c83dfbeaa1657024b7569c3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716839"
---
# <a name="systemimagecolorspace"></a>System. image. ColorSpace

Colorspace incorporé dans l’image. Extrait des informations EXIF (Exchangeable Image File).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SRGB
            value = 1
            text = sRGB
            defineToken = IMAGE_COLORSPACE_SRGB
         enum
            name = Uncalibrated
            value = 0xFFFF
            text = Uncalibrated
            defineToken = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = sRGB
            defineName = IMAGE_COLORSPACE_SRGB
         enum
            value = 0xFFFF
            text = Uncalibrated
            defineName = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="remarks"></a>Remarques

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

 

 
