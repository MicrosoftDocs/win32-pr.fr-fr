---
description: Notifications de fin de flux
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Notifications de fin de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b83552d1c03bbb90062c2eec672ac122a2cbdc498f58d01817bd1a26e8f02b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997849"
---
# <a name="end-of-stream-notifications"></a>Notifications de fin de flux

Lorsqu’un filtre source a terminé l’envoi de données, il appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée en aval. Le filtre en aval propage l’appel au filtre suivant, et ainsi de suite. lorsque l’appel **EndOfStream** atteint le convertisseur, le convertisseur envoie un événement [**EC \_ complet**](ec-complete.md) à Filter Graph Manager. Si le convertisseur a plusieurs broches d’entrée, il remet l' \_ événement EC complet après chaque broche d’entrée a reçu la notification de fin de flux.

Un filtre doit sérialiser les appels [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) avec d’autres appels de streaming, tels que [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive). (En d’autres termes, le filtre en aval doit toujours recevoir les appels dans le bon ordre.)

Dans certains cas, un filtre en aval peut détecter la fin du flux avant que le filtre source ne le fasse. (Par exemple, le filtre en aval peut analyser le flux.) Dans ce cas, le filtre en aval peut envoyer la notification de fin de flux. dans ce cas, il doit retourner S \_ false à partir de [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) jusqu’à ce que le graphique s’arrête ou vide. La \_ valeur de retour false indique au filtre source d’arrêter l’envoi de données.

### <a name="default-handling-of-ec_complete"></a>Gestion par défaut de l’EC \_ Complete

par défaut, le gestionnaire de Graph de filtre ne transfère pas tous \_ les événements EC complet à l’application. Au lieu de cela, il attend que tous les flux aient des signaux EC \_ complets, puis envoie un seul \_ événement EC Complete. Ainsi, l’application reçoit l’événement une fois que chaque flux est terminé.

pour déterminer le nombre de flux, le gestionnaire de Graph de filtre compte le nombre de filtres qui prennent en charge la recherche (via [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)) et ont une broche d’entrée *rendue* , qui est définie comme une broche d’entrée sans sortie correspondante. le gestionnaire de Graph de filtre détermine si un code confidentiel est rendu de l’une des deux façons suivantes :

-   La méthode [**IPIN :: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) du pin retourne zéro dans le paramètre *nPin* .
-   Le filtre expose l’interface [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) et retourne l' \_ indicateur de \_ convertisseur des indicateurs divers du filtre AM \_ \_ \_ .

### <a name="end-of-stream-notifications-in-pull-mode"></a>Notifications de fin de flux en mode par extraction

Dans une connexion [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) , le filtre source n’envoie pas de notification de fin de flux. Instread, cette opération est effectuée par le filtre en aval, qui est généralement un filtre d’analyseur. L’analyseur envoie l’appel [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en aval. Elle n’envoie pas un en amont au filtre source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transmission de la fin du flux](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



