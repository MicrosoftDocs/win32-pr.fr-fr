---
description: Les ensembles de stations analysés par le biais d’un lien tiers sont modélisés comme un appareil de ligne et éventuellement un appareil téléphonique associé.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529459"
---
# <a name="stations"></a><span data-ttu-id="31654-103">Stations</span><span class="sxs-lookup"><span data-stu-id="31654-103">Stations</span></span>

<span data-ttu-id="31654-104">Les ensembles de stations analysés par le biais d’un lien tiers sont modélisés comme un appareil de ligne et éventuellement un appareil téléphonique associé.</span><span class="sxs-lookup"><span data-stu-id="31654-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="31654-105">Le périphérique de ligne peut avoir plusieurs adresses, si le terminal modélisé prend en charge plusieurs numéros de répertoire (DN).</span><span class="sxs-lookup"><span data-stu-id="31654-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="31654-106">Plusieurs apparences d’appel sur le même DN peuvent être modélisées comme une adresse unique qui prend en charge plusieurs appels.</span><span class="sxs-lookup"><span data-stu-id="31654-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="31654-107">Les appels entre deux stations sur le commutateur ont deux handles d’appel, l’un donnant la vue d’appel à partir de la première station (sur son périphérique de ligne) et l’autre qui donne la vue d’appel à partir de la deuxième station (sur son appareil de ligne).</span><span class="sxs-lookup"><span data-stu-id="31654-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="31654-108">Par exemple, un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) tiers placé par une application sur le serveur est dirigé vers le périphérique de ligne associé à la station à partir de laquelle l’appel doit être composé ; un descripteur d’appel est créé sur cette ligne, sur l’adresse spécifiée dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (ce qui permet de contrôler le DN utilisé sur un téléphone qui prend en charge plusieurs DNS).</span><span class="sxs-lookup"><span data-stu-id="31654-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="31654-109">Lorsque l’appel est offert à l’adresse de destination, un nouveau descripteur d’appel présentant un appel dans l’état d' *offre* est créé ; les applications savent qu’il s’agissait d’une autre vue du même appel par le membre **dwCallID** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) étant égal pour les deux appels.</span><span class="sxs-lookup"><span data-stu-id="31654-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="31654-110">Les deux appels sont *inactifs* lors de la suppression de l’appel ; un appel peut être supprimé de l’application tierce en procédant à un [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sur l’un ou l’autre des handles d’appel.</span><span class="sxs-lookup"><span data-stu-id="31654-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



