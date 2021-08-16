---
description: Cette propriété est la même que celle de System. Search. UrlToIndex, à ceci près qu’elle comprend l’heure de la dernière modification de l’URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7869005084379db1bdf288c6237a420666634c349eee47ca7942af2bb271a39d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464769"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. Search. UrlToIndexWithModificationTime

Cette propriété est la même que celle de [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , à ceci près qu’elle comprend l’heure de la dernière modification de l’URL. Il s’agit d’une optimisation pour l’indexeur afin qu’il n’ait pas à rappeler le gestionnaire de protocole pour demander ces informations afin de déterminer si le contenu doit être indexé à nouveau.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Remarques

Cette propriété [System. Search. UrlToIndexWithModificationTime]() est la même que la propriété [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , sauf que vous transmettez également l’heure de la dernière modification du document. Si l’heure de la dernière modification correspond, l’indexeur suppose que le document est déjà indexé et lève la notification. Cette propriété est un vecteur avec deux éléments, une valeur **VT \_ LPWStr** qui contient l’URL et une valeur de la **VT \_ fileTime** qui contient l’heure de la dernière modification.

[System. Search. UrlToIndexWithModificationTime]() a été appelé PID \_ GTHR \_ DIRLINK \_ avec \_ le temps dans les versions antérieures du système d’exploitation Windows.

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
