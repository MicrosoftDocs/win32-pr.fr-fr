---
description: Après avoir créé une requête et y avoir ajouté des compteurs, appelez la fonction PdhCollectQueryData pour récupérer les données brutes actuelles de tous les compteurs de la requête.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Collecte des données de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f65280190e67e27783ea7e7387eac0e348aad1a53ad016df3010ae0bfd2ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061237"
---
# <a name="collecting-performance-data"></a>Collecte des données de performances

Après avoir [créé une requête](creating-a-query.md) et y avoir ajouté des compteurs, appelez la fonction [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) pour récupérer les données brutes actuelles de tous les compteurs de la requête.

De nombreux compteurs, tels que les compteurs de taux, requièrent deux échantillons de données pour calculer une valeur de données mise en forme. PDH gère les données de l’exemple actuel et de l’exemple collecté précédemment. La procédure suivante décrit comment collecter des valeurs de compteur qui requièrent deux exemples pour calculer une valeur affichable.

**Pour collecter des valeurs de compteur qui requièrent deux exemples pour calculer une valeur affichable**

1.  Appelez [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) pour collecter le premier exemple.
2.  Appelez la fonction [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) pour attendre au moins une seconde entre les collections.
3.  Appelez à nouveau [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) pour collecter le deuxième exemple.
4.  Appelez la fonction [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) pour calculer une valeur affichable.
5.  Répétez les étapes 2 à 4.

Au lieu d’implémenter vous-même une période d’attente, vous pouvez appeler la fonction [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) , qui crée un thread de minutage qui attend un laps de temps spécifié, collecte l’exemple, puis déclenche un événement défini par l’application.

Si vous souhaitez interroger des données de performances à partir d’un fichier journal, vous pouvez également définir une plage de temps. L’intervalle de temps limite la requête aux échantillons collectés dans l’intervalle de temps (chaque échantillon contient un horodatage pour le moment où il a été collecté). Pour plus d’informations sur la façon de définir et de récupérer des plages de temps, consultez [définition d’une plage de temps pour une requête](setting-a-time-range-for-a-query.md).

Si vous souhaitez collecter des données de performances et les écrire dans un fichier journal, vous devez appeler la fonction [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) au lieu d’appeler [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Pour plus d’informations, consultez [utilisation des fichiers journaux](working-with-log-files.md) et [écriture de données de performances dans un fichier journal](writing-performance-data-to-a-log-file.md).

Pour plus d’informations sur le calcul d’une valeur d’échantillon affichable, consultez [affichage des données de performances](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Fonctionnement des compteurs à plusieurs processeurs

Certains compteurs de performances ont été conçus pour les systèmes à un seul processeur et peuvent ne pas être précis pour les ordinateurs multiprocesseurs. Par exemple, un processus est limité à 100% d’un processeur unique. Toutefois, ses threads peuvent utiliser plusieurs processeurs, en totalisant plus de 100%.

La \\ valeur du compteur « processeur ( \_ total) \\ % temps processeur » correspond à l’utilisation moyenne de tous les processeurs. Par exemple, si vous avez deux processeurs, un à 100% et un autre à 0 pour cent, ce compteur indique 50%. La plage est comprise entre 0 et 100.

La \\ valeur du compteur « process (X) \\ % Process Time » est la somme de l’utilisation du processeur par tous les threads du processus X. Par exemple, sur un ordinateur doté de deux processeurs, si un processus a deux threads, l’un occupant 75% de l’UC et l’autre qui prend 80% d’un autre processeur, ce compteur indique 155 pour cent. La plage de ce compteur est comprise entre 0 et 100 \* ProcessorCount.

* * Windows Server 2003 et Windows XP : * *

Vous pouvez recevoir des valeurs en dehors de la plage de valeurs attendue pour l’utilisation de l’UC. Pour calculer le pourcentage d’utilisation de l’UC, PDH a besoin de deux exemples (chacun avec une valeur brute et un horodatage). Comme PDH utilise uniquement le nom de l’instance pour correspondre aux processus, il peut parfois utiliser deux exemples de processus différents. Par exemple, si trois processus sont échantillonnés et qu’un processus se termine après le troisième exemple, un autre processus est déplacé vers l’emplacement libéré par ce processus terminé. Par conséquent, un compteur mis en forme fournit une valeur incorrecte quand vous mettez en forme le quatrième exemple, car il utilise le troisième exemple du processus terminé et le quatrième exemple du processus qui a été déplacé dans l’emplacement du processus terminé.

Le tableau suivant montre comment cela peut se produire si un processus est arrêté pendant la collecte des données. Le tableau affiche cinq exemples de valeur de compteur pour trois instances du processus X. Les échantillons sont collectés dans un intervalle d’une seconde. Une fois le troisième échantillon collecté, le processus X de l’emplacement 1 est terminé. Lorsque le processus X de l’emplacement 1 est terminé, le processus X dans l’emplacement 2 se déplace vers l’emplacement 1. Lorsque vous collectez le quatrième exemple pour le processus X dans l’emplacement 2, la première valeur est maintenant 20 au lieu de 1 000, et la deuxième valeur est 1 500. Lorsque vous mettez en forme la valeur de compteur, vous recevez 1 480 millisecondes au lieu des 500 millisecondes attendues. Lorsque vous mettez en forme le cinquième exemple de valeur, vous devez récupérer la valeur attendue.

| Exemple   | Emplacement 0 pour le processus X | Emplacement 1 pour le processus X           | Emplacement 2 pour le processus X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Exemple 1 | 0                    | 0                              | 0                                        |
| Exemple 2 | 20                   | 10                             | 500                                      |
| Exemple 3 | 40                   | 20                             | 1 000                                    |
| Exemple 4 | 60                   | 1 500 (à partir de l’emplacement 2 précédent) | Non applicable. Désormais collectées dans l’emplacement 1. |
| Exemple 5 | 80                   | 2 000                          | Non applicable. Désormais collectées dans l’emplacement 1. |



 

 

 
