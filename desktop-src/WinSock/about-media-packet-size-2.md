---
description: La taille des paquets multimédias a une incidence sur la capacité des protocoles IPX à transférer des données sur les réseaux et peut s’avérer difficile à gérer, indépendamment du transport.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: À propos de la taille des paquets multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03be30402dc94b22315292b281565572f04cbc89803eeed79f67d55a77ceeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412189"
---
# <a name="about-media-packet-size"></a>À propos de la taille des paquets multimédias

La taille des paquets multimédias a une incidence sur la capacité des protocoles IPX à transférer des données sur les réseaux et peut s’avérer difficile à gérer, indépendamment du transport. IPX ne segmente pas les paquets, pas plus qu’il ne signale les pertes de paquets en raison de violations de taille. Cela signifie qu’une entité de la station de fin doit conserver la connaissance de la taille de paquet maximale à utiliser sur n’importe quel chemin d’accès réseau donné. Traditionnellement, les datagrammes IPX et les services orientés connexion SPX ont laissé cette charge pour l’application, tandis que SPXII a utilisé une grande négociation de paquets Internet pour la gérer de manière transparente.

Winsock tente de définir des limites de taille de paquet rationnelle pour ses différents protocoles IPX, comme décrit dans la section suivante. Ces limites peuvent être consultées et modifiées par les applications via les options de socket Set/Set. Lors de la détermination de la taille maximale des paquets, les trois points importants sont les suivants :

-   \# Taille du paquet multimédia
-   \# Taille des paquets routables
-   \# Taille du paquet de station finale

La *taille des paquets multimédias* reflète la taille maximale des paquets acceptable sur tous les supports que le paquet traverse vers sa destination. La taille des paquets varie en fonction des supports tels que Ethernet et Token Ring. La quantité d’espace de données dans un paquet peut également varier au sein d’un média donné, en fonction de la disposition de l’en-tête de paquet. Par exemple, la taille des données effectives d’un paquet Ethernet varie selon qu’il est de type Ethernet II, Ethernet 802,2 ou Ethernet.

La *taille des paquets routables* reflète la taille maximale des paquets qu’un routeur intermédiaire est disposé à transférer. La plupart des routeurs IPX sont conçus pour acheminer n’importe quel datagramme de taille, à condition qu’il reste dans la taille du média du réseau d’envoi et de réception. Toutefois, les routeurs plus anciens peuvent limiter la taille maximale des paquets à 576 octets, y compris les en-têtes de protocole.

La taille des paquets de la *station finale* reflète la taille des mémoires tampons d’écoute que les stations finales ont publiées pour recevoir des paquets entrants. Même lorsque les limites des supports et des routeurs autorisent un paquet, elles peuvent être ignorées par la station finale si l’application réceptrice a publié une mémoire tampon plus petite. De nombreuses applications IPX/SPX traditionnelles limitent la taille de la mémoire tampon de réception, de sorte que la partie des données ne doit pas être supérieure à 512 ou 1024 octets.

 

 



