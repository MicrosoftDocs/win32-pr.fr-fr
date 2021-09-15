---
description: Type canonique de l’élément.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784a72c46e92ac5956532994df4f36758d42f440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521300"
---
# <a name="systemitemtype"></a>System. ItemType

Type canonique de l’élément.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

La valeur de System. ItemType est conçue pour être analysée par programmation et peut être l’une des suivantes :

-   Extension de fichier qui pointe vers une valeur ProgID ( \_ classe HKEY \_ root \\ &lt; ProgID &gt; ) qui contient le nom complet du type.
-   Valeur ProgID (classes HKEY \_ \_ RROOT \\ &lt; ProgID &gt; ), contenant le nom complet du type.

L’élément FriendlyTypeName d’un ProgID doit être une version localisée du nom de l’application ( @winword.dll ,-42), tandis que la valeur par défaut de la clé ProgID est un nom non localisé (Word. document. 12).

S’il n’existe aucun type canonique, la valeur est VT \_ vide. Si l’élément est un fichier ([System. FileName](./props-system-filename.md) n’est pas de VT \_ vide), la valeur est la même que celle de [System. FileExtension](./props-system-fileextension.md). Utilisez [System. ItemTypeText](./props-system-itemtypetext.md) lorsque vous souhaitez afficher le type pour les utilisateurs finaux dans une vue.

> [!Note]  
> Si l’élément est un fichier, le passage de la valeur [System. ItemType]() à [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) entraîne la même valeur que [System. ItemTypeText](./props-system-itemtypetext.md).

 

Exemples de valeurs



| Chemin d’accès                                   | itemType         |
|----------------------------------------|------------------|
| c : \\hello.txt de la \\ barre mydir \\              | .txt             |
| \\\\goodnews.doc du partage de serveur \\ \\ mydir \\ | .doc             |
| \\\\\\dossier partage du serveur \\              | Répertoire        |
| c : \\ mydir \\ mondossier                    | Répertoire        |
| \[desktop\]                            | Dossier           |
| Compte/Mailbox/boîte de réception/'re : Bonjour ! '    | MAPI/IPM. Message |



 

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
</dt> <dt>

[Identificateurs programmatiques](../shell/fa-progids.md)
</dt> </dl>

 

 
