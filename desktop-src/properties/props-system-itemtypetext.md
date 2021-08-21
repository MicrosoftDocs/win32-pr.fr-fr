---
description: Nom de type convivial de l’élément.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553749"
---
# <a name="systemitemtypetext"></a>System. ItemTypeText

Nom de type convivial de l’élément. Cette valeur n’est pas destinée à être analysée par programmation.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si [System. ItemType](./props-system-itemtype.md) est \_ un VT vide, la valeur de cette propriété est également une valeur VT \_ vide. Si l’élément est un fichier, la valeur de cette propriété est la même que si vous avez passé la valeur System. ItemType du fichier à [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Cette propriété ne doit pas être confondue avec [System. Kind](./props-system-kind.md), qui est un nom de type de haut niveau et convivial. Par exemple, pour un fichier de document .doc, les différentes propriétés sont les suivantes :



| Propriété                                               | Valeur                   |
|--------------------------------------------------------|-------------------------|
| [System. Kind](./props-system-kind.md)                 | Document                |
| [System. ItemType](./props-system-itemtype.md)         | .doc                    |
| [System. ItemTypeText]() | Microsoft Word Document |



 

Exemples de valeurs



| Chemin                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c : \\hello.txt de la \\ barre mydir \\              | Fichier texte               |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | Microsoft Word Document |
| \\\\\\dossier partage du serveur \\              | Dossier de fichiers             |
| c : \\ mydir \\ mondossier                    | Dossier de fichiers             |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | Outlook Message électronique  |



 

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

 

 
