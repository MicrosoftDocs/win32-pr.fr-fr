---
description: Les exemples d’applications WMI de cette section sont écrits en C++.
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: Exemples d’applications WMI C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517607"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="7765a-103">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="7765a-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="7765a-104">Les exemples d’applications WMI de cette section sont écrits en C++.</span><span class="sxs-lookup"><span data-stu-id="7765a-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="7765a-105">Ils illustrent une série de tâches qui peuvent être effectuées à l’aide de composants WMI et offrent une alternative à l’utilisation de scripts de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7765a-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="7765a-106">Chaque application est divisée en une série d’étapes de manière similaire afin que les sections de code des différents exemples puissent être facilement combinées pour former des applications personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7765a-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="7765a-107">Le tableau suivant répertorie les exemples C++ de cette section.</span><span class="sxs-lookup"><span data-stu-id="7765a-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="7765a-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="7765a-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="7765a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7765a-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7765a-110">Exemple : obtention de données WMI à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="7765a-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="7765a-111">Cet exemple se connecte à l’espace de noms WMI sur l’ordinateur local et récupère les données d’une requête sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7765a-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="7765a-112">Les données sont collectées semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="7765a-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="7765a-113">Exemple : obtention de données WMI à partir de l’ordinateur local de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="7765a-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="7765a-114">Cet exemple se connecte à l’espace de noms WMI sur l’ordinateur local et récupère les données d’une requête sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7765a-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="7765a-115">Les données sont collectées de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7765a-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="7765a-116">Exemple : obtention de données WMI à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="7765a-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="7765a-117">Cet exemple se connecte à l’espace de noms WMI sur un ordinateur distant et récupère les données à partir d’une requête sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="7765a-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="7765a-118">Les données sont collectées semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="7765a-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="7765a-119">Exemple : appel d’une méthode de fournisseur</span><span class="sxs-lookup"><span data-stu-id="7765a-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="7765a-120">Cet exemple se connecte à l’espace de noms WMI sur l’ordinateur local et appelle une méthode dans WMI.</span><span class="sxs-lookup"><span data-stu-id="7765a-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="7765a-121">La méthode est exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="7765a-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="7765a-122">Exemple : réception de notifications d’événements via WMI</span><span class="sxs-lookup"><span data-stu-id="7765a-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="7765a-123">Cet exemple se connecte à l’espace de noms WMI sur l’ordinateur local et reçoit un événement de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7765a-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="7765a-124">L’événement est reçu semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="7765a-124">The event is received semisynchronously.</span></span>   |



 

 

 



