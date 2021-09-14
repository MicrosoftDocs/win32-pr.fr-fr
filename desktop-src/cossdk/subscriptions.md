---
description: 'Les données d’abonnement résident dans le catalogue COM+ de l’abonnement. Vous pouvez créer un abonnement à l’aide de l’outil d’administration Services de composants ou par programme à l’aide de l’interface ICOMAdminCatalog :: InstallComponent.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310917"
---
# <a name="subscriptions"></a>Abonnements

Les données d’abonnement résident dans le catalogue COM+ de l’abonnement. Vous pouvez créer un abonnement à l’aide de l’outil d’administration Services de composants ou par programme à l’aide de l’interface [**ICOMAdminCatalog :: InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .

La collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) permet d’ajouter, de supprimer ou de modifier des informations relatives aux abonnements. La collection **SubscriptionsForComponent** est une collection enfant d’un composant. Pour ajouter un abonnement, récupérez la collection **SubscriptionsForComponent** du composant et utilisez la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) pour ajouter une entrée à la collection. Pour définir les différentes propriétés de l’objet d’abonnement, utilisez la propriété [**value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) . Pour enregistrer les modifications, utilisez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet de collection **SubscriptionsForComponent** .

Vous pouvez également utiliser l’outil d’administration Services de composants pour modifier certaines des propriétés de l’abonnement, mais pas toutes. Les abonnements spécifient les informations suivantes :

-   Identité et emplacement de l’abonné
-   Méthode de remise
-   Méthodes d’événements à remettre
-   Objet de classe d’événements et propriété PublisherID d’un composant de classe d’événements à partir duquel l’abonné souhaite recevoir des événements

Les abonnements existent indépendamment des objets de la classe d’événements. Vous pouvez désactiver un abonnement en affectant la valeur false à la propriété Enabled. Un abonnement désactivé n’est pas appelé par les événements COM+.

Les trois types d’abonnements sont les suivants :

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Manière
</dt> <dd>

Les abonnements persistants résident dans le catalogue COM+ et sont indépendants de la durée de vie de l’abonné. Les abonnements persistants survivent au redémarrage du système. En règle générale, un abonnement persistant est créé lorsqu’une application est installée sur l’ordinateur d’un abonné et supprimée lorsque l’application est supprimée. Après la création d’un abonnement persistant, les événements COM+ activent l’abonné chaque fois qu’un événement lui est fourni.

Lorsqu’un serveur de publication instancie et effectue un appel sur un objet de [classe d’événements](the-com--event-class-object.md) , l’objet recherche tous les abonnements persistants dans le catalogue com+ et crée une nouvelle instance de chaque objet. Le processus de création peut être direct ou par le biais d’un moniker pour les composants en file d’attente. Spécifiez l’objet d’abonné par la propriété [**SubscriberMoniker**](subscriptionsforcomponent.md) de l’abonnement. Les objets abonnés créés par un abonnement persistant sont toujours libérés après chaque appel d’événement.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Provisoire
</dt> <dd>

Pour les abonnements temporaires, vous pouvez utiliser la collection [**TransientSubscriptions**](transientsubscriptions.md) , dont l’objet parent est l’objet catalogue racine. Les abonnements temporaires demandent un événement pour un objet d’abonné spécifique qui existe déjà. Les abonnements temporaires sont stockés dans le catalogue COM+, mais l’abonnement est supprimé si le système d’événements ou le système d’exploitation est arrêté. Contrairement aux abonnements persistants, les abonnements temporaires sont liés à un objet particulier et sont stockés uniquement dans le système d’événements. Les abonnements temporaires peuvent être plus efficaces que les abonnements persistants, mais vous devez gérer leurs cycles de vie d’objet. Pour plus d’informations sur l’inscription d’un abonnement temporaire, consultez [inscription d’un abonnement temporaire](registering-a-transient-subscription.md).

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Par utilisateur
</dt> <dd>

Les abonnements par utilisateur peuvent remettre des événements uniquement lorsque l’abonné est connecté à l’ordinateur du système d’événement. Lorsque l’abonné ouvre une session, le système d’événements active tous les abonnements pour lesquels l’indicateur de *PerUser* est défini sur **true** *et le nom d’utilisateur* est défini sur le nom de l’utilisateur qui a ouvert une session. Lorsque l’abonné ferme une session, les abonnements sont désactivés.

Les abonnements par utilisateur sont effectifs uniquement lorsque le serveur de publication et l’abonné se trouvent sur le même ordinateur. L’ouverture et la fermeture de session sont détectées uniquement sur l’ordinateur de l’éditeur, et non sur l’ordinateur sur lequel réside l’objet de l’abonné.

</dd> </dl>

Le système d’événements utilise des méta-événements pour notifier les abonnés intéressés chaque fois que des objets de classe d’événements ou des abonnements sont créés, modifiés ou supprimés. Pour recevoir des méta-événements du système d’événements, les applications doivent créer un abonnement qui réside sur l’ordinateur du système d’événements et qui spécifie l’ID d’interface de déclenchement (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Objet de classe d’événements COM+](the-com--event-class-object.md)
</dt> <dt>

[Utilisation d’événements COM+ avec des composants en file d’attente COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



