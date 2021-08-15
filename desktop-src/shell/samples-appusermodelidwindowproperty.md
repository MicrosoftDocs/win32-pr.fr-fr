---
description: Montre comment contrôler le comportement de regroupement de la barre des tâches des fenêtres d’une application par le biais de la propriété System.AppUserModel.ID.
title: Propriété de fenêtre d’ID de modèle d’utilisateur d’application, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a6a4b0daca8b6bd4147c1e36d921b58b3802d975e678e49a9b9153761e61820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219879"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Exemple de propriété de fenêtre AppID (application User Model ID)

Montre comment contrôler le comportement de regroupement de la barre des tâches des fenêtres d’une application par le biais de la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple montre comment définir la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) à l’aide de l’implémentation [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la fenêtre, obtenue par le biais de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Configuration requise



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AppUserModelIDWindowProperty** .
2.  Entrez `msbuild AppUserModelIDWindowProperty.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **AppUserModelIDWindowProperty** .
2.  Double-cliquez sur l’icône du fichier AppUserModelIDWindowProperty. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  Sur la ligne de commande, entrez `AppUserModelIDWindowProperty.exe` . vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de AppUserModelIDWindowProperty.exe.
3.  Pour illustrer l’effet des ID de modèle utilisateur de l’application (AppUserModelIDs) sur le regroupement de la barre des tâches, lancez au moins trois instances de l’application en même temps.
4.  Utilisez le menu pour définir une valeur AppUserModelID différente sur chacune des trois fenêtres. Notez que chaque AppUserModelID distincte produit un bouton distinct de la barre des tâches et que Windows peut modifier son identité au moment de l’exécution.
5.  Définissez au moins deux fenêtres à la seconde AppUserModelID. Notez qu’ils se déplacent tous deux dans le même groupe de la barre des tâches.
6.  Ouvrez la fenêtre **des propriétés de la barre des tâches et du menu Démarrer** en cliquant avec le bouton droit sur la barre des tâches et en sélectionnant **Propriétés** dans le menu contextuel. Modifiez les **boutons de la barre des tâches :** liste déroulante entre la **combinaison lorsque la barre des tâches est complète** et **ne jamais combiner** les valeurs. Notez que chaque fenêtre peut obtenir un bouton distinct, mais que les boutons sont regroupés par AppUserModelID.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
