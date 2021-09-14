---
description: Interdépendances entre les propriétés
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdépendances entre les propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118490"
---
# <a name="interdependencies-between-properties"></a>Interdépendances entre les propriétés

Lorsque vous définissez des propriétés, le catalogue COM+ met en œuvre une logique de cohérence pour vous assurer que vous configurez les éléments de manière raisonnable. Cette logique peut être implémentée de deux manières, comme suit :

-   **Dépendances.** Vous risquez de ne pas pouvoir apporter des modifications, car une autre propriété dépend d’un paramètre particulier pour une propriété que vous essayez de définir. Par exemple, si un composant est défini avec les transactions d’attribut requises et si vous tentez ensuite de modifier le paramètre de synchronisation sur aucun, une erreur est générée lorsque vous tentez d’appeler [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , car les transactions dépendent de la synchronisation.
-   **Effets secondaires.** Certaines propriétés peuvent être modifiées pour vous si vous ne les définissez pas explicitement. Par exemple, si vous définissez un composant avec l’attribut transactions requis, la synchronisation est définie sur obligatoire. C’est vraiment le côté inverse des dépendances : une propriété est prioritaire sur une autre, et sa dépendance est exprimée par la première définition de la propriété secondaire, puis par le blocage des modifications.

Dans la liste des propriétés exposées par les éléments d’une collection, tous les éléments répertoriés dans les [collections d’administration com+](com--administration-collections.md), les dépendances et les effets secondaires sont indiqués pour chaque propriété. Quand vous configurez des applications et des composants COM+, vous devez connaître les contraintes imposées aux configurations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention et définition des propriétés](getting-and-setting-properties.md)
</dt> <dt>

[Interrogation des propriétés disponibles](querying-for-available-properties.md)
</dt> <dt>

[Enregistrement ou rejet des modifications](saving-or-discarding-changes.md)
</dt> </dl>

 

 



