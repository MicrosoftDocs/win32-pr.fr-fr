---
title: Opération WFP
description: Windows La plateforme de filtrage (WFP) effectue ses tâches en intégrant les couches, les filtres, les shims et les légendes des entités de base suivantes.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015387"
---
# <a name="wfp-operation"></a>Opération WFP

Windows La plateforme de filtrage (WFP) effectue ses tâches en intégrant les entités de base suivantes : *couches*, *filtres*, *shims* et *légendes*.

## <a name="layers"></a>Calques

Une *couche* est un conteneur géré par le moteur de filtre dont la fonction est d’organiser les filtres en ensembles. Une couche n’est pas un module de la pile réseau. Chaque couche possède un schéma qui définit le type de filtres qui peuvent y être ajoutés. Pour plus d’informations, consultez [conditions de filtrage disponibles à chaque couche de filtrage](filtering-conditions-available-at-each-filtering-layer.md) .

Les couches peuvent contenir des sous-couches pour gérer les exigences de filtre conflictuelles telles que « bloquer les ports TCP au-dessus de 1024 » et « ouvrir le port 1080 ». Les règles de gestion des conflits de filtrage sont déterminées par l' [arbitrage de filtre](filter-arbitration.md).

WFP contient un ensemble de [sous-couches intégrées](management-filtering-sublayer-identifiers.md). Chaque couche hérite de toutes les sous-couches intégrées. Les utilisateurs peuvent également ajouter leurs propres sous-couches.

La liste des couches du moteur de filtre est fournie dans la rubrique de la section de référence [**filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtres

Un *filtre* est une règle qui correspond à des paquets entrants ou sortants. La règle indique au moteur de filtrage ce qu’il doit faire avec le paquet, y compris pour appeler un module de légende pour l’inspection Poussée des paquets ou du flux. Par exemple, un filtre peut spécifier « bloquer le trafic avec un port TCP supérieur à 1024 » ou « appeler des ID pour tout le trafic qui n’est pas sécurisé ».

Un filtre au moment du démarrage est un filtre appliqué au démarrage dès que le pilote de pile TCP/IP (tcpip.sys) démarre. Un filtre au moment du démarrage est désactivé au démarrage de BFE. Un filtre est marqué comme au moment du démarrage en définissant l’indicateur de [**\_ filtre FWPM \_ \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) lorsque [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) est appelé.

Un filtre au moment de l’exécution est un filtre appliqué après le démarrage de BFE. Un filtre au moment de l’exécution peut être statique, dynamique ou persistant en fonction de la façon dont il a été créé. Pour plus d’informations sur les différents types de filtres au moment de l’exécution et leur durée de vie, consultez [gestion des objets](object-management.md) .

## <a name="shims"></a>Shims

Un *shim* est un composant en mode noyau qui prend des décisions de filtrage en classifiant les couches du moteur de filtre. Chaque shim est classé par rapport à une ou plusieurs couches. par exemple, le shim de Module de couche transport est classé par rapport à la couche de transport entrante, à la couche de transport sortant et à la Connecter ALE et aux couches Receive-Accept pour le premier paquet d’un workflow.

Dans la mesure où les paquets, les flux et les événements traversent la pile réseau, les shims les analysent pour extraire les conditions et valeurs de la valeur, puis appellent le moteur de filtre pour les évaluer par rapport aux filtres d’une couche donnée. Le moteur de filtre peut appeler un ou plusieurs appels dans le cadre de la classification. Les shims effectuent le déplacement réel des paquets, des flux et des événements en fonction du résultat de la classification effectuée par le moteur de filtre.

## <a name="callouts"></a>Légendes

Une *légende* est un ensemble de fonctions exposées par un pilote et utilisée pour un filtrage spécialisé. Ils sont utilisés pour effectuer une analyse et une manipulation des paquets, tels que l’analyse antivirus, le contrôle parental recherche de contenu inapproprié, l’analyse des données de paquets pour les outils de surveillance. Certains appels, tels que le pilote de traduction d’adresses réseau (NAT), sont intégrés au système d’exploitation. D’autres, telles qu’une légende de contrôle parental HTTP ou la légende système de détection d’intrusion (IDS), peuvent être fournies par des éditeurs de logiciels indépendants (ISV). Les fonctions de légende sont appelées par le moteur de filtre lorsqu’un filtre de légende correspondant est mis en correspondance au niveau d’une couche donnée.

Les légendes peuvent être inscrites sur n’importe quelle couche WFP en mode noyau. Les légendes peuvent retourner une action (« bloquer », « autoriser » et, lors de l’inspection des flux de données, « différer », « nécessiter plus de données », « supprimer la connexion ») et peuvent modifier et sécuriser le trafic réseau entrant et sortant.

Une fois qu’une légende est inscrite auprès du moteur de filtre, elle peut recevoir le trafic réseau à traiter. Le trafic peut être des paquets, des flux ou des événements en fonction de la couche. Un agent de pare-feu ou d’application provoque le transfert du trafic vers une légende en ajoutant un filtre dont l’action est « légende » et dont l’ID de légende est l’identificateur de cette légende. Les légendes peuvent indiquer au moteur de filtre de retourner « bloquer » ou « autoriser » au shim. Les légendes peuvent également retourner « continuer » pour permettre à d’autres filtres de traiter le paquet.

Plusieurs légendes peuvent être exposées par un pilote de légende.

Une légende doit être ajoutée (avec [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) et enregistrée (avec [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) avant de pouvoir être utilisée. Un appel à **FwpmCalloutAdd0** est requis avant la création de filtres qui font référence à la légende. Un appel à FwpsCalloutRegister est nécessaire pour que la protection de code à plateforme puisse appeler la légende lorsque les filtres de légende sont mis en correspondance. Par défaut, les filtres qui font référence à des appels qui ont été ajoutés mais n’ont pas encore été enregistrés avec le moteur de filtre sont traités comme des filtres de « bloc ». L’ordre d’appel de **FwpmCalloutAdd0** et de FwpsCalloutRegister n’a pas d’importance. Une légende persistante doit être ajoutée une seule fois et doit être enregistrée chaque fois que le pilote qui implémente la légende démarre (par exemple, après un redémarrage).

## <a name="classification"></a>Classification

La classification est le processus qui consiste à appliquer des filtres au trafic réseau (paquet, flux ou événement) afin de déterminer le résultat « autoriser » ou « bloquer » pour ce trafic. Pour un paquet, un flux ou un événement, il existe un seul appel de classification par couche.

Pendant la classification, les propriétés (par exemple, adresse source) du paquet, du flux ou de l’événement sont comparées aux conditions de filtre définies sur les filtres de la couche où la classification est appelée. Lorsque des correspondances sont trouvées, l’algorithme d' [arbitrage de filtre](filter-arbitration.md) est utilisé pour déterminer le résultat du processus de classification.

Une demande de classification est déclenchée par un shim.

Les actions de classification peuvent être :

-   Permit
-   Bloquer
-   Légende
    -   Permit
    -   Bloquer
    -   Continuer
    -   Fenêtres
    -   Besoin de plus de données
    -   Supprimer la connexion

## <a name="wfp-operation"></a>Opération WFP

Au moment du démarrage, dès que le pilote de pile TCP/IP (tcpip.sys) démarre, le moteur de filtre en mode noyau applique la stratégie de sécurité du système par le biais des filtres au moment du démarrage.

Une fois que le moteur de filtrage de base (BFE) démarre en mode utilisateur, les filtres persistants sont ajoutés à la plateforme, les filtres de démarrage sont désactivés et les notifications sont envoyées aux pilotes de légende qui s’abonnent à l’aide de [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). Les notifications sont distribuées immédiatement après l’initialisation de la BFE. La plateforme est maintenant prête pour l’enregistrement des légendes et pour l’ajout d’objets au moment de l’exécution.

La transition du temps de démarrage au mode de filtrage persistant peut être de quelques secondes, voire plus sur une machine lente. Il est atomique. par conséquent, si un fournisseur a à la fois le temps de démarrage et un filtre persistant, aucune fenêtre n’est jamais appliquée.

Après le démarrage de BFE, les filtres d’exécution peuvent être ajoutés par des agents de pare-feu ou par des solutions de pare-feu personnalisées. BFE traite ces filtres et les envoie à la couche appropriée du moteur de filtre pour la mise en œuvre. BFE accepte également les paramètres d’authentification et envoie ces paramètres aux modules de génération de clé IPsec (IKE/AuthIP). Pour plus d’informations, consultez [configuration IPSec](ipsec-configuration.md) .

À tout moment, des filtres et des paramètres d’authentification peuvent être ajoutés, supprimés ou modifiés dans le système par le biais de l’interface RPC exposée par le BFE. Les sous-couches et les modules de légende peuvent également être ajoutés ou supprimés.

Data Flow :

1.  Un paquet arrive dans la pile réseau.
2.  La pile réseau détecte et appelle un shim.
3.  Le shim appelle le processus de classification au niveau d’une couche particulière.
4.  Pendant la classification, les filtres sont mis en correspondance et l’action résultante est effectuée. (Voir [arbitrage de filtre](filter-arbitration.md).)
5.  Si des filtres de légende sont mis en correspondance au cours du processus de classification, les légendes correspondantes sont appelées.
6.  Le shim agit sur la décision de filtrage finale (par exemple, déposer le paquet).

Le trafic de données sortant suit un modèle similaire.

Les rubriques suivantes décrivent plus en détail le fonctionnement de la protection des plateformes.

-   [Flux de paquets TCP](tcp-packet-flows.md)
-   [Flux de paquets UDP](udp-packet-flows.md)
-   [Arbitrage de filtre](filter-arbitration.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle objet](object-model.md)
</dt> <dt>

[Gestion des objets](object-management.md)
</dt> </dl>

 

 