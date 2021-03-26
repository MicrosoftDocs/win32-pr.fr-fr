---
description: Illustre une barre d’outils miniatures, un contrôle de barre d’outils actif incorporé dans la miniature d’une fenêtre, utilisé pour fournir l’accès aux commandes clés d’une fenêtre sans effectuer la restauration de l’utilisateur ou activer la fenêtre de l’application.
title: Barre d’outils de miniatures de barre des tâches, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973534"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Barre d’outils de miniatures de barre des tâches, exemple

Illustre une barre d’outils miniatures, un contrôle de barre d’outils actif incorporé dans la miniature d’une fenêtre, utilisé pour fournir l’accès aux commandes clés d’une fenêtre sans effectuer la restauration de l’utilisateur ou activer la fenêtre de l’application.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple montre comment fournir une barre d’outils simple à un aperçu miniature de la barre des tâches. La barre d’outils se compose de trois boutons. En cliquant sur un bouton, une fenêtre s’affiche pour confirmer que le bouton a été activé. Les API suivantes sont illustrées :

-   [**ITaskbarList3 :: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3 :: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) , structure

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple TaskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **TaskbarThumbnailToolbar** .
2.  Entrez `msbuild ThumbnailToolbar.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **TaskbarThumbnailToolbar** .
2.  Double-cliquez sur l’icône du fichier ThumbnailToolbar. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable (par exemple,) à l' `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` aide de l’invite de commandes ou de l’Explorateur Windows.

    -   Si vous utilisez la ligne de commande, entrez `ThumbnailToolbar.exe` .
    -   Si vous utilisez l’Explorateur Windows, double-cliquez sur l’icône de ThumbnailToolbar.exe.

    Une nouvelle fenêtre s’ouvre, avec un bouton de barre des tâches associé.

2.  Placez le curseur sur le bouton **ThumbnailToolbar** de la barre des tâches pour afficher l’aperçu. Cliquez sur l’un des trois boutons (vert, jaune, rouge) affichés dans la barre d’outils de l’aperçu.
3.  Choisissez **quitter** dans le menu **fichier** de la fenêtre pour mettre fin au programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extensions de la barre des tâches](taskbar-extensions.md)
</dt> </dl>

 

 



