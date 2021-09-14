---
description: Un périphérique de ligne peut représenter un pool de ressources homogènes (canaux) utilisées pour établir des appels. Sur un ordinateur client, un TSP fournit généralement un accès à un ou plusieurs périphériques de ligne.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configurations de ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722dab15763822f6535783ecc8bc18e681e13ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217785"
---
# <a name="line-configurations"></a>Configurations de ligne

Un périphérique de ligne peut représenter un pool de ressources homogènes (canaux) utilisées pour établir des appels. Sur un ordinateur client, un TSP fournit généralement un accès à un ou plusieurs périphériques de ligne.

Voici quelques exemples de la façon dont un fournisseur de services peut modéliser diverses configurations :

**Exemple 1 :** Une ligne POTS unique dans les modèles de connexion centrée sur l’ordinateur ou sur le téléphone. Le modèle le plus simple est un appareil à ligne unique avec un canal.

**Exemple 2 :** Une seule ligne BRI-RNIS dans les modèles de connexion centrée sur l’ordinateur ou sur le téléphone. Le fournisseur de services a un certain nombre d’options quant à la façon dont il peut le modéliser, par exemple :

-   Modélisez la ligne BRI comme un appareil à ligne unique avec un pool de deux canaux B permettant de combiner les deux canaux pour établir des appels de 128 Kbits/s.
-   Modéliser chaque canal B en tant que périphérique de ligne distinct et interdire la combinaison des deux canaux en un seul canal 128 kbps.
-   Modélisez la connexion BRI en tant que deux appareils de ligne distincts, chacun d’entre eux étant constitué de deux canaux d’un pool partagé de deux canaux B.
-   Modèle en tant qu’appareils à trois lignes, un pour chaque canal B et un pour la combinaison. Clairement dans les deux derniers modèles, les ressources peuvent être affectées à des appareils de ligne différents à des moments différents.

**Exemple 3 :** Dans les systèmes client/serveur, un pool de ports téléphoniques reliés à un serveur peut être partagé entre plusieurs ordinateurs clients sur un réseau local. Le pool peut être administré pour affecter un nombre maximal de périphériques en ligne (quota) à chaque station de travail cliente. Il n’est pas rare que la somme de tous les quotas dépasse le nombre total de lignes. En outre, un client donné avec un quota égal à 2 peut être satisfait en utilisant les ports 1 et 2 à la fois et les ports 7 et 11 ultérieurement. Le fournisseur de services pour le pool peut modéliser cette organisation en donnant à chaque station de travail cliente l’accès à deux appareils en ligne.

Supposons que la configuration des fournisseurs de services pour un ordinateur donné soit telle que ce fournisseur de services particulier obtient un **DeviceIDBase** de 3. Cela implique que les identificateurs de périphérique (fixes) associés à ce client sont 3 et 4. Si l’application appelle ultérieurement la fonction TAPI 2 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) pour l’appareil 3 et à nouveau pour l’appareil 4, elle doit être en mesure de supposer que les fonctionnalités de l’appareil pour chacun de ces périphériques sont constantes, car il s’agit du modèle d’appareil. Tant que la configuration du fournisseur de services de l’ordinateur donné reste constante, les identificateurs d’appareil qui apparaissent au niveau TSPI restent constants, même si le serveur modifie les allocations de port. Pour les périphériques serveur regroupés comme décrit dans l’exemple 3, cela contient uniquement les périphériques de ligne qui possèdent des fonctionnalités d’appareil identiques. Bien entendu, si la configuration du fournisseur de service de l’ordinateur donné est modifiée, de telle sorte que ce fournisseur de services obtient un **DeviceIDBase** différent, les identificateurs d’appareil changent en conséquence.

**Exemple 4 :** Lien basculer vers l’hôte :

-   Pour fournir une téléphonie personnelle à chaque poste de travail, le fournisseur de services peut modéliser la ligne PBX couplée avec l’ordinateur en tant qu’appareil à ligne unique avec un canal. Chaque ordinateur client disposerait d’un périphérique de ligne disponible.
-   Chaque station tierce peut être modélisée en tant qu’appareil de ligne distincte. Cela permet à l’application de contrôler les appels sur d’autres stations. Cette solution exige que l’application ouvre chaque ligne qu’elle souhaite manipuler ou surveiller, ce qui peut être parfait si seul un petit nombre de lignes est intéressant, mais peut générer un grand nombre de surcharges si un grand nombre de lignes est impliqué.
-   L’ensemble de toutes les stations tierces peut être modélisé comme un appareil à ligne unique avec une adresse (numéro de téléphone) qui lui est affectée par station. Un seul appareil doit être ouvert, ce qui permet de surveiller et de contrôler toutes les adresses sur la ligne (toutes les stations). Pour établir un appel sur l’une de ces stations, l’application doit uniquement spécifier l’adresse de la station pour l’opération qui effectue l’appel. Aucune opération d’ouverture supplémentaire n’est requise. Cette modélisation implique que toutes les stations possèdent les mêmes fonctionnalités de périphérique en ligne, bien que leurs fonctionnalités d’adresse puissent être différentes.

> [!Note]  
> Tous ces exemples sont simplement différentes façons dont un fournisseur de services peut choisir d’implémenter le mappage du comportement du périphérique de ligne sur une réalisation physique.

 

 

 
