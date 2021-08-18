---
description: Nom du fichier, y compris son extension.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8a92febe0a4f2dfe8cc9d5741118fdb76bcb56c7bcd1ef5c3d881e8c0f9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096918"
---
# <a name="systemfilename"></a>System. FileName

Nom du fichier, y compris son extension. System. FileExtension est dérivé de cette propriété.

Il est possible que l’élément n’existe pas sur un système de fichiers (autrement dit, il ne peut pas être ouvert à l’aide de CreateFile). Néanmoins, si l’élément est représenté sous la forme d’un fichier et que son nom respecte la syntaxe de nom de fichier Win32 standard, la source de données doit émettre cette propriété. Si l’élément n’est pas un fichier, la source de données doit émettre cette propriété sous la forme VT \_ vide.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

L’élément n’existe peut-être pas sur un système de fichiers (autrement dit, il ne peut pas être ouvert à l’aide de CreateFile), mais si l’élément est représenté sous la forme d’un fichier du sens logique et que son nom respecte la syntaxe de nom de fichier Win32 standard, la source de données doit émettre cette propriété. Si un élément n’est pas un fichier, la valeur de cette propriété est VT \_ vide. Consultez System. ItemNameDisplay. Elle a la même valeur que System. ParsingName pour les éléments fournis par le dossier de fichiers de l’interpréteur de commandes.

Le tableau suivant répertorie des exemples de valeurs de propriété de chemin d’accès et de nom de fichier :



| Chemin                               | Valeur de propriété |
|------------------------------------|----------------|
| c : \\ fichiers \\ \\hello.txt personnels     | hello.txt      |
| \\\\news.doc du partage de serveur \\ \\ mydir \\ | news.doc       |
| \\\\\\numbers.xls de partage de serveur \\     | numbers.xls    |
| c : \\ Stuff \\                | Mondossier       |
| \[message électronique\]                  | VT \_ vide      |
| \[chanson. WMA sur un appareil mobile\]    | chanson. WMA       |



 

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

 

 
