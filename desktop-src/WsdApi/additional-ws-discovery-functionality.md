---
description: L’objectif de cette rubrique est de décrire les fonctionnalités de découverte implémentées par WSDAPI, mais non décrites dans les spécifications de DPWS ou de WS-Discovery.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Fonctionnalités de WS-Discovery supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209990"
---
# <a name="additional-ws-discovery-functionality"></a>Fonctionnalités de WS-Discovery supplémentaires

Dans certains cas, le [profil de périphériques pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) et les spécifications associées ne définissent pas explicitement les fonctionnalités d’implémentation. Par exemple, la spécification [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) ne définit pas le comportement du client et de l’hôte dans les environnements multirésidents. Lorsque WSDAPI a été implémenté, certaines fonctionnalités de découverte ont été ajoutées au-delà de la fonctionnalité définie dans la spécification.

WSDAPI implémente également des parties sélectionnées du CD1 WS-Discovery v 1.1 pour communiquer avec un proxy de découverte via HTTP.

L’objectif de cette rubrique est de décrire les fonctionnalités de découverte implémentées par WSDAPI, mais non décrites dans les spécifications de DPWS ou de WS-Discovery.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Adresses IPv6 et format d’URI SOAP. UDP

SOAP-sur-UDP et WS-Discovery ne décrivent pas explicitement la manière dont une adresse IPv6 littérale est représentée dans le format d’URI SOAP. UDP. La [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), intitulée « Uniform Resource Identifiers (Uri) : Generic Syntax », indique que les adresses IPv6 littérales ne sont pas prises en charge par le format d’URI SOAP. UDP.

Par souci de simplicité, WSDAPI reconnaît les adresses IPv6 entre crochets dans le schéma SOAP. UDP. Par exemple, l’adresse `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` est reconnue par wsdapi. Cela est similaire à la façon dont les adresses IPv6 sont gérées dans HTTP.

## <a name="hello-and-xaddrs"></a>Hello et XAddrs

L’objet d’hébergement DPWS d’un WSDAPI n’enverra jamais de message WS-Discovery [Hello](hello-message.md) avec [XAddrs](xaddr-validation-rules.md) dans le corps du message. Un client enverra toujours un message de [résolution](resolve-message.md) après avoir reçu un message de salutation si le client doit obtenir le XAddrs.

Cette approche présente deux avantages. Tout d’abord, un appareil basé sur WSDAPI n’exposera jamais XAddrs qui divulguera les adresses IP des réseaux privés. Deuxièmement, un appareil basé sur WSDAPI expose uniquement les XAddrs qui sont accessibles au client, ce qui signifie que les adresses IPv6 ne sont jamais envoyées à un client IPv4.

Lorsqu’une [sonde](probe-message.md) ou un message de résolution est reçu, un seul XAddr est envoyé en réponse. Le XAddr envoyé correspond à l’adresse locale sur laquelle la demande a été reçue. Si la demande a été reçue sur des sous-réseaux via IPv6, WSDAPI fournit une adresse IPv6 globale dans la réponse.

## <a name="preferred-addresses"></a>Adresses préférées

Un appareil peut fournir plusieurs XAddrs dans un message [Hello](hello-message.md), [ProbeMatch](probematches-message.md)ou [ResolveMatch](resolvematches-message.md) . Un service peut également être disponible sur plusieurs points de terminaison avec des adresses de transport différentes. Dans ce cas, WSDAPI tente de communiquer avec l’appareil sur la première adresse utilisable qu’il trouve. Une adresse est utilisable si elle provient d’un protocole disponible, tel que IPv4 sur un ordinateur sur lequel IPv4 est installé ou IPv6 sur un ordinateur sur lequel IPv6 est installé. En outre, si l’adresse provient d’un périphérique ou d’un service qui ne se trouve pas sur le sous-réseau local, elle est utilisable uniquement s’il s’agit d’une adresse IPv4, locale de site IPv6 ou d’un lien IPv6 local.

## <a name="wsdl-in-metadata-exchange"></a>WSDL dans l’échange de métadonnées

Les appareils et services basés sur WSDAPI ne fournissent pas leur WSDL dans l’échange de métadonnées, sauf s’ils sont étendus par l’application pour fournir ces informations. Par défaut, la configuration WSDL ne fait pas partie du modèle de programmation.

## <a name="app_max_delay"></a>\_délai maximal de l’application \_

DPWS définit \_ \_ le délai maximal pour l’application, l’intervalle aléatoire entre la réception d’une [sonde](probe-message.md) et l’envoi d’un [ProbeMatch](probematches-message.md), comme 5 000 millisecondes. Le pare-feu Windows requiert que le modèle de réponse de demande/monodiffusion de multidiffusion pour UDP ne fonctionne que dans la fenêtre de pare-feu 4 secondes. Par conséquent, WSDAPI transmet les réponses en 2 500 ms ou moins, au lieu de la fenêtre 5 000 MS décrite par le \_ délai maximal de l’application \_ .

## <a name="iana-port-reservations"></a>Réservations de port IANA

WSDAPI utilise le port TCP 5357 pour le trafic HTTP et le port TCP 5358 pour le trafic HTTPs par défaut. Ces ports sont réservés aux processus avec privilèges inférieurs via une réservation d’URL dans HTTP.sys et sont également réservés à l’IANA.

## <a name="udp-port-sharing"></a>Partage de ports UDP

WSDAPI utilise le partage de ports. Les messages de monodiffusion envoyés au port 3702 peuvent ne pas être correctement gérés par toutes les applications WSDAPI. Si une application se lie exclusivement au port 3702, elle peut empêcher les applications WSDAPI d’utiliser correctement ce port.

## <a name="ws-discovery-v11-cd1-proxy"></a>Proxy CD1 WS-Discovery v 1.1

WSDAPI recherche et communique avec un proxy de découverte qui implémente le protocole WS-Discovery v 1.1 CD1 en mode managé. WS-Discovery v 1.1 CD1 est la première révision de WS-Discovery pour inclure une description explicite d’un protocole HTTP pour la communication entre un proxy et un client ou un appareil.

Pour limiter le nombre de versions simultanées utilisées dans les demandes de multidiffusion, WSDAPI envoie une demande de sondage WS-Discovery dans l’espace de noms 2005/04, mais recherche le type de DiscoveryProxy du CD1 WS-Discovery v 1.1. Si un proxy répond, WSDAPI envoie une sonde HTTP ou la demande de résolution au point de terminaison proxy spécifié, tel qu’il est défini dans le CD1 WS-Discovery v 1.1.

 

 



