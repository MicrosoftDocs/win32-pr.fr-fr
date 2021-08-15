---
description: Spécifie l’icône utilisée pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970838"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System. AppUserModel. RelaunchIconResource

Spécifie l’icône utilisée pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton. Il s’agit de l’icône utilisée pour le groupe de la barre des tâches et est affichée pour une application épinglée, que cette application soit en cours d’exécution ou non. Il doit être spécifié dans l’un des formats suivants :

-   Format de ressource standard, par exemple « % systemdir% \\ system32 \\shell32.dll,-128 ». Le caractère « - » avant l’ID de ressource est requis. N’utilisez pas le caractère « @ » au début de la chaîne du chemin d’accès.
-   chemin d’accès Direct à un fichier d’icône, tel que « % programfiles% \\ Microsoft \\ Bloc-notes \\ Bloc-notes. ico, 0 ». Notez que dans la mesure où les fichiers. ico peuvent contenir plusieurs ressources d’icône, un ID de ressource est requis dans la chaîne. Si le fichier. ico est une image unique, utilisez « 0 » (sans le caractère « - ») comme ID de ressource.

[System. AppUserModel. RelaunchIconResource]() est une propriété facultative. S’il n’est pas défini, l’icône de la cible de la commande relancer ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) est utilisée. Toutefois, étant donné que cela peut entraîner des résultats indésirables, nous vous encourageons vivement à fournir une icône de manière explicite par le biais de cette propriété.

Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la fenêtre n’a pas de AppUserModelID explicite (System.AppUserModel.ID), cette propriété est ignorée et la fenêtre est regroupée et épinglée comme si elle faisaient partie de son processus propriétaire. Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md). Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut. Pour plus d’informations, consultez [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

Si une valeur AppUserModelID explicite est définie sur la fenêtre, mais que cette propriété n’est pas définie, le système tente de trouver un raccourci avec la même valeur AppUserModelID et épingle ce raccourci à la barre des tâches pour représenter la fenêtre. Si ce raccourci ne peut pas être trouvé, l’exécutable de sauvegarde du processus qui le possède est utilisé.

> [!Note]  
> Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini. Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.

 

Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchIconResource]() de cette fenêtre.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
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

 

 
