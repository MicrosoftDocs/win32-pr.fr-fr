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
ms.openlocfilehash: 332d9c907e7c25f81d01bc8adf48c6d4d91a7b17763a1b0daf0007a8534ac4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934738"
---
# <a name="flow-of-control"></a>Flow de contrôle

les données Audio entrent en Lecteur Windows Media en continu via un fichier ou un flux. Ces données sont transmises à votre visualisation. vous dessinez sur une surface définie et repassez cette surface à Lecteur Windows Media. Cet échange se produit plusieurs fois par seconde et, pour l’utilisateur, le résultat est une animation agréable qui se déplace dans le temps jusqu’à la musique.

Voici la séquence spécifique du déroulement du programme de visualisation :

1.  à un intervalle de temps, Lecteur Windows Media prend un instantané de l’audio qui est joué.
2.  Lecteur Windows Media fournit les données de cet instantané à votre visualisation via la fonction **Render** et la fonction **RenderWindowed** .
3.  Vous devez écrire du code qui s’exécutera lors de l’appel de **Render** et **RenderWindowed** . votre code dessine à l’aide d’un contexte de périphérique défini par Lecteur Windows Media lors du rendu sans fenêtre, ou à l’aide d’une fenêtre que vous créez lors du rendu de fenêtre.
4.  dans une région spécifiée par l’apparence actuelle, Lecteur Windows Media affiche ce que votre code a dessiné.
5.  Ce processus se répète plusieurs fois par seconde, créant ainsi des animations graphiques chronométrées à la musique. Lorsque la musique s’arrête, la visualisation s’arrête.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble du développeur**](developer-overview.md)
</dt> </dl>

 

 




