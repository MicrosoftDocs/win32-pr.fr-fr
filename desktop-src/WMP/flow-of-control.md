---
title: Flow de contrôle
description: Flow de contrôle
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualisations, déroulement du programme
- visualisations personnalisées, déroulement du programme
- visualisations, Flow Control
- visualisations personnalisées, Flow Control
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- visualisations, fonction RenderWindow
- visualisations personnalisées, fonction RenderWindow
- Fonction Render, déroulement du programme de visualisation
- RenderWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939724"
---
# <a name="flow-of-control"></a>Flow de contrôle

Les données audio arrivent en permanence dans le lecteur Windows Media via un fichier ou un flux. Ces données sont transmises à votre visualisation. Vous dessinez sur une surface définie et repassez cette surface au lecteur Windows Media. Cet échange se produit plusieurs fois par seconde et, pour l’utilisateur, le résultat est une animation agréable qui se déplace dans le temps jusqu’à la musique.

Voici la séquence spécifique du déroulement du programme de visualisation :

1.  À un intervalle de temps, le lecteur Windows Media prend un instantané de l’audio qui est joué.
2.  Le lecteur Windows Media fournit les données de cet instantané à votre visualisation via la fonction **Render** et la fonction **RenderWindowed** .
3.  Vous devez écrire du code qui s’exécutera lors de l’appel de **Render** et **RenderWindowed** . Votre code dessine à l’aide d’un contexte de périphérique défini par le lecteur Windows Media lors du rendu sans fenêtre, ou à l’aide d’une fenêtre que vous créez lors du rendu de fenêtre.
4.  Dans une région spécifiée par l’apparence actuelle, le lecteur Windows Media affiche ce que votre code a dessiné.
5.  Ce processus se répète plusieurs fois par seconde, créant ainsi des animations graphiques chronométrées à la musique. Lorsque la musique s’arrête, la visualisation s’arrête.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble du développeur**](developer-overview.md)
</dt> </dl>

 

 




