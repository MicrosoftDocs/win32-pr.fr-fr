---
description: montre comment écouter les notifications de modification de l’interpréteur de commandes sur un dossier ou un élément de l’espace de noms Windows Explorer.
title: Observateur de notification de changement, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196456"
---
# <a name="change-notify-watcher-sample"></a>Observateur de notification de changement, exemple

montre comment écouter les notifications de modification de l’interpréteur de commandes sur un dossier ou un élément de l’espace de noms Windows Explorer.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple ChangeNotifyWatcher](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ChangeNotifyWatcher** .
2.  Entrez `msbuild ChangeNotifyWatcher.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **ChangeNotifyWatcher** .
2.  Double-cliquez sur l’icône du fichier ChangeNotifyWatcher. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  À l'invite de commandes, entrez `ChangeNotifyWatcher.exe`. vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de ChangeNotifyWatcher.exe.
3.  pour illustrer l’effet, les id de modèle d’utilisateur d’Application (AppUserModelIDs) sélectionnent un dossier à surveiller en cliquant sur **« Pick... »** ou en utilisant le glisser-déplacer sur un dossier à partir d’une fenêtre de l’explorateur de Windows dans l’affichage de liste de l’exemple.

 

 



