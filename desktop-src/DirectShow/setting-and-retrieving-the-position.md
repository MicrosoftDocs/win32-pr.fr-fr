---
description: Définition et récupération de la position
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Définition et récupération de la position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745412"
---
# <a name="setting-and-retrieving-the-position"></a>Définition et récupération de la position

Le graphique de filtre conserve deux valeurs de position, la position actuelle et la position d’arrêt. Ceux-ci sont définis comme suit :

-   Lorsque le graphique est en cours d’exécution, la position actuelle est la position de lecture actuelle, par rapport au début de la source. Lorsque le graphique est arrêté ou suspendu, la position actuelle est le point où la diffusion en continu commence à la prochaine exécution de la commande.
-   La position d’arrêt est le point où le flux se termine. Lorsque le graphique atteint la position d’arrêt, aucune donnée n’est diffusée en continu, et le gestionnaire de graphique de filtre publie un événement [**ce \_ complet**](ec-complete.md) . (Toutefois, le graphique ne bascule pas automatiquement vers un état arrêté. Pour plus d’informations, consultez [réponse aux événements](responding-to-events.md).)

Pour récupérer ces valeurs, appelez la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) . Les valeurs retournées sont toujours relatives à la source du média d’origine. Par défaut, les valeurs sont en unités de temps de référence. Dans certains cas, vous pouvez modifier les unités de temps. Pour plus d’informations, consultez [formats d’heure pour les commandes de recherche](time-formats-for-seek-commands.md).

Pour rechercher une nouvelle position ou définir une nouvelle position d’arrêt, appelez la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , comme indiqué dans l’exemple suivant :


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> Une seconde est 10 millions unités de temps de référence. Pour plus de commodité, l’exemple définit cette valeur comme une \_ seconde. Si vous utilisez la bibliothèque de classes de base DirectShow, les unités constantes ont la même valeur.

 

Le paramètre *rtNow* spécifie la nouvelle position actuelle. Le deuxième paramètre est un indicateur qui définit comment interpréter *rtNow*. Dans cet exemple, l' \_ indicateur AM recherché \_ AbsolutePositioning indique que *rtNow* spécifie une position absolue dans la source. Par conséquent, le graphique de filtre effectue une recherche sur une position de deux secondes à partir du début du flux. Le paramètre *rtStop* indique l’heure d’arrêt. Le dernier paramètre spécifie que *rtStop* est également une position absolue.

Pour spécifier une position par rapport à la valeur de position précédente, utilisez l' \_ indicateur AM recherché \_ RelativePositioning. Pour ne pas modifier l’une des valeurs de position, utilisez l' \_ indicateur AM recherché \_ noposition. Dans ce cas, le paramètre de temps correspondant peut avoir la **valeur null** . L’exemple suivant recherche par progression de 10 secondes, mais laisse la position d’arrêt inchangée :


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Si le graphique de filtre est arrêté, le convertisseur vidéo ne met pas à jour l’image après une opération de recherche. Pour l’utilisateur, il apparaît comme si la recherche ne s’est pas déproduite. Pour mettre à jour l’image, suspendez le graphique après l’opération de recherche. La suspension du graphique signale une nouvelle image vidéo pour le convertisseur vidéo. Vous pouvez utiliser la méthode [**IMediaControl :: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , qui suspend le graphique, puis l’arrête.

 

 



