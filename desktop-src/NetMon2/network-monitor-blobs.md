---
description: Le Moniteur réseau objet BLOB (Binary Large Object) est une structure de données générique qui contient des informations de configuration et d’emplacement de cartes d’interface réseau (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Objets BLOB Moniteur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d15ce2a8f85860720c6f38b0d6c019a33e57df0a1b589ba23455db0319d0436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799549"
---
# <a name="network-monitor-blobs"></a>Objets BLOB Moniteur réseau

Le Moniteur réseau objet BLOB (Binary Large Object) est une structure de données générique qui contient des informations de configuration et d’emplacement de cartes d’interface réseau (NIC). Utilisez des objets BLOB pour représenter des cartes réseau et filtrer les entrées d’une liste de cartes réseau. Les objets BLOB peuvent également contenir des données spécifiques à l’application sans affecter les autres données qu’ils contiennent. L’implémentation d’objet BLOB est opaque à tous les niveaux qui doivent accéder aux objets BLOB avec les API d’objets BLOB.

## <a name="blob-structure"></a>Structure d’objet BLOB

Un objet BLOB peut être considéré comme une arborescence hiérarchique utilisée pour désigner des chaînes. Cette arborescence comporte trois couches : propriétaire, catégorie et étiquette. Owner est une chaîne qui indique, en général, qui lit une entrée. La catégorie est également une chaîne, qui désigne un regroupement fonctionnel général de balises sous le propriétaire. La balise est le nom réel de l’entrée.

Les caractéristiques structurelles des objets BLOB sont les suivantes :

-   Les applications auxiliaires d’objets BLOB dans un processus sont protégées les unes des autres par un mutex intégré à chaque objet BLOB.
-   Chaque objet BLOB a un numéro de version interne afin que les applications d’assistance puissent gérer à la fois les formulaires BLOB présents et futurs. Des conflits de version peuvent se produire si vous envoyez un objet BLOB à un autre ordinateur par le biais d’un appel de procédure distante.
-   L’objet BLOB lui-même est un pointeur vers une valeur void. Sachez que les applications doivent allouer des objets BLOB avec le modificateur **const** pour éviter de modifier le contenu.
-   Chacun des indicateurs, ainsi que leurs valeurs, sont des chaînes. N’oubliez pas que les chaînes retournées par les fonctions **GetString** sont en fait des pointeurs dans l’objet BLOB et qu’elles ne doivent pas être modifiées. Pour cette raison, ces chaînes doivent être spécifiées en tant que **const char** _ \_ PX * pour empêcher les applications de les modifier accidentellement.

En général, tous les paramètres avec le désignateur **const** encouragent l’appelant à s’abstenir de modifier les valeurs plutôt que d’interdire la modification des fonctions d’assistance. En fait, les fonctions d’assistance modifient généralement ces valeurs.

 

 



