---
description: Heures d’horloge
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Heures d’horloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239087"
---
# <a name="clock-times"></a>Heures d’horloge

DirectShow définit deux heures d’horloge associées : le temps de référence et le temps de flux.

-   Le *temps de référence* est l’heure absolue retournée par l’horloge de référence. (Voir [horloges de référence](reference-clocks.md).)
-   Le *temps de flux* est défini par rapport au moment où l’exécution du dernier graphique a commencé.
    -   Pendant que le graphique est en cours d’exécution, le temps de flux est égal à l’heure de référence moins l’heure de début.
    -   Lorsque le graphique est suspendu, le temps de flux reste à l’heure du flux lorsqu’il a été suspendu.
    -   Après une opération de recherche, le temps de flux se réinitialise à zéro.
    -   Lorsque le graphique est arrêté, le temps de flux n’est pas défini.

Quand un échantillon de média a un horodatage *t*, cela signifie que l’exemple doit être rendu au temps de flux *t*. C’est la raison pour laquelle le temps de flux est également appelé *heure de présentation*.

quand une application appelle [**IMediaControl :: run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique de filtre, le gestionnaire de Graphs de filtre appelle [**IMediaFilter :: run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) sur chaque filtre. pour compenser le temps de démarrage de l’exécution des filtres, le gestionnaire de Graph de filtre spécifie une heure de début à l’avenir.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Horodatages](time-stamps.md)
</dt> </dl>

 

 



