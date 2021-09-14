---
description: Les mesures sont utilisées pour mesurer les aspects des performances du réseau et du protocole.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: terminologie réseau (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414519"
---
# <a name="network-terminology-windows-sockets-2"></a>terminologie réseau (Windows sockets 2)

Les mesures sont utilisées pour mesurer les aspects des performances du réseau et du protocole. Les valeurs de ces métriques dans différents scénarios indiquent le niveau de performances d’une application réseau. Cette section définit les termes et métriques utilisés à l’ensemble du secteur pour mesurer les performances des applications réseau. Ces termes sont utilisés dans le reste de ce guide.

-   Temps aller-retour (RTT)

    Durée, en millisecondes, nécessaire à la demande d’effectuer un voyage d’un ordinateur source vers un ordinateur de destination, puis de nouveau. Des valeurs inférieures indiquent de meilleures performances. Les heures de chemin d’accès direct et de retour ne sont pas nécessairement égales.

    Les valeurs RTT sont affectées par l’infrastructure réseau, la distance entre les nœuds, les conditions réseau et la taille des paquets. Taille du paquet, congestion et impact de la compressibilité sur la surcharge sur les liaisons lentes, telles que les connexions d’accès à distance. D’autres facteurs affectent RTT, y compris la correction des erreurs de transfert et la compression de données, qui introduisent des mémoires tampons et des files d’attente qui augmentent RTT et, par conséquent, réduisent les performances.

-   Goodput

    Mesure des données d’application utiles traitées avec succès par le destinataire, en bits par seconde. Goodput permet de mesurer le débit effectif ou utile et comprend uniquement les données d’application. les en-têtes de paquet, de protocole et de média sont considérés comme des surcharges et ne font pas partie de goodput.

-   Surcharge de protocole

    Octets qui ne sont pas des applications, y compris les trames de protocole et de support, divisés par le nombre total d’octets transmis. La valeur est exprimée sous la forme d’un pourcentage. Des valeurs plus élevées indiquent une baisse des performances.

    La surcharge est calculée pour les deux directions dans ce guide, mais peut être calculée séparément pour chaque direction.

-   Bandwidth-Delay produit

    Produit de la bande passante bits par seconde du réseau et temps RTT (en secondes). Cette valeur correspond au nombre de bits nécessaires pour remplir la bande passante réseau disponible. Lorsque la valeur de la largeur de bande-délai du produit est élevée, la pile TCP/IP doit gérer de grandes quantités de données non acquittées afin de garder le pipeline complet. La bande passante-délai du produit est une mesure de bout en bout clé pour les applications de streaming.

 

 



