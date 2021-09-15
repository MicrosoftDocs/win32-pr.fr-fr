---
description: Nom complet dans &\# 0034 ; la plus complète&\# 0034 ; formulaire.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404267"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Nom complet dans le formulaire « le plus complet ». Il s’agit de la représentation unique du nom d’élément le plus approprié pour les utilisateurs finaux.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Cette valeur est le concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) et [System. ItemName](./props-system-itemname.md).

Si l’élément est un fichier, cette propriété comprend le nom complet comme indiqué dans l’Explorateur de fichiers. Il existe des cas acceptables lorsque [System. FileName](./props-system-filename.md) est donné, mais la valeur de cette propriété est totalement différente. Les messages électroniques sont un bon exemple. Si l’élément est un message électronique, le nom de l’élément est normalement l’objet. Dans ce cas, la valeur doit être la concaténation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) et [System. ItemName](./props-system-itemname.md). Étant donné que la valeur de System. ItemNamePrefix exclut les espaces de fin, la concaténation doit inclure un espace lors de la génération de [System. ItemNameDisplay](). Notez que cette propriété n’est pas nécessairement unique, mais qu’elle est conçue pour promouvoir le candidat le plus probable qui peut être unique et qui paraîtra logique pour les utilisateurs finaux.

Par exemple, pour les documents, [System. title](./props-system-title.md) peut être utilisé en tant que [System. ItemNameDisplay](), mais dans la pratique, le titre des documents peut ne pas être utile ou être suffisamment unique pour fonctionner en tant que System. ItemNameDisplay unique. Au lieu de cela, il est préférable de fournir [System. FileName](./props-system-filename.md) comme valeur de System. ItemNameDisplay. dans Windows courrier électronique, le courrier électronique est stocké dans le système de fichiers en tant que fichiers. eml. Les valeurs System. FileName de ces fichiers ne sont pas conviviales, car il s’agit de GUID. Dans cet exemple, la promotion de [System. Subject](./props-system-subject.md) en tant que System. ItemNameDisplay est plus appropriée.

**Remarques sur la compatibilité :**

-   implémentations de dossiers Shell sur Windows Vista : utilisez \_ le nom de colonne ItemNameDisplay pour la colonne nom lorsque vous souhaitez que Windows Explorer appelle [**IShellFolder :: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ NORMAL) pour obtenir la valeur du nom. utilisez un autre nom de la base de IShellFolder2, tel que le \_ nom de la propriété _ type. si vous souhaitez que Windows Explorer appelle la banque de propriétés du dossier ou [**:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) pour obtenir la valeur du nom.
-   implémentations de dossiers Shell sur Windows XP : la première colonne doit être la colonne name et Windows Explorer appelle [**IShellFolder :: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer la valeur du nom. Le SCID/le n’a pas d’importance.



| Type d’élément     | Exemple                   |
|---------------|---------------------------|
| Fichier          | hello.txt                 |
| Message       | Re : où est la réunion ? |
| Dossier de l’appareil | chanson. WMA                  |
| Dossier        | Documents                 |



 

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

 

 
