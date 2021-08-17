---
title: Exemple d’animation Application-Driven
description: affiche Windows Animation dans la configuration pilotée par l’application à l’aide de Direct2D pour animer la couleur d’arrière-plan d’une fenêtre et la synchronisation avec la fréquence d’actualisation.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfbb5ce71ddeff6a37c2d872e0e1e93fdc58cde9fcc8359560d9d386ba7a0834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137372"
---
# <a name="application-driven-animation-sample"></a>Exemple d’animation Application-Driven

affiche Windows Animation dans la configuration pilotée par l’application à l’aide de Direct2D pour animer la couleur d’arrière-plan d’une fenêtre et la synchronisation avec la fréquence d’actualisation.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement                               | Chemin d’accès/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de développement logiciel Windows | [Kit de développement logiciel (sdk) Microsoft Windows 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galerie de code                           | [Windows Exemple de code du gestionnaire d’animations](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation. par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples.

## <a name="building-the-sample"></a>Génération de l'exemple

Utilisez l’une des méthodes suivantes pour générer l’exemple.

**Pour générer l’exemple à partir de l’invite de commandes**

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet AppDriven. par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Multimedia \\ WindowsAnimation \\ AppDriven.

2.  Exécutez la commande suivante : **MSBuild AppDriven. sln**

**pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**

1.  ouvrez Windows Explorer et accédez au répertoire du projet AppDriven.

2.  Double-cliquez sur l’icône du fichier AppDriven. sln pour ouvrir le projet dans Visual Studio.

    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio Solution ».

     

3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple :

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.

2.  exécutez **AppDriven.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de AppDriven.exe dans Windows Explorer.

3.  Cliquez n’importe où dans la zone cliente et la couleur d’arrière-plan de la fenêtre passe à une couleur aléatoire.

 

 




