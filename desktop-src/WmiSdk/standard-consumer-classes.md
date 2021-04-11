---
description: Le tableau suivant répertorie les classes pour les consommateurs permanents préinstallés par WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Classes de consommateur standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210735"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="8a33c-103">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="8a33c-103">Standard Consumer Classes</span></span>

<span data-ttu-id="8a33c-104">Le tableau suivant répertorie les classes pour les consommateurs permanents préinstallés par WMI.</span><span class="sxs-lookup"><span data-stu-id="8a33c-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="8a33c-105">Vous pouvez créer des instances de ces classes pour fournir à la classe de consommateur permanente la possibilité de fournir le consommateur logique qui répond lorsqu’il est déclenché par les événements spécifiés dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="8a33c-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="8a33c-106">Par exemple, utilisez la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour définir le script qui s’exécute lorsqu’un événement spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="8a33c-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="8a33c-107">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md) et [surveillance des événements](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="8a33c-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="8a33c-108">Classe</span><span class="sxs-lookup"><span data-stu-id="8a33c-108">Class</span></span>                                                                        | <span data-ttu-id="8a33c-109">Description</span><span class="sxs-lookup"><span data-stu-id="8a33c-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a33c-110">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="8a33c-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="8a33c-111">Exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="8a33c-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="8a33c-112">Exemple : [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="8a33c-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="8a33c-113">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="8a33c-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="8a33c-114">Lance un processus arbitraire dans le contexte du système local lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="8a33c-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="8a33c-115">Exemple : [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="8a33c-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="8a33c-116">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="8a33c-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="8a33c-117">Écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis.</span><span class="sxs-lookup"><span data-stu-id="8a33c-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="8a33c-118">Exemple : [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="8a33c-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="8a33c-119">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="8a33c-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="8a33c-120">Enregistre un message spécifique dans le journal des événements Windows lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="8a33c-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="8a33c-121">Exemple : [journalisation dans le journal des événements NT en fonction d’un événement](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="8a33c-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="8a33c-122">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="8a33c-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="8a33c-123">Fournit des données d’inscription communes à toutes les instances de la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="8a33c-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="8a33c-124">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="8a33c-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="8a33c-125">Envoie un message électronique à l’aide du protocole SMTP à chaque fois qu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="8a33c-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="8a33c-126">Exemple : [envoi d’un E-mail basé sur un événement](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="8a33c-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="8a33c-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a33c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a33c-128">Événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="8a33c-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="8a33c-129">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="8a33c-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="8a33c-130">Exécution d’un script basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="8a33c-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="8a33c-131">Envoi de courrier électronique à partir d’un événement</span><span class="sxs-lookup"><span data-stu-id="8a33c-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




