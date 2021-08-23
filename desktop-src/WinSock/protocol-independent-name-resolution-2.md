---
description: la résolution de noms indépendante du protocole et les sockets de Windows (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Résolution de noms Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f214619d4bf54f3ac39d24008f07aa12715fc75ac1bf6ea74280ed80d31d7bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993599"
---
# <a name="protocol-independent-name-resolution"></a>Résolution de noms Protocol-Independent

Lors du développement d’une application client/serveur indépendante du protocole, deux exigences de base existent en ce qui concerne la résolution de noms et l’inscription :

-   La capacité du serveur de l’application (service) à inscrire son existence dans (ou à être accessible) à un ou plusieurs espaces de noms.
-   Capacité de l’application cliente à rechercher le service dans un espace de noms et à obtenir le protocole de transport et les informations d’adressage requis.

Pour ceux qui sont habitués au développement d’applications basées sur TCP/IP, cela peut sembler un peu plus grand que la recherche d’une adresse d’hôte, puis l’utilisation d’un numéro de port convenu. Toutefois, d’autres schémas de mise en réseau autorisent l’emplacement du service, le protocole utilisé pour le service et d’autres attributs à découvrir au moment de l’exécution. pour prendre en charge la grande diversité des fonctionnalités disponibles dans les services de noms existants, l’interface Windows sockets 2 adopte le modèle décrit dans les rubriques de cette section.

Cette section décrit les fonctionnalités de résolution de noms indépendantes des protocoles disponibles pour les développeurs Winsock. La liste suivante décrit les rubriques de cette section :

-   [Modèle de résolution de noms](name-resolution-model-2.md)
-   [Résumé des fonctions de résolution de noms](summary-of-name-resolution-functions-2.md)
-   [Structures de données de résolution de noms](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



