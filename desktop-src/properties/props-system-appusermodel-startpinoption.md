---
description: Définir cette propriété sur un raccourci pour (1) empêcher une application d’être épinglée automatiquement à l’écran de démarrage lors de l’installation ; ou (2) indique qu’un élément est ajouté par programmation au lanceur via une action de l’utilisateur (ce qui implique automatiquement l’épinglage pour démarrer et supprimer en désépinglage).
ms.assetid: 247ad0a6-ce65-45f1-a0d5-51ad135000aa
title: System. AppUserModel. StartPinOption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cdef82a90488ce87bbf182323b00d62a5cdfea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524205"
---
# <a name="systemappusermodelstartpinoption"></a>System. AppUserModel. StartPinOption

Définir cette propriété sur un raccourci pour (1) empêcher une application d’être épinglée automatiquement à l’écran de démarrage lors de l’installation ; ou (2) indique qu’un élément est ajouté par programmation au lanceur via une action de l’utilisateur (ce qui implique automatiquement l’épinglage pour démarrer et supprimer en désépinglage).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.AppUserModel.StartPinOption
   shellPKey = PKEY_AppUserModel_StartPinOption
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = false
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Default
            value = 0
            text = Default
            defineToken = APPUSERMODEL_STARTPINOPTION_DEFAULT
         enum
            name = NoPinOnInstall
            value = 1
            text = NoPinOnInstall
            defineToken = APPUSERMODEL_STARTPINOPTION_NOPINONINSTALL
         enum
            name = UserPinned
            value = 2
            text = UserPinned
            defineToken = APPUSERMODEL_STARTPINOPTION_USERPINNED
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

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

 

 
