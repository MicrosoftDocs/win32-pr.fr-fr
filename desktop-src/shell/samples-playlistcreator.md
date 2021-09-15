---
description: Montre comment créer un verbe qui fonctionne sur un élément de Shell ou un conteneur sélectionné pour créer une sélection.
title: Créateur de playlist, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294719"
---
# <a name="playlist-creator-sample"></a>Créateur de playlist, exemple

Montre comment créer un verbe qui fonctionne sur un élément de Shell ou un conteneur sélectionné pour créer une sélection.

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
| GitHub  | [Exemple PlaylistCreator](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PlaylistCreator** .
2.  Entrez `msbuild PlaylistCreator.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

> [!Note]  
> cet exemple peut également être utilisé avec l’édition Visual C++ Express si la Visual Studio complète n’est pas disponible.

 

1.  ouvrez Windows Explorer et accédez au répertoire du projet **PlaylistCreator** .
2.  Double-cliquez sur l’icône du fichier PlaylistCreator. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.
    > [!Note]  
    > si vous compilez 64 bits à l’aide de l’édition Visual C++ Express, vous devez utiliser le compilateur croisé x64 fourni avec le SDK Windows.

     

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  Sur la ligne de commande, entrez `PlaylistCreator.exe` . vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de PlaylistCreator.exe.
3.  cliquez avec le bouton droit sur un fichier ou un dossier de musique contenant des fichiers musicaux dans Windows Explorer afin de créer une sélection pour afficher le menu contextuel.
4.  Vous pouvez créer une sélection. m3u ou. wpl. Les sélections sont créées dans le `%userprofile%\Music\Playlists` dossier.
    > [!Note]  
    > vous trouverez de nouveaux verbes dans le menu contextuel dans le dossier **Musique** , les piles musicales, les piles de la **bibliothèque Musique** et les collections de fichiers musicaux.

     

 

 



