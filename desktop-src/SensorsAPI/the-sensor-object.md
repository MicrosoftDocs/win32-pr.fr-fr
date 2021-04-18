---
description: L’objet capteur représente un capteur particulier.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Objet capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526152"
---
# <a name="the-sensor-object"></a><span data-ttu-id="2de2e-103">Objet capteur</span><span class="sxs-lookup"><span data-stu-id="2de2e-103">The Sensor Object</span></span>

<span data-ttu-id="2de2e-104">L’objet capteur représente un capteur particulier.</span><span class="sxs-lookup"><span data-stu-id="2de2e-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="2de2e-105">L’API de capteur représente chaque capteur sous la forme d’un objet de capteur.</span><span class="sxs-lookup"><span data-stu-id="2de2e-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="2de2e-106">Vous pouvez utiliser un objet de capteur particulier par le biais de son interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) .</span><span class="sxs-lookup"><span data-stu-id="2de2e-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="2de2e-107">Cette interface vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2de2e-107">This interface enables you to:</span></span>

-   <span data-ttu-id="2de2e-108">Récupérez les métadonnées relatives au capteur, telles que son ID, son type ou son nom convivial.</span><span class="sxs-lookup"><span data-stu-id="2de2e-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="2de2e-109">Récupérez des informations sur les données spécifiques que le capteur peut fournir.</span><span class="sxs-lookup"><span data-stu-id="2de2e-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="2de2e-110">Récupérez les données, de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="2de2e-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="2de2e-111">Récupérez les informations d’État, par exemple si le capteur est prêt.</span><span class="sxs-lookup"><span data-stu-id="2de2e-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="2de2e-112">Spécifiez les événements que votre programme recevra.</span><span class="sxs-lookup"><span data-stu-id="2de2e-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="2de2e-113">Spécifiez l’interface de rappel que l’API de capteur peut utiliser pour fournir à votre programme des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="2de2e-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



