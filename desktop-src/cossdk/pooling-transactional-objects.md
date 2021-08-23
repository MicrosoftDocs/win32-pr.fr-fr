---
description: Les composants transactionnels à regrouper ont des exigences particulières.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Regroupement d’objets transactionnels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60180011305d0a03fee10fe1a4838f847306393709dc1bfef39f0ea8f69e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047307"
---
# <a name="pooling-transactional-objects"></a>Regroupement d’objets transactionnels

Les composants transactionnels à regrouper ont des exigences particulières.

## <a name="manually-enlisting-resources"></a>Inscription manuelle des ressources

Les objets regroupables qui participent à des transactions doivent inscrire manuellement les ressources managées. Si un objet contient des ressources managées entre des clients, le gestionnaire de ressources n’aura aucun moyen de s’inscrire automatiquement dans une transaction lorsque l’objet est activé dans un contexte donné.

L’objet lui-même doit gérer la logique de détection de la transaction, de désactivation de l’inscription automatique de Resource Manager et de l’inscription manuelle des ressources qu’il contient. Les étapes de cette procédure sont spécifiques au gestionnaire de ressources que vous utilisez. Si vous devez effectuer une inscription manuelle, consultez la documentation de votre gestionnaire de ressources.

Comme décrit ci-dessous, les objets peuvent être regroupés avec l’affinité de transaction alors qu’une transaction est active et peuvent être activés avec l’affinité de transaction si elle est appelée par un client associé à cette transaction. Avant d’inscrit des ressources, vous devez d’abord vérifier l’affinité de transaction. Si l’objet a été extrait du pool spécifique à cette transaction, il a déjà effectué un travail dans cette transaction et inscrit ses ressources.

## <a name="turning-off-automatic-enlistment"></a>Désactivation de l’inscription automatique

L’inscription automatique doit être désactivée après l’acquisition de la ressource, généralement dans le constructeur de l’objet. Autrement dit, vous désactivez l’inscription automatique, puis vous vous connectez.

La désactivation de l’inscription automatique peut parfois être une procédure subtile, en particulier dans le cas de fournisseurs d’accès aux données en couches. L’inscription automatique est parfois couplée au regroupement de connexions, comme avec ODBC, et parfois pas, comme avec OLE DB. Vous devrez peut-être vous assurer que l’inscription automatique est désactivée à plusieurs niveaux de fournisseurs.

## <a name="implementing-iobjectcontrol"></a>Implémentation de IObjectControl

Les objets regroupables qui participent à des transactions doivent surveiller l’état actuel des ressources qu’ils détiennent. Si l’objet détecte qu’il est dans un État non réutilisable (par exemple, si une connexion est incorrecte), il doit retourner false pour [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Cela aura pour effet d’ignorer l’instance de l’objet et de condamne la transaction en cours.

## <a name="transaction-specific-pools"></a>Pools de Transaction-Specific

Un pool d’objets est généralement homogène, et tout objet mis en pool qui n’est pas en cours d’utilisation est correct pour revenir à n’importe quel client. La seule exception à cette règle est dans le cas d’objets transactionnels, pour lesquels la mise en pool d’objets est optimisée. Lorsque le client qui demande un objet a une transaction associée, COM+ analyse le pool pour rechercher un objet disponible qui est déjà associé à cette transaction. Si un objet avec l’affinité de transaction est trouvé, il est retourné au client ; dans le cas contraire, un objet du pool général est retourné.

De cette manière, les sous-pools spéciaux sont conservés et contiennent des objets avec affinité pour une transaction particulière. Lorsque la transaction est validée ou abandonnée, ces objets sont retournés au pool général sans affinité de transaction, prêt à être utilisé par n’importe quel client.

Pour cette raison, lorsque votre composant inscrit manuellement ses ressources managées dans une transaction, il doit d’abord vérifier s’il est déjà inscrit. Dans ce cas, il n’est pas nécessaire d’inscrire.

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

[Conditions requises pour les objets regroupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



