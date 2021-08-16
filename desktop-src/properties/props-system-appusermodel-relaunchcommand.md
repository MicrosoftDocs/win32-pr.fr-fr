---
description: Spécifie une commande qui peut être exécutée via ShellExecute pour lancer une application lorsqu’elle est épinglée à la barre des tâches ou lorsqu’une nouvelle instance de l’application est lancée par le biais de la liste de raccourcis de l’application.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2ce3783aa9ab3d76124b8d62f9d9d9ad2e1f5d4b92622716df111456dbabd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554519"
---
# <a name="systemappusermodelrelaunchcommand"></a>System. AppUserModel. RelaunchCommand

Spécifie une commande qui peut être exécutée via [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour lancer une application lorsqu’elle est épinglée à la barre des tâches ou lorsqu’une nouvelle instance de l’application est lancée par le biais de la liste de raccourcis de l’application.

En voici quelques exemples :


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la fenêtre n’a pas de AppUserModelID explicite, cette propriété est ignorée et la fenêtre est regroupée et épinglée comme s’il s’agissait d’une partie du processus qui le possède. Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).

Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut.

> [!Note]  
> [System. AppUserModel. RelaunchCommand]() et [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) doivent toujours être définis ensemble. Si l’une de ces propriétés n’est pas définie, aucune n’est utilisée.

 

Cette propriété, associée à [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) et [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) , peut être utilisée pour définir visuellement une fenêtre en tant qu’application pour l’utilisateur. Cela est utile pour les scénarios d’application hôte, où une seule instance d’hôte exécute plusieurs applications enfants. Par exemple, un ordinateur virtuel qui héberge plusieurs applications virtualisées peut souhaiter que ces applications virtualisées apparaissent en tant qu’applications individuelles pour l’utilisateur. L’ordinateur virtuel peut étiqueter chaque fenêtre avec un AppUserModelID explicite et les propriétés de relancement appropriées pour les faire apparaître en tant qu’applications. L’utilisateur peut ensuite les épingler à la barre des tâches et « relancer » l’instance épinglée.

> [!Note]  
> Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini. Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.

 

Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchCommand]() de cette fenêtre.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
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

 

 
