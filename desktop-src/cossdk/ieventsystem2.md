---
description: Utilisé par le service de notification d’événements système (SENS) de Microsoft Internet Explorer pour accéder au magasin de données d’événements. Cette interface étend l’interface IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interface IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483600"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="70cb6-104">Interface IEventSystem2</span><span class="sxs-lookup"><span data-stu-id="70cb6-104">IEventSystem2 interface</span></span>

<span data-ttu-id="70cb6-105">Utilisé par le service de notification d’événements système (SENS) de Microsoft Internet Explorer pour accéder au magasin de données d’événements.</span><span class="sxs-lookup"><span data-stu-id="70cb6-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="70cb6-106">Cette interface étend l’interface [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .</span><span class="sxs-lookup"><span data-stu-id="70cb6-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="70cb6-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="70cb6-107">When to implement</span></span>

<span data-ttu-id="70cb6-108">Vous n’avez pas besoin d’implémenter l’interface **IEventSystem2** .</span><span class="sxs-lookup"><span data-stu-id="70cb6-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="70cb6-109">Un objet système d’événements fourni par le système (CLSID \_ CEventSystem) implémente **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="70cb6-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="70cb6-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="70cb6-110">When to use</span></span>

<span data-ttu-id="70cb6-111">Si vous utilisez SENS, vous pouvez appeler les méthodes de **IEventSystem2** pour ajouter et supprimer des objets dans le magasin d’événements et pour obtenir des objets à partir du magasin d’événements.</span><span class="sxs-lookup"><span data-stu-id="70cb6-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="70cb6-112">Étant donné que [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) et l’objet du serveur de publication ne sont plus pris en charge, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) n’est pas appelé sur la méthode [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .</span><span class="sxs-lookup"><span data-stu-id="70cb6-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="70cb6-113">Membres</span><span class="sxs-lookup"><span data-stu-id="70cb6-113">Members</span></span>

<span data-ttu-id="70cb6-114">L’interface **IEventSystem2** hérite de **IEventSystem**.</span><span class="sxs-lookup"><span data-stu-id="70cb6-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="70cb6-115">**IEventSystem2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70cb6-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="70cb6-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70cb6-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70cb6-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70cb6-117">Methods</span></span>

<span data-ttu-id="70cb6-118">L’interface **IEventSystem2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="70cb6-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="70cb6-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="70cb6-119">Method</span></span>                                                                         | <span data-ttu-id="70cb6-120">Description</span><span class="sxs-lookup"><span data-stu-id="70cb6-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="70cb6-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="70cb6-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="70cb6-122">Récupère le numéro de version du système d’événements.</span><span class="sxs-lookup"><span data-stu-id="70cb6-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="70cb6-123">**VerifyTransientSubscribers**</span><span class="sxs-lookup"><span data-stu-id="70cb6-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="70cb6-124">Vérifie l’existence de tous les abonnés temporaires dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="70cb6-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="70cb6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70cb6-125">Requirements</span></span>



| <span data-ttu-id="70cb6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70cb6-126">Requirement</span></span> | <span data-ttu-id="70cb6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="70cb6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="70cb6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70cb6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="70cb6-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70cb6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70cb6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70cb6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="70cb6-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70cb6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="70cb6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70cb6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cb6-133">**IEventSystem**</span><span class="sxs-lookup"><span data-stu-id="70cb6-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

