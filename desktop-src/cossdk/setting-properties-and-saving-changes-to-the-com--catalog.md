---
description: Chaque élément d’une collection expose des propriétés.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Modification des propriétés dans le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748276"
---
# <a name="editing-properties-in-the-com-catalog"></a>Modification des propriétés dans le catalogue COM+

Chaque élément d’une collection expose des propriétés. Ces propriétés permettent de conserver les données de configuration de l’élément représenté par l’élément. Dans l’outil d’administration Services de composants, ces propriétés s’affichent sur une page de propriétés à laquelle vous accédez en cliquant avec le bouton droit sur un élément dans un dossier.

Étant donné que les éléments d’une collection donnée représentent le même type d’élément, ces éléments exposent un ensemble de propriétés qui est cohérent dans la collection. Par exemple, la collection d' [**applications**](applications.md) expose une propriété Name, une propriété AppID, et ainsi de suite. Cela est analogue à la façon dont chaque application de l’outil d’administration Services de composants dispose d’une page de propriétés régulièrement structurée disponible. Pour obtenir la liste des propriétés disponibles pour la collection d' **applications** , consultez **applications**. Pour obtenir la liste des propriétés disponibles pour la collection de [**composants**](components.md) , consultez **composants**.

Pour obtenir la liste complète des propriétés exposées par les éléments de chaque collection, consultez [regroupements d’administration com+](com--administration-collections.md).

Vous représentez un élément dans une collection à l’aide d’un objet créé à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Cet objet vous permet de définir et d’accéder à l’une des propriétés exposées par l’élément. Lors de la définition des propriétés, il est également possible que vous soyez en mesure d’utiliser un autre enregistreur dans le catalogue COM+. Pour plus d’informations, consultez [obtention et définition des propriétés](getting-and-setting-properties.md).

Une fois que vous avez défini les propriétés, aucune modification n’est réellement validée tant que vous n’avez pas enregistré explicitement les modifications. Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).

Lorsque vous enregistrez des modifications, le catalogue COM+ met en œuvre une logique de configuration pour s’assurer que vous ne définissez pas de configurations incompatibles. Elle modifie également certaines propriétés lorsque vous modifiez explicitement certaines autres propriétés. Pour plus d’informations, consultez [interdépendances entre les propriétés](interdependencies-between-properties.md).

En outre, COM+ dispose d’une fonctionnalité qui vous permet d’effectuer des requêtes dynamiques pour voir quelles propriétés sont disponibles pour les éléments d’une collection donnée. Pour plus d’informations, consultez [interrogation des propriétés disponibles](querying-for-available-properties.md).

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

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



