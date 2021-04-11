---
description: La famille d’adresses IPX définit la structure d’adressage pour les protocoles qui utilisent l’adressage de socket IPX standard. Pour ces transports, une adresse de point de terminaison se compose d’un numéro de réseau, d’une adresse de nœud et d’un numéro de Socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Famille d’adresses AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113111"
---
# <a name="af_ipx-address-family"></a>\_Famille d’adresses IPX AF

La famille d’adresses IPX définit la structure d’adressage pour les protocoles qui utilisent l’adressage de socket IPX standard. Pour ces transports, une adresse de point de terminaison se compose d’un numéro de réseau, d’une adresse de nœud et d’un numéro de Socket.

Le numéro de réseau est un domaine d’administration et nomme généralement un segment Ethernet ou Token Ring unique. Le numéro de nœud est l’adresse physique d’une station. La combinaison du filet et du nœud constitue une adresse de station unique supposée être unique dans le monde. Les numéros de nœud net et de nœud sont représentés en texte ASCII, en notation de bloc ou en pointillés, comme suit : ' 0101a040, 00001b498765 'ou' 01-01-a0-40, 00-00-1b-49-87-65 '. Les zéros non significatifs ne doivent pas être présents.

Le numéro de socket IPX est un numéro de service de réseau/transport similaire à un numéro de port TCP. il ne doit pas être confondu avec le descripteur de socket Winsock. Les numéros de socket IPX sont globaux pour la station finale et ne peuvent pas être liés à des adresses net/node spécifiques. Par exemple, si la station finale a deux cartes d’interface réseau, un socket lié peut envoyer et recevoir sur les deux cartes. En particulier, les sockets de datagrammes recevaient des datagrammes de diffusion sur les deux cartes.

> [!Caution]  
> SOCKADDR \_ IPX a une longueur de 14 octets et est plus petite que la structure de référence [**sockaddr**](sockaddr-2.md) de 16 octets. Les implémentations IPX/SPX peuvent accepter la longueur de 16 octets, ainsi que la longueur réelle. Si vous utilisez SOCKADDR \_ IPX et une longueur codée en dur de 16 octets, l’implémentation peut supposer qu’elle a accès aux 2 octets qui suivent votre structure.

 



| Champ           | Valeur                                    |
|-----------------|------------------------------------------|
| **\_famille sa**  | Famille d’adresses AF \_ IPX dans l’ordre de l’ordinateur hôte.    |
| **Sa \_ netnum**  | Identificateur du réseau IPX dans l’ordre du réseau. |
| **Sa \_ nodeNum** | Adresse du nœud de station, vidée de droite.     |
| **\_Socket sa**  | Numéro de socket IPX dans l’ordre des réseaux.      |



 

 

 



