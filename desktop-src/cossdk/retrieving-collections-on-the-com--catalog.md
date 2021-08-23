---
description: Récupération des regroupements sur le catalogue COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Récupération des regroupements sur le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf70f6fe6a7ab25ebed0338e56db1abfc0b869134725d52108b83473b9182d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812583"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Récupération des regroupements sur le catalogue COM+

Les données du catalogue COM+ sont stockées dans une hiérarchie de regroupements. Dans l’outil d’administration Services de composants, un grand nombre de ces regroupements s’affichent sous la forme de dossiers dans l’arborescence de la console. Les regroupements qui n’apparaissent pas en tant que dossiers sont accessibles uniquement par programme. Les collections servent de conteneurs pour les éléments. Les éléments d’une collection donnée sont tous d’un type cohérent ; autrement dit, elles représentent toutes le même type d’élément, et il peut y avoir un nombre arbitraire d’éléments dans une collection. Par exemple, la collection d' [**applications**](applications.md) contient un élément pour chaque application com+ installée sur l’ordinateur. Ce regroupement s’affiche dans l’outil d’administration en tant que dossier **applications com+** .

Les collections se produisent dans une structure hiérarchique, car les éléments qu’elles contiennent suivent un ordre d’inclusion inné. Par exemple, étant donné que les composants sont installés dans une application COM+, la collection de [**composants**](components.md) est incluse logiquement sous la collection d' [**applications**](applications.md) . Plus particulièrement, pour conserver les composants installés dans cette application particulière, il existe une collection de **composants** distincts pour chaque élément de la collection d' **applications** .

Vous devez obtenir une collection sur le catalogue chaque fois que vous souhaitez récupérer un élément et définir ses propriétés. Dans le cas général, vous devez effectuer un pas à pas détaillé dans plusieurs collections pour accéder à l’élément de votre choix. Pour connaître la procédure à suivre, consultez [navigation dans la hiérarchie des collections com+](navigating-the-com--collection-hierarchy.md).

Une fois que vous avez récupéré une collection et que vous pouvez travailler directement avec les éléments qu’elle contient, vous devez remplir la collection, qui extrait les données du contenu de la collection à partir du catalogue COM+. Pour plus d’informations, consultez [remplissage des collections com+](populating-com--collections.md).

En outre, vous pouvez utiliser une fonctionnalité qui vous permet d’effectuer des requêtes dynamiques pour voir les regroupements connexes disponibles à partir d’un regroupement donné que vous êtes en possession. Pour plus d’informations, consultez [interrogation des collections associées disponibles](querying-for-available-related-collections.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations d’administration COM+ dans les transactions](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestion des erreurs d’administration COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemple d’introduction utilisant le catalogue d’administration COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



