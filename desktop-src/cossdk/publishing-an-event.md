---
description: Publication d'un événement
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publication d'un événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514352"
---
# <a name="publishing-an-event"></a><span data-ttu-id="1fa2c-103">Publication d'un événement</span><span class="sxs-lookup"><span data-stu-id="1fa2c-103">Publishing an Event</span></span>

<span data-ttu-id="1fa2c-104">Pour publier un événement, il vous suffit d’instancier un objet d’événement en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou la méthode Microsoft Visual Basic **CreateObject** en utilisant EventClassID ou événements comme argument.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="1fa2c-105">Le serveur de publication appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet d’événement pour obtenir les interfaces prises en charge par l’objet de classe d’événements et appelle une méthode sur l’objet d’événement par le biais de l’interface pour publier l’événement.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="1fa2c-106">Le système d’événements publie ensuite des événements sur la classe d’événements CLSID \_ EventObjectChange avec l’ID d’interface IID \_ IEventObjectChange.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="1fa2c-107">Pour prendre en charge la remise d’événements à plusieurs abonnés, les méthodes de classe d’événements doivent contenir uniquement des paramètres in.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="1fa2c-108">En utilisant la propriété FireInParallel de l’objet de [classe d’événements](the-com--event-class-object.md) , les éditeurs peuvent demander que le système d’événements utilise plusieurs threads pour remettre un événement à plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="1fa2c-109">La sélection d’un mécanisme de remise en parallèle ne garantit pas la remise simultanée de l’événement à plusieurs abonnés, mais il indique au service d’événements COM+ de l’autoriser à se produire.</span><span class="sxs-lookup"><span data-stu-id="1fa2c-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fa2c-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fa2c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa2c-111">Publication et diffusion d’événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="1fa2c-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
