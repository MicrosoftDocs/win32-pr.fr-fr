---
description: Résolution de noms indépendante du protocole et Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Résolution de noms Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318366"
---
# <a name="protocol-independent-name-resolution"></a>Résolution de noms Protocol-Independent

Lors du développement d’une application client/serveur indépendante du protocole, deux exigences de base existent en ce qui concerne la résolution de noms et l’inscription :

-   La capacité du serveur de l’application (service) à inscrire son existence dans (ou à être accessible) à un ou plusieurs espaces de noms.
-   Capacité de l’application cliente à rechercher le service dans un espace de noms et à obtenir le protocole de transport et les informations d’adressage requis.

Pour ceux qui sont habitués au développement d’applications basées sur TCP/IP, cela peut sembler un peu plus grand que la recherche d’une adresse d’hôte, puis l’utilisation d’un numéro de port convenu. Toutefois, d’autres schémas de mise en réseau autorisent l’emplacement du service, le protocole utilisé pour le service et d’autres attributs à découvrir au moment de l’exécution. Pour prendre en charge la grande diversité des fonctionnalités disponibles dans les services de noms existants, l’interface Windows Sockets 2 adopte le modèle décrit dans les rubriques de cette section.

Cette section décrit les fonctionnalités de résolution de noms indépendantes des protocoles disponibles pour les développeurs Winsock. La liste suivante décrit les rubriques de cette section :

-   [Modèle de résolution de noms](name-resolution-model-2.md)
-   [Résumé des fonctions de résolution de noms](summary-of-name-resolution-functions-2.md)
-   [Structures de données de résolution de noms](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



