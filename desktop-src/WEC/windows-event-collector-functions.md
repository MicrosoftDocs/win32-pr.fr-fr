---
title: Fonctions du collecteur d’événements Windows
description: La liste suivante décrit brièvement les fonctions utilisées dans le collecteur d’événements Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309190"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="740a8-103">Fonctions du collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="740a8-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="740a8-104">La liste suivante décrit brièvement les fonctions utilisées dans le collecteur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="740a8-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="740a8-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="740a8-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="740a8-106">**EcClose**</span><span class="sxs-lookup"><span data-stu-id="740a8-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="740a8-107">Ferme un handle reçu à partir d’autres fonctions du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="740a8-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-108">**EcDeleteSubscription**</span><span class="sxs-lookup"><span data-stu-id="740a8-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="740a8-109">Supprime un abonnement existant.</span><span class="sxs-lookup"><span data-stu-id="740a8-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-110">**EcEnumNextSubscription**</span><span class="sxs-lookup"><span data-stu-id="740a8-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="740a8-111">Continue l’énumération des abonnements inscrits sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="740a8-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-112">**EcGetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="740a8-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="740a8-113">Récupère les valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-114">**EcGetObjectArraySize**</span><span class="sxs-lookup"><span data-stu-id="740a8-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="740a8-115">Récupère le nombre d’index du tableau de valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-116">**EcGetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="740a8-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="740a8-117">Récupère une valeur de propriété à partir d’un objet d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-118">**EcGetSubscriptionRunTimeStatus**</span><span class="sxs-lookup"><span data-stu-id="740a8-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="740a8-119">Récupère les informations d’état d’exécution pour une source d’événement d’un abonnement ou de l’abonnement lui-même.</span><span class="sxs-lookup"><span data-stu-id="740a8-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-120">**EcInsertObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="740a8-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="740a8-121">Insère un objet vide dans un tableau de valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-122">**EcOpenSubscriptionEnum**</span><span class="sxs-lookup"><span data-stu-id="740a8-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="740a8-123">Crée un énumérateur d’abonnement pour énumérer tous les abonnements inscrits sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="740a8-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-124">**EcOpenSubscription**</span><span class="sxs-lookup"><span data-stu-id="740a8-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="740a8-125">Ouvre un abonnement existant ou crée un nouvel abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-126">**EcSaveSubscription**</span><span class="sxs-lookup"><span data-stu-id="740a8-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="740a8-127">Enregistre les informations de configuration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-128">**EcSetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="740a8-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="740a8-129">Définit une valeur de propriété dans un tableau de valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-130">**EcSetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="740a8-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="740a8-131">Définit de nouvelles valeurs ou met à jour les valeurs existantes d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-132">**EcRemoveObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="740a8-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="740a8-133">Supprime un élément d’un tableau d’objets qui contiennent des valeurs de propriété pour les sources d’événements d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="740a8-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="740a8-134">**EcRetrySubscription**</span><span class="sxs-lookup"><span data-stu-id="740a8-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="740a8-135">Effectue une nouvelle tentative de connexion à la source d’événement d’un abonnement qui n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="740a8-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




