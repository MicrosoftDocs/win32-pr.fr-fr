---
description: Titre de l’élément.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b575c3dac43ec742f3b15068731afc6ddb15c7bf660a048c416abd7bc5976ab6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058279"
---
# <a name="systemtitle"></a>System.Title

Titre de l’élément. Par exemple, le titre d'un document, l'objet d'un message, la légende d'une photo ou le nom d'une piste de musique.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Cette propriété est mappée au *titre* de la propriété de document OLE. [System. title]() est une propriété couramment utilisée, en particulier dans des listes hétérogènes d’éléments où les éléments peuvent être de nombreux types différents. Par conséquent, il est recommandé que les gestionnaires de propriétés remplissent cette propriété même si elle est redondante ; par exemple, un message électronique, qui remplirait à la fois System. title et [System. Subject](./props-system-subject.md) avec la même valeur.

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

 

 
