---
description: Lorsqu’une erreur se produit, l’administrateur système ou le représentant du support technique doit déterminer la cause de l’erreur, tenter de récupérer les données perdues et empêcher l’erreur de se reproduire.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: À propos de la journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034095"
---
# <a name="about-event-logging"></a><span data-ttu-id="65b33-103">À propos de la journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="65b33-103">About Event Logging</span></span>

<span data-ttu-id="65b33-104">Lorsqu’une erreur se produit, l’administrateur système ou le représentant du support technique doit déterminer la cause de l’erreur, tenter de récupérer les données perdues et empêcher l’erreur de se reproduire.</span><span class="sxs-lookup"><span data-stu-id="65b33-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="65b33-105">Il est utile si les applications, le système d’exploitation et d’autres services système enregistrent des événements importants, tels que des conditions de mémoire insuffisante ou des tentatives excessives d’accès à un disque.</span><span class="sxs-lookup"><span data-stu-id="65b33-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="65b33-106">L’administrateur système peut ensuite utiliser le journal des événements pour déterminer les conditions à l’origine de l’erreur et identifier le contexte dans lequel elle s’est produite.</span><span class="sxs-lookup"><span data-stu-id="65b33-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="65b33-107">En affichant régulièrement le journal des événements, l’administrateur système peut être en mesure d’identifier les problèmes (tels qu’un disque dur défaillant) avant qu’ils ne provoquent des dommages.</span><span class="sxs-lookup"><span data-stu-id="65b33-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="65b33-108">L’API de journalisation des événements a été conçue pour les applications qui s’exécutent sur le système d’exploitation Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="65b33-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="65b33-109">Dans Windows Vista, l’infrastructure de journalisation des événements a été repensée.</span><span class="sxs-lookup"><span data-stu-id="65b33-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="65b33-110">Les applications conçues pour s’exécuter sur les systèmes d’exploitation Windows Vista ou version ultérieure doivent désormais utiliser le [Journal des événements Windows](/windows/desktop/WES/windows-event-log) pour consigner les événements.</span><span class="sxs-lookup"><span data-stu-id="65b33-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="65b33-111">Cette section décrit l’interface de programmation pour l’écriture et l’utilisation d’événements à l’aide de la journalisation des événements.</span><span class="sxs-lookup"><span data-stu-id="65b33-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="65b33-112">Types d’événements</span><span class="sxs-lookup"><span data-stu-id="65b33-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="65b33-113">Instructions de journalisation</span><span class="sxs-lookup"><span data-stu-id="65b33-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="65b33-114">Éléments de journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="65b33-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="65b33-115">Opérations de journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="65b33-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="65b33-116">Modèle de journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="65b33-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="65b33-117">Sécurité de la journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="65b33-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="65b33-118">Les applications qui publient des événements d’une taille supérieure à 64 kilo-octets sur un ordinateur Windows Server 2003, Windows XP ou Windows 2000 ne seront pas en mesure de publier des événements sur un ordinateur Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="65b33-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
