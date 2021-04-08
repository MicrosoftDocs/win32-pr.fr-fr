---
title: Base de données MIB (Management Information base) SNMP
description: Une base d’informations de gestion (MIB) décrit un ensemble d’objets gérés. Une application de console de gestion SNMP peut manipuler les objets sur un ordinateur spécifique si le service SNMP a une DLL d’agent d’extension qui prend en charge la MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672085"
---
# <a name="the-snmp-management-information-base-mib"></a>Base de données MIB (Management Information base) SNMP

Une base d’informations de gestion (MIB) décrit un ensemble d’objets gérés. Une application de console de gestion SNMP peut manipuler les objets sur un ordinateur spécifique si le service SNMP a une DLL d’agent d’extension qui prend en charge la MIB.

Chaque objet géré dans un MIB a un identificateur unique. L’identificateur comprend le type de l’objet (par exemple, compteur, chaîne, jauge ou adresse), le niveau d’accès de l’objet (par exemple, lecture ou lecture/écriture), les restrictions de taille et les informations de plage.

Le tableau suivant contient une liste partielle des MIB fournis avec le système. Ils sont installés avec le service SNMP dans le répertoire% SystemRoot% \\ system32. Pour obtenir la liste complète des MIB, reportez-vous au kit de ressources Windows.



| MIB         | Description                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCP. MIB    | La MIB définie par Microsoft qui contient des types d’objet pour analyser le trafic réseau entre les hôtes distants et les serveurs DHCP                        |
| HOSTMIB. MIB | Contient les types d’objets pour l’analyse et la gestion des ressources hôtes                                                                                 |
| LMMIB2. MIB  | Couvre les services de station de travail et de serveur                                                                                                           |
| MIB \_ II. MIB | Contient la base d’informations de gestion (MIB-II), qui fournit une architecture et un système simples et réalisables pour la gestion des adresses Internet TCP/IP |
| WINS. MIB    | La MIB définie par Microsoft pour le service WINS (Windows Internet Name Service)                                                                               |



 

**Windows NT :** En règle générale, vous pouvez copier une MIB à partir de l’agent d’extension SNMP qui prend en charge la MIB particulière. Des MIB supplémentaires sont disponibles avec le kit de ressources Windows NT 4,0.

Les dll de l’agent d’extension pour MIB-II, LAN Manager MIB-II et la MIB des ressources de l’ordinateur hôte sont installées avec le service SNMP. Les dll de l’agent d’extension pour les autres MIB sont installées lors de l’installation de leurs services respectifs. Au moment du démarrage du service, le service SNMP charge toutes les dll de l’agent d’extension répertoriées dans le registre.

Les utilisateurs peuvent ajouter d’autres DLL d’agent d’extension qui implémentent des MIB supplémentaires. Pour ce faire, ils doivent ajouter une entrée de Registre pour la nouvelle DLL sous le service SNMP. Ils doivent également inscrire la nouvelle MIB auprès de l’application de la console de gestion SNMP. Pour plus d’informations, consultez la documentation fournie avec votre application console de gestion.

Pour plus d’informations, consultez [MIB Name Tree](mib-name-tree.md).

 

 




