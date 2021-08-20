---
title: Plug-in de magasin en ligne de type 2
description: Plug-in de magasin en ligne de type 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Lecteur Windows Media des magasins en ligne, plug-ins
- magasins en ligne, plug-ins
- tapez 2 magasins en ligne, plug-ins
- Lecteur Windows Media des magasins en ligne, interface IWMPSubscriptionService
- magasins en ligne, interface IWMPSubscriptionService
- types 2 magasins en ligne, interface IWMPSubscriptionService
- plug-ins, Lecteur Windows Media magasins en ligne
- plug-ins, magasins en ligne
- plug-ins, type 2 magasins en ligne
- plug-ins, interface IWMPSubscriptionService
- Lecteur Windows Media les plug-ins, tapez 2 magasins en ligne
- plug-ins Lecteur Windows Media, magasins en ligne
- plug-ins Lecteur Windows Media, Lecteur Windows Media les magasins en ligne
- plug-ins Lecteur Windows Media, interface IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254fe0aeed0d03f4437c408f4c00c181fdeb07cf75df8ff9d7a1139ea284150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117476"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in de magasin en ligne de type 2

Un plug-in de magasin en ligne de type 2 est un composant COM qui implémente l’interface [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) et éventuellement l’interface [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) . Lecteur Windows Media 9 appelle les méthodes de l’interface **IWMPSubscriptionService** . Lecteur Windows Media 10 ou version ultérieure appelle les méthodes des interfaces **IWMPSubscriptionService** et **IWMPSubscriptionService2** .

Un plug-in de magasin en ligne de type 2 est empaqueté en tant que serveur COM in-process. autrement dit, le plug-in est implémenté dans un fichier de .dll qui est mappé dans le processus de Lecteur Windows Media.

Lecteur Windows Media active les plug-ins de magasin en ligne de type 2 en fonction des besoins. Par exemple, supposons que l’utilisateur tente de lire une chanson protégée et qu’il n’y ait pas de licence actuelle pour le lire. dans ce cas, Lecteur Windows Media inspecte l’attribut **ContentDistributor** dans l’en-tête de fichier ou l’en-tête DRM. s’il existe une valeur qui correspond au nom de clé d’un magasin en ligne, Lecteur Windows Media vérifie le registre pour déterminer si ce magasin en ligne a fourni un plug-in de type 2. si le plug-in existe, Lecteur Windows Media charge le plug-in et appelle ses méthodes pour déterminer si l’utilisateur dispose des droits nécessaires pour lire la chanson.

la liste suivante décrit certains des scénarios dans lesquels Lecteur Windows Media appelle un plug-in de magasin en ligne de type 2.

-   **L’utilisateur tente de lire le contenu de la boutique en ligne.** dans ce cas, Lecteur Windows Media appelle la méthode [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) du plug-in, en passant un pointeur vers l’élément multimédia numérique que l’utilisateur tente de lire. Le magasin en ligne peut l’utiliser comme opportunité de mettre à jour la licence de l’utilisateur pour lire le contenu ou interdire la lecture. si le plug-in retourne la **valeur TRUE** dans le paramètre *pfAllowPlay* , Lecteur Windows Media tente de lire le contenu. La lecture échouera quand une licence valide n’existe pas ; Ce processus ne contourne pas la gestion des droits numériques (DRM).
-   **L’utilisateur demande l’autorisation de graver du contenu sur un CD ou un DVD.** dans ce cas, Lecteur Windows Media appelle la méthode [IWMPSubscriptionService :: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) du plug-in.
-   **l’utilisateur tente de synchroniser le contenu de la boutique en ligne avec un appareil, ou Lecteur Windows Media est prêt à synchroniser automatiquement le contenu de la boutique en ligne avec un appareil.** dans ce cas, Lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 ::p repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) du plug-in pour signaler à la banque en ligne qu’un élément multimédia est sur le point d’être synchronisé avec un appareil particulier, identifié par son nom canonique. Il s’agit d’une opportunité pour le magasin en ligne de déterminer si l’utilisateur est autorisé à synchroniser l’élément multimédia avec l’appareil. Il est également possible pour le magasin en ligne de préparer l’appareil pour la synchronisation et de mettre à jour les enregistrements, tels que les nombres de synchronisation, associés à l’appareil ou à l’élément multimédia. Le plug-in doit passer l’autorisation, la préparation et les tâches d’enregistrement à un thread distinct et retourner immédiatement à partir de **prepareForSync**. lorsque le thread distinct a terminé son travail, il doit notifier Lecteur Windows Media en appelant [IWMPSubscriptionServiceCallback :: onComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Un appareil est disponible pour le traitement en arrière-plan.** quand un appareil est connecté, Lecteur Windows Media alerte le magasin en ligne que l’appareil est disponible et inactif en appelant [IWMPSubscriptionService2 ::d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **l’utilisateur clique sur un bouton pour activer un magasin en ligne dans Lecteur Windows Media.** lorsque cela se produit, Lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 :: serviceEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) du plug-in. Lecteur Windows Media appelle également cette méthode lorsque l’utilisateur bascule vers un autre service.
-   **Lecteur Windows Media entre dans un état de faible activité.** Dans ce cas, le lecteur appelle la méthode [IWMPSubscriptionService :: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) du plug-in. Le magasin en ligne peut utiliser cette opportunité pour démarrer ou réveiller tous les threads qui effectuent des tâches en arrière-plan, tels que le renouvellement des licences expirées ou la compilation des données de lecture-nombre.
-   **Lecteur Windows Media entre dans un état d’activité élevée.** dans ce cas, Lecteur Windows Media appelle la méthode [IWMPSubscriptionService2 :: stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) du plug-in. Cela indique au plug-in qu’il doit suspendre les threads effectuant des tâches en arrière-plan.

Lecteur Windows Media libère le composant de magasin en ligne lorsque la session du lecteur se termine. Lors de la mise en production, le composant doit interrompre tout traitement en arrière-plan en cours, puis s’arrêter.

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

 

 




