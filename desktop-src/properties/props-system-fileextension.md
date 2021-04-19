---
description: Identifie l’extension de fichier de l’élément basé sur un fichier, y compris le point de début.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517815"
---
# <a name="systemfileextension"></a>System. FileExtension

Identifie l’extension de fichier de l’élément basé sur un fichier, y compris le point de début. Cette propriété est dérivée de System. FileName. Si System. FileName n’a pas d’extension de fichier ou si VT est \_ vide, la valeur de cette propriété doit être VT \_ vide.

Pour obtenir le type d’un élément (y compris un élément qui n’est pas un fichier), utilisez System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si [System. FileName](./props-system-filename.md) est un VT \_ vide, cette propriété doit également être vide. Sinon, cette propriété doit être dérivée de manière appropriée par la source de données à partir de System. FileName. Si System. FileName n’inclut pas d’extension de fichier, [System. FileExtension]() doit être VT \_ vide. Pour obtenir le type d’un élément (y compris un élément qui n’est pas un fichier), utilisez [System. ItemType](./props-system-itemtype.md).

Exemples de propriétés de chemin d’accès et d’extension de fichier. 

| Chemin d’accès                               | Extension de fichier |
|------------------------------------|----------------|
| c : \\ fichiers \\ \\hello.txt personnels     | .txt           |
| \\\\news.doc du partage de serveur \\ \\ mydir \\ | .doc           |
| \\\\\\numbers.xls de partage de serveur \\     | .xls           |
| \\\\\\dossier partage du serveur \\          | VT \_ vide      |
| c : \\ Stuff \\                | VT \_ vide      |
| \[desktop\]                        | VT \_ vide      |



 

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

 

 
