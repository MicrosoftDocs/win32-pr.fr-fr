---
description: Certaines techniques de programmation s’exécutent dans des problèmes de performances liés à l’implémentation de TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problèmes spécifiques à TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518307"
---
# <a name="tcpip-specific-issues"></a>Problèmes spécifiques à TCP/IP

Certaines techniques de programmation s’exécutent dans des problèmes de performances liés à l’implémentation de TCP/IP. De tels problèmes de performances ne suggèrent pas que le protocole TCP/IP est inefficace ou un goulot d’étranglement des performances. au lieu de cela, ces problèmes sont observés lorsque les opérations TCP/IP ne sont pas comprises.

Les problèmes suivants identifient les scénarios courants dans lesquels la combinaison des choix d’opérations TCP/IP et de développement d’applications réseau entraîne une baisse des performances.

-   Connectez-vous à des applications lourdes.

    Certaines applications instancient une nouvelle connexion TCP pour chaque transaction. L’établissement de connexions TCP prend du temps, fournit des RTTs supplémentaires et est soumis à un démarrage lent. En outre, les connexions fermées sont soumises à TIME-WAIT, qui consomme des ressources système.

    Les applications à connexion intensive sont courantes, car elles sont faciles à créer. le test et la gestion des erreurs sont très simples. La détection des erreurs sur une connexion permanente peut nécessiter du code et des efforts considérables, et par conséquent, elle n’est parfois pas terminée.

    Résolvez cette situation en réutilisant la connexion TCP. Cela peut entraîner une sérialisation sur la connexion TCP, sauf si les transactions sont multiplexées sur plusieurs connexions. Si cette approche est prise, le nombre de connexions doit être limité à deux, et l’encadrement de la couche application et la gestion avancée des erreurs sont requis.

-   Mémoires tampons d’envoi de longueur nulle et blocages envoyés.

    La désactivation de la mise en mémoire tampon à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir la mémoire tampon d’envoi ( \_ SNDBUF) sur zéro est semblable à la désactivation de la mise en cache du disque. Lors de la définition de la mémoire tampon d’envoi à zéro et de l’émission d’envois de blocage, une application a une chance de 50% d’atteindre un accusé de réception retardé de 200 millisecondes.

    Ne désactivez pas la mise en mémoire tampon d’envoi, sauf si vous avez pris en compte l’impact sur tous les environnements réseau. Une exception : les données de streaming utilisant des e/s avec chevauchement doivent définir la mémoire tampon d’envoi sur zéro.

-   Modèle de programmation Send-Send-Receive.

    La structuration d’une application pour exécuter send-send-receives augmente vos chances de rencontrer l’algorithme Nagle, ce qui entraîne un délai de RTT + 200 ms. L’algorithme Nagle peut être rencontré si le dernier envoi est inférieur à la taille maximale du segment TCP (MSS, le nombre maximal de données dans un seul datagramme). MSS peut être une valeur très élevée (64 Ko dans IPv4, et même plus grand dans IPv6). par conséquent, ne comptez pas sur un MSS généralement de petite taille. Une meilleure option consiste à combiner les deux envois en une seule envoi à l’aide de la fonction [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou **memcpy** .

-   Un grand nombre de connexions simultanées.

    Les connexions simultanées ne doivent pas dépasser deux, sauf dans les applications à usage spécial. Le dépassement de deux connexions simultanées entraîne l’ingaspillage des ressources. Une bonne règle consiste à avoir jusqu’à quatre connexions à courte durée de vie, ou deux connexions persistantes par destination.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comportement de l’application](application-behavior-2.md)
</dt> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[L’algorithme Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



