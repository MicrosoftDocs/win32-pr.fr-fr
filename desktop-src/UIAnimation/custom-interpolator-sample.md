---
title: Exemple d’interpolateur personnalisé
description: montre comment utiliser Windows Animation avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c801822bd50eebe9f405cad00bc8ffcd7ac2d611924a3ff0bae91d30bc9f249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999699"
---
# <a name="custom-interpolator-sample"></a>Exemple d’interpolateur personnalisé

montre comment utiliser Windows Animation avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu. Les exemples d’images sont chargés à partir de la bibliothèque d’images.

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

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet CustomInterpolator. par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Multimedia \\ WindowsAnimation \\ CustomInterpolator

2.  Exécutez la commande suivante : **MSBuild CustomInterpolator. sln**

**pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**

1.  ouvrez Windows Explorer et accédez au répertoire du projet CustomInterpolator.

    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio Solution ».

     

2.  Double-cliquez sur l’icône du fichier CustomInterpolator. sln pour ouvrir le projet dans Visual Studio.

3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple :

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.

2.  exécutez **CustomInterpolator.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de CustomInterpolator.exe dans Windows Explorer.
3.  Redimensionnez la fenêtre ou appuyez sur la barre d’espace, et les images se réorganiseront de manière aléatoire au milieu de la zone cliente.

4.  Appuyez sur la flèche haut ou bas. les images s’accélèrent vers le haut ou le bas de la zone cliente.

 

 




