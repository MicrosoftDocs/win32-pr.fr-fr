---
description: Cette documentation est destinée aux applications en mode utilisateur qui souhaitent utiliser ETW. Pour plus d’informations sur l’instrumentation des pilotes de périphérique qui s’exécutent en mode noyau, voir WPP Software Tracing et ajout d’Event Tracing to Kernel-Mode drivers in the Windows Driver Kit (WDK) (en anglais).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320706"
---
# <a name="event-tracing"></a><span data-ttu-id="291fa-104">Suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="291fa-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="291fa-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="291fa-105">Purpose</span></span>

<span data-ttu-id="291fa-106">Suivi d’v nements pour Windows (ETW) fournit aux programmeurs d’applications la possibilité de démarrer et d’arrêter les sessions de suivi d’événements, d’instrumenter une application pour fournir des événements de trace et de consommer des événements de trace.</span><span class="sxs-lookup"><span data-stu-id="291fa-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="291fa-107">Les événements de trace contiennent un en-tête d’événement et des données définies par le fournisseur qui décrivent l’état actuel d’une application ou d’une opération.</span><span class="sxs-lookup"><span data-stu-id="291fa-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="291fa-108">Vous pouvez utiliser les événements pour déboguer une application et effectuer une analyse de la capacité et des performances.</span><span class="sxs-lookup"><span data-stu-id="291fa-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="291fa-109">Cette documentation est destinée aux applications en mode utilisateur qui souhaitent utiliser ETW.</span><span class="sxs-lookup"><span data-stu-id="291fa-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="291fa-110">Pour plus d’informations sur l’instrumentation des pilotes de périphérique qui s’exécutent en mode noyau, voir [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) et [Ajout d’Event tracing to Kernel-Mode drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK) (en anglais).</span><span class="sxs-lookup"><span data-stu-id="291fa-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="291fa-111">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="291fa-111">Where applicable</span></span>

<span data-ttu-id="291fa-112">Utilisez ETW lorsque vous souhaitez instrumenter votre application, consigner des événements utilisateur ou de noyau dans un fichier journal, et consommer des événements à partir d’un fichier journal ou en temps réel.</span><span class="sxs-lookup"><span data-stu-id="291fa-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="291fa-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="291fa-113">Developer audience</span></span>

<span data-ttu-id="291fa-114">ETW est conçu pour les développeurs C et C++ qui écrivent des applications en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="291fa-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="291fa-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="291fa-115">Run-time requirements</span></span>

<span data-ttu-id="291fa-116">ETW est inclus dans Microsoft Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="291fa-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="291fa-117">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.</span><span class="sxs-lookup"><span data-stu-id="291fa-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="291fa-118">Traiter les traces ETW dans le code .NET</span><span class="sxs-lookup"><span data-stu-id="291fa-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="291fa-119">Vous pouvez utiliser l' [API .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) pour analyser les traces ETW pour vos applications et d’autres composants logiciels.</span><span class="sxs-lookup"><span data-stu-id="291fa-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="291fa-120">Cette API est utilisée en interne chez Microsoft pour analyser les données ETW produites par le système d’ingénierie Windows, et elle est également utilisée pour alimenter plusieurs tables dans l' [Analyseur de performances Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="291fa-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="291fa-121">Cette API est disponible sous la forme d’un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="291fa-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="291fa-122">Pour plus d’informations, consultez [cet article](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="291fa-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="291fa-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="291fa-123">In this section</span></span>



| <span data-ttu-id="291fa-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="291fa-124">Topic</span></span>                                                                     | <span data-ttu-id="291fa-125">Description</span><span class="sxs-lookup"><span data-stu-id="291fa-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="291fa-126">Nouveautés du suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="291fa-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="291fa-127">Nouvelles fonctionnalités qui ont été ajoutées au suivi d’événements dans chaque version.</span><span class="sxs-lookup"><span data-stu-id="291fa-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="291fa-128">À propos du suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="291fa-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="291fa-129">Informations générales sur le suivi des événements.</span><span class="sxs-lookup"><span data-stu-id="291fa-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="291fa-130">Utilisation du suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="291fa-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="291fa-131">Rubriques relatives aux tâches qui décrivent comment utiliser l’API ETW.</span><span class="sxs-lookup"><span data-stu-id="291fa-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="291fa-132">Référence de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="291fa-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="291fa-133">Description détaillée des fonctions ETW et d’autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="291fa-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
