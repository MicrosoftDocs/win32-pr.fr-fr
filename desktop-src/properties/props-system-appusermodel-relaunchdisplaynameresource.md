---
description: Spécifie le nom complet utilisé pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b0af752fb345dd5dd5f1b091a22255e856031affaca266ff6307045f148cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233021"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. AppUserModel. RelaunchDisplayNameResource

Spécifie le nom complet utilisé pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton. La valeur de cette propriété doit être l’une des suivantes :

-   Une chaîne de ressource indirecte telle que « @% systemdir% \\ system32 \\shell32.dll,-19263 ». Notez que le caractère « @ » est requis pour distinguer une chaîne indirecte d’une chaîne de texte brut (décrite dans le paragraphe à puces suivant). Cette chaîne indirecte se compose d’un fichier binaire et d’un ID de ressource de la chaîne contenue dans ce binaire. nous vous recommandons vivement d’utiliser ce format de chaîne indirecte, qui garantit que le nom d’affichage change de manière appropriée lorsque la langue du système est modifiée via le interface utilisateur multilingue (MUI). Le caractère « - » avant l’ID de ressource est requis.
-   Chaîne de texte brut qui ne pointe pas vers une ressource. Cela doit être utilisé uniquement lorsque le nom complet est calculé dynamiquement ou obtenu à partir d’une source de données qui ne prend pas en charge MUI. par exemple, la chaîne peut être le nom d’un périphérique, tel que « Microsoft Zune », dans les cas où l’application s’affiche lorsque l’appareil est attaché à l’ordinateur.

> [!Note]  
> [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) et [System. AppUserModel. RelaunchDisplayNameResource]() doivent toujours être définis ensemble. Si l’une de ces propriétés n’est pas définie, aucune n’est utilisée.

 

Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la fenêtre n’a pas de AppUserModelID explicite, cette propriété est ignorée et la fenêtre est regroupée et épinglée comme s’il s’agissait d’une partie du processus qui le possède. Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md). Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut. Pour plus d’informations, consultez [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini. Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.

 

Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchDisplayNameResource]() de cette fenêtre.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
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

 

 
