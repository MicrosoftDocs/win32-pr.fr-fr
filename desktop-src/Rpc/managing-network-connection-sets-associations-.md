---
title: Gestion des groupes de connexions réseau (associations)
description: à partir de Windows 2000, le temps d’exécution RPC peut gérer plusieurs connexions entre le client et le serveur.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Gestion des ensembles de connexions réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def88053639c2911dca26d57a080c7fbcbd71728000bee2f12ca7440cb56320b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928385"
---
# <a name="managing-network-connection-sets-associations"></a>Gestion des groupes de connexions réseau (associations)

à partir de Windows 2000, le temps d’exécution RPC peut gérer plusieurs connexions entre le client et le serveur. Cela facilite l’opération sur les transports qui ne prennent pas en charge la modification de l’identité du client sans rétablir la connexion, les clients multithread et les clients asynchrones. L’ensemble de connexions entre un processus client et un point de terminaison de serveur est appelé *Association* dans la terminologie RPC. La compréhension des associations peut améliorer l’implémentation de RPC.

Dans un scénario d’identité à un seul client et à un seul thread, RPC ouvre une connexion entre un processus client et un point de terminaison de serveur pour effectuer des appels RPC. Lorsqu’un appel RPC synchrone est effectué, le client envoie la demande au serveur sur cette connexion et reçoit également la réponse. Lorsque le nombre de threads qui effectuent des appels RPC dans le processus client augmente, l’identité de sécurité du client peut changer. Lorsque les appels asynchrones/de canaux sont mélangés à des appels synchrones sur le client, RPC peut nécessiter plusieurs connexions réseau. Toutes les connexions dans le jeu sont placées dans un pool de connexions appelé Association.

Un appel de procédure distante synchrone utilise exclusivement une connexion donnée pour se conformer aux normes RPC. Une connexion utilisée par un appel RPC synchrone est considérée comme occupée si une demande a été envoyée, mais qu’aucune réponse n’a été reçue. Aucun autre trafic n’est autorisé sur cette connexion tant que la réponse n’est pas reçue. Le temps d’exécution RPC tente de multiplexer les appels RPC asynchrones et de canal sur la même connexion. Les appels synchrones/asynchrones/de canal ne peuvent pas être mélangés sur la même connexion, ce qui signifie qu’une connexion donnée peut être utilisée pour les appels RPC synchrones ou pour les appels RPC/de canal asynchrone.

RPC tente de réutiliser les connexions à partir du pool de manière agressive. Lorsqu’un nouvel appel RPC est effectué, RPC tente de trouver une connexion appropriée à partir du pool et crée une nouvelle connexion uniquement si une connexion appropriée est introuvable. Pour qu’une connexion soit considérée comme appropriée, elle doit :

-   Être du type approprié (synchrone ou asynchrone/de canal).
-   Soyez gratuit.
-   Avoir la même identité de sécurité que le handle de liaison sur lequel l’appel est effectué. Si le suivi dynamique des identités est utilisé, l’identité du descripteur de liaison est actualisée à partir du jeton de thread au début de l’appel. Si le suivi d’identité statique est utilisé, l’identité du client marquée sur le handle de liaison est utilisée.

Lorsque l’appel est terminé, une fois la réponse reçue, la connexion est marquée comme étant libre et peut être utilisée pour d’autres appels RPC.

Impossible de modifier l’identité de sécurité sur une connexion. Par exemple, si un grand nombre d’appels au même serveur sont effectués sous différentes identités de sécurité, le nombre de connexions dans le pool de threads augmente. L’Association est comptée comme une référence, et lorsque toutes les références ont disparu, elle arrête et ferme toutes les connexions. Chaque handle de liaison et chaque handle de contexte contiennent une référence sur l’Association. Lorsque tous les sont fermés, l’Association disparaît. sur Windows XP, les associations ne disparaissent pas nécessairement immédiatement ; ils peuvent rester pendant une brève période (la période cible est de 20 secondes, mais le temps d’exécution RPC peut choisir de différer la destruction de l’Association si aucun thread n’est disponible pour l’exécution de la tâche). Si vous ne souhaitez pas que l’Association reste active après la fermeture du dernier handle de contexte/handle de liaison, utilisez l’option de désactivation de l’appel de procédure distante RPC \_ C \_ \_ \_ pour forcer le runtime RPC à fermer immédiatement la connexion.

 

 




