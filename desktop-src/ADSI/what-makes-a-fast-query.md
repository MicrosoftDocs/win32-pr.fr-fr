---
title: Qu’est-ce qui fait une requête rapide ?
description: Cette rubrique répertorie les méthodes de programmation par défaut à utiliser lors de l’interrogation d’un répertoire.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Ce qui rend une requête ADSI rapide
- interroge ADSI, ce qui effectue une requête rapide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842730"
---
# <a name="what-makes-a-fast-query"></a>Qu’est-ce qui fait une requête rapide ?

Tenez compte des concepts d’amélioration des performances suivants lors de l’exécution d’une requête :

-   Si possible, filtrez uniquement sur les attributs indexés. Utilisez les attributs d’index dont vous vous attendez à générer le plus petit nombre d’accès. Pour plus d’informations et pour obtenir une liste complète des attributs indexés pour Windows, consultez [Active Directory schéma](/windows/desktop/ADSchema/active-directory-schema).
-   Recherchez **objectCategory** au lieu de **objectClass** , car **objectClass** n’est pas une propriété indexée.
-   Tenez compte des références. Envisagez de rechercher le catalogue global si vos attributs sont répertoriés en tant que GC répliqué.
-   Évitez de rechercher du texte au milieu et à la fin d’une chaîne. Par exemple, « CN = \* Hill \* » ou « CN = \* larouse ».
-   Supposons qu’une recherche de sous-arborescence retourne un jeu de résultats volumineux. Utilisez la pagination lorsque vous effectuez des recherches sous-arborescences. Le serveur sera ensuite en mesure de diffuser un grand jeu de résultats dans des segments pour réduire les ressources de mémoire côté serveur. Cela aplanit efficacement l’utilisation du réseau et réduit le besoin d’envoyer des blocs de données extrêmement volumineux sur le réseau.
-   Exposez correctement vos recherches afin de ne pas récupérer plus que nécessaire.
-   Effectuez une recherche complexe sur plusieurs attributs, car elle est moins gourmande en performances que l’exécution de plusieurs recherches. L’une des recherches d’un objet qui lit deux attributs est plus efficace que deux pour le même objet, chacun retournant un attribut.
-   Pour la lecture d’un attribut avec un grand nombre de valeurs, utilisez des limites de plage pour réduire la taille de la recherche afin de pouvoir lire quelques milliers de membres à la fois. Pour plus d’informations sur la spécification des limites de plage d’attributs, consultez [récupération de plage d’attributs](attribute-range-retrieval.md).
-   La liaison à un objet contient le handle de liaison pour le reste de votre session. Ne pas lier et annuler la liaison pour chaque appel. Si vous utilisez ADO ou OLE DB, ne créez pas de nombreux objets de connexion.
-   Lisez le rootDSE une fois et rappelez son contenu pour le reste de votre session.

 

 