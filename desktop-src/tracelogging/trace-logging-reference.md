---
title: Référence TraceLogging
description: Les rubriques suivantes fournissent des informations sur l’API TraceLogging native. TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382708"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="0fa90-103">Référence TraceLogging</span><span class="sxs-lookup"><span data-stu-id="0fa90-103">TraceLogging Reference</span></span>

<span data-ttu-id="0fa90-104">Les rubriques suivantes fournissent des informations sur l’API TraceLogging native.</span><span class="sxs-lookup"><span data-stu-id="0fa90-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="0fa90-105">TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.</span><span class="sxs-lookup"><span data-stu-id="0fa90-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="0fa90-106">TraceLogging vous permet d’inclure des données structurées avec des événements, de mettre en corrélation des événements et ne requiert pas de fichier XML de manifeste d’instrumentation distinct.</span><span class="sxs-lookup"><span data-stu-id="0fa90-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="0fa90-107"><span class="underline">Pour les développeurs WinRT</span></span><span class="sxs-lookup"><span data-stu-id="0fa90-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="0fa90-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) a été étendu dans Windows 10 pour consigner les événements de suivi d’v nements pour Windows autodescriptifs (ETW) sans nécessiter de manifeste.</span><span class="sxs-lookup"><span data-stu-id="0fa90-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="0fa90-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) a été étendu dans Windows 10 afin de fournir des méthodes de démarrage et d’arrêt de l’activité qui permettent de contrôler le format et le contenu des événements de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0fa90-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="0fa90-110">En outre, les activités peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="0fa90-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="0fa90-111"><span class="underline">Pour les développeurs de code managé (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="0fa90-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="0fa90-112">La classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fournie avec les versions précédentes du .NET Framework prend déjà en charge l’écriture d’événements ETW sans nécessiter de manifeste.</span><span class="sxs-lookup"><span data-stu-id="0fa90-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="0fa90-113">Toutefois, les développeurs devaient utiliser EventSource comme classe de base et ajouter automatiquement des attributs et des méthodes à la classe dérivée qui ont été transformés en manifeste ETW.</span><span class="sxs-lookup"><span data-stu-id="0fa90-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="0fa90-114">Désormais, les développeurs n’ont pas besoin de dériver de EventSource et peuvent plutôt utiliser EventSource directement pour consigner les événements à Description automatique qui ne nécessitent pas de manifeste.</span><span class="sxs-lookup"><span data-stu-id="0fa90-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="0fa90-115"><span class="underline">Pour les développeurs C/C++</span></span><span class="sxs-lookup"><span data-stu-id="0fa90-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="0fa90-116">TraceLoggingProvider. h est l’API recommandée pour les développeurs C/C++ en mode utilisateur ou en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="0fa90-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="0fa90-117">Cette API n’est pas bien adaptée à une utilisation dans des scénarios dynamiques (scriptés) tels que JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0fa90-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="0fa90-118">Les liens suivants décrivent l’API C/C++.</span><span class="sxs-lookup"><span data-stu-id="0fa90-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="0fa90-119">Classes</span><span class="sxs-lookup"><span data-stu-id="0fa90-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="0fa90-120">Fonctions</span><span class="sxs-lookup"><span data-stu-id="0fa90-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="0fa90-121">Macros</span><span class="sxs-lookup"><span data-stu-id="0fa90-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="0fa90-122">Notez que la valeur de WINVER aura un impact sur le comportement de TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="0fa90-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="0fa90-123">Si WINVER n’est pas défini avant d’inclure <Windows. h>, <Windows. h> affectera à WINVER une valeur par défaut correspondant à la version du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="0fa90-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="0fa90-124">Si vous utilisez TraceLoggingProvider. h avec WINVER défini sur 0x0602 (Windows 8) ou une version ultérieure, le programme ne s’exécutera pas sur Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0fa90-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="0fa90-125">Si vous utilisez TraceLoggingProvider. h avec WINVER défini sur 0x0600 (Windows Vista) ou 0x0601 (Windows 7), le programme sera configuré pour la compatibilité et fonctionnera sur les versions spécifiées de Windows.</span><span class="sxs-lookup"><span data-stu-id="0fa90-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 