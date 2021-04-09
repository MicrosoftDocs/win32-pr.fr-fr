---
description: Les fonctions de débogage peuvent être utilisées pour créer un débogueur de base basé sur les événements.
ms.assetid: 3c9e186b-6844-4126-b035-a3541880e109
title: À propos du débogage de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa3e2889d860d747978f2e8866094b0f866910c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860821"
---
# <a name="about-basic-debugging"></a><span data-ttu-id="aa701-103">À propos du débogage de base</span><span class="sxs-lookup"><span data-stu-id="aa701-103">About Basic Debugging</span></span>

<span data-ttu-id="aa701-104">Les [fonctions de débogage](debugging-functions.md) peuvent être utilisées pour créer un débogueur de base basé sur les événements.</span><span class="sxs-lookup"><span data-stu-id="aa701-104">The [debugging functions](debugging-functions.md) can be used to create a basic, event-driven debugger.</span></span> <span data-ttu-id="aa701-105">*Piloté par événement* signifie que le débogueur est averti chaque fois que certains événements se produisent dans le processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="aa701-105">*Event-driven* means that the debugger is notified every time certain events occur in the process being debugged.</span></span> <span data-ttu-id="aa701-106">La notification permet au débogueur de prendre les mesures appropriées en réponse aux événements.</span><span class="sxs-lookup"><span data-stu-id="aa701-106">Notification enables the debugger to take appropriate action in response to the events.</span></span>

<span data-ttu-id="aa701-107">Pour obtenir une vue d’ensemble des termes du débogage, consultez la [terminologie relative au débogage](debugging-terminology.md).</span><span class="sxs-lookup"><span data-stu-id="aa701-107">For an overview of debugging terms, see [Debugging Terminology](debugging-terminology.md).</span></span>

<span data-ttu-id="aa701-108">La [prise en charge du débogage à partir des fonctions de processus, de thread et d’exception](debug-support-from-process-thread-and-exception-functions.md) décrit les fonctionnalités spécifiques au débogage de certains processus, threads et fonctions de gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="aa701-108">[Debug Support from Process, Thread, and Exception Functions](debug-support-from-process-thread-and-exception-functions.md) describes the debugging-specific features of certain process, thread, and exception-handling functions.</span></span>

<span data-ttu-id="aa701-109">La [création d’un débogueur de base](creating-a-basic-debugger.md) décrit l’utilisation des fonctions de débogage de base pour créer un débogueur simple.</span><span class="sxs-lookup"><span data-stu-id="aa701-109">[Creating a Basic Debugger](creating-a-basic-debugger.md) describes using the basic debugging functions to create a simple debugger.</span></span> <span data-ttu-id="aa701-110">Ces fonctions permettent à une application d’attendre les événements de débogage, de provoquer des exceptions de point d’arrêt, de transférer le contrôle d’exécution au débogueur, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="aa701-110">These functions enable an application to wait for debugging events, cause breakpoint exceptions, transfer execution control to the debugger, and so on.</span></span>

<span data-ttu-id="aa701-111">Les [événements de débogage](debugging-events.md) décrivent le mécanisme d’événement de débogage.</span><span class="sxs-lookup"><span data-stu-id="aa701-111">[Debugging Events](debugging-events.md) describes the debug event mechanism.</span></span> <span data-ttu-id="aa701-112">Les événements de débogage entraînent le système à notifier le débogueur.</span><span class="sxs-lookup"><span data-stu-id="aa701-112">Debugging events cause the system to notify the debugger.</span></span>

 

 



