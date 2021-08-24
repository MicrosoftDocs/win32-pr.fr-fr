---
title: Vue d’ensemble de DNS
description: DNS est un service standard utilisé pour localiser des ordinateurs sur un réseau IP (Internet Protocol).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a47874606491c1baf5c52ca7934d7e0c3156a6ab99f9726e6c000d9eb3cb65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967469"
---
# <a name="dns-overview"></a>Vue d’ensemble de DNS

DNS est un service standard utilisé pour localiser des ordinateurs sur un réseau IP (Internet Protocol). les réseaux IP, tels que les réseaux Internet et Windows 2000, s’appuient sur des adresses basées sur des nombres, telles que composées, pour les informations de ferry sur le réseau. Les utilisateurs du réseau s’appuient sur des noms basés sur des caractères, tels que `www.microsoft.com` . Par conséquent, il est nécessaire de traduire des adresses de type caractère ou convivial ( `www.microsoft.com` ) en adresses basées sur un nombre (composées) que le réseau peut reconnaître. DNS est le service de choix dans Windows 2000 pour localiser les ressources et les traduire en adresses IP correspondantes.

DNS utilise une base de données spécialisée d’enregistrements de ressources, communément appelée RR, pour répondre aux requêtes de résolution de noms de client. Avant DNS, la résolution de noms sur Internet a été obtenue avec le [*fichier hosts*](h-gly.md), qui sont des fichiers créés manuellement qui associent des noms d’hôtes à des adresses IP.

Lorsqu’un nouveau client a été ajouté au réseau, un administrateur devait mettre à jour manuellement le fichier hosts, puis copier (répliquer) ce fichier sur tous les autres ordinateurs du réseau afin que le nouvel hôte soit accessible par tous. Au fur et à mesure de la croissance d’Internet, cette forme de résolution de noms était clairement insuffisante ; Il a été trop gourmand en gestion et n’a pas été mis à l' [*échelle*](s-gly.md). Le fichier hosts vient d’être plus volumineux, et parce qu’il a utilisé un [*espace de noms plat*](f-gly.md) (voir aussi [espace de nom](name-space.md)), il n’a pas pu être partitionné et devait être distribué dans son intégralité. La solution était DNS.

-   DNS a remplacé l’espace de noms plat du fichier des hôtes par un [*espace de noms hiérarchique*](h-gly.md). Avec un espace de noms hiérarchique, les informations sur les noms d’hôtes et les adresses IP peuvent être partitionnées et distribuées. ainsi, l’évolutivité est obtenue. Par exemple, dans le domaine widgets.products.microsoft.com fictif, la responsabilité de la résolution de noms peut être partitionnée afin que plusieurs serveurs puissent gérer la résolution de noms pour différentes parties de l’espace de noms :
    -   Un serveur peut être responsable de la résolution de la première partie (microsoft.com) et peut ensuite transférer la demande de résolution de nom au serveur DNS suivant dans la hiérarchie.
    -   Le serveur DNS suivant peut être responsable de la résolution de la partie suivante de l’espace de noms (produits).
    -   Enfin, la requête peut être transférée à un troisième serveur DNS chargé de résoudre la dernière partie du nom (widgets).

Les serveurs DNS dans chaque partie de l’espace de noms hiérarchique doivent gérer une base de données d’enregistrements de ressources pour les hôtes, mais uniquement dans leur partie de la hiérarchie. Ainsi, le serveur (ou les serveurs) dans la partie Products de widgets.products.microsoft.com conserve les RR uniquement pour la partie Products de l’espace de noms hiérarchique, et non pour la partie microsoft.com ou les widgets de l’espace de noms.

 

 




