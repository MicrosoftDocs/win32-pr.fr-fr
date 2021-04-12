---
description: Date d’acquisition du fichier ou du support.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210335"
---
# <a name="systemdateacquired"></a>System. DateAcquired

Date d’acquisition du fichier ou du support. Cette propriété est liée à un utilisateur ou à un groupe d’utilisateurs particulier. Par exemple, ces données sont utilisées comme axe de tri principal pour le dossier virtuel **New Music**, ce qui permet aux utilisateurs de parcourir les derniers ajouts à leur collection.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

[DateAcquired]() est stocké en tant que valeur dans le flux principal du fichier, mais il n’est pas toujours présent. Dans ces cas, la date d’acquisition peut être estimée en fonction d’autres dates connues pour le contenu. Le gestionnaire de métadonnées doit utiliser un ensemble de règles pour déterminer la date à renvoyer. L’exemple suivant illustre cela pour les fichiers musicaux.

-   Pour la musique achetée, l’heure de création du fichier doit être utilisée si aucune date d’acquisition n’est présente. Toutefois, le fournisseur de téléchargement doit définir la propriété [DateAcquired]() dans le fichier.
-   Pour les fichiers musicaux que l’utilisateur ou le groupe « a extraits » (copie de musique ou de vidéo à partir d’un CD ou d’un DVD sur un disque dur), la date d’acquisition doit correspondre à la date à laquelle l’action a eu lieu. Par exemple, l’attribut [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) .
-   Pour la musique copiée à partir d’un autre emplacement, l’heure de création du fichier doit être utilisée comme date d’acquisition.

La date et l’heure de l’acquisition d’images à partir d’un appareil photo ou de l’achat de musique en ligne sont des exemples de [System. DateAcquired]() . Ce n’est pas le même que [System. DateImported](./props-system-dateimported.md).

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

 

 
