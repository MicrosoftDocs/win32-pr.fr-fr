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
# <a name="change-notifications"></a><span data-ttu-id="99adb-103">Notifications de modifications</span><span class="sxs-lookup"><span data-stu-id="99adb-103">Change Notifications</span></span>

<span data-ttu-id="99adb-104">Les notifications de modification du moteur de filtrage de base (BFE) suivent le modèle de publication/abonnement : afin de recevoir l’une des notifications de modifications publiées, une application doit s’y abonner.</span><span class="sxs-lookup"><span data-stu-id="99adb-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="99adb-105">Les notifications de modification de BFE publiées sont ajouter et supprimer pour les [**légendes**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), les [**filtres**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), les [**fournisseurs**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), les [**contextes de fournisseur**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)et les [**sous-couches**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span><span class="sxs-lookup"><span data-stu-id="99adb-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="99adb-106">Pour s’abonner à l’une des notifications ci-dessus, une application appelle la fonction de gestion [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) correspondante (par exemple, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="99adb-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="99adb-107">La fonction de rappel passée comme argument à **Fwpm \* SubscribeChanges0** est appelée par BFE lorsque la modification à laquelle elle s’est abonnée se produit.</span><span class="sxs-lookup"><span data-stu-id="99adb-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="99adb-108">Pour annuler l’abonnement à l’une des notifications ci-dessus, une application appelle la fonction de gestion **Fwpm \* UnsubscribeChanges0** correspondante (par exemple, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="99adb-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="99adb-109">Pour afficher les abonnements actuels pour l’une des notifications ci-dessus, une application appelle la fonction de gestion [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) correspondante (par exemple [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="99adb-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="99adb-110">Les notifications de modification offertes par le BFE sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="99adb-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="99adb-111">Asynchrone : l’appel de fonction qui a déclenché une notification peut retourner avant que la notification soit distribuée à tous les abonnés.</span><span class="sxs-lookup"><span data-stu-id="99adb-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="99adb-112">Non fiable : aucune garantie n’est faite pour que les notifications soient remises avec succès.</span><span class="sxs-lookup"><span data-stu-id="99adb-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="99adb-113">Les abonnés ne reçoivent pas de notifications pour les modifications apportées au handle de session qu’ils ont utilisé pour s’abonner.</span><span class="sxs-lookup"><span data-stu-id="99adb-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="99adb-114">En règle générale, les abonnés doivent être informés uniquement des modifications apportées par d’autres utilisateurs. ils savent déjà quelles modifications ont été apportées à eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="99adb-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 




