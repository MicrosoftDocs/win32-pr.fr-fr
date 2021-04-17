---
title: Inclusion d’attributs dans le catalogue global
description: Le catalogue global d’une forêt comprend un réplica partiel de chaque objet de la forêt.
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- Attributs inclus dans l’AD du catalogue global
- Attributs AD, inclus dans le catalogue global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462938"
---
# <a name="including-attributes-in-the-global-catalog"></a>Inclusion d’attributs dans le catalogue global

Le catalogue global d’une forêt comprend un réplica partiel de chaque objet de la forêt. Pour chaque objet, le catalogue global comprend uniquement un sous-ensemble des attributs de chaque objet. L’attribut [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) d’un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) a la valeur **true** si l’attribut est répliqué dans le catalogue global.

Les attributs ayant les caractéristiques suivantes sont appropriés pour le stockage dans le catalogue global :

-   L’attribut est globalement intéressant, soit parce que l’attribut est requis pour localiser des objets qui peuvent apparaître n’importe où dans la forêt, soit parce que l’accès en lecture à l’attribut est utile, même lorsque l’objet complet n’est pas accessible. Un exemple du premier type est l’attribut [**location**](/windows/desktop/ADSchema/a-location) , qui peut être utilisé pour rechercher un objet [**PrintQueue**](/windows/desktop/ADSchema/c-printqueue) . Un exemple du second type est [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber), car vous pouvez appeler quelqu’un même si vous ne pouvez pas accéder à un réplica complet de son objet [**utilisateur**](/windows/desktop/ADSchema/c-user) .
-   La volatilité de l’attribut est très faible. Cela est important, car si une classe d’attributs est incluse dans le catalogue global, les modifications apportées à chaque valeur de cette classe d’attributs dans la forêt d’entreprise sont répliquées sur tous les serveurs de catalogue global de l’entreprise.
-   La taille de la valeur de l’attribut est petite. « Petite » est très subjective : lorsque vous placez un attribut dans le catalogue global, prenez en compte l’impact de la réplication de l’attribut sur tous les serveurs de catalogue global de l’entreprise. Plus l’attribut est petit, plus l’impact est faible. Étant donné que la réplication se produit uniquement lorsque l’attribut change, l’impact de la réplication est également plus petit que la volatilité diminue, donc un attribut volumineux avec une volatilité très faible peut avoir un impact global inférieur à celui d’un petit attribut avec une volatilité élevée.

Lorsque vous décidez de placer ou non un attribut dans le catalogue global, n’oubliez pas que vous effectuez une réplication accrue et augmentez le stockage sur disque sur les serveurs de catalogue global pour des performances de requête potentiellement plus rapides. En règle générale, vous utilisez le catalogue global pour rechercher un objet d’intérêt afin de pouvoir lire les attributs sélectionnés de l’objet. Si les attributs qui vous intéressent sont répliqués dans le catalogue global, vous pouvez les lire directement à partir du catalogue global. Sinon, pour lire les attributs qui ne sont pas répliqués dans le catalogue global, vous devez effectuer des étapes supplémentaires pour les récupérer. Dans ce cas, après avoir effectué une recherche dans le catalogue global pour trouver l’objet qui vous intéresse, vous devez lire le nom unique de l’objet à partir du catalogue global, utiliser le DN pour effectuer une liaison directe avec un réplica complet de l’objet, qui peut se trouver sur un autre serveur et enfin lire les attributs non globaux du catalogue à partir du réplica complet de l’objet.

Les attributs fréquemment interrogés et référencés, tels que le nom de l’employé et le numéro de téléphone, sont corrects à inclure dans le catalogue global. Un attribut rarement référencé, tel que « driverVersion » pour les imprimantes, est mieux conservé dans le catalogue global.

 

 