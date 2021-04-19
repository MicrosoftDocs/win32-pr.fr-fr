---
description: Quand vous configurez un composant à regrouper, COM+ gère les instances de celui-ci dans un pool, prêt à être activé pour n’importe quel client demandant le composant. Toute demande de création d’objet sera gérée par le gestionnaire de pool.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Fonctionnement du regroupement d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513319"
---
# <a name="how-object-pooling-works"></a>Fonctionnement du regroupement d’objets

Quand vous configurez un composant à regrouper, COM+ gère les instances de celui-ci dans un pool, prêt à être activé pour n’importe quel client demandant le composant. Toute demande de création d’objet sera gérée par le gestionnaire de pool.

Les pools sont configurés et gérés pour chaque composant. Un pool se compose d’objets homogènes qui partagent le même CLSID. La seule exception concerne les objets transactionnels, pour lesquels les sous-pools sont conservés et qui contiennent des objets qui ont une affinité de transaction alors qu’une transaction est en attente.

Lorsque l’application démarre, le pool est rempli au niveau minimal que vous avez spécifié de manière administrative, à condition que la création de l’objet aboutisse. À mesure que les demandes des clients du composant arrivent, elles sont satisfaites sur la base du premier arrivé, premier servi. Si aucun objet regroupé n’est disponible et que le pool n’est pas encore à son niveau maximal spécifié, un nouvel objet est créé et activé pour le client.

Lorsque le pool atteint son niveau maximal, les demandes des clients sont mises en file d’attente et reçoivent le premier objet disponible du pool. Le nombre d’objets, y compris activés et désactivés, ne dépassera jamais la valeur maximale du pool. Les demandes de création d’objet expirent après une période spécifiée administrativement, ce qui vous permet de contrôler la durée pendant laquelle les clients attendent la création de l’objet. En cas de dépassement du délai d’attente, le client renvoie l’erreur E \_ Timeout de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Chaque fois que cela est possible, COM+ tente de réutiliser un objet une fois qu’il a été libéré par un client, jusqu’à ce que le pool atteigne son niveau maximal. L’objet est chargé de surveiller son état afin de déterminer s’il peut être réutilisé et doit retourner une valeur appropriée pour [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Lorsqu’un objet regroupé est créé, il est agrégé dans un objet plus grand qui gère la durée de vie de l’objet. L’objet externe appelle les méthodes sur [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) aux moments opportuns dans le cycle de vie de l’objet, comme suit :

-   La méthode [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) est appelée chaque fois que l’objet est retourné à un client, activé dans un contexte spécifique.
-   La méthode [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) est appelée chaque fois qu’un objet est libéré par le client ou, dans le cas d’un objet activé juste-à-temps, lorsqu’il est désactivé.
-   La méthode [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) est appelée chaque fois qu’un objet doit être retourné au pool général. Si l’objet détecte qu’une ressource réutilisable est dans un état incorrect, il doit retourner la **valeur false** pour cette méthode et le gestionnaire de pool ignore l’objet.

Un objet n’a pas nécessairement besoin d’implémenter [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Si ce n’est pas le cas, les instances sont toujours réutilisées jusqu’à ce que le niveau maximal du pool soit atteint.

Pour plus d’informations sur la façon de configurer les composants à regrouper, consultez [configuration d’un composant à regrouper](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chaînes du constructeur d’objet COM+](com--object-constructor-strings.md)
</dt> <dt>

[Contrôle de la durée de vie et de l’état des objets](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Amélioration des performances avec la mise en pool d’objets](improving-performance-with-object-pooling.md)
</dt> <dt>

[Regroupement d’objets transactionnels](pooling-transactional-objects.md)
</dt> <dt>

[Conditions requises pour les objets regroupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
