---
description: Un événement chronométré ou répété est un événement qui se produit à une date et une heure spécifiques, ou à intervalles réguliers à intervalles réguliers. Par exemple, un événement peut se produire à minuit le 2 décembre, 2015 ou une fois par semaine, le mardi à 2:31 h 00.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Réception d’un événement chronométré ou répété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202181"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="10e4e-104">Réception d’un événement chronométré ou répété</span><span class="sxs-lookup"><span data-stu-id="10e4e-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="10e4e-105">Un événement chronométré ou répété est un événement qui se produit à une date et une heure spécifiques, ou à intervalles réguliers à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="10e4e-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="10e4e-106">Par exemple, un événement peut se produire à minuit le 2 décembre, 2015 ou une fois par semaine, le mardi à 2:31 h 00.</span><span class="sxs-lookup"><span data-stu-id="10e4e-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="10e4e-107">Le tableau suivant répertorie les différentes classes utilisées pour créer un événement chronométré ou répétitif.</span><span class="sxs-lookup"><span data-stu-id="10e4e-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="10e4e-108">Classe</span><span class="sxs-lookup"><span data-stu-id="10e4e-108">Class</span></span>                                                                                            | <span data-ttu-id="10e4e-109">Description</span><span class="sxs-lookup"><span data-stu-id="10e4e-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e4e-110">[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="10e4e-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="10e4e-111">Modèle d’événement Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="10e4e-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="10e4e-112">Pour plus d’informations, consultez [création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="10e4e-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="10e4e-113">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="10e4e-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="10e4e-114">Technique héritée.</span><span class="sxs-lookup"><span data-stu-id="10e4e-114">Legacy technique.</span></span><br/> <span data-ttu-id="10e4e-115">Pour plus d’informations, consultez [création d’un événement de minuterie avec \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="10e4e-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="10e4e-116">Si vous souhaitez planifier une tâche ou une tâche pour qu’elle se produise à un moment donné ou à plusieurs reprises, utilisez la classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) et ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="10e4e-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="10e4e-117">Cette classe représente un travail créé à l’aide de la commande AT dans une fenêtre de commande depuis **Démarrer** , puis **exécuter**, ou à partir des **tâches planifiées** dans le **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="10e4e-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

