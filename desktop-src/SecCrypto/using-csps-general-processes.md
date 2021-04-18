---
description: Lorsque vous utilisez des fournisseurs de services de chiffrement, gardez à l’esprit les conventions suivantes.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Utilisation des fournisseurs de services de chiffrement : processus généraux'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516063"
---
# <a name="using-csps-general-processes"></a>Utilisation des fournisseurs de services de chiffrement : processus généraux

Lorsque vous utilisez des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) , gardez à l’esprit les conventions suivantes.

## <a name="private-key-caching"></a>Mise en cache des clés privées

Un CSP peut mettre en cache certaines [*clés privées*](../secgloss/p-gly.md). Il est possible de contrôler cette mise en cache de clé privée sur une base globale, mais pas propre à l’application. La mise en cache des modifications s’effectue en modifiant certains paramètres du Registre. Pour plus d’informations, consultez [**constantes de mise en cache de clés privées**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Exemples de conventions de code

Pour fournir un code plus concis et plus lisible, certains principes de bonnes pratiques de programmation ne sont pas toujours suivis dans les exemples. En particulier :

-   Seules les réponses d’erreur limitées sont affichées. Les programmes correctement écrits et complets vérifient les codes d’erreur renvoyés et effectuent les actions appropriées lorsqu’une erreur est rencontrée.
-   Seule la gestion de la mémoire et des ressources est limitée. Les programmes bien écrits et complets détruisent l’ensemble des clés et des [*hachages*](../secgloss/h-gly.md), libèrent toute la mémoire allouée, ferment tous les fichiers et libèrent tous les descripteurs. Ces exemples fournissent uniquement des démonstrations limitées de l’utilisation des fonctions qui effectuent ces tâches. Ces exemples n’effectuent aucune tâche de gestion de la mémoire ou des ressources en cas d’arrêt du programme en raison d’erreurs.

Les rubriques suivantes présentent des informations générales sur les exemples de procédures, ainsi que des exemples de code.

-   [Récupération de données de longueur inconnue](retrieving-data-of-unknown-length.md)
-   [Énumération des protocoles pris en charge](enumerating-supported-protocols.md)

 

 
