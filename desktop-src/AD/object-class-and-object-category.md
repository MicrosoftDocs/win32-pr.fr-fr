---
title: Classe d’objet et catégorie d’objet
description: Chaque instance d’une classe d’objet a une propriété objectClass à valeurs multiples qui identifie la classe dont l’objet est une instance, ainsi que toutes les superclasses structurelles ou abstraites à partir desquelles cette classe est dérivée.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35e7f461caa27e8668cfc47cd94852bf53b291658b828ea017e3dc00a19d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185696"
---
# <a name="object-class-and-object-category"></a>Classe d’objet et catégorie d’objet

Chaque instance d’une classe d’objet a une propriété [**objectClass**](/windows/desktop/ADSchema/a-objectclass) à valeurs multiples qui identifie la classe dont l’objet est une instance, ainsi que toutes les superclasses structurelles ou abstraites à partir desquelles cette classe est dérivée. Ainsi, la propriété **objectClass** d’un objet utilisateur identifie les classes [**Top**](/windows/desktop/ADSchema/c-top), [**Person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)et [**User**](/windows/desktop/ADSchema/c-user) . La propriété **objectClass** n’inclut pas les classes auxiliaires dans la liste. Le système définit la valeur **objectClass** lorsque l’instance d’objet est créée et ne peut pas être modifiée.

Chaque instance d’une classe d’objet a également une propriété [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , qui est une propriété à valeur unique qui contient le nom unique de la classe dont l’objet est une instance ou l’une de ses superclasses. Lorsqu’un objet est créé, le système définit sa propriété **objectCategory** sur la valeur spécifiée par la propriété [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de sa classe Object. La propriété **objectCategory** d’un objet ne peut pas être modifiée.

Pour plus d’informations et pour obtenir un exemple de code qui récupère la propriété [**objectClass**](/windows/desktop/ADSchema/a-objectclass) d’un objet, consultez [extraction de l’attribut objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> avant Windows Server 2008, l’attribut [**objectClass**](/windows/desktop/ADSchema/a-objectclass) n’est pas indexé. Cela est dû au fait qu’elle a plusieurs valeurs et qu’elle est hautement non unique ; autrement dit, chaque instance de l’attribut **objectClass** comprend la classe [**Top**](/windows/desktop/ADSchema/c-top) . Cela signifie qu’un index serait très volumineux et inefficace. Pour localiser des objets d’une classe donnée, utilisez l’attribut [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , qui est à valeur unique et indexée. Pour plus d’informations sur l’utilisation de ces propriétés dans les filtres de recherche, consultez [choix des éléments à rechercher](deciding-what-to-find.md).

 

Pour la plupart des classes, [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) est le nom unique de l’objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) de la classe. Par exemple, le **defaultObjectCategory** pour la classe [**ORGANIZATIONALUNIT**](/windows/desktop/ADSchema/c-organizationalunit) est « CN = Organization-Unit, CN = Schema, cn = Configuration, <DC = forestroot> ». Toutefois, certaines classes font référence à une autre classe en tant que **defaultObjectCategory**. Cela permet à une requête de rechercher facilement des groupes d’objets connexes, même s’ils sont de classes différentes. Par exemple, les classes [**User**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)et [**contact**](/windows/desktop/ADSchema/c-contact) identifient toutes la classe **Person** dans leurs propriétés **defaultObjectCategory** . Cela permet aux filtres de recherche comme (objectCategory = person) de localiser les instances de toutes ces classes avec une seule requête. Les requêtes pour les personnes sont très courantes. il s’agit donc d’une simple optimisation.

Si vous créez une sous-classe à partir d’une classe structurelle, la meilleure pratique consiste à définir la valeur [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de la nouvelle classe sur le même nom unique de la superclasse. Cela permet à l’interface utilisateur standard de « rechercher » la sous-classe.

 

 