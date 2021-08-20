---
description: Un ID de modèle d’utilisateur d’application explicite (AppUserModelID) utilisé pour associer des processus, des fichiers et des fenêtres à une application particulière.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033737"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Un ID de modèle d’utilisateur d’application explicite (AppUserModelID) utilisé pour associer des processus, des fichiers et des fenêtres à une application particulière. Dans certains cas, il suffit de s’appuyer sur la AppUserModelID interne assignée à un processus par le système. Toutefois, une application qui possède plusieurs processus ou une application en cours d’exécution dans un processus hôte peut avoir besoin de s’identifier de manière explicite par le biais de cette propriété afin de pouvoir regrouper ses fenêtres dans un même bouton de la barre des tâches et contrôler le contenu de la liste de raccourcis de cette application.

Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System.AppUserModel.ID]() de cette fenêtre.

Pour plus d’informations, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).

Au moment de la définition de la propriété [System.AppUserModel.ID]() , la barre des tâches est notifiée pour actualiser ses informations dans la fenêtre ou le raccourci donné à ce AppUserModelID.

D’autres propriétés de fenêtre et de raccourci peuvent être utilisées conjointement avec une AppUserModelID explicite pour mieux contrôler le regroupement et l’épinglage associés à une fenêtre, le nom complet et l’icône utilisés dans la barre des tâches, ainsi que la commande de lancement d’une application épinglée à la barre des tâches ou d’une nouvelle instance de l’application via la liste de raccourcis de cette application. Ces propriétés doivent être définies avant de définir la propriété [System.AppUserModel.ID]() . Pour plus d'informations, voir les rubriques suivantes :

-   [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md)
-   [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md)
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

 

 
