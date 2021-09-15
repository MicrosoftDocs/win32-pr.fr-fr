---
description: Obtention et définition des propriétés
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtention et définition des propriétés (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519324"
---
# <a name="getting-and-setting-properties-component-services"></a>Obtention et définition des propriétés (services de composants)

Avant de pouvoir lire ou écrire des propriétés particulières exposées par un élément dans une collection, vous devez effectuer les étapes suivantes :

1.  Récupérez la collection.
2.  Remplissez la collection pour y lire les données à partir du catalogue COM+.
3.  Récupérez l’élément spécifique dans la collection, en le représentant avec un objet de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Pour obtenir un exemple qui illustre ces étapes, consultez [navigation dans la hiérarchie des collections com+](navigating-the-com--collection-hierarchy.md).

Étant donné que les propriétés particulières exposées peuvent varier en fonction de ce que représente l’élément ; autrement dit, un élément représentant un composant a des propriétés différentes de celles qui représentent une application COM+. Définissez l’une de ces propriétés à l’aide d’une propriété générique unique, la propriété Value, sur [**COMAdminCatalogObject**](comadmincatalogobject.md).

La propriété valeur vous permet d’obtenir ou de définir n’importe quelle propriété nommée spécifique exposée par un élément, en retournant une valeur pour une propriété nommée lors de l’obtention et de la prise d’un nom et d’une valeur lors de la définition de.

Aucune modification n’est réellement enregistrée dans le catalogue COM+ tant que vous n’avez pas enregistré explicitement les modifications à l’aide de la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Les modifications en attente pour toutes les propriétés de tous les éléments d’une collection donnée sont enregistrées en même temps. Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).

Toutes les modifications que vous apportez ne seront pas acceptées. Le catalogue COM+ applique une certaine logique de cohérence pour s’assurer que vous configurez les éléments de manière raisonnable. En outre, lorsque vous modifiez certaines propriétés, d’autres peuvent changer automatiquement à l’aide de la même logique de cohérence. Ces effets s’affichent lorsque vous tentez d’enregistrer des modifications.

> [!Note]  
> Vous pouvez être en conflit avec un autre enregistreur dans le catalogue COM+. Entre les appels à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour une collection donnée, vous ne disposez d’aucun verrou sur l’une de ces données dans le catalogue. Plusieurs parties peuvent configurer simultanément des éléments dans une collection donnée et peuvent être en concurrence lorsqu’ils enregistrent des modifications. Cela signifie qu’un autre utilisateur peut modifier les paramètres d’un objet avant ou après l’exécution, soit en exécutant un programme à l’aide des objets comadmin ou à l’aide de l’outil d’administration Services de composants, localement ou à distance. La règle générale avec l’écriture d’objets sur le catalogue est que toutes les propriétés d’un objet sont écrites en même temps. Autrement dit, le dernier enregistreur gagne : l’objet est enregistré de manière précise dans le catalogue, comme le dernier enregistreur l’a configuré.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interdépendances entre les propriétés](interdependencies-between-properties.md)
</dt> <dt>

[Interrogation des propriétés disponibles](querying-for-available-properties.md)
</dt> <dt>

[Enregistrement ou rejet des modifications](saving-or-discarding-changes.md)
</dt> </dl>

 

 



