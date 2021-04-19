---
description: De nombreuses applications enregistrent des erreurs et des événements dans des journaux d’erreurs propriétaires, chacun avec leur propre format et leur propre interface utilisateur.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Journalisation des événements (journalisation des événements)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534704"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="d022f-103">Journalisation des événements (journalisation des événements)</span><span class="sxs-lookup"><span data-stu-id="d022f-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="d022f-104">De nombreuses applications enregistrent des erreurs et des événements dans des journaux d’erreurs propriétaires, chacun avec leur propre format et leur propre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d022f-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="d022f-105">Les données provenant de différentes applications ne peuvent pas être facilement fusionnées dans un rapport complet, ce qui oblige les administrateurs système ou les représentants du support à vérifier diverses sources pour diagnostiquer les problèmes.</span><span class="sxs-lookup"><span data-stu-id="d022f-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="d022f-106">La journalisation des événements offre une méthode standard et centralisée pour les applications (et le système d’exploitation) pour enregistrer des événements logiciels et matériels importants.</span><span class="sxs-lookup"><span data-stu-id="d022f-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="d022f-107">Le service de journalisation des événements enregistre les événements provenant de différentes sources et les stocke dans une collection unique appelée *Journal des événements*.</span><span class="sxs-lookup"><span data-stu-id="d022f-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="d022f-108">Le observateur d’événements vous permet d’afficher les journaux ; l’interface de programmation vous permet également d’examiner les journaux.</span><span class="sxs-lookup"><span data-stu-id="d022f-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="d022f-109">À propos de la journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="d022f-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="d022f-110">Utilisation de la journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="d022f-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="d022f-111">Référence de journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="d022f-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="d022f-112">L’API de journalisation des événements a été conçue pour les applications qui s’exécutent sur le système d’exploitation Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d022f-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="d022f-113">Dans Windows Vista, l’infrastructure de journalisation des événements a été repensée.</span><span class="sxs-lookup"><span data-stu-id="d022f-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="d022f-114">Les applications conçues pour s’exécuter sur des systèmes d’exploitation Windows Vista ou versions ultérieures doivent utiliser le [Journal des événements Windows](/windows/desktop/WES/windows-event-log) pour consigner les événements.</span><span class="sxs-lookup"><span data-stu-id="d022f-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
