---
title: Exemple d’animation Timer-Driven
description: Montre comment utiliser l’animation Windows avec le minuteur d’animation, tout en utilisant GDI+ pour animer la couleur d’arrière-plan d’une fenêtre.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314585"
---
# <a name="timer-driven-animation-sample"></a>Exemple d’animation Timer-Driven

Montre comment utiliser l’animation Windows avec le minuteur d’animation, tout en utilisant GDI+ pour animer la couleur d’arrière-plan d’une fenêtre.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement                               | Chemin d’accès/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de développement logiciel Windows | [Kit de développement logiciel (SDK) Microsoft Windows 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galerie de code                           | [Exemple de code du gestionnaire d’animations Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation. Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.

## <a name="building-the-sample"></a>Génération de l'exemple

Utilisez l’une des méthodes suivantes pour générer l’exemple.

**Pour générer l’exemple à partir de l’invite de commandes**

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet TimerDriven. Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ TimerDriven.

2.  Exécutez la commande suivante : **MSBuild TimerDriven. sln**

**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet TimerDriven.

2.  Double-cliquez sur l’icône du fichier TimerDriven. sln pour ouvrir le projet dans Visual Studio.

    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».

     

3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple :

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.

2.  Exécutez **TimerDriven.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de TimerDriven.exe dans l’Explorateur Windows.

3.  Cliquez n’importe où dans la zone cliente et la couleur d’arrière-plan de la fenêtre passe à une couleur aléatoire.

 

 




