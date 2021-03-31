---
description: Montre comment créer un verbe qui fonctionne sur des éléments de Shell et des conteneurs qui lit des éléments ou ajoute des éléments à une file d’attente.
title: Player, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203258"
---
# <a name="player-verb-sample"></a>Player, exemple de verbe

Montre comment créer un verbe qui fonctionne sur des éléments de Shell et des conteneurs qui lit des éléments ou ajoute des éléments à une file d’attente. Cet exemple est particulièrement utile pour les applications multimédias.

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
| GitHub  | [Exemple PlayerVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PlayerVerbSample** .
2.  Entrez `msbuild PlayerVerbSample.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **PlayerVerbSample** .
2.  Double-cliquez sur l’icône du fichier PlayerVerbSample. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Sur la ligne de commande, entrez `PlayerVerbSample.exe` . Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de PlayerVerbSample.exe.
3.  Sélectionnez `Register Verbs` dans la boîte de dialogue **exemple de verbe de joueur** .
4.  Cliquez avec le bouton droit sur les éléments d’image (fichier, dossier ou pile) dans l’Explorateur Windows pour les ajouter à une file d’attente ou les lire dans l’exemple d’application. Utilisez des éléments musicaux lorsque vous modifiez l’exemple pour utiliser de la musique.

 

 



