---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103733645"
---
# <a name="tracelogging"></a><span data-ttu-id="b20ac-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="b20ac-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="b20ac-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="b20ac-104">Purpose</span></span>

<span data-ttu-id="b20ac-105">TraceLogging est la nouvelle infrastructure de suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="b20ac-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="b20ac-106">TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.</span><span class="sxs-lookup"><span data-stu-id="b20ac-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b20ac-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b20ac-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20ac-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b20ac-108">Topic</span></span></th>
<th><span data-ttu-id="b20ac-109">Description</span><span class="sxs-lookup"><span data-stu-id="b20ac-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b20ac-110"><a href="trace-logging-about.md">À propos de TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="b20ac-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="b20ac-111">TraceLogging est le nouveau suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="b20ac-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="b20ac-112">TraceLogging est un format pour l’auto-Description Suivi d’v nements pour Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="b20ac-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="b20ac-113">TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.</span><span class="sxs-lookup"><span data-stu-id="b20ac-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b20ac-114"><a href="tracelogging-using-tracelogging.md">Utilisation de TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="b20ac-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="b20ac-115">Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.</span><span class="sxs-lookup"><span data-stu-id="b20ac-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b20ac-116"><a href="trace-logging-reference.md">Référence TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="b20ac-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="b20ac-117">Les rubriques suivantes fournissent des informations sur l’API TraceLogging native.</span><span class="sxs-lookup"><span data-stu-id="b20ac-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="b20ac-118">TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.</span><span class="sxs-lookup"><span data-stu-id="b20ac-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="b20ac-119">TraceLogging vous permet d’inclure des données structurées avec des événements, de mettre en corrélation des événements et ne requiert pas de fichier XML de manifeste d’instrumentation distinct.</span><span class="sxs-lookup"><span data-stu-id="b20ac-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="b20ac-120"><span class="underline">Pour les développeurs WinRT</span></span><span class="sxs-lookup"><span data-stu-id="b20ac-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="b20ac-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> a été étendu dans Windows 10 pour consigner les événements de suivi d’v nements pour Windows autodescriptifs (ETW) sans nécessiter de manifeste.</span><span class="sxs-lookup"><span data-stu-id="b20ac-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="b20ac-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> a été étendu dans Windows 10 afin de fournir des méthodes de démarrage et d’arrêt de l’activité qui permettent de contrôler le format et le contenu des événements de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="b20ac-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="b20ac-123">En outre, les activités peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="b20ac-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="b20ac-124">
<span class="underline">Pour les développeurs de code managé (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="b20ac-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="b20ac-125">La classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fournie avec les versions précédentes du .NET Framework prend déjà en charge l’écriture d’événements ETW sans nécessiter de manifeste.</span><span class="sxs-lookup"><span data-stu-id="b20ac-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="b20ac-126">Toutefois, les développeurs devaient utiliser EventSource comme classe de base et ajouter automatiquement des attributs et des méthodes à la classe dérivée qui ont été transformés en manifeste ETW.</span><span class="sxs-lookup"><span data-stu-id="b20ac-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="b20ac-127">Désormais, les développeurs n’ont pas besoin de dériver de EventSource et peuvent plutôt utiliser EventSource directement pour consigner les événements à Description automatique qui ne nécessitent pas de manifeste.</span><span class="sxs-lookup"><span data-stu-id="b20ac-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="b20ac-128">
<span class="underline">Pour les développeurs C/C++</span></span><span class="sxs-lookup"><span data-stu-id="b20ac-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="b20ac-129">TraceLoggingProvider. h est l’API recommandée pour les développeurs C/C++ en mode utilisateur ou en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="b20ac-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="b20ac-130">Cette API n’est pas bien adaptée à une utilisation dans des scénarios dynamiques (scriptés) tels que JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b20ac-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="b20ac-131">Les liens suivants décrivent l’API C/C++.</span><span class="sxs-lookup"><span data-stu-id="b20ac-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="b20ac-132">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="b20ac-132">Developer audience</span></span>

<span data-ttu-id="b20ac-133">TraceLogging est conçu pour être utilisé par les développeurs d’applications en mode utilisateur et les développeurs de pilotes en mode noyau qui souhaitent ajouter le suivi à leur code.</span><span class="sxs-lookup"><span data-stu-id="b20ac-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

