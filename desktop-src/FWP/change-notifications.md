---
title: Notifications de modifications
description: Les notifications de modification du moteur de filtrage de base (BFE) suivent le modèle de publication/abonnement.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103940703"
---
# <a name="change-notifications"></a>Notifications de modifications

Les notifications de modification du moteur de filtrage de base (BFE) suivent le modèle de publication/abonnement : afin de recevoir l’une des notifications de modifications publiées, une application doit s’y abonner.

Les notifications de modification de BFE publiées sont ajouter et supprimer pour les [**légendes**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), les [**filtres**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), les [**fournisseurs**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), les [**contextes de fournisseur**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)et les [**sous-couches**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).

Pour s’abonner à l’une des notifications ci-dessus, une application appelle la fonction de gestion [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) correspondante (par exemple, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). La fonction de rappel passée comme argument à **Fwpm \* SubscribeChanges0** est appelée par BFE lorsque la modification à laquelle elle s’est abonnée se produit.

Pour annuler l’abonnement à l’une des notifications ci-dessus, une application appelle la fonction de gestion **Fwpm \* UnsubscribeChanges0** correspondante (par exemple, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Pour afficher les abonnements actuels pour l’une des notifications ci-dessus, une application appelle la fonction de gestion [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) correspondante (par exemple [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Les notifications de modification offertes par le BFE sont les suivantes :

-   Asynchrone : l’appel de fonction qui a déclenché une notification peut retourner avant que la notification soit distribuée à tous les abonnés.
-   Non fiable : aucune garantie n’est faite pour que les notifications soient remises avec succès.

Les abonnés ne reçoivent pas de notifications pour les modifications apportées au handle de session qu’ils ont utilisé pour s’abonner. En règle générale, les abonnés doivent être informés uniquement des modifications apportées par d’autres utilisateurs. ils savent déjà quelles modifications ont été apportées à eux-mêmes.

 

 




