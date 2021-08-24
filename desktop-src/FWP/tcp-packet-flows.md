---
title: Flux de paquets TCP
description: ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues pendant une session TCP classique.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d4836da7a1912a6e39358b54e2a3086dd80efe844d6a301d079014d4a5b209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746629"
---
# <a name="tcp-packet-flows"></a>Flux de paquets TCP

cette section décrit l’ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues pendant une session TCP classique.

> [!Note]  
> Les flux de paquets TCP pour IPv6 suivent le même modèle que pour IPv4.

 

> [!Note]  
> Les flux de paquets non TCP suivent le même modèle que les [flux de paquets UDP](udp-packet-flows.md).

 

## <a name="tcp-connection-establishment"></a>Établissement de la connexion TCP

<dl> Le serveur (récepteur) effectue une ouverture passive

-   liaison : FWPM \_ \_ \_ \_ V4 de redirection de liaison ALE \_ de couche (Windows 7/Windows Server 2008 R2 uniquement)
-   liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_
-   écouter : FWPM \_ \_ V4 d' \_ écoute d’authentification ALE \_ de couche \_

  
Le client (expéditeur) effectue une ouverture active

-   liaison : FWPM \_ \_ \_ \_ V4 de redirection de liaison ALE \_ de couche (Windows 7/Windows Server 2008 R2 uniquement)
-   liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_
-   connexion : FWPM \_ \_ \_ \_ de redirection ALE de la couche ALE \_ (Windows 7/Windows Server 2008 R2 uniquement)
-   connexion : FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_
-   SYN : \_ couche FWPM \_ v4 de \_ transport \_ sortant
-   SYN : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

  
Serveur

-   SYN : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   SYN : \_ couche FWPM \_ \_ v4 transport entrant \_
-   SYN : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4
-   SYN-ACK : \_ couche FWPM \_ v4 de \_ transport \_ sortant
-   SYN-ACK : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

  
Client

-   SYN-ACK : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   SYN-ACK : \_ transport entrant de couche FWPM \_ \_ \_ v4
-   FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_
-   ACK : \_ couche FWPM \_ v4 de \_ transport \_ sortant
-   ACK : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

  
Serveur

-   ACK : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   ACK : \_ couche FWPM \_ \_ v4 transport entrant \_
-   FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_
-   Listen est terminé. Le serveur peut effectuer une acceptation.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN reçu sans écoute sur le port ou le protocole

Serveur (récepteur)

-   SYN : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   SYN : \_ couche FWPM \_ \_ v4 transport entrant \_ \_ rejeté
-   RST : \_ transport sortant de couche FWPM \_ \_ \_ v4
-   RST : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

> [!Note]  
> TCP SYN sans point de terminaison est indiqué dans TRANSPORT ignore avec une condition d’erreur spécifique. Bloquer ce paquet au niveau du TRANSPORT rejeté pour empêcher la pile d’envoyer l’événement correspondant (RST). Pour obtenir un exemple de filtrage en mode furtif, consultez [prévention de l’analyse des ports](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Données transmises via une connexion TCP

<dl> Client (expéditeur)

-   Envoyer
-   données : FWPM \_ de \_ flux de couche \_ v4
-   Segments TCP : FWPM \_ couche de \_ \_ transport sortant \_ v4
-   Datagrammes IP : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

  
Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Segments TCP : FWPM \_ couche de \_ \_ transport entrant \_ v4
-   données : FWPM \_ de \_ flux de couche \_ v4
-   Les données sont disponibles pour la lecture.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Réautorisation réussie d’un paquet TCP

Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Segment TCP : \_ couche FWPM \_ \_ v4 transport entrant \_
-   Segment TCP : FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues accepter la \_ \_ v4
-   données : FWPM \_ \_ de flux \_ de couche V4 (entrant)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Échec de la réautorisation d’un paquet TCP

Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Segment TCP : \_ couche FWPM \_ \_ v4 transport entrant \_
-   Segment TCP : FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues accepter la \_ \_ v4
-   Segment TCP : FWPM \_ V4 d’authentification ALE de la couche \_ ALE \_ \_ \_ \_ \_ ignorée

## <a name="tcp-connection-termination"></a>Arrêt de la connexion TCP

L’arrêt de la connexion TCP n’est pas indiqué dans une couche WFP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




