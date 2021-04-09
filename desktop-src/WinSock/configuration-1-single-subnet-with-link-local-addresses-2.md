---
description: La première configuration ne nécessite pas de configuration supplémentaire au-delà de l’installation du protocole Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuration 1 : sous-réseau unique avec adresses lien-local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033986"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Configuration 1 : sous-réseau unique avec adresses lien-local

La première configuration ne nécessite pas de configuration supplémentaire au-delà de l’installation du protocole Microsoft IPv6 Technology Preview. Cette configuration se compose d’au moins deux nœuds sur le même sous-réseau. Dans la terminologie IPv6, les deux nœuds se trouvent sur le même lien sans routeurs intermédiaires.

L’illustration suivante montre la configuration de deux nœuds sur un sous-réseau unique à l’aide d’adresses lien-local.

![deux nœuds utilisant des adresses lien-local.](images/v6mig-1.png)

Par défaut, IPv6 configure les adresses IP de lien local pour chaque interface correspondant aux cartes réseau Ethernet installées. Les adresses lien-local ont le préfixe FE80 ::/64. Les 64 derniers bits de l’adresse IPv6 sont appelés identificateurs d’interface et sont dérivés de l’adresse MAC 48 bits de la carte réseau.

Pour créer l’identificateur d’interface IPv6 à partir de l’adresse MAC Ethernet 48 bits (6 octets) :

-   Les chiffres hexadécimaux 0xFF-Fe sont insérés entre le troisième et le quatrième octet de l’adresse MAC.
-   Le bit universel/local, le deuxième bit de poids faible du premier octet de l’adresse MAC, est complété. S’il s’agit d’un 1, il prend la valeur 0 et, s’il s’agit d’un 0, il est converti en 1.

Par exemple, pour l’adresse MAC 00-60-08-52-F9-D8 :

-   Les chiffres hexadécimaux 0xFF-Fe sont insérés entre 0x08 (le troisième octet) et 0x52 (quatrième octet) de l’adresse MAC, formant l’adresse 64 bits 00-60-08-FF-Fe-52-F9-D8.
-   Le bit universel/local, le deuxième bit de poids faible de 0x00 (le premier octet) de l’adresse MAC est complété. Le deuxième bit de poids faible de 0x00 est 0, qui, lorsqu’il est complété, devient 1. Le résultat est que, pour le premier octet, 0x00 devient 0x02.

Par conséquent, l’identificateur d’interface IPv6 correspondant à l’adresse MAC Ethernet 00-60-08-52-F9-D8 est 02-60-08-FF-Fe-52-F9-D8.

L’adresse lien-local d’un nœud est la combinaison du préfixe FE80 ::/64 et de l’identificateur d’interface 64 bits, exprimée en notation hexadécimale à deux-points IPv6. Par conséquent, l’adresse lien-local de cet exemple de nœud avec le préfixe FE80 ::/64 et l’identificateur d’interface 02-60-08-FF-Fe-52-F9-D8 est FE80 :: 260:8FF : FE52 : F9D8.

Vous pouvez afficher votre adresse de lien local à l’aide de IPv6 si, comme illustré dans l’exemple suivant :

**IPv6 si**

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

L’interface 4 est une interface qui correspond à une carte Ethernet installée avec l’adresse lien-local FE80 :: 210:5aff : FEAA : 20a2.

Pour plus d’informations sur l’adressage IPv6 et une vue d’ensemble des concepts IPv6, consultez le livre blanc Introduction à IPv6.

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Test de la connectivité entre deux hôtes lien-local

Vous pouvez effectuer une requête ping simple (échange de messages ICMPv6 de demande d’écho et de réponse à écho) à l’aide de IPv6 entre deux hôtes lien-local.

**Pour exécuter une commande ping à l’aide d’IPv6 entre deux hôtes lien-local**

1.  Installez la version préliminaire de la technologie Microsoft IPv6 pour Windows sur deux hôtes Windows (hôte A et hôte B) qui se trouvent sur le même lien (sous-réseau).
2.  Utilisez IPv6 si sur l’hôte A pour obtenir l’adresse lien-local de l’interface Ethernet.

    Exemple : l’adresse lien-local de l’hôte A est FE80 :: 210:5aff : FEAA : 20a2.

3.  Utilisez IPv6 si sur l’hôte B pour obtenir l’adresse lien-local de l’interface Ethernet.

    Exemple : l’adresse lien-local de l’hôte B est FE80 :: 260:97FF : FE02:6EA5.

4.  À partir de l’hôte A, exécutez une commande ping sur l’hôte B avec Ping6.exe.

    Exemple : ping6 FE80 :: 260:97FF : FE02:6EA5

Pour spécifier l’adresse source à partir de laquelle les messages de demande d’écho sont envoyés, vous pouvez également utiliser l’option Ping6.exe-s. Par exemple, pour envoyer des demandes d’écho à l’hôte B à partir de l’adresse IPv6 FE80 :: 210:5aff : FEAA : 20a2, utilisez la commande suivante :

**ping6-s FE80 :: 210:5aff : FEAA : 20a2% 4 FE80 :: 260:97FF : FE02:6EA5**

Lors du test ping d’une adresse de lien local ou de site local, il est recommandé de spécifier l’ID d’étendue pour rendre l’adresse de destination non ambiguë. La notation permettant de spécifier l’ID de portée est adresse% Scope-ID. Pour les adresses lien-local, l’ID d’étendue est égal au numéro d’interface tel qu’il est affiché dans la commande IPv6 if. Pour les adresses locales de site, l’ID d’étendue est égal au numéro de site tel qu’il est affiché dans la commande IPv6 if. Par exemple, pour envoyer des messages de demande d’écho à l’hôte B à l’aide de l’ID de portée 4, utilisez la commande suivante :

**ping6 FE80 :: 260:97FF : FE02:6EA5% 4**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configurations recommandées pour IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



