---
description: Les objets regroupables doivent répondre à certaines exigences pour permettre l’utilisation d’une instance d’objet unique par plusieurs clients.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Conditions requises pour les objets regroupables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922924"
---
# <a name="requirements-for-poolable-objects"></a>Conditions requises pour les objets regroupables

Les objets regroupables doivent répondre à certaines exigences pour permettre l’utilisation d’une instance d’objet unique par plusieurs clients.

## <a name="stateless"></a>Sans état

Pour assurer la sécurité, la cohérence et l’isolation, les objets regroupables ne doivent pas conserver un état spécifique au client du client au client. Vous pouvez gérer n’importe quel état par client à l’aide de [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), en effectuant une initialisation spécifique au contexte avec [**IObjectControl :: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) et en nettoyant tout état du client avec [**IObjectControl ::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Pour plus d’informations, consultez contrôle de la [durée de vie et](controlling-object-lifetime-and-state.md)de l’état d’un objet.

## <a name="no-thread-affinity"></a>Aucune affinité de thread

Les objets regroupables ne peuvent pas être liés à un thread particulier ; dans le cas contraire, les performances peuvent être désastreuses. Pour cette raison, les objets regroupables ne peuvent pas être marqués pour s’exécuter dans le modèle cloisonné ; ils doivent s’exécuter dans le cloisonnement multithread ou le cloisonnement neutre. En outre, les objets regroupables ne doivent pas utiliser le stockage local des threads et ne doivent pas agréger le marshaleur libre de threads. Pour plus d’informations sur les threads dans COM+, consultez [modèles de thread com+](com--threading-models.md).

> [!Note]  
> les environnements de développement Microsoft Visual Basic 6,0 et versions antérieures peuvent créer uniquement des composants de modèle cloisonné. toutefois, dans Visual Basic .net, les composants peuvent être regroupés.

 

## <a name="aggregatable"></a>Aggregatable

Les objets regroupables doivent prendre en charge l’agrégation, autrement dit, ils doivent prendre en charge la création en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec un argument *pUnkOuter* non null. Lorsque COM+ active un objet mis en pool, il crée un agrégat pour gérer la durée de vie de l’objet regroupé et pour appeler des méthodes sur [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Pour plus d’informations sur l’écriture d’objets agrégés, consultez [agrégation](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Composants transactionnels

Les objets regroupables qui participent à des transactions doivent inscrire manuellement les ressources managées. Lorsqu’il est mis en pool, si votre objet contient une ressource managée telle qu’une connexion de base de données, il n’est pas possible que le gestionnaire de ressources s’inscrive automatiquement dans une transaction lorsque l’objet est activé dans le contexte donné. Par conséquent, l’objet lui-même doit gérer la logique de la détection de la transaction, la désactivation de l’inscription automatique de Resource Manager et l’inscription manuelle des ressources qu’il contient. En outre, un objet mis en pool transactionnel doit refléter l’état actuel de ses ressources dans les valeurs de paramètre de [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Pour plus d’informations, consultez [regroupement d’objets transactionnels](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implémentez IObjectControl pour gérer la durée de vie des objets

Les objets regroupables doivent implémenter [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), bien qu’il ne soit pas strictement nécessaire de le faire. Toutefois, les composants transactionnels regroupés doivent implémenter **IObjectControl**. Ces composants doivent surveiller l’état des ressources qu’ils contiennent et indiquer quand ils ne peuvent pas être réutilisés. Lorsque [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) retourne false, une transaction est arrête. Pour plus d’informations, consultez contrôle de la [durée de vie et](controlling-object-lifetime-and-state.md)de l’état d’un objet.

## <a name="language-restrictions"></a>Restrictions de langue

les composants développés à l’aide de Microsoft Visual Basic 6,0 et versions antérieures ne peuvent pas être mis en pool, car ces composants sont des threads cloisonnés. toutefois, dans Visual Basic .net, les composants peuvent être regroupés.

## <a name="legacy-components"></a>Composants hérités

Tant qu’elles ne sont pas transactionnelles et conformes aux exigences précédentes appropriées, les composants peuvent être regroupés même s’ils n’ont pas été spécifiquement écrits avec la fonctionnalité de regroupement à l’esprit. Il n’est pas nécessaire d’implémenter [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); un composant qui ne le fait pas ne participe pas tout simplement à la gestion de sa durée de vie. Si [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) n’est pas implémenté, l’objet continuera à être réutilisé jusqu’à ce que le pool atteigne la taille maximale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chaînes du constructeur d’objet COM+](com--object-constructor-strings.md)
</dt> <dt>

[Contrôle de la durée de vie et de l’état des objets](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Fonctionnement du regroupement d’objets](how-object-pooling-works.md)
</dt> <dt>

[Amélioration des performances avec la mise en pool d’objets](improving-performance-with-object-pooling.md)
</dt> <dt>

[Regroupement d’objets transactionnels](pooling-transactional-objects.md)
</dt> </dl>

 

 
