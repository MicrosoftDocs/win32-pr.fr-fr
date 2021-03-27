---
description: Les sessions de suivi d’événements enregistrent des événements à partir d’un ou de plusieurs fournisseurs.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Contrôle des sessions de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972231"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="06dc5-103">Contrôle des sessions de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="06dc5-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="06dc5-104">Les sessions de suivi d’événements enregistrent des événements à partir d’un ou de plusieurs [fournisseurs](providing-events.md).</span><span class="sxs-lookup"><span data-stu-id="06dc5-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="06dc5-105">Le contrôleur définit la session et active les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="06dc5-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="06dc5-106">La définition de la session comprend généralement la spécification du nom de la session et du fichier journal, du type de fichier journal à utiliser et de la résolution de l’horodatage utilisé pour enregistrer les événements.</span><span class="sxs-lookup"><span data-stu-id="06dc5-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="06dc5-107">Les contrôleurs peuvent également mettre à jour et interroger les sessions de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="06dc5-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="06dc5-108">Les rubriques suivantes montrent comment définir et mettre à jour une session et activer les fournisseurs de suivi d’événements :</span><span class="sxs-lookup"><span data-stu-id="06dc5-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="06dc5-109">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="06dc5-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="06dc5-110">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="06dc5-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="06dc5-111">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="06dc5-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="06dc5-112">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="06dc5-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="06dc5-113">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="06dc5-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="06dc5-114">Récupération de données de suivi d’événements supplémentaires</span><span class="sxs-lookup"><span data-stu-id="06dc5-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="06dc5-115">Pour plus d’informations sur le vidage et l’interrogation des sessions, consultez [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) et [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivement.</span><span class="sxs-lookup"><span data-stu-id="06dc5-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="06dc5-116">Seuls les utilisateurs qui exécutent des privilèges d’administration élevés, les utilisateurs du groupe utilisateurs du journal de performances et les applications qui s’exécutent en tant que LocalSystem, LocalService ou NetworkService peuvent contrôler les sessions de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="06dc5-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="06dc5-117">Pour accorder à un utilisateur restreint la possibilité de contrôler les sessions de suivi, ajoutez-les au groupe utilisateurs du journal de performances.</span><span class="sxs-lookup"><span data-stu-id="06dc5-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="06dc5-118">**Windows XP et windows 2000 :** Tout le monde peut contrôler une session de suivi.</span><span class="sxs-lookup"><span data-stu-id="06dc5-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
