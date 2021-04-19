---
title: Événements SystemMonitor
description: La classe SystemMonitor a les événements suivants
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509776"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="4a94c-103">Événements SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="4a94c-103">SystemMonitor Events</span></span>

<span data-ttu-id="4a94c-104">La classe [**systemmonitor**](systemmonitor.md) a les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="4a94c-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="4a94c-105">**OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="4a94c-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="4a94c-106">**OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="4a94c-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="4a94c-107">**OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="4a94c-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="4a94c-108">**OnDblClick**</span><span class="sxs-lookup"><span data-stu-id="4a94c-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="4a94c-109">**OnSampleCollected**</span><span class="sxs-lookup"><span data-stu-id="4a94c-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="4a94c-110">Vous devez retourner à partir du gestionnaire d’événements avant l’expiration de l' [**intervalle de mise à jour**](systemmonitor-updateinterval.md) ; dans le cas contraire, SYSMON affiche une boîte de message indiquant à l’utilisateur qu’il n’a pas pu échantillonner les valeurs de compteur pour l’intervalle de mise à jour précédent.</span><span class="sxs-lookup"><span data-stu-id="4a94c-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




