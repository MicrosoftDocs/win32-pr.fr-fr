---
description: En savoir plus sur la propriété System. ItemFolderPathDisplay, qui représente le chemin d’affichage convivial du dossier parent d’un élément.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fd2288f12073fe8e36707bf49aca2bc5e000d0bbe25d95fba0736b4e77af44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822339"
---
# <a name="systemitemfolderpathdisplay"></a>System. ItemFolderPathDisplay

Chemin d’accès d’affichage convivial du dossier parent d’un élément.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si [System. ItemPathDisplay](./props-system-itempathdisplay.md) est un VT \_ vide, cette propriété doit également être vide. Dans le cas contraire, elle doit être dérivée de manière appropriée par la source de données à partir de System. ItemPathDisplay.

Exemples de valeurs



| Chemin                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c : \\ fichiers \\ \\hello.txt personnels         | c : \\ fichiers \\ personnels      |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | \\\\\\mydir de partage de serveur \\ |
| \\\\\\numbers.xls de partage de serveur \\         | \\\\partage de serveur \\        |
| c : \\ nourriture \\ mondossier                     | c : \\ nourriture                 |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | Compte/Mailbox/boîte de réception   |



 

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

 

 
