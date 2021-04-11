---
description: Il existe deux façons de déterminer la procédure de diagnostic à utiliser.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Résolution des problèmes de Prise en main avec WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202269"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Résolution des problèmes de Prise en main avec WSDAPI

Ce guide de dépannage contient un ensemble de [procédures de diagnostic](wsdapi-diagnostic-procedures.md) qui peuvent être utilisées pour aider à identifier la cause des problèmes d’application. Une fois la cause du problème identifiée, les solutions suggérées dans la procédure de diagnostic peuvent être appliquées afin de résoudre le problème.

Il existe deux façons de déterminer la procédure de diagnostic à utiliser. L’une des méthodes consiste à accéder à la page de résolution des problèmes pour le type de client pour afficher une liste pas à pas des procédures de diagnostic à utiliser pour dépanner le client. L’autre méthode consiste à accéder à la aide-mémoire de dépannage ci-dessous pour afficher des tableaux récapitulatifs qui présentent des problèmes courants avec les applications WSDAPI et les procédures à suivre pour diagnostiquer les problèmes.

## <a name="troubleshooting-by-type-of-client"></a>Résolution des problèmes par type de client

Les rubriques suivantes présentent les procédures de diagnostic appropriées par type de client. Ces rubriques affichent également les modèles de message associés au type de client.

-   [Dépannage des applications WSDAPI à l’aide de la découverte dirigée](troubleshooting-applications-using-directed-discovery.md)
-   [Résolution des problèmes des clients de découverte des fonctions](troubleshooting-function-discovery-clients.md)
-   [Résolution des problèmes voisinage immédiat/réunions près de moi](troubleshooting-people-near-me-meetings-near-me.md)
-   [Résolution des problèmes liés à l’Assistant Ajout d’imprimante](troubleshooting-the-add-printer-wizard.md)
-   [Résolution des problèmes de l’Explorateur réseau](troubleshooting-the-network-explorer.md)
-   [Résolution des problèmes de l’Assistant projecteur](troubleshooting-the-projector-wizard.md)
-   [Résolution des problèmes liés aux autres applications WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Aide-mémoire pour la résolution des problèmes

Les tableaux suivants présentent certains problèmes qui peuvent empêcher les clients et hôtes WSDAPI de se voir sur le réseau et d’échanger des métadonnées d’appareil. Les tables affichent également les procédures de diagnostic à exécuter et les critères à utiliser pour évaluer si l’application subit un problème particulier.

### <a name="network-environment-problems"></a>Problèmes d’environnement réseau



| Problème                                                                                                                                                                                              | Procédure de diagnostic                                                                                                                                                                                                                             | Identification du problème                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le pare-feu bloque le trafic de découverte du réseau.                                                                                                                                                       | [Inspection des paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | L’activation de l’exception découverte du réseau sur le pare-feu résout le problème.                                                                                                                      |
| Les exceptions de pare-feu spécifiques à l’application bloquent les messages.                                                                                                                               | [Inspection des paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La désactivation du pare-feu résout le problème. WF. msc affiche les règles de pare-feu spécifiques à l’application.                                                                                                      |
| L’appareil ne répond pas aux demandes UDP en envoyant un message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) en temps opportun (moins de 4 secondes). | [Inspection des paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La désactivation du pare-feu résout le problème et un hôte générique qui répond en moins de 4 secondes fonctionne correctement.                                                                            |
| Le contexte de sécurité de l’application est incorrect (autrement dit, le client et l’hôte ne disposent pas des autorisations adéquates sur le réseau).                                                                 | [Utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) ou [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L’adresse de l’appareil n’est pas affichée dans la sortie du client de débogage WSD. L’exécution de l’application en tant qu’administrateur résout le problème.                                                                          |
| Une stratégie IPSec bloque les messages.                                                                                                                                                                | [Utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) ou [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L’adresse de l’appareil n’est pas affichée dans la sortie du client de débogage WSD. Le problème n’est pas résolu en désactivant le pare-feu. Le problème ne peut pas être reproduit sur une machine qui n’est soumise à aucune stratégie IPSec. |



 

### <a name="discovery-traffic-problems"></a>Problèmes de trafic de découverte



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problème</th>
<th>Procédure de diagnostic</th>
<th>Identification du problème</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Les messages <a href="hello-message.md">Hello</a>, <a href="probe-message.md">Probe</a>ou <a href="resolve-message.md">Resolve</a> ne sont pas transmis sur le réseau, car l’application n’énumère pas correctement les interfaces réseau de multidiffusion.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion</a></td>
<td>Les messages Hello, Probe ou Resolve n’apparaissent pas dans la sortie du client de débogage WSD. Les paquets n’apparaissent pas sur le réseau. Les paquets ne sont pas générés pour l’interface de bouclage ou pour d’autres interfaces.</td>
</tr>
<tr class="even">
<td>Les messages de <a href="probe-message.md">sondage</a> ne sont pas envoyés par la multidiffusion UDP au port 3702 (pour les applications qui n’utilisent pas la découverte dirigée).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a></td>
<td>L’inspection du message indique qu’il a été envoyé au mauvais port.</td>
</tr>
<tr class="odd">
<td>Le message de <a href="probe-message.md">sondage</a> ne contient pas d’élément <strong>types</strong> , ou l’élément <strong>types</strong> est vide.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection du message indique que l’élément <strong>types</strong> n’est pas présent ou vide.</td>
</tr>
<tr class="even">
<td>L’élément <strong>types</strong> d’un message de <a href="probe-message.md">sonde</a> ne contient pas les types auxquels un hôte doit répondre.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection du message indique que l’élément <strong>types</strong> contient une valeur incorrecte ou incorrecte.</td>
</tr>
<tr class="odd">
<td>Un message <a href="probematches-message.md">messages ProbeMatches</a> n’a pas été envoyé en monodiffusion au port UDP à partir duquel la <a href="probe-message.md">sonde</a> a été envoyée.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection de la sortie indique qu’aucun message <a href="probematches-message.md">messages ProbeMatches</a>) n’a été envoyé ou que le message a été envoyé au mauvais port.
<blockquote>
[!Note]<br />
Pour les applications qui utilisent la découverte dirigée, le <a href="probematches-message.md">messages ProbeMatches</a> doit être envoyé via HTTP ou HTTPS en réponse au message de <a href="probe-message.md">sondage</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Le message <a href="probematches-message.md">messages ProbeMatches</a> ne contient pas d’élément <strong>latesto</strong> , ou l’élément <strong>latesto</strong> est vide.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection du message indique que l’élément <strong>latesto</strong> n’est pas présent ou vide.</td>
</tr>
<tr class="odd">
<td>La valeur de l’élément <strong>latesto</strong> dans un message <a href="probematches-message.md">messages ProbeMatches</a> ne correspond pas à la valeur de l’élément <strong>MessageID</strong> du message de <a href="probe-message.md">sondage</a> correspondant.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection du message indique que l’élément <strong>latesto</strong> contient une valeur incorrecte ou incorrecte.</td>
</tr>
<tr class="even">
<td>L’élément <strong>XAddrs</strong> inclus dans un message <a href="probematches-message.md">messages ProbeMatches</a> n’est pas conforme aux <a href="xaddr-validation-rules.md">règles de validation XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection du message indique que les <strong>XAddrs</strong> ne sont pas valides.</td>
</tr>
<tr class="odd">
<td>La <a href="resolve-message.md">résolution</a> des messages n’est pas envoyée par la multidiffusion UDP au port 3702 (pour les applications qui n’utilisent pas la découverte dirigée).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection de la sortie indique que le message de <a href="resolve-message.md">résolution</a> a été envoyé au mauvais port.</td>
</tr>
<tr class="even">
<td>Un message <a href="resolvematches-message.md">ResolveMatches</a> n’a pas été envoyé en monodiffusion au port UDP à partir duquel un message de <a href="resolve-message.md">résolution</a> a été envoyé.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspection des suivis réseau pour UDP WS-Discovery</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspection des traces réseau pour les applications à l’aide de la découverte dirigée</a></td>
<td>L’inspection de la sortie indique qu’aucun message <a href="resolvematches-message.md">ResolveMatches</a> n’a été envoyé ou que le message a été envoyé au mauvais port.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Problèmes d’échange de métadonnées



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problème</th>
<th>Procédure de diagnostic</th>
<th>Identification du problème</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>L’adresse de transport publiée par l’hôte est incorrecte.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées HTTP</a></td>
<td>L’inspection de XAddrs dans la sortie du client de débogage WSD indique que l’adresse de transport est incorrecte ou incorrecte.</td>
</tr>
<tr class="even">
<td>Impossible d’établir une connexion TCP pour l’échange de métadonnées.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>La sortie de l’analyseur de paquets n’affiche pas l’échange de paquets suivant :
<ul>
<li>Paquet TCP SYN envoyé à partir du client</li>
<li>Paquet TCP SYN/ACK envoyé à partir de l’hôte</li>
<li>Paquet TCP ACK envoyé par le client</li>
</ul></td>
</tr>
<tr class="odd">
<td>Le client n’a pas envoyé de requête HTTP obtenir valide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>Il n’y a aucune requête HTTP d’extraction dans la sortie de l’analyseur de paquets, ou la requête est incorrecte.</td>
</tr>
<tr class="even">
<td>Le client n’a pas envoyé de message d' WS-Transfer d' <a href="get--metadata-exchange--http-request-and-message.md">extraction</a> valide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>Il n’existe aucun WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">recevoir</a> de message dans la sortie de l’analyseur de paquets, ou le message est incorrect.</td>
</tr>
<tr class="odd">
<td>L’hôte n’écoute pas sur le chemin d’accès de l’URL spécifié dans la requête HTTP.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>Il n’y a aucune réponse HTTP dans la sortie de l’analyseur de paquets.</td>
</tr>
<tr class="even">
<td>Le WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">obtenir</a> le message ne contient pas <strong>d’élément à</strong> , ou l’élément <strong>à</strong> est vide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>L’inspection du message indique que l’élément <strong>to</strong> n’est pas présent ou vide.</td>
</tr>
<tr class="odd">
<td>La valeur de l’élément <strong>to</strong> d’un WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">obtenir</a> le message ne correspond pas à l’une des adresses de point de terminaison de l’hôte.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>L’inspection du message indique que la valeur de l’élément <strong>to</strong> ne correspond pas à l’une des adresses de point de terminaison publiées dans le message <a href="probematches-message.md">messages ProbeMatches</a> ou <a href="resolvematches-message.md">ResolveMatches</a> de l’hôte.</td>
</tr>
<tr class="even">
<td>L’hôte n’a pas envoyé d’en-tête de réponse HTTP valide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>Il n’y a aucune réponse HTTP dans la sortie de l’analyseur de paquets, ou la requête est incorrecte.</td>
</tr>
<tr class="odd">
<td>L’en-tête de réponse HTTP envoyé par l’hôte indique que la demande ne peut pas être terminée.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>L’en-tête de réponse a un code d’État autre que HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>L’hôte n’a pas envoyé de message <a href="getresponse--metadata-exchange--message.md">GetResponse</a> valide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>Il n’existe aucun message <a href="getresponse--metadata-exchange--message.md">GetResponse</a> dans la sortie de l’analyseur de paquets ou le message est incorrect.</td>
</tr>
<tr class="odd">
<td>Le message <a href="getresponse--metadata-exchange--message.md">GetResponse</a> ne contient pas d’élément <strong>latesto</strong> , ou l’élément <strong>latesto</strong> est vide.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>L’inspection du message indique que l’élément <strong>latesto</strong> n’est pas présent ou vide.</td>
</tr>
<tr class="even">
<td>La valeur de l’élément <strong>latesto</strong> dans un message <a href="getresponse--metadata-exchange--message.md">GetResponse</a> ne correspond pas à la valeur de l’élément <strong>MessageID</strong> du message d' <a href="get--metadata-exchange--http-request-and-message.md">extraction</a> correspondant.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspection des suivis réseau pour l’échange de métadonnées HTTP</a></td>
<td>L’inspection du message indique que l’élément <strong>latesto</strong> contient une valeur incorrecte ou incorrecte.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de résolution des problèmes WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
