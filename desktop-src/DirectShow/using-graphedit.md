---
description: Utilisation de GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Utilisation de GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529523"
---
# <a name="using-graphedit"></a>Utilisation de GraphEdit

GraphEdit est disponible dans le kit de développement logiciel (SDK) Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

Le nom de l’application GraphEdit est « graphedt.exe ». Une fois que vous avez installé le kit de développement logiciel (SDK), « graphedt.exe » se trouve dans le répertoire suivant : \[ Program Files \] \\ Microsoft SDK \\ Windows \\ \[ version \] \\ bin \\ .

Avant d’exécuter GraphEdit, utilisez l’utilitaire regsvr32 pour inscrire les dll suivantes, qui se trouvent dans le même répertoire :

-   proppage.dll
-   evrprop.dll

Ces dll permettent à GraphEdit d’afficher des pages de propriétés pour certains des filtres DirectShow intégrés.

## <a name="build-a-file-playback-graph"></a>Créer un graphique de lecture de fichier

GraphEdit peut générer un graphique de filtre pour la lecture de fichiers. Cette fonctionnalité est équivalente à l’appel de la méthode [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) dans une application. Dans le menu **fichier** , cliquez sur **afficher le fichier multimédia**. GraphEdit affiche une boîte de dialogue **ouvrir un fichier** . Sélectionnez un fichier multimédia, puis cliquez sur **ouvrir**. GraphEdit crée un graphique de filtre pour lire le fichier que vous avez sélectionné.

Vous pouvez également afficher un fichier multimédia situé dans une URL. Dans le menu **fichier** , cliquez sur **afficher l’URL**. GraphEdit affiche une boîte de dialogue dans laquelle vous pouvez taper l’URL.

## <a name="build-a-filter-graph"></a>Créer un graphique de filtre

GraphEdit peut créer un graphique de filtre personnalisé à l’aide de n’importe quel filtre enregistré sur votre système. Dans le menu **graphique** , cliquez sur **Insérer des filtres**. Une boîte de dialogue s’affiche avec une liste des filtres sur votre système, organisés par catégorie de filtre. GraphEdit génère cette liste à partir des informations du Registre. L’illustration suivante montre la boîte de dialogue.

![Quels filtres voulez-vous insérer ?](images/gedit12.png)

Pour ajouter un filtre au graphique, sélectionnez le nom du filtre, cliquez sur le bouton **Insérer des filtres** ou double-cliquez sur le nom du filtre. Une fois que vous avez ajouté les filtres, vous pouvez connecter deux filtres en faisant glisser la souris de la broche de sortie d’un filtre vers la broche d’entrée d’un autre filtre. Si les codes confidentiels acceptent la connexion, GraphEdit dessine une flèche les connectant.

![connexion de deux filtres](images/gedit-connect.png)

## <a name="run-the-graph"></a>Exécuter le graphique

Une fois que vous avez créé un graphique de filtre dans la modification de graphique, vous pouvez exécuter le graphique pour voir s’il fonctionne comme prévu. Le menu **graphique** contient les commandes de menu **lecture**, **Pause** et **arrêt**. Ces commandes appellent respectivement les [](/windows/desktop/api/Control/nn-control-imediacontrol) méthodes IMediaControl [**exécuter**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**suspendre**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)et [**arrêter**](/windows/desktop/api/Control/nf-control-imediacontrol-stop). La barre d’outils GraphEdit contient également des boutons pour ces commandes :

![boutons suspendre, lire et arrêter](images/gedit-toolbar.png)

> [!Note]  
> La commande GraphEdit **Stop** interrompt d’abord le graphique et cherche à l’heure zéro (en supposant que le graphique est recherché). Pour la lecture de fichier, cette action réinitialise la fenêtre vidéo sur le premier frame. GraphEdit appelle [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Si le graphique est recherché, vous pouvez le Rechercher en faisant glisser la barre de curseur qui apparaît sous la barre d’outils. Si vous faites glisser la barre du curseur, la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) est appelée.

## <a name="view-property-pages"></a>Afficher les pages de propriétés

Certains filtres prennent en charge des pages de propriétés personnalisées, qui fournissent une interface utilisateur pour définir des propriétés sur le filtre. Pour afficher la page de propriétés d’un filtre dans GraphEdit, cliquez avec le bouton droit sur le filtre et sélectionnez **Propriétés** dans la fenêtre contextuelle. GraphEdit affiche une page de propriétés qui contient les feuilles de propriétés définies par le filtre (le cas échéant). En outre, GraphEdit comprend une feuille de propriétés pour chaque code confidentiel sur le filtre. Les feuilles de propriétés de code confidentiel sont définies par GraphEdit, et non par le filtre. Si le code PIN est connecté, la feuille de propriétés du code confidentiel affiche le type de média pour la connexion. Dans le cas contraire, elle répertorie les types de média préférés du pin.

> [!Note]  
> Pour utiliser les pages de propriétés intégrées de GraphEdit, vous devez inscrire proppage.dll. Cette DLL est disponible dans le SDK Windows. La DLL contient également des pages de propriétés supplémentaires pour certains filtres DirectShow. Ces pages de propriétés sont fournies à des fins de débogage uniquement.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Simulation de la génération de graphiques avec GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



