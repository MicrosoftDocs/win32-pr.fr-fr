---
title: Prévention des blocages côté client
description: Il existe deux manières pour lesquelles votre client peut bloquer la connectivité réseau, les demandes du serveur peuvent être perdues ou le serveur lui-même peut se bloquer. Avec les options par défaut, RPC n’expire jamais un appel, et votre thread client attend indéfiniment une réponse.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC appel de procédure distante, meilleures pratiques, prévention des blocages du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da79573e59e30c58a7c236b35293b678c93dde6bf999b477de054d6f3c62971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927294"
---
# <a name="preventing-client-side-hangs"></a>Prévention des blocages côté client

Il existe deux façons de bloquer le client : la connectivité réseau peut entraîner la perte des demandes du serveur, ou le serveur lui-même peut se bloquer. Avec les options par défaut, RPC n’expire jamais un appel, et votre thread client attend indéfiniment une réponse.

Il existe deux méthodes pour éviter cela : conserver les actifs et les délais d’expiration.

## <a name="tcp-keep-alives"></a>TCP Keep Alive

Le client peut être configuré pour effectuer un test ping périodique du serveur afin de s’assurer que le serveur est actif et en cours d’exécution. Les pings sont des connexions TCP persistantes pour les séquences de protocole [**\_ http**](/windows/desktop/Midl/ncacn-http) [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) et ncacn, et par conséquent, elles sont efficaces dans l’utilisation du processeur et la bande passante réseau. Pour activer Keep Alive sur un appel de procédure distante donné, utilisez la fonction [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) avant d’initier l’appel. Cette fonction prend un handle de liaison et un délai d’attente comme arguments. Chaque appel de procédure distante sur ce handle de liaison après **RpcMgmtSetComTimeout** utilise le délai d’expiration fourni.

Le paramètre timeout de la fonction [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) spécifie la durée d’attente de l’exécution de l’appel de procédure distante avant qu’il active Keep Alive. Le délai d’attente est une valeur comprise entre 0 et 10, où 0 correspond au délai d’expiration minimal et 10 à un délai d’attente infini (pas de délai d’attente). Le délai d’attente n’est pas en secondes. la traduction de la valeur de délai d’attente fournie à la fonction **RpcMgmtSetComTimeout** en secondes est effectuée par le runtime RPC, et est spécifique à l’implémentation.

le tableau suivant fournit la traduction en secondes pour Windows 2000 et Windows XP. les futures versions de Windows peuvent modifier le mappage entre le paramètre Timeout et la valeur du délai d’attente, en secondes :

| Paramètre timeout                       | Délai d’expiration réel en secondes |
|-----------------------------------------|----------------------------|
| 0 ( \_ \_ \_ délai d’expiration minimal de liaison RPC C \_ )       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 ( \_ \_ \_ délai d’attente par défaut de liaison C RPC \_ )   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 ( \_ \_ délai maximal de liaison RPC C \_ \_ )       | 1200                       |
| 10 ( \_ \_ \_ délai d’expiration infini de liaison RPC c \_ ) | Délai d’expiration infini          |



 

Une fois les connexions persistantes activées, le client envoie un paquet Keep Alive chaque seconde. S’il n’y a pas d’accusé de réception du serveur pour trois ou plusieurs Keep Alive, le client déclare que la connexion est inactive et fait échouer l’appel de procédure distante. Si le serveur envoie une réponse dans le délai imparti, Keep Alive n’est pas activé. Si le serveur répond à Keep Alive, mais ne répond pas à l’appel de procédure distante, le client continue à envoyer Keep Alive. Une fois que le serveur répond à l’appel RPC, les connexions persistantes sont désactivées. pour Windows 2000, conserver les actifs sont activés uniquement pour les appels RPC synchrones. pour Windows XP, conserver les actifs sont activés pour les appels RPC asynchrones.

Il est tentant de définir Keep Alive à la valeur la plus faible pour garantir que l’application cliente réponde aux problèmes de réseau en temps opportun. Une attention particulière doit être apportée à une telle tentation, et les contrôles appliqués déterminent si une valeur agressive est justifiée. Une fois la connectivité restaurée, un serveur qui perd temporairement la connectivité peut se trouver submergé par l’activité Keep Alive à partir de nombreux clients. En outre, des tâches de calcul longues peuvent prendre plus de deux minutes et le serveur peut se retrouver consacrer plus de temps processeur à conserver les Alives que l’exécution d’un travail utile. Par conséquent, il convient d’utiliser l’utilisation de Keep Alive avec modération. Si le client ne peut pas tolérer que son thread soit lié pendant de longues périodes, il convient de prendre en compte RPC asynchrone.

D’autres séquences de protocole peuvent implémenter des mécanismes différents pour détecter les serveurs qui ne répondent pas, en fonction du transport utilisé. Le transport [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) n’utilise pas Keep Alive. Étant donné que toutes les communications dans **Ncalrpc** sont locales, si le serveur ne répond pas pendant qu’un appel est en cours, l’exécution de RPC sur le client échoue immédiatement à l’appel.

## <a name="call-time-outs"></a>Délais d’appel

Le protocole TCP Keep Alive est parfait si la connectivité réseau est perdue ou si le serveur tombe en panne. Toutefois, si le serveur bloque les blocages en mode utilisateur, TCP Keep Alive retourne correctement, mais l’appel ne retourne jamais. pour traiter ce scénario, une nouvelle option d’exécution a été ajoutée pour Windows XP : \_ \_ \_ délai d’attente de l’appel RPC C OPT \_ . Cette option indique à l’exécution RPC de configurer un minuteur chaque fois qu’il envoie une demande au serveur. Si le minuteur expire, l’appel est automatiquement annulé et se termine avec \_ l' \_ appel RPC S \_ annulé. Tant que le serveur répond dans le délai imparti, le client n’annule pas l’appel. Cela signifie qu’un appel multifragment peut prendre plus de temps que le délai d’attente, car chaque réponse du serveur est reçue pendant le délai d’attente, même si la durée de l’arrivée de toutes les réponses était supérieure à celle du délai d’attente.

En outre, lorsqu’un appel est annulé, le serveur n’est pas averti de l’annulation. Par conséquent, le serveur exécutera probablement l’appel à un moment donné et le client ignorera simplement la réponse du serveur.

Le piège le plus dangereux avec délais d’appel est d’établir un court délai d’attente et de retenter l’appel sur le même serveur. Le scénario suivant illustre les dangers de cette approche :

Imagine un serveur qui fonctionne en proche de sa capacité. Il a un certain nombre de clients avec des délais très courts, par exemple cinq secondes. Une perte temporaire de la connectivité réseau ou de l’encombrement sur un routeur provoque des réponses de quelques secondes à l’expiration du serveur. Sur les réseaux Ethernet, cette situation peut être facilement due à une rafale d’activité sur un lien que le serveur partage avec un autre ordinateur. Le serveur ne gère pas pour envoyer toutes les réponses avant l’expiration du délai de cinq secondes. Les clients obtiennent leurs appels annulés, puis réessayent immédiatement. Le serveur n’a pas conscience que les appels sont retentés et les exécutent également. Par conséquent, au lieu d’exécuter sa charge de travail normale des appels, il exécute 30-50% d’appels supplémentaires, en fonction du nombre de clients ayant dépassé le délai d’attente. Si cela dépasse sa capacité et que le serveur ne peut pas répondre à tous les clients dans un délai de cinq secondes, un autre appel est envoyé au serveur. Les clients continuent de réémettre les mêmes appels, et étant donné que le serveur est surchargé par le traitement des appels précédents, il ne peut pas répondre dans le délai imparti. Une fois qu’il répond, les clients ont atteint le délai d’expiration, émis un nouvel appel et ignoré la réponse. Dans le pire des cas, le serveur ne récupérera pas jusqu’au redémarrage, et selon le modèle d’accès client, risque de ne pas être récupéré tant qu’un nombre suffisant de clients ne sont pas arrêtés.

> [!Note]  
> Les expirations de délai d’appel fonctionnent uniquement sur les séquences de protocole [**\_ http**](/windows/desktop/Midl/ncacn-http) [**\_ IP ncacn \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) et ncacn.

 

 

 