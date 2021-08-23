---
description: 'Préfixe d’un élément, utilisé pour les messages électroniques où le sujet commence par le préfixe &\# 0034 ; Re : &\# 0034 ;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7830f63c3e9e0f6026099c95d11820a1d8592928cece72ebe72d76936d8467
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598459"
---
# <a name="systemitemnameprefix"></a>System. ItemNamePrefix

Préfixe d’un élément, utilisé pour les messages électroniques où le sujet commence par le préfixe « re : ».

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Si l’élément est un fichier, la valeur de cette propriété est VT \_ vide. Si l’élément est un message, la valeur de cette propriété est le préfixe de transfert ou de réponse (y compris le signe deux-points, mais aucun espace blanc), ou VT \_ vide s’il n’y a aucun préfixe.

Exemples de valeurs



| System. ItemNamePrefix | System. ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ vide             | « Bonne journée »      | « Bonne journée »            |
| « Re : »                 | « Bonne journée »      | « Re : excellent jour »        |
| « FWD : »               | « Budget mensuel » | « FWD : budget mensuel »  |
| VT \_ vide             | accounts.xls     | accounts.xls           |



 

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

 

 
