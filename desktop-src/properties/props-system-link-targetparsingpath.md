---
description: Chemin d’accès de l’espace de noms du shell à la cible de l’élément de lien.
ms.assetid: 05bd6cae-68b2-49ce-ad4f-e395ec88407a
title: System. Link. TargetParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69196ca35f197178a148b5a5c202df39ea1bdc200732b3e1e1979a57b9dc3e55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090959"
---
# <a name="systemlinktargetparsingpath"></a>System. Link. TargetParsingPath

Chemin d’accès de l’espace de noms du shell à la cible de l’élément de lien.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Link.TargetParsingPath
   shellPKey = PKEY_Link_TargetParsingPath
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Ce chemin d’accès peut être passé à [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) pour analyser le chemin d’accès au dossier shell approprié. Si l’élément cible est un fichier, la valeur est identique à [System. ItemPathDisplay](./props-system-itempathdisplay.md). Si l’élément cible n’est pas accessible par le biais de l’espace de noms Shell, cette valeur est de type VT \_ vide.

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

 

 
