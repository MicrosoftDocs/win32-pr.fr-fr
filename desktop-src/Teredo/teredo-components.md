---
title: Composants Teredo
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'En savoir plus sur : composants Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013385"
---
# <a name="teredo-components"></a>Composants Teredo

L’infrastructure [Teredo](about-teredo.md) est constituée des composants suivants :

## <a name="teredo-clients"></a>Clients Teredo

Un client Teredo est un nœud IPv6/IPv4 qui prend en charge une interface de tunneling Teredo par le biais de laquelle les paquets sont acheminés vers d’autres clients ou nœuds Teredo sur Internet IPv6 (via un relais Teredo). Un client Teredo communique avec un serveur Teredo pour obtenir un préfixe d’adresse à partir duquel une adresse IPv6 basée sur Teredo est configurée ou utilisée pour faciliter la communication avec d’autres clients ou hôtes Teredo sur Internet IPv6.

Windows xp avec service pack 1 (sp1) avec le Pack de mise en réseau avancée, Windows XP avec service pack 2 (sp2), Windows server 2003 avec service pack 1 (sp1), Windows server 2003 avec service pack 2 (sp2), Windows Vista et Windows Server 2008 incluent tous le client Teredo.

## <a name="teredo-servers"></a>Serveurs Teredo

Un serveur Teredo est un nœud IPv6/IPv4 connecté à la fois à l’Internet IPv4 et à Internet IPv6, et prend en charge une interface de tunneling Teredo sur laquelle les paquets sont reçus. Le rôle général du serveur Teredo est d’aider à la configuration d’adresse des clients Teredo et à faciliter la communication initiale entre les clients Teredo et d’autres clients Teredo ou entre les clients Teredo et les hôtes IPv6 uniquement. Le serveur Teredo écoute le trafic Teredo sur le port UDP 3544.

Contrairement au client, le serveur Teredo n’est pas inclus dans les plateformes d’exploitation Microsoft. pour faciliter la communication entre les ordinateurs clients teredo Windows, Microsoft a déployé des serveurs teredo sur Internet IPv4.

## <a name="teredo-relays"></a>Relais Teredo

Un relais Teredo est un routeur IPv6/IPv4 qui peut transférer des paquets entre des clients Teredo sur Internet IPv4 (à l’aide d’une interface de tunnel Teredo) et des hôtes IPv6 uniquement. Dans certains cas, le relais Teredo interagit avec un serveur Teredo pour faciliter la communication initiale entre les clients Teredo et les hôtes IPv6 uniquement. Le relais Teredo écoute le trafic Teredo sur le port UDP 3544.

À l’instar du serveur Teredo, les plateformes d’exploitation Microsoft n’incluent pas la fonctionnalité de relais Teredo. Microsoft ne prévoit pas actuellement de déployer des relais Teredo sur Internet IPv4. Les relais Teredo ne sont pas requis pour communiquer avec les relais Teredo spécifiques à l’hôte.

## <a name="teredo-host-specific-relays"></a>Relais de Host-Specific Teredo

La communication entre les clients Teredo et les hôtes IPv6 qui sont configurés avec une adresse globale doit passer par un relais Teredo. Cela est nécessaire pour les hôtes IPv6 uniquement connectés à Internet IPv6. Toutefois, lorsque l’hôte IPv6 prend en charge IPv6 et IPv4 et connecté à la fois à l’Internet IPv4 et à Internet IPv6, la communication doit se produire entre le client Teredo et l’hôte IPv6 sur Internet IPv4, au lieu d’avoir à traverser l’Internet IPv6 et à passer par un relais Teredo.

Un relais Teredo spécifique à l’hôte est un nœud IPv6/IPv4 qui dispose d’une interface et d’une connectivité à l’Internet IPv4 et à Internet IPv6 et peut communiquer directement avec les clients Teredo sur Internet IPv4, sans qu’il soit nécessaire de recourir à un relais Teredo intermédiaire. La connectivité à l’Internet IPv4 peut se faire via une adresse IPv4 publique ou via une adresse IPv4 privée et un traducteur d’adresses réseau (NAT) voisin. La connectivité à Internet IPv6 peut être effectuée via une connexion directe à Internet IPv6 ou via une technologie de transition IPv6 telle que 6to4, où les paquets IPv6 sont transférés via le tunnel sur Internet IPv4. Le relais Teredo spécifique à l’hôte est à l’écoute sur le port UDP 3544 pour le trafic Teredo.

Windows xp avec le pack de mise en réseau avancée, Windows xp avec sp2, Windows server 2003 avec sp1, Windows server 2003 avec sp2, Windows Vista et Windows server 2008 incluent une fonctionnalité de relais spécifique à l’hôte Teredo, qui est automatiquement activée si une adresse globale est affectée à l’ordinateur. Une adresse globale est assignée dans un message d’annonce de routeur reçu à partir d’un routeur IPv6 natif, d’un routeur ISATAP ou d’un routeur 6to4. Si l’ordinateur n’a pas d’adresse globale, la fonctionnalité du client Teredo est activée.

le relais teredo spécifique à l’hôte permet aux clients teredo de communiquer efficacement avec les hôtes 6to4, les hôtes IPv6 avec un préfixe global non-6to4, ou les hôtes ISATAP ou 6over4 au sein d’organisations qui utilisent un préfixe global pour leurs adresses, à condition que les deux ordinateurs hôtes utilisent une version de Windows qui prend en charge Teredo.

 

 




