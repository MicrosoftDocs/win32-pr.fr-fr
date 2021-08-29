---
description: Contrôle de la durée de vie et de l’état des objets
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Contrôle de la durée de vie et de l’état des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2159f491267ac4d83a75c003005bd6bf7707d0db769d467fcfdfc3799ea08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128821"
---
# <a name="controlling-object-lifetime-and-state"></a>Contrôle de la durée de vie et de l’état des objets

Un objet mis en pool peut participer à la façon dont COM+ gère son activité dans le pool en implémentant [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Lorsqu’un objet regroupé est créé, il est agrégé dans un objet plus volumineux qui gère l’objet en appelant les méthodes suivantes sur **IObjectControl** à des points réguliers dans le cycle de vie de l’objet :

-   [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): appelée chaque fois que l’objet est retourné à un client, activé dans un contexte spécifique.
-   [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): appelée chaque fois qu’un objet est libéré par le client ou, dans le cas d’un objet activé juste-à-temps, lorsqu’il est désactivé.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): appelée chaque fois qu’un objet doit être retourné au pool général.

L’implémentation de [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) est facultative, à l’exception des objets transactionnels, qui doivent toujours implémenter [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) pour surveiller l’état des ressources qu’ils détiennent. Toutefois, il est recommandé d’implémenter **IObjectControl** dans la plupart des cas, car il offre un moyen efficace de gérer le comportement d’un objet regroupé, comme décrit ci-dessous.

## <a name="performing-context-specific-initialization"></a>Exécution d' Context-Specific

À l’aide de l' [**activation**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), vous pouvez initialiser l’objet dans le contexte dans lequel il est activé pour un client donné. Par exemple, pour déterminer si l’objet a une affinité de transaction (ses ressources peuvent déjà être inscrites), vous pouvez obtenir l’ID de transaction associé au contexte.

En général, vous utilisez [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)pour effectuer l’initialisation qui est cohérente dans toutes les méthodes exposées par l’objet, en le traitant comme une partie spécifique au contexte du constructeur de l’objet.

## <a name="cleaning-up-any-client-state"></a>Nettoyage de l’état du client

À l’aide de la fonction [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), vous pouvez supprimer tout état spécifique du client qui peut exister afin que votre objet retourne au pool dans un état totalement générique et puisse ensuite être utilisé par n’importe quel client sans compromettre la sécurité ou l’isolation.

## <a name="controlling-reuse-of-the-object"></a>Contrôle de la réutilisation de l’objet

À l’aide de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), vous pouvez surveiller l’état interne de votre objet et signaler s’il est adapté à sa réutilisation. Si **CanBePooled** retourne la valeur true et que le nombre maximal de pools n’a pas été atteint, l’objet est remis dans le pool général. Si **CanBePooled** retourne la valeur false, l’objet est ignoré. Dans le cas des composants transactionnels, retourner false arrête la transaction en cours.

En règle générale, vous conservez un membre de données global pour l’objet et, si vous détectez une connexion comme étant incorrecte ou une ressource d’un type dont l’État est incorrect, définissez cette valeur pour refléter la situation actuelle et la renvoyer via [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Si un objet n’implémente pas [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), les instances continuent à être réutilisées jusqu’à ce que le niveau maximal du pool soit atteint.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chaînes du constructeur d’objet COM+](com--object-constructor-strings.md)
</dt> <dt>

[Fonctionnement du regroupement d’objets](how-object-pooling-works.md)
</dt> <dt>

[Amélioration des performances avec la mise en pool d’objets](improving-performance-with-object-pooling.md)
</dt> <dt>

[Regroupement d’objets transactionnels](pooling-transactional-objects.md)
</dt> <dt>

[Conditions requises pour les objets regroupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



