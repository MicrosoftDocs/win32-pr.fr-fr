---
description: Lorsque vous travaillez avec des graphiques homologues, les fonctions doivent être appelées dans un ordre spécifique. Le déroulement des appels varie selon que vous créez ou que vous ouvrez un graphique homologue. Cette rubrique identifie le déroulement des appels de fonction dans une application graphique d’homologue simple.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Utilisation des graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007192"
---
# <a name="working-with-graphs"></a>Utilisation des graphiques

Lorsque vous travaillez avec des graphiques homologues, les fonctions doivent être appelées dans un ordre spécifique. Le déroulement des appels varie selon que vous créez ou que vous ouvrez un graphique homologue. Cette rubrique identifie le déroulement des appels de fonction dans une application graphique d’homologue simple.

## <a name="starting-up-a-graph"></a>Démarrage d’un Graph

Avant qu’une application appelle une fonction dans l’API de représentation graphique d’homologue, [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) doit être appelé pour initialiser l’API de représentation graphique des homologues pour une application, puis définir la version prise en charge.

## <a name="creating-a-peer-graph"></a>Création d’un Graph homologue

La procédure suivante identifie le déroulement des appels pour la création d’un graphique homologue.

> [!IMPORTANT]
> Un seul homologue doit appeler [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Tous les autres pairs doivent appeler [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Plusieurs appels à **PeerGraphCreate** invalident un graphique.

 

-   Créez un graphique homologue. Appelez [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Inscrivez-vous aux événements homologues. Appelez [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Pour plus d’informations sur l’inscription des événements homologues, consultez [infrastructure des événements](peer-events-infrastructure.md).

     

-   Écouter les connexions à un graphique homologue. Appelez [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).
-   Exécuter des fonctions dépendantes de l’application pour le reste du temps d’exécution, par exemple, traiter des événements homologues et utiliser des connexions.
-   Fermez la connexion à un graphique homologue. Appelez [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="opening-a-peer-graph"></a>Ouverture d’un Graph homologue

Le déroulement des appels de fonction pour ouvrir un graphique homologue dépend de la valeur de retour de l’appel à [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Les valeurs les plus importantes sont **s \_ OK** et les **données d’homologue \_ \_ \_ créées**, qui sont décrites dans les sections suivantes de cette rubrique.

> [!Note]  
> Si un appel à [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) ne retourne pas les données **s \_ OK** ou **Peer \_ s \_ \_ créées**, gérez l’erreur.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Quand PeerGraphOpen retourne S \_ OK

Lorsqu’un appel à [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retourne la valeur **\_ OK**, un graphique homologue et une base de données existante ont été ouverts. La procédure suivante identifie ce que vous pouvez faire pour ouvrir un graphique homologue lorsqu’un appel à **PeerGraphOpen** retourne **S \_ OK**

-   Inscrivez-vous aux événements homologues. Appelez [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Pour plus d’informations sur l’inscription des événements, consultez [infrastructure des événements](peer-events-infrastructure.md).

     

-   Localisez un nœud. Il s’agit d’un processus exécuté en dehors de l’infrastructure de représentation graphique des pairs, à l’aide d’une méthode ou d’une application que vous identifiez. L’API graphique d’homologue ne fournit pas de mécanisme spécifique pour rechercher un nœud de graphique initial auquel se connecter. Une application doit utiliser un autre mécanisme, tel que l’API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , pour localiser le nœud initial.
-   Si un nœud est trouvé, connectez-vous à celui-ci. Appelez [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), puis appelez [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) pour écouter les connexions au graphique homologue.
    > [!Note]  
    > Si un nœud est introuvable, n’appelez pas [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) et [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Exécuter des fonctions dépendantes de l’application pour le reste du temps d’exécution, par exemple, traiter des événements homologues et utiliser des connexions, selon que le nœud est connecté ou non au graphique d’homologue. Par exemple, l’application peut choisir d’effectuer un délai d’expiration ou de procéder périodiquement à la détection d’un nœud actif dans le graphique.
-   Fermez la connexion au graphique homologue. Appelez [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Quand PeerGraphOpen retourne les données de l’HOMOLOGUe \_ \_ \_ créées

Quand [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retourne les **données d’homologue \_ \_ \_ créées**, cela signifie qu’une base de données pour un graphique homologue est introuvable, une nouvelle base de données est créée et c’est la première fois qu’elle est ouverte. Pour utiliser ou écouter un graphique homologue, un homologue doit être connecté à un graphique homologue et être synchronisé avec celui-ci.

La procédure suivante identifie ce que vous pouvez faire pour ouvrir un graphique homologue lorsqu’un appel à [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retourne les données de l' **homologue \_ \_ \_ créées**.

-   Ouvrez un graphique homologue. Appelez [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).
-   Inscrivez-vous aux événements homologues. Appelez [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Pour plus d’informations sur l’inscription des événements homologues, consultez [infrastructure des événements](peer-events-infrastructure.md).

     

-   Localisez un nœud. Il s’agit d’un processus exécuté en dehors de l’infrastructure de représentation graphique des pairs, à l’aide d’une méthode ou d’une application que vous identifiez. L’API graphique d’homologue ne fournit pas de mécanisme spécifique pour rechercher un nœud de graphique initial auquel se connecter. Une application doit utiliser un autre mécanisme, tel que l’API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , pour localiser le nœud initial.
-   Si un nœud est trouvé, connectez-vous à celui-ci. Appelez [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), puis appelez [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) pour écouter les connexions au graphique homologue.
    > [!Note]  
    > Si un nœud est introuvable, n’appelez pas [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) et [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Exécuter des fonctions dépendantes de l’application pour le reste du temps d’exécution, par exemple, traiter des événements homologues et utiliser des connexions, selon que le nœud est connecté ou non au graphique d’homologue. Par exemple, l’application peut choisir d’effectuer un délai d’expiration ou de procéder périodiquement à la détection d’un nœud actif dans le graphique.
-   Fermez la connexion au graphique homologue. Appelez [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

 

 



