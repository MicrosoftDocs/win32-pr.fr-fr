---
description: Chemin d’accès d’affichage convivial de l’élément.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115458"
---
# <a name="systemitempathdisplay"></a>System. ItemPathDisplay

Chemin d’accès d’affichage convivial de l’élément.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si l’élément est un fichier ou un dossier, cette propriété comprend l’extension dans tous les cas, et est localisée si un nom localisé est disponible. Pour les autres éléments, il s’agit de l’équivalent convivial de l’utilisateur, en supposant que l’élément existe dans le stockage hiérarchique.

Contrairement à [System. ItemUrl](./props-system-itemurl.md), cette valeur de propriété n’inclut pas le schéma d’URL. Pour analyser un chemin d’accès à un élément, utilisez System. ItemUrl ou [System. ParsingPath](./props-system-parsingpath.md). Pour référencer des éléments d’espace de noms Shell à l’aide d’API Shell, utilisez System. ParsingPath.

Exemples de valeurs



| Chemin d’accès                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c : \\hello.txt de la \\ barre mydir \\              | c : \\hello.txt de la \\ barre mydir \\              |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ |
| \\\\\\numbers.xls de partage de serveur \\         | \\\\\\numbers.xls de partage de serveur \\         |
| c : \\ mydir \\ mondossier                    | c : \\ mydir \\ mondossier                    |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | Compte/Mailbox/boîte de réception/'re : Bonjour ! '    |



 

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

 

 
