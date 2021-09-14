---
description: Internet Protocol Helper (assistance IP) aide l’administration réseau de l’ordinateur local en permettant aux applications de récupérer des informations sur la configuration réseau de l’ordinateur local et de modifier cette configuration.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: À propos de l’assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50587b4abdcbad0cddd6d6ce3281c908fdebef4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223940"
---
# <a name="about-ip-helper"></a>À propos de l’assistance IP

Internet Protocol Helper (assistance IP) aide l’administration réseau de l’ordinateur local en permettant aux applications de récupérer des informations sur la configuration réseau de l’ordinateur local et de modifier cette configuration. L’assistance IP fournit également des mécanismes de notification pour garantir qu’une application est avertie lorsque certains aspects de la modification de la configuration du réseau de l’ordinateur local sont modifiés.

La plupart des fonctions d’assistance IP passent des paramètres de structure qui représentent des types de données associés à la technologie de [base d’informations de gestion](/previous-versions/windows/desktop/mib/about-management-information-base) . Les fonctions d’assistance IP utilisent ces structures pour représenter diverses informations de mise en réseau, telles que les entrées de cache ARP. Étant donné que ces structures sont également utilisées par l’API MIB, elles sont décrites dans la [référence de base d’informations de gestion](/previous-versions/windows/desktop/mib/management-information-base-reference). Bien que l’API d’assistance IP utilise ces structures, l’application d’assistance IP est distincte de la base d’informations de gestion (MIB) et du protocole SNMP (simple Network Management Protocol).

La documentation de l’assistance IP utilise les termes « adaptateur » et « interface » de manière intensive. Un « adaptateur » est un terme hérité qui est une forme abrégée de carte réseau, qui a initialement fait l’appel d’une certaine forme de matériel réseau. Un adaptateur est une abstraction au niveau de Datalink.

Une « interface » est un terme plus récent utilisé dans les documents RFC de l’IETF. Les documents RFC définissent une interface en tant que concept abstrait qui représente la pièce jointe d’un nœud à un lien. Une interface est une abstraction au niveau de l’adresse IP.

Les termes de l’adaptateur et de l’interface sont utilisés de manière interchangeable dans la documentation de l’assistance IP. Dans la documentation de l’assistance IP, une liste de cartes peut inclure une interface de réseau étendu (WAN) logicielle, ainsi que l’interface de bouclage (aucune d’elles ne fait référence à un périphérique matériel). Dans les API d’assistance IP, il existe un mappage un-à-un entre les adaptateurs et les interfaces.

L’assistance IP fournit des fonctionnalités dans les domaines suivants :

-   [Récupération d’informations sur la configuration réseau](retrieving-information-about-network-configuration.md)
-   [Gestion des cartes réseau](managing-network-adapters.md)
-   [Gestion des interfaces](managing-interfaces.md)
-   [Gestion des adresses IP](managing-ip-addresses.md)
-   [Utilisation du protocole de résolution d’adresses](using-the-address-resolution-protocol.md)
-   [Récupération d’informations sur le protocole Internet et le protocole de message de contrôle Internet](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Gestion du routage](managing-routing.md)
-   [Réception des notifications d’événements réseau](receiving-notification-of-network-events.md)
-   [Récupération d’informations sur le protocole de contrôle de transmission et le protocole de datagramme utilisateur](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
