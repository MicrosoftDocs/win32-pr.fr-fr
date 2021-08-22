---
title: Noms d’hôtes et adresses IP
description: Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Noms d’hôtes et adresses IP SNMP
- Noms d’hôtes, résolution SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009507"
---
# <a name="host-names-and-ip-addresses"></a>Noms d’hôtes et adresses IP

Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion. les ordinateurs qui s’exécutent sur le système d’exploitation Windows utilisent un fichier d’hôte qui, à cet effet, mappe les noms d’hôte à des adresses IP.

Le fichier hôte est un fichier texte qui répertorie les noms d’hôte et les adresses IP explicites. Le fichier hôte est automatiquement chargé en mémoire au démarrage et consulté lorsqu’un nom d’hôte requiert une résolution. Si le fichier hôte ne contient pas les informations de mappage requises pour résoudre un nom d’hôte spécifique en son adresse IP, une requête de résolution est effectuée sur un serveur DNS.

SNMP utilise le Service de nommage Windows Internet (WINS) pour la résolution de nom d’hôte. WINS permet de mapper des noms NetBIOS, ou des noms de machine, à des adresses IP sur des réseaux TCP/IP. Si l’ordinateur ne peut pas accéder à un serveur WINS, le service SNMP utilise le fichier d’hôte pour résoudre les noms d’hôte en adresses IP.

Le service SNMP prend en charge l’utilisation des noms d’hôtes et des adresses IP. Toutefois, lorsque vous avez le choix entre utiliser des noms d’hôte ou des adresses IP pour identifier les emplacements réseau, vos applications de gestion SNMP doivent utiliser des noms d’hôte. Si vous utilisez des noms d’hôte, ajoutez tous les mappages de nom d’hôte et d’adresse IP des systèmes participants au fichier hôte.

 

 




