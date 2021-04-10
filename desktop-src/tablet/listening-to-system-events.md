---
description: Les applications peuvent écouter les événements système à l’aide de l’objet InkCollector et en écoutant l’événement SystemGesture.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Écoute des événements système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042780"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="dffc7-103">Écoute des événements système</span><span class="sxs-lookup"><span data-stu-id="dffc7-103">Listening to System Events</span></span>

<span data-ttu-id="dffc7-104">Les applications peuvent écouter les événements système à l’aide de l’objet [**InkCollector**](inkcollector-class.md) et en écoutant l’événement [**SystemGesture**](inkcollector-systemgesture.md) .</span><span class="sxs-lookup"><span data-stu-id="dffc7-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="dffc7-105">Vous pouvez définir les événements que l’application écoute.</span><span class="sxs-lookup"><span data-stu-id="dffc7-105">You can set which events an application listens to.</span></span> <span data-ttu-id="dffc7-106">Lorsqu’une action de stylet de tablette se produit, l’événement **SystemGesture** correspondant est envoyé à l’application sur son objet **InkCollector** .</span><span class="sxs-lookup"><span data-stu-id="dffc7-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="dffc7-107">Une application peut annuler le message de souris qui correspond à un événement **SystemGesture** donné lorsqu’il reçoit l’événement.</span><span class="sxs-lookup"><span data-stu-id="dffc7-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="dffc7-108">Pour plus d’informations sur l’annulation des messages de la souris, consultez événement **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="dffc7-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



