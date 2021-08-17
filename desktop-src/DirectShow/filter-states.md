---
description: États de filtre
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: États de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015737"
---
# <a name="filter-states"></a>États de filtre

Les filtres ont trois États possibles : arrêté, suspendu et en cours d’exécution. L’objectif de l’état suspendu est de signaler des données dans le graphique, afin qu’une commande Run réponde immédiatement. le gestionnaire de Graph de filtre contrôle toutes les transitions d’état. quand une application appelle [**imediacontrol :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**imediacontrol ::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)ou [**imediacontrol :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), le gestionnaire de Graph de filtre appelle la méthode [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) correspondante sur tous les filtres. les transitions entre arrêt et exécution passent toujours par l’état en pause. par conséquent, si l’application appelle **s’exécuter** sur un graphique arrêté, le gestionnaire de Graph de filtre interrompt le graphique avant de l’exécuter.

Pour la plupart des filtres, les États en cours d’exécution et en pause sont identiques. Examinez le graphique de filtre suivant :

Convertisseur de > de > source

Supposons que le filtre source ne soit pas une source de capture dynamique. Quand le filtre source est suspendu, il crée un thread qui génère de nouvelles données et les écrit dans des exemples de média aussi rapidement que possible. Le thread « pousse » les exemples en aval en appelant [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée du filtre de transformation. Le filtre de transformation reçoit les exemples sur le thread du filtre source. Il peut utiliser un thread de travail pour remettre les exemples au convertisseur, mais il les remet généralement sur le même thread. Pendant que le convertisseur est suspendu, il attend de recevoir un exemple. Une fois qu’il en reçoit un, il bloque et maintient cet exemple indéfiniment. S’il s’agit d’un convertisseur vidéo, il affiche l’échantillon sous la forme d’une image d’affiche, en redessinant l’image si nécessaire.

À ce stade, le flux est entièrement qualifié et prêt pour le rendu. Si le graphique reste en pause, les échantillons se « accumulent » dans le graphique derrière le premier exemple, jusqu’à ce que chaque filtre soit bloqué dans [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Cependant, aucune donnée n’est perdue. Une fois que le thread source est débloqué, il reprend simplement à partir du point où il est bloqué.

Le filtre source et le filtre de transformation ignorent le passage de l’état suspendu à l’État en cours d’exécution. ils continuent simplement à traiter les données aussi rapidement que possible. Toutefois, lorsque le convertisseur s’exécute, il démarre le rendu des exemples. Tout d’abord, il restitue l’exemple qu’il a conservé pendant qu’il a été suspendu. Ensuite, chaque fois qu’il reçoit un nouvel échantillon, il calcule l’heure de présentation de l’exemple. (Pour plus d’informations, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).) Le convertisseur conserve chaque échantillon jusqu’à l’heure de la présentation, à partir duquel il affiche l’exemple. Pendant qu’il attend l’heure de la présentation, il bloque la méthode de [**réception**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou reçoit de nouveaux exemples sur un thread de travail avec une file d’attente. Les filtres en amont du convertisseur ne sont pas impliqués dans la planification.

Les sources en direct, telles que les appareils de capture, sont une exception à cette architecture générale. Avec une source dynamique, il n’est pas approprié de signaler des données à l’avance. L’application peut suspendre le graphique et attendre un certain temps avant de l’exécuter. Le graphique ne doit pas restituer des exemples « obsolètes ». Par conséquent, une source dynamique ne produit aucun échantillon en pause, uniquement lors de l’exécution. pour signaler ce fait au gestionnaire de Graph de filtre, la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) du filtre source retourne \_ VFW \_ s \_ . Ce code de retour indique que le filtre est passé à l’état suspendu, même si le convertisseur n’a pas reçu de données.

Lorsqu’un filtre s’arrête, il rejette tout autre échantillon qui lui est remis. Les filtres sources arrêtent leurs threads de diffusion en continu et d’autres filtres arrêtent les threads de travail qu’ils ont pu créer. Épingle les allocateurs à la validation.

### <a name="state-transitions"></a>Transitions d’état

le gestionnaire de Graph du filtre effectue toutes les transitions d’état dans l’ordre ascendant, en commençant par le convertisseur et en remontant jusqu’au filtre source. Ce classement est nécessaire pour empêcher la suppression des exemples et empêcher le blocage du graphique. Les transitions d’état les plus importantes sont comprises entre pause et arrêt :

-   Arrêté pour être suspendu : lorsque chaque filtre est suspendu, il est prêt à recevoir des exemples à partir du filtre suivant. Le filtre source est le dernier à être suspendu. Il crée le thread de streaming et commence à envoyer des exemples. Étant donné que tous les filtres en aval sont suspendus, aucun filtre ne rejette les échantillons. le gestionnaire de Graph de filtre n’effectue pas la transition tant que chaque convertisseur du graphique n’a pas reçu d’exemple (à l’exception des sources en direct, comme décrit précédemment).
-   Suspendu à arrêté : lorsqu’un filtre s’arrête, il libère tous les exemples qu’il contient, qui débloque les filtres en amont en attente dans [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Si le filtre attend une ressource à l’intérieur de la méthode [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , il cesse d’attendre et retourne de **Receive**, ce qui débloque le filtre appelant. par conséquent, lorsque le gestionnaire de Graph de filtre arrête le filtre amont suivant, ce filtre n’est pas bloqué dans **GetBuffer** ou **Receive** et peut répondre à la commande stop. Le filtre amont peut fournir quelques exemples supplémentaires avant d’obtenir la commande arrêter, mais le filtre en aval les rejette simplement, car il est déjà arrêté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[données Flow dans le filtre Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



