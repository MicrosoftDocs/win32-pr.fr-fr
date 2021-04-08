---
title: Noms d’hôtes et adresses IP
description: Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Noms d’hôtes et adresses IP SNMP
- Noms d’hôtes, résolution SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672586"
---
# <a name="host-names-and-ip-addresses"></a>Noms d’hôtes et adresses IP

Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion. Les ordinateurs qui exécutent le système d’exploitation Windows utilisent un fichier d’hôte qui, à cet effet, mappe les noms d’hôte à des adresses IP.

Le fichier hôte est un fichier texte qui répertorie les noms d’hôte et les adresses IP explicites. Le fichier hôte est automatiquement chargé en mémoire au démarrage et consulté lorsqu’un nom d’hôte requiert une résolution. Si le fichier hôte ne contient pas les informations de mappage requises pour résoudre un nom d’hôte spécifique en son adresse IP, une requête de résolution est effectuée sur un serveur DNS.

SNMP utilise le service WINS (Windows Internet Service de nommage) pour la résolution de noms d’hôte. WINS permet de mapper des noms NetBIOS, ou des noms de machine, à des adresses IP sur des réseaux TCP/IP. Si l’ordinateur ne peut pas accéder à un serveur WINS, le service SNMP utilise le fichier d’hôte pour résoudre les noms d’hôte en adresses IP.

Le service SNMP prend en charge l’utilisation des noms d’hôtes et des adresses IP. Toutefois, lorsque vous avez le choix entre utiliser des noms d’hôte ou des adresses IP pour identifier les emplacements réseau, vos applications de gestion SNMP doivent utiliser des noms d’hôte. Si vous utilisez des noms d’hôte, ajoutez tous les mappages de nom d’hôte et d’adresse IP des systèmes participants au fichier hôte.

 

 




