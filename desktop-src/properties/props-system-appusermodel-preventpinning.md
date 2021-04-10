---
description: Désactive la possibilité d’épingler un raccourci ou une fenêtre dans la barre des tâches ou dans le menu Démarrer. Cette propriété rend également l’élément inéligible pour l’inclusion dans la liste des plus fréquemment utilisés (MFU) du menu Démarrer.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865565"
---
# <a name="systemappusermodelpreventpinning"></a>System. AppUserModel. PreventPinning

Désactive la possibilité d’épingler un raccourci ou une fenêtre dans la barre des tâches ou dans le menu **Démarrer** . Cette propriété rend également l’élément inéligible pour l’inclusion dans la liste des plus fréquemment utilisés (MFU) du menu **Démarrer** .

Cette propriété doit être définie sur une fenêtre avant la propriété de l’ID de groupe de [ \_ \_ sécurité AppUserModel](./props-system-appusermodel-id.md) . Une fois que \_ la \_ propriété ID de la AppUserModel de la valeur du groupe [de \_ \_ ]() sécurité

Pour plus d’informations sur les ID de modèle d’utilisateur d’application (AppUserModelIDs) et d’autres méthodes d’exclusion d’un élément de l’épinglage à la barre des tâches et de l’inclusion MFU, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).

Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. PreventPinning]() de cette fenêtre.

La définition de cette propriété entraîne l’ignorance des propriétés suivantes :

-   [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a>Notes

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
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

[aliasInfo](./propdesc-schema-aliasinfo.md)
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

[variables](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
