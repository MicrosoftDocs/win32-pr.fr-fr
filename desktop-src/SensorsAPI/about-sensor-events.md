---
description: L’API de capteur peut fournir des notifications d’événements.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: À propos des événements d’API de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867621"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="1c39c-103">À propos des événements d’API de capteur</span><span class="sxs-lookup"><span data-stu-id="1c39c-103">About Sensor API Events</span></span>

<span data-ttu-id="1c39c-104">L’API de capteur peut fournir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="1c39c-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="1c39c-105">Lorsque vous vous inscrivez pour recevoir des événements, par l’intermédiaire de [**ISensor :: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) ou [**ISensorManager :: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), vous devez fournir un pointeur vers une interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="1c39c-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="1c39c-106">Vous devez implémenter les méthodes de l’interface de rappel dans votre code.</span><span class="sxs-lookup"><span data-stu-id="1c39c-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="1c39c-107">L’API Sensor définit les interfaces de rappel suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c39c-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="1c39c-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="1c39c-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="1c39c-109">Implémentez cette interface pour recevoir des événements des capteurs.</span><span class="sxs-lookup"><span data-stu-id="1c39c-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="1c39c-110">Les capteurs peuvent informer votre application sur les nouvelles données, les modifications de l’état du capteur, la déconnexion du capteur et les événements personnalisés définis par le fabricant du capteur.</span><span class="sxs-lookup"><span data-stu-id="1c39c-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="1c39c-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="1c39c-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="1c39c-112">Implémentez cette interface pour recevoir des événements du gestionnaire de capteurs.</span><span class="sxs-lookup"><span data-stu-id="1c39c-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="1c39c-113">Le gestionnaire de capteurs peut notifier votre application lorsqu’un capteur se connecte et peut donc être utilisé.</span><span class="sxs-lookup"><span data-stu-id="1c39c-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="1c39c-114">Vous pouvez annuler les notifications d’événements en appelant à nouveau [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) , cette fois-ci, en passant une valeur **null** par le biais du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c39c-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c39c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c39c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c39c-116">Utilisation d’événements d’API de capteur</span><span class="sxs-lookup"><span data-stu-id="1c39c-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
