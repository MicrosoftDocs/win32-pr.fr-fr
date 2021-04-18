---
description: Les concepteurs de fournisseurs de services doivent tenter de réduire la durée d’exécution des opérations synchrones.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Requêtes synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533690"
---
# <a name="synchronous-requests"></a>Requêtes synchrones

Les concepteurs de fournisseurs de services doivent tenter de réduire la durée d’exécution des opérations synchrones. Par exemple, il existe une opération « Open » appelée au moment de l’initialisation, qui prépare le fournisseur de services et l’interface TAPI pour les opérations suivantes sur un appareil. Un fournisseur de services dont l’implémentation est fractionnée entre l’ordinateur client et un serveur dédié peut avoir une certitude raisonnable qu’il peut communiquer avec son serveur distant. Son implémentation de « Open » peut simplement allouer et initialiser des structures de données pour représenter l’appareil et le retour, en différant la communication de bout en bout jusqu’à ce qu’une opération réelle soit demandée.

Toute implémentation « optimiste » d’une opération synchrone peut par la suite rencontrer des problèmes de ressources ou de communication distante. En général, même une approche « conservatrice » ne peut pas entièrement empêcher ces problèmes ; les concepteurs de fournisseurs de services doivent choisir le meilleur compromis entre fiabilité et performances. Une défaillance de ce type doit être traitée correctement dans la mesure du possible. Du point de vue des appareils TSPI, ils doivent rester valides à des fins de « comptabilité » même s’ils renvoient l’état d’échec pour toute opération demandée.

L’implémentation d’une approche optimiste pour les requêtes synchrones ne doit pas être effectuée au détriment de la sémantique correcte pour l’opération. Si vous revenez à l’exemple « Open », si l’ouverture d’un appareil doit rivaliser pour et réserver une ressource rare et non partageable telle que les ports de communication, il devrait y parvenir, même si cela prend du temps.

**TAPI 2. x :** Une opération qui se termine de façon synchrone effectue tout son traitement dans l’appel de fonction effectué par l’application. La fonction retourne des valeurs différentes en fonction de la réussite ou de l’échec :

-   **Réussite synchrone.** Si la requête ou le service correspondant à la fonction a été exécuté avec succès, la fonction retourne zéro, ce qui indique une réussite. Toutes les valeurs écrites à la suite de l’appel de fonction sont fiables et peuvent être utilisées immédiatement.
-   **Échec synchrone.** Si la fonction détecte une erreur et que la demande n’est pas exécutée, un numéro d’erreur négatif est retourné pour identifier l’erreur.

 

 



