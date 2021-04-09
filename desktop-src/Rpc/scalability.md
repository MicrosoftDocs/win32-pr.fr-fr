---
title: Extensibilité
description: Extensibilité
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Extensibilité
- RPC appel de procédure distante, meilleures pratiques, évolutivité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0728e35d9c9b27494014363c448be9965e39eea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840621"
---
# <a name="scalability"></a>Extensibilité

Le terme, scalabilité, est souvent utilisé de façon inutilisée. Pour cette section, une double définition est fournie :

-   L’évolutivité est la possibilité d’utiliser pleinement la puissance de traitement disponible sur un système multiprocesseur (2, 4, 8, 32 ou plus).
-   L’évolutivité est la possibilité de traiter un grand nombre de clients.

Ces deux définitions associées sont communément appelées *mise à l’échelle*. La fin de cette rubrique fournit des conseils sur la *montée* en charge.

Cette discussion porte exclusivement sur l’écriture de serveurs évolutifs, et non sur des clients évolutifs, car les serveurs évolutifs sont des exigences plus courantes. Cette section traite également de l’évolutivité dans le contexte des serveurs RPC et RPC uniquement. Les meilleures pratiques en matière d’évolutivité, telles que la réduction de la contention, l’évitement des échecs fréquents de cache sur les emplacements de mémoire globaux ou l’évitement de faux partage, ne sont pas abordées ici.

## <a name="rpc-threading-model"></a>Modèle de thread RPC

Lors de la réception d’un appel RPC par un serveur, la routine de serveur (routine de gestionnaire) est appelée sur un thread fourni par RPC. RPC utilise un pool de threads adaptatif qui augmente et diminue à mesure que la charge de travail fluctue. À compter de Windows 2000, le cœur du pool de threads RPC est un port de terminaison. Le port de terminaison et son utilisation par RPC sont réglés pour les routines de serveur de contention de zéro à faible. Cela signifie que le pool de threads RPC augmente agressivement le nombre de threads de maintenance si certains sont bloqués. Il s’agit du présomption que le blocage est rare, et si un thread est bloqué, il s’agit d’une condition temporaire qui est rapidement résolue. Cette approche permet d’obtenir de l’efficacité pour les serveurs de contention insuffisants. Par exemple, un serveur RPC appel void fonctionnant sur un serveur 550MHz à huit processeurs accessible via un réseau SAN à haut débit occupe plus de 30 000 appels void par seconde à partir de plus de 200 clients distants. Cela représente plus de 108 millions appels par heure.

Le résultat est que le pool de threads agressif est réellement utilisé lorsque la contention sur le serveur est élevée. À titre d’illustration, imaginez un serveur lourd utilisé pour accéder à distance à des fichiers. Supposons que le serveur adopte l’approche la plus simple : il lit simplement/écrit le fichier de façon synchrone sur le thread sur lequel le RPC appelle la routine du serveur. Par ailleurs, supposons que nous disposons d’un serveur à quatre processeurs desservant de nombreux clients.

Le serveur démarre avec cinq threads (cela varie en réalité, mais cinq threads sont utilisés pour des raisons de simplicité). Une fois que RPC sélectionne le premier appel RPC, il distribue l’appel à la routine du serveur et la routine du serveur émet les e/s. Rarement, il manque le cache de fichiers, puis bloque l’attente du résultat. Dès qu’il se bloque, le cinquième thread est libéré pour récupérer une demande, et un sixième thread est créé en tant que secours à chaud. En supposant que chaque dixième opération d’e/s n’a pas atteint le cache et se bloque pendant 100 millisecondes (une valeur temporelle arbitraire), et en supposant que le serveur à quatre processeurs fait environ 20 000 appels par seconde (5 000 appels par processeur), une modélisation simpliste prédirea que chaque processeur générera environ 50 threads. Cela suppose un appel qui se bloquera toutes les 2 millisecondes, et après 100 millisecondes, le premier thread est libéré à nouveau afin que le pool se stabilise à environ 200 threads (50 par processeur).

Le comportement réel est plus compliqué, car le nombre élevé de threads entraîne des changements de contexte supplémentaires qui ralentissent le serveur et ralentissent également le taux de création de nouveaux threads, mais l’idée de base est claire. Le nombre de threads s’affiche rapidement à mesure que les threads sur le serveur commencent à se bloquer et attendent un événement (qu’il s’agit d’une e/s ou d’un accès à une ressource).

RPC et le port de terminaison qui permet aux demandes entrantes de gérer le nombre de threads RPC utilisables dans le serveur sont égaux au nombre de processeurs sur l’ordinateur. Cela signifie que sur un serveur à quatre processeurs, une fois qu’un thread revient à RPC, s’il y a quatre threads RPC ou plus utilisables, le cinquième thread n’est pas autorisé à récupérer une nouvelle requête, mais il se trouve à la place dans un état de secours dans le cas où l’un des threads actuellement utilisables est bloqué. Si le cinquième thread attend suffisamment longtemps comme un secours sans que le nombre de threads RPC utilisants ne se libère sous le nombre de processeurs, il est libéré, autrement dit, le pool de threads diminue.

Imaginez un serveur avec de nombreux threads. Comme expliqué précédemment, un serveur RPC finit avec un grand nombre de threads, mais uniquement si les threads se bloquent souvent. Sur un serveur où les threads se bloquent souvent, un thread qui retourne à RPC est bientôt retiré de la liste de secours, car tous les threads actuellement utilisables sont bloqués et reçoivent une demande de traitement. Lorsqu’un thread se bloque, le répartiteur de threads dans le noyau bascule le contexte vers un autre thread. Ce changement de contexte lui-même consomme des cycles d’UC. Le thread suivant va exécuter un code différent, accéder à différentes structures de données et aura une pile différente, ce qui signifie que le taux d’accès au cache mémoire (caches L1 et L2) sera beaucoup plus faible, ce qui ralentit l’exécution. Les nombreux threads qui s’exécutent simultanément augmentent la contention des ressources existantes, telles que le segment de mémoire, les sections critiques dans le code serveur, et ainsi de suite. Cela augmente davantage la contention en tant que convois sur les ressources. Si la mémoire est faible, la sollicitation de la mémoire exercée par le nombre important et croissant de threads provoquera des défauts de page, ce qui augmentera encore la vitesse à laquelle les threads se bloquent et entraînera la création d’un plus grand nombre de threads. En fonction de la fréquence de blocage et de la quantité de mémoire physique disponible, le serveur peut se stabiliser à un niveau de performance inférieur avec un taux de changement de contexte élevé, ou se détériorer jusqu’au point où il accède uniquement au disque dur et au basculement de contexte sans effectuer de travail réel. Cette situation ne s’affiche pas sous la charge de travail légère, bien entendu, mais une charge de travail lourde pose rapidement le problème à la surface.

Comment cela peut-il être évité ? Si les threads sont censés être bloqués, déclarez les appels comme asynchrones, et une fois que la demande entre dans la routine du serveur, faites-la mettre en file d’attente vers un pool de threads de travail qui utilisent les fonctionnalités asynchrones du système d’e/s et/ou RPC. Si le serveur est à son tour, les appels RPC deviennent asynchrones et s’assurent que la file d’attente ne devient pas trop volumineuse. Si la routine de serveur effectue des e/s de fichier, utilisez des e/s de fichier asynchrones pour mettre en file d’attente plusieurs demandes dans le système d’e/s et n’avoir que quelques threads en file d’attente et récupérer les résultats. Si la routine de serveur fait des e/s réseau, utilisez de nouveau les fonctionnalités asynchrones du système pour émettre les requêtes et récupérer les réponses de façon asynchrone et utilisez le moins de threads possible. Une fois que l’e/s est terminée ou que l’appel RPC effectué par le serveur est terminé, terminez l’appel RPC asynchrone qui a fourni la demande. Cela permet au serveur de s’exécuter avec le moins de threads possible, ce qui augmente les performances et le nombre de clients qu’un serveur peut traiter.

## <a name="scale-out"></a>Scale Out

RPC peut être configuré pour fonctionner avec l’équilibrage de la charge réseau (NLB) si NLB est configuré de telle sorte que toutes les demandes d’une adresse de client donnée sont dirigées vers le même serveur. Étant donné que chaque client RPC ouvre un pool de connexions (pour plus d’informations, voir [RPC et le réseau](rpc-and-the-network.md)), il est essentiel que toutes les connexions à partir du pool du client donné finissent sur le même ordinateur serveur. Tant que cette condition est remplie, un cluster d’équilibrage de la charge réseau peut être configuré pour fonctionner comme un serveur RPC volumineux avec une évolutivité potentiellement excellente.

 

 




