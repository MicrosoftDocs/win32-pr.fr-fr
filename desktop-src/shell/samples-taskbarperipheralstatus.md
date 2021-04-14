---
description: Présente les superpositions d’icône de barre des tâches et les barres de progression.
title: État du périphérique de barre des tâches, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991745"
---
# <a name="taskbar-peripheral-status-sample"></a>État du périphérique de barre des tâches, exemple

Présente les superpositions d’icône de barre des tâches et les barres de progression.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple crée un exemple de bouton de la barre des tâches sur lequel il illustre l’utilisation de [**ITaskbarList3 :: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) en vous permettant d’appliquer plusieurs superpositions choisies à partir d’un menu.

L’exemple offre également la possibilité de simuler un indicateur de progression sur le bouton, en illustrant l’utilisation de [**ITaskbarList3 :: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) et [**ITaskbarList3 :: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) en affichant au début un indicateur de progression indéterminé (TBPF \_ indéterminé), puis un indicateur proportionnel normal (TBPF \_ normal).

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple TaskBarPeripheralStatus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **TaskbarPeripheralStatus** .
2.  Entrez `msbuild PeripheralStatus.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **TaskbarPeripheralStatus** .
2.  Double-cliquez sur l’icône du fichier PeripheralStatus. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable (par exemple,) à l' `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` aide de l’invite de commandes ou de l’Explorateur Windows.

    -   Si vous utilisez la ligne de commande, entrez `PeripheralStatus.exe` .
    -   Si vous utilisez l’Explorateur Windows, double-cliquez sur l’icône de PeripheralStatus.exe.

    Une nouvelle fenêtre s’ouvre, avec un bouton de barre des tâches associé.

2.  Pour illustrer les superpositions, choisissez superposition **1** ou **superposition 2** dans le menu **État du périphérique** de la fenêtre. La superposition choisie s’affiche sur le bouton de la barre des tâches. Pour supprimer la superposition, choisissez **effacer la superposition**.
3.  Pour illustrer la barre de progression, choisissez **simuler la progression** dans le menu **État du périphérique** de la fenêtre. Le bouton de la barre des tâches affiche un indicateur de progression indéterminé, puis passe à un indicateur normal.
4.  Choisissez **quitter** dans le menu **fichier** de la fenêtre pour mettre fin au programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extensions de la barre des tâches](taskbar-extensions.md)
</dt> </dl>

 

 



