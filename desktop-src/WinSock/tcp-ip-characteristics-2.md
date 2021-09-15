---
description: TCP/IP a des caractéristiques qui permettent au protocole de fonctionner comme des exigences de mise en œuvre standardisées.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Caractéristiques de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520889"
---
# <a name="tcpip-characteristics"></a>Caractéristiques de TCP/IP

TCP/IP a des caractéristiques qui permettent au protocole de fonctionner comme des exigences de mise en œuvre standardisées. Ces caractéristiques peuvent être combinées à des choix de développement qui entraînent des performances médiocres. L’impact de ces caractéristiques TCP/IP sur une application varie selon que l’application est transactionnelle ou de diffusion en continu.

Les applications transactionnelles sont affectées par la surcharge requise pour l’établissement et l’arrêt de la connexion. Par exemple, chaque fois qu’une connexion est établie sur un réseau Ethernet, trois paquets d’environ 60 octets chacun doivent être envoyés, et environ un RTT est requis pour l’échange. Lorsque l’arrêt d’une connexion se produit, quatre paquets sont échangés. C’est le cas pour chaque connexion ; une application qui ouvre et ferme des connexions entraîne souvent cette surcharge sur chaque occurrence.

Un autre aspect de TCP/IP est le *démarrage lent*, qui a lieu chaque fois qu’une connexion est établie. Le démarrage lent est une limite artificielle sur le nombre de segments de données qui peuvent être envoyés avant la réception de l’accusé de réception de ces segments. Le démarrage lent est conçu pour limiter l’encombrement du réseau. Lorsqu’une connexion sur Ethernet est établie, quelle que soit la taille de la fenêtre du récepteur, une transmission de 4 Ko peut prendre jusqu’à 3-4 de temps RTT en raison d’un démarrage lent.

Une optimisation TCP/IP appelée l’algorithme Nagle peut également limiter la vitesse de transfert de données sur une connexion. L’algorithme Nagle est conçu pour réduire la surcharge de protocole pour les applications qui envoient de petites quantités de données, telles que Telnet, qui envoie un caractère unique à la fois. Au lieu d’envoyer immédiatement un paquet avec un grand nombre d’en-têtes et de petites données, la pile attend davantage de données de l’application, ou un accusé de réception, avant de continuer.

Les accusés de réception différés, communément appelés *accusés de réception différés*, sont également conçus dans TCP/IP pour permettre une intégration plus efficace des accusés de réception lorsque les données de retour sont à venir de l’application côté réception. Malheureusement, si ces données ne sont pas à venir et que le côté expéditeur attend un accusé de réception, des retards d’environ 200 millisecondes par envoi peuvent se produire.

Lorsqu’une connexion TCP est fermée, les ressources de connexion au niveau du nœud qui a initié la fermeture sont placées dans un état d’attente, appelé temps-attente, pour assurer la protection contre la corruption des données si des paquets en double restent dans le réseau. Cela permet de s’assurer que les deux extrémités sont terminées avec la connexion. Cela peut entraîner une épuisement des ressources requises par connexion, telles que la RAM et les ports, lorsque les applications ouvrent et ferment fréquemment des connexions.

En plus d’être affectées par un accusé de réception retardé et d’autres schémas d’évitement de congestion, les applications de streaming peuvent également être affectées par une taille de fenêtre de réception par défaut trop petite à l’extrémité de réception.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comportement de l’application](application-behavior-2.md)
</dt> <dt>

[Applications de sockets Windows hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[L’algorithme Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



