---
title: Résolution de noms pour Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'En savoir plus sur : résolution de noms pour Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d9c41685977ef5a4ae3e94996a8d1a59db5f9812e2ed8efe758878a9055c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001687"
---
# <a name="name-resolution-for-teredo"></a>Résolution de noms pour Teredo

L’interface Teredo utilise actuellement les protocoles suivants pour la résolution de noms :

## <a name="domain-name-system"></a>Système de nom de domaine

Le système DNS (Domain Name System) est actuellement la technologie de résolution de noms la plus importante sur Internet. La plupart des serveurs Web inscrivent les adresses URL avec les serveurs DNS. Toutefois, les adresses d’un réseau privé ne sont pas inscrites auprès des serveurs DNS, car la plupart des utilisateurs privés obtiennent des adresses IP via le protocole DHCP (Dynamic Host Configuration Protocol) à partir de leur fournisseur de services Internet. Les baux DHCP sont relativement courts et prennent entre 48 et 72 heures pour propager un nom dans le Cloud DNS. Par conséquent, DNS a prouvé qu’il s’agit d’une méthode inefficace pour obtenir l’adresse IP publique d’un utilisateur d’une famille. Une adresse Teredo comprend l’adresse IPv4 publique et hérite donc au moins la même volatilité des adresses IPv4. Par conséquent, les adresses Teredo ne sont actuellement pas inscrites dans DNS.

## <a name="peer-name-resolution-protocol"></a>Protocole PNRP

Le protocole PNRP (Peer Name Resolution Protocol) est une technologie DNS distribuée qui stocke des adresses IP sur des milliers d’ordinateurs utilisateur qui font partie d’un Cloud PNRP. à l’aide de Windows Vista, n’importe quel utilisateur privé peut choisir de devenir membre d’un cloud pnrp et de publier son adresse IPv6 Teredo sur le réseau pnrp. Contrairement aux adresses fournies aux serveurs DNS, la propagation des adresses sur le réseau PNRP prend généralement moins d’une minute. Étant donné que les adresses Teredo peuvent changer fréquemment (l’adresse IPv4 externe fournie par le fournisseur de services Internet peut changer ou que le port externe utilisé par le périphérique de passerelle Internet de l’utilisateur peut changer), PNRP s’est avéré être un mécanisme efficace pour les particuliers. Les noms PNRP, les adresses se terminant par « . pnrp.net » sont basés sur des propriétés système uniques qui ne changent pas. Par conséquent, un nom PNRP est un moyen fiable de se connecter à un utilisateur à distance. L’API [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) peut être utilisée pour obtenir l’adresse IP à l’aide de la technologie PNRP (noms DNS se terminant par « . PNRP.net ») et établir une connexion avec d’autres hôtes.

 

 
