---
title: Flux de paquets UDP
description: ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues pendant une session UDP classique.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e850f67bce9a001d41ebb54b17d3d0d86b94b22f083529e4589d6b69841b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746639"
---
# <a name="udp-packet-flows"></a>Flux de paquets UDP

cette section décrit l’ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues au cours d’une session UDP classique.

> [!Note]  
> Les flux de paquets UDP pour IPv6 suivent le même modèle que pour IPv4.

 

> [!Note]  
> Tous les flux de paquets non-TCP suivent le même modèle que les flux de paquets UDP.

 

## <a name="udp-connection-establishment"></a>Établissement de la connexion UDP

<dl> Le serveur (récepteur) effectue une ouverture passive

-   liaison : FWPM \_ \_ \_ \_ V4 de redirection de liaison ALE \_ de couche (Windows 7/Windows Server 2008 R2 uniquement)
-   liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_

  
Le client (expéditeur) effectue une ouverture active

-   liaison : FWPM \_ \_ \_ \_ V4 de redirection de liaison ALE \_ de couche (Windows 7/Windows Server 2008 R2 uniquement)
-   liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_
-   sendto : FWPM \_ \_ \_ \_ redirection de la connexion ALE de la couche ALE \_ (Windows 7/Windows Server 2008 R2 uniquement)
-   SendTo : FWPM \_ de \_ \_ connexion d’authentification ALE de couche ALE \_ \_
-   FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_
-   données : données de datagramme de la \_ couche FWPM \_ \_ \_ v4
-   Message UDP : FWPM \_ couche de \_ \_ transport sortant \_ v4
-   Datagrammes IP : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4

  
Serveur

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_
-   Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4
-   FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_
-   données : données de datagramme de la \_ couche FWPM \_ \_ \_ v4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Message UDP reçu sans écoute sur le port ou le protocole

Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Datagrammes IP : FWPM \_ couche de \_ sortie \_ IPPACKET \_ v4 \_ ignorée
-   Dest ICMP inaccessible : \_ erreur ICMP de sortie de la couche FWPM \_ \_ \_ \_ v4
-   Transfert ICMP impossible : \_ \_ \_ v4 de transport sortant \_ de la couche FWPM
-   Dest ICMP inaccessible : FWPM \_ couche \_ sortante \_ IPPACKET \_ v4

> [!Note]  
> UDP sans point de terminaison est indiqué dans IPPACKET ignorée avec une condition d’erreur spécifique. Bloquer ce paquet sur IPPACKET ignore pour empêcher la pile d’envoyer l’événement correspondant (erreur ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Réautorisation réussie d’un paquet UDP

Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_
-   Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4
-   Message UDP : \_ \_ données de datagramme de la couche FWPM \_ \_ V4 (entrant)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Échec de la réautorisation d’un paquet UDP

Serveur (récepteur)

-   Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4
-   Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_
-   Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4
-   Message UDP : FWPM de l' \_ authentification ALE de la couche \_ ALE \_ \_ reçues \_ accepter la \_ v4 \_ Ignorer

## <a name="udp-connection-termination"></a>Arrêt de la connexion UDP

L’arrêt de la connexion UDP n’est pas indiqué dans une couche WFP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




