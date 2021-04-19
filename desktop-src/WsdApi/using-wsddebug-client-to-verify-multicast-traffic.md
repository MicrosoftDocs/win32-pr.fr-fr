---
description: Si l’hôte et le client génériques peuvent s’afficher mutuellement sur le réseau, mais que l’hôte et le client réels ne le sont pas, il est probable que le problème se trouve dans les messages envoyés entre les points de terminaison sur le réseau.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380663"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion

Si l’hôte et le client génériques peuvent s’afficher mutuellement sur le réseau, mais que l’hôte et le client réels ne le sont pas, il est probable que le problème se trouve dans les messages envoyés entre les points de terminaison sur le réseau. Pour plus d’informations sur l’hôte et le client génériques, consultez [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md). Étant donné que les traces de réseau complètes peuvent être difficiles à collecter, à filtrer et à lire, l’outil client de débogage WSD peut être utilisé pour imprimer les côtés de la multidiffusion des messages WS-Discovery.

Le client de débogage WSD en mode multidiffusion ne peut inspecter que la moitié des messages, puisque le client ne peut pas imprimer les messages de monodiffusion. Si le trafic monodiffusion est digne d’intérêt, passez directement à l' [inspection des suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Cette procédure présente une méthode qui affiche tout le trafic de multidiffusion sur le réseau. Pour afficher uniquement le trafic de multidiffusion à destination et en provenance de l’appareil, consultez la section [filtrage des résultats du client de débogage WSD](#filtering-wsd-debug-client-results) ci-dessous.

**Pour utiliser le client de débogage WSD afin de vérifier le trafic de multidiffusion**

1.  Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).
2.  Ouvrez une invite de commandes et exécutez la commande suivante : **WSDDebug \_client.exe la multidiffusion/mode**
3.  Reproduisez l’erreur en démarrant l’hôte et le client ou en appuyant sur F5 dans l’Explorateur réseau.
4.  Vérifiez que les messages sont en cours de multidiffusion.

Si les messages requis s’affichent dans la sortie du client de débogage WSD, l’échec de l’application peut être dans le contenu du message de multidiffusion, ou dans l’existence ou le contenu des messages de réponse de monodiffusion correspondants. Poursuivez la résolution des problèmes en suivant les instructions fournies dans [inspection des suivis réseau pour UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Si les messages requis s’affichent dans la sortie du client de débogage WSD, il est probable que la source du problème de l’application a été identifiée. Il est probable que le trafic de multidiffusion n’est pas transmis sur le réseau. Cet échec peut se produire lorsque l’application n’énumère pas correctement les adaptateurs de multidiffusion. Les applications doivent envoyer explicitement le trafic de multidiffusion sur toutes les interfaces réseau ; dans le cas contraire, les paquets ne peuvent pas être générés pour l’interface de bouclage ou pour d’autres interfaces. Pour vérifier que les paquets ne s’affichent pas sur le réseau, suivez les instructions de la procédure d' [inspection des suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md) et recherchez la preuve de l’absence de messages de multidiffusion.

## <a name="verifying-that-messages-are-being-multicast"></a>Vérification de la multidiffusion des messages

Vérifiez toujours que les messages de [sondage](probe-message.md) sont en cours de multidiffusion. Si vous le souhaitez, vérifiez que les messages de [salutation](hello-message.md) et de [résolution](resolve-message.md) sont en cours de multidiffusion. Notez que toutes les applications n’utilisent pas les messages de résolution. Pour plus d’informations sur les modèles de message utilisés par les clients et les hôtes, consultez [modèles de message d’échange de métadonnées](discovery-and-metadata-exchange-message-patterns.md) et de découverte et [prise en main avec résolution des problèmes wsdapi](getting-started-with-wsdapi-troubleshooting.md).

Les messages doivent être déclenchés pour pouvoir être envoyés comme décrit à l’étape 3 ci-dessus. Le client de débogage WSD affiche le message SOAP brut comme sortie. Étant donné que tous les messages imprimés par le client de débogage WSD en mode de multidiffusion sont reçus sur un socket de multidiffusion, l’adresse de destination du message n’est pas affichée.

L’exemple suivant de sortie du client de débogage WSD affiche un message de sondage. L' \<wsa:Action> élément identifie le message en tant que message de sondage. Examinez le \<wsa:Action> champ pour vérifier que le message reçu était un message de sondage.

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

L’exemple suivant de sortie du client de débogage WSD affiche un message de salutation. L' \<wsa:Action> élément identifie le message en tant que message de salutation.

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a>Filtrage des résultats du client de débogage WSD

Le filtrage des résultats du client de débogage WSD peut aider à identifier le trafic d’incidents impliquant l’appareil. Le filtrage est uniquement nécessaire sur les réseaux bruyants.

Il existe deux façons de filtrer les résultats. Les adresses IP à filtrer peuvent être identifiées explicitement lors du démarrage du client de débogage WSD. Les adresses IP peuvent également être spécifiées après le démarrage du client. Cette section décrit les deux méthodes.

**Pour spécifier des adresses IP à filtrer au démarrage du client de débogage WSD**

1.  Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).
2.  Collectez la ou les adresses IP de l’appareil. Si l’appareil a plusieurs adresses (par exemple, il a à la fois des adresses IPv4 et IPv6), toutes les adresses doivent être collectées.
3.  Ouvrez une invite de commandes et exécutez la commande suivante : **WSDDebug \_client.exe/mode multicast/IP Add***<device IP>*

*<device IP>* est une adresse IP. La liste suivante présente quelques exemples de formats pour cette adresse IP.

-   192.168.0.1
-   ::1
-   mydevice.contoso.com

Le client de débogage WSD résout automatiquement les noms d’hôte fournis à l’invite de commandes.

**Pour filtrer les résultats après le démarrage du client de débogage WSD**

1.  Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).
2.  Collectez la ou les adresses IP de l’appareil. Si l’appareil a plusieurs adresses (par exemple, il a à la fois des adresses IPv4 et IPv6), toutes les adresses doivent être collectées.
3.  Ouvrez une invite de commandes et exécutez la commande suivante : **WSDDebug \_client.exe la multidiffusion/mode**
4.  À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : **Ajout d’adresses IP***<device IP>*
5.  Répétez l’étape 4 jusqu’à ce que toutes les adresses IP d’appareil aient été ajoutées.

La procédure suivante suppose que le client de débogage WSD a été démarré et que le filtrage par adresse IP se produit.

**Pour vérifier que les adresses IP correctes sont filtrées**

-   À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : **Print IP**

    La liste des adresses IP filtrées s’affiche.

La procédure suivante suppose que le client de débogage WSD a été démarré et que le filtrage par adresse IP se produit.

**Pour désactiver le filtrage**

-   À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : **IP Clear**

    Tout le trafic de multidiffusion s’affiche désormais dans la sortie de débogage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



