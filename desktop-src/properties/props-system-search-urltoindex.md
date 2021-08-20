---
description: Émis par un IFilter de conteneur pour chaque URL enfant dans le conteneur. Les enfants sont finalement analysés par l’indexeur s’ils sont dans la portée.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb964f146831561174f3713d5b827a2c736c59f93e034ac8494f86a0fc6584bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864765"
---
# <a name="systemsearchurltoindex"></a>System. Search. UrlToIndex

Émis par un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de conteneur pour chaque URL enfant dans le conteneur. Les enfants sont finalement analysés par l’indexeur s’ils sont dans la portée.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Remarques

Cette propriété contient une URL et est émise par un gestionnaire de protocole pour chaque URL enfant ou sous l’URL actuelle. L’indexeur rappelle le gestionnaire de protocole et demande ce document à indexer. [system. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) s’appelait PID \_ GTHR \_ DIRLINK dans les versions antérieures du système d’exploitation Windows.

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Search. UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

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

 

 
