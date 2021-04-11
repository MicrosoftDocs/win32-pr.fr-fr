---
description: Chemin d’accès d’affichage convivial de l’élément.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209768"
---
# <a name="systemitempathdisplaynarrow"></a>System. ItemPathDisplayNarrow

Chemin d’accès d’affichage convivial de l’élément.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Pour optimiser pour une colonne d’affichage étroite, le format de la chaîne doit être adapté afin que le nom soit d’abord.

Si l’élément est un fichier, la valeur de la propriété exclut l’extension de fichier, mais inclut les noms localisés s’ils sont présents. Si l’élément est un message, la valeur comprend [System. ItemNamePrefix](./props-system-itemnameprefix.md). Pour analyser un chemin d’accès à un élément, utilisez [System. ItemUrl](./props-system-itemurl.md) ou [System. ParsingPath](./props-system-parsingpath.md).

Exemples de valeurs



| Chemin d’accès                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c : \\hello.txt de la \\ barre mydir \\              | Bonjour (c : \\ mydir \\ bar)              |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | goodnews ( \\ \\ partage de serveur \\ \\ mydir) |
| \\\\\\dossier partage du serveur \\              | dossier ( \\ \\ partage de serveur \\ )          |
| c : \\ mydir \\ mondossier                    | Mondossier (c : \\ mydir)                |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | Re : Bonjour ! (Compte/Mailbox/boîte de réception) |



 

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

 

 
