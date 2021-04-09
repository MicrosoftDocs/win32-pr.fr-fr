---
description: Chemin d’accès à l’espace de noms Shell de l’élément.
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. ParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864617"
---
# <a name="systemparsingpath"></a>System. ParsingPath

Chemin d’accès à l’espace de noms Shell de l’élément.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Cette valeur peut être passée à [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) pour analyser le chemin d’accès au dossier shell approprié. Si l’élément est un fichier, la valeur est identique à [System. ItemPathDisplay](./props-system-itempathdisplay.md). Si l’élément n’est pas accessible par le biais de l’espace de noms Shell, cette valeur est de type VT \_ vide.

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

 

 
