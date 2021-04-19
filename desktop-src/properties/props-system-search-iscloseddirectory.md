---
description: Émis comme TRUE par un élément conteneur pour indiquer que ses éléments enfants n’ont pas besoin d’être énumérés par un indexeur si l’élément conteneur n’a pas été modifié depuis la dernière analyse incrémentielle de vérification de l’index.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538704"
---
# <a name="systemsearchiscloseddirectory"></a>System. Search. IsClosedDirectory

Émis comme **true** par un élément conteneur pour indiquer que ses éléments enfants n’ont pas besoin d’être énumérés par un indexeur si l’élément conteneur n’a pas été modifié depuis la dernière analyse incrémentielle de vérification de l’index. Cela contribue à l’optimisation des performances de l’indexeur. Dans ces cas de conteneurs (par exemple, un courrier électronique avec des pièces jointes ou un fichier compressé avec une extension de nom. zip), les éléments enfants sont inséparables de leur élément parent. Par exemple, si la propriété [System. DateModified](./props-system-datemodified.md) d’un élément contenu change, la valeur System. DateModified du conteneur est modifiée pour correspondre à. En outre, si un élément parent est supprimé, tous les éléments enfants sont également supprimés. Par conséquent, si le conteneur n’a pas changé, l’indexeur sait que rien dans celui-ci n’a changé et n’a pas besoin d’ouvrir le conteneur pour examiner le contenu individuellement.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

> [!IMPORTANT]
> Si un élément émet la **valeur true** pour cette propriété, chacun de ses éléments enfants doit émettre la propriété [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) comme **true** pour empêcher la suppression de ces éléments de l’index.

 

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

 

 
