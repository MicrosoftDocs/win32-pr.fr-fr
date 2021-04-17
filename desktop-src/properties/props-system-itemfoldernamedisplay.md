---
description: Nom complet convivial du dossier parent d’un élément.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203834"
---
# <a name="systemitemfoldernamedisplay"></a>System. ItemFolderNameDisplay

Nom complet convivial du dossier parent d’un élément.

Cela est dérivé de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md). Si cette propriété est une propriété VT \_ vide, cette propriété doit être également.

Si le dossier est un dossier de fichiers, la valeur sera localisée si un nom localisé est disponible.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) est un VT \_ vide, cette propriété doit également être vide. Dans le cas contraire, elle doit être dérivée de manière appropriée par la source de données à partir de System. ItemFolderPathDisplay.

Exemples :



| Chemin d’accès donné                             | Nom complet du dossier |
|----------------------------------------|---------------------|
| c : \\ myfiles \\ texte \\hello.txt           | Texte                |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | mydir               |
| \\\\\\numbers.xls de partage de serveur \\         | partager               |
| c : \\ dossiers \\ mondossier                  | Dossiers             |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | Inbox               |



 

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

 

 
