---
title: Plug-in de magasin en ligne de type 2
description: Plug-in de magasin en ligne de type 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- tapez 2 magasins en ligne, plug-ins
- Windows Media Player Online stores, interface IWMPSubscriptionService
- magasins en ligne, interface IWMPSubscriptionService
- types 2 magasins en ligne, interface IWMPSubscriptionService
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 2 magasins en ligne
- plug-ins, interface IWMPSubscriptionService
- Plug-ins du lecteur Windows Media, type 2 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, interface IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101356"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in de magasin en ligne de type 2

Un plug-in de magasin en ligne de type 2 est un composant COM qui implémente l’interface [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) et éventuellement l’interface [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) . Le lecteur Windows Media 9 appelle les méthodes de l’interface **IWMPSubscriptionService** . Le lecteur Windows Media 10 ou version ultérieure appelle les méthodes des interfaces **IWMPSubscriptionService** et **IWMPSubscriptionService2** .

Un plug-in de magasin en ligne de type 2 est empaqueté en tant que serveur COM in-process. Autrement dit, le plug-in est implémenté dans un fichier. dll qui est mappé dans le processus du lecteur Windows Media.

Le lecteur Windows Media active les plug-ins de magasin de type 2 en fonction des besoins. Par exemple, supposons que l’utilisateur tente de lire une chanson protégée et qu’il n’y ait pas de licence actuelle pour le lire. Dans ce cas, le lecteur Windows Media inspecte l’attribut **ContentDistributor** dans l’en-tête de fichier ou l’en-tête DRM. S’il existe une valeur qui correspond au nom de clé d’un magasin en ligne, le lecteur Windows Media vérifie le registre pour déterminer si ce magasin en ligne a fourni un plug-in de type 2. Si le plug-in existe, le lecteur Windows Media charge le plug-in et appelle ses méthodes pour déterminer si l’utilisateur dispose des droits nécessaires pour lire la chanson.

La liste suivante décrit certains des scénarios dans lesquels le lecteur Windows Media appelle un plug-in de magasin en ligne de type 2.

-   **L’utilisateur tente de lire le contenu de la boutique en ligne.** Dans ce cas, le lecteur Windows Media appelle la méthode [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) du plug-in, en passant un pointeur vers l’élément multimédia numérique que l’utilisateur tente de lire. Le magasin en ligne peut l’utiliser comme opportunité de mettre à jour la licence de l’utilisateur pour lire le contenu ou interdire la lecture. Si le plug-in retourne la **valeur true** dans le paramètre *PfAllowPlay* , le lecteur Windows Media tente de lire le contenu. La lecture échouera quand une licence valide n’existe pas ; Ce processus ne contourne pas la gestion des droits numériques (DRM).
-   **L’utilisateur demande l’autorisation de graver du contenu sur un CD ou un DVD.** Dans ce cas, le lecteur Windows Media appelle la méthode [IWMPSubscriptionService :: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) du plug-in.
-   **L’utilisateur tente de synchroniser le contenu de la boutique en ligne avec un appareil, ou le lecteur Windows Media est prêt à synchroniser automatiquement le contenu de la boutique en ligne avec un appareil.** Dans ce cas, le lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 ::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) du plug-in pour signaler à la Banque en ligne qu’un élément multimédia est sur le point d’être synchronisé avec un appareil particulier, identifié par son nom canonique. Il s’agit d’une opportunité pour le magasin en ligne de déterminer si l’utilisateur est autorisé à synchroniser l’élément multimédia avec l’appareil. Il est également possible pour le magasin en ligne de préparer l’appareil pour la synchronisation et de mettre à jour les enregistrements, tels que les nombres de synchronisation, associés à l’appareil ou à l’élément multimédia. Le plug-in doit passer l’autorisation, la préparation et les tâches d’enregistrement à un thread distinct et retourner immédiatement à partir de **prepareForSync**. Lorsque le thread distinct a terminé son travail, il doit notifier le lecteur Windows Media en appelant [IWMPSubscriptionServiceCallback :: OnComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Un appareil est disponible pour le traitement en arrière-plan.** Quand un appareil est connecté, le lecteur Windows Media signale au magasin en ligne que l’appareil est disponible et inactif en appelant [IWMPSubscriptionService2 ::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **L’utilisateur clique sur un bouton pour activer un magasin en ligne dans le lecteur Windows Media.** Dans ce cas, le lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 :: serviceEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) du plug-in. Le lecteur Windows Media appelle également cette méthode lorsque l’utilisateur bascule vers un autre service.
-   **Le lecteur Windows Media passe à l’État faible activité.** Dans ce cas, le lecteur appelle la méthode [IWMPSubscriptionService :: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) du plug-in. Le magasin en ligne peut utiliser cette opportunité pour démarrer ou réveiller tous les threads qui effectuent des tâches en arrière-plan, tels que le renouvellement des licences expirées ou la compilation des données de lecture-nombre.
-   **Le lecteur Windows Media passe à l’État activité élevée.** Dans ce cas, le lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 :: stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) du plug-in. Cela indique au plug-in qu’il doit suspendre les threads effectuant des tâches en arrière-plan.

Le lecteur Windows Media diffuse le composant de la Banque d’aide en ligne à la fin de la session du lecteur. Lors de la mise en production, le composant doit interrompre tout traitement en arrière-plan en cours, puis s’arrêter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interface IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Interface IWMPSubscriptionServiceCallback**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Exemples de magasins en ligne de type 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




