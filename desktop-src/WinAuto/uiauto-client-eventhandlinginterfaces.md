---
title: Interfaces de gestion des événements pour les clients
description: Cette section décrit les interfaces de gestion des événements pour les applications clientes UI Automation non managées.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512686"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="4382d-103">Interfaces de gestion des événements pour les clients</span><span class="sxs-lookup"><span data-stu-id="4382d-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="4382d-104">Cette section décrit les interfaces de gestion des événements pour les applications clientes UI Automation non managées.</span><span class="sxs-lookup"><span data-stu-id="4382d-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4382d-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4382d-105">In this section</span></span>



| <span data-ttu-id="4382d-106">Interface</span><span class="sxs-lookup"><span data-stu-id="4382d-106">Interface</span></span>                                                                                                              | <span data-ttu-id="4382d-107">Description</span><span class="sxs-lookup"><span data-stu-id="4382d-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4382d-108">**IUIAutomationChangesEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="4382d-109">Expose une méthode pour gérer les événements Microsoft UI Automation qui se produisent lorsqu’une propriété est modifiée.</span><span class="sxs-lookup"><span data-stu-id="4382d-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="4382d-110">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="4382d-111">Expose une méthode pour gérer les événements UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4382d-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="4382d-112">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="4382d-113">Expose une méthode pour gérer les événements déclenchés lorsque le focus clavier se déplace vers un autre élément UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4382d-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="4382d-114">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="4382d-115">Expose une méthode pour gérer les événements de notification UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4382d-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="4382d-116">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="4382d-117">Expose une méthode pour gérer les événements UI Automation qui se produisent lorsqu’une propriété est modifiée.</span><span class="sxs-lookup"><span data-stu-id="4382d-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="4382d-118">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="4382d-119">Expose une méthode pour gérer les événements qui se produisent lorsque l’arborescence UI Automation est modifiée.</span><span class="sxs-lookup"><span data-stu-id="4382d-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="4382d-120">**IUIAutomationTextEditTextChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4382d-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="4382d-121">Expose une méthode pour gérer les événements qui se produisent quand UI Automation signale un événement de modification de texte à partir de contrôles d’édition de texte.</span><span class="sxs-lookup"><span data-stu-id="4382d-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4382d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4382d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4382d-123">Clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="4382d-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





