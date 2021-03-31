---
description: Les rubriques suivantes décrivent comment utiliser l’API ETW pour le suivi d’événements.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Utilisation du suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201703"
---
# <a name="using-event-tracing"></a><span data-ttu-id="97d73-103">Utilisation du suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="97d73-103">Using Event Tracing</span></span>

<span data-ttu-id="97d73-104">Les rubriques suivantes décrivent comment utiliser l’API ETW pour le suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="97d73-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="97d73-105">Rubrique</span><span class="sxs-lookup"><span data-stu-id="97d73-105">Topic</span></span>                                                                          | <span data-ttu-id="97d73-106">Description</span><span class="sxs-lookup"><span data-stu-id="97d73-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97d73-107">Contrôle des sessions de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="97d73-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="97d73-108">Décrit comment gérer les sessions de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="97d73-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="97d73-109">Fournir des événements</span><span class="sxs-lookup"><span data-stu-id="97d73-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="97d73-110">Décrit comment inscrire et instrumenter un fournisseur de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="97d73-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="97d73-111">Événements de consommation</span><span class="sxs-lookup"><span data-stu-id="97d73-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="97d73-112">Décrit comment implémenter des fonctions de rappel utilisées pour consommer et traiter des événements à partir d’un fichier journal de suivi ou en temps réel.</span><span class="sxs-lookup"><span data-stu-id="97d73-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="97d73-113">Préprocesseur de trace du logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="97d73-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="97d73-114">Fournit un mécanisme efficace pour consigner et consommer des événements qui se produisent pendant l’exécution d’une application ou d’un pilote.</span><span class="sxs-lookup"><span data-stu-id="97d73-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="97d73-115">Incluez le fichier d’en-tête Wmistr. h avant d’inclure le fichier d’en-tête Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="97d73-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



