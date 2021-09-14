---
title: Initialisation de la page
description: Initialisation de la page
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Lecteur Windows Media des magasins en ligne, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media des magasins en ligne, initialisation des pages
- magasins en ligne, initialiser des pages
- type 2 magasins en ligne, initialisation des pages
- Lecteur Windows Media, gestionnaire de téléchargement
- Lecteur Windows Media Gestionnaire de téléchargement
- Gestionnaire de téléchargement
- initialisation des pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217033"
---
# <a name="initializing-the-page"></a>Initialisation de la page

Lors du chargement de la page Web, la fonction **init** s’exécute. Ce code extrait tout d’abord toutes les données stockées dans une session précédente. Pour plus d’informations, consultez [mise à jour des informations de session](maintaining-session-information.md). Il crée ensuite l’objet **downloadmanager** et le stocke dans la variable globale nommée g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



Ensuite, la fonction connecte l’événement **OnColorChange** à la fonction nommée **OnAppColor** , puis appelle la fonction directement pour initialiser la couleur d’arrière-plan. consultez [correspondance des couleurs de Lecteur Windows Media](matching-the-windows-media-player-colors.md).

Enfin, la fonction démarre un minuteur avec un intervalle d’une seconde et initialise les zones de liste qui affichent les collections téléchargées en attente et les éléments téléchargés. Cela est important, car il peut y avoir des sessions en cours la dernière fois que le magasin en ligne est fermé et que ces informations doivent être de nouveau affichées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> </dl>

 

 




