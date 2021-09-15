---
description: Émis comme TRUE par tous les éléments enfants d’un conteneur (par exemple, un message électronique ou un fichier compressé avec une extension de nom de .zip) qui émet System. Search. IsClosedDirectory comme TRUE. Cela permet de s’assurer que les éléments enfants sont inclus dans l’index de recherche.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313346"
---
# <a name="systemsearchisfullycontained"></a>System. Search. IsFullyContained

Émis comme **true** par tous les éléments enfants d’un conteneur (par exemple, un message électronique ou un fichier compressé avec une extension de nom de .zip) qui émet [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) comme **true**. Cela permet de s’assurer que les éléments enfants sont inclus dans l’index de recherche.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

La propriété [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) permet d’optimiser les performances de l’indexeur en permettant à l’indexeur d’ignorer l’énumération des éléments enfants d’un conteneur. Toutefois, ces éléments enfants sont marqués par l’indexeur comme non visités et, par conséquent, ils sont supprimés de l’index. En émettant [System. Search. IsFullyContained]() comme **true**, un élément n’est pas supprimé de l’index, même s’il n’a pas été visité.

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

 

 
