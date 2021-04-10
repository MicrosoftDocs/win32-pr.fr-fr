---
title: TraceLogging C/C++ Démarrage rapide
description: La section suivante décrit les étapes de base requises pour ajouter TraceLogging au code en mode utilisateur natif.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2020
ms.locfileid: "103940733"
---
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="9e75e-103">TraceLogging C/C++ Démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="9e75e-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="9e75e-104">La section suivante décrit les étapes de base requises pour ajouter TraceLogging au code en mode utilisateur natif.</span><span class="sxs-lookup"><span data-stu-id="9e75e-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e75e-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="9e75e-105">Prerequisites</span></span>

-   <span data-ttu-id="9e75e-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e75e-106">Windows 10</span></span>
-   <span data-ttu-id="9e75e-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="9e75e-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="9e75e-108">Le kit de développement logiciel (SDK) Windows 10 est requis pour écrire un fournisseur en mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="9e75e-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="9e75e-109">Windows Driver Kit (WDK) pour Windows 10 est requis pour écrire un fournisseur en mode noyau</span><span class="sxs-lookup"><span data-stu-id="9e75e-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e75e-110">Pour compiler ces exemples, liez advapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="9e75e-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="9e75e-111">SimpleTraceLoggingExample. h</span><span class="sxs-lookup"><span data-stu-id="9e75e-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="9e75e-112">Cet en-tête d’exemple comprend les API TraceLogging et Forward déclare le handle du fournisseur qui sera utilisé pour enregistrer les événements.</span><span class="sxs-lookup"><span data-stu-id="9e75e-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="9e75e-113">Toute classe qui souhaite utiliser TraceLogging inclura cet en-tête et pourra ensuite commencer la journalisation.</span><span class="sxs-lookup"><span data-stu-id="9e75e-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="9e75e-114">Le fichier d’en-tête comprend TraceLoggingProvider. h qui définit l’API TraceLogging native.</span><span class="sxs-lookup"><span data-stu-id="9e75e-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="9e75e-115">Vous devez d’abord inclure Windows. h, car il définit les constantes utilisées par TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="9e75e-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="9e75e-116">Le fichier d’en-tête Forward déclare le descripteur de fournisseur `g_hMyComponentProvider` que vous allez transmettre aux API TraceLogging pour enregistrer les événements.</span><span class="sxs-lookup"><span data-stu-id="9e75e-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="9e75e-117">Ce descripteur doit être accessible à tout code qui souhaite utiliser TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="9e75e-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="9e75e-118">[**TRACELOGGING \_ Le \_ fournisseur DECLARE**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) est une macro qui crée un `extern const TraceLoggingHProvider` handle en utilisant le nom que vous fournissez, dans l’exemple ci-dessus `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="9e75e-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="9e75e-119">Vous allez allouer la variable de handle du fournisseur réel dans un fichier de code.</span><span class="sxs-lookup"><span data-stu-id="9e75e-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="9e75e-120">SimpleTraceLoggingExample. cpp</span><span class="sxs-lookup"><span data-stu-id="9e75e-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="9e75e-121">L’exemple suivant inscrit le fournisseur, journalise un événement et annule l’inscription du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e75e-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

<span data-ttu-id="9e75e-122">L’exemple ci-dessus inclut SimpleTraceLoggingExample. h, qui contient la variable de fournisseur globale que votre code utilisera pour consigner les événements.</span><span class="sxs-lookup"><span data-stu-id="9e75e-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="9e75e-123">La macro de [**\_ définition de \_ fournisseur TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) alloue le stockage et définit la variable de handle du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e75e-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="9e75e-124">Le nom de la variable que vous fournissez à cette macro doit correspondre au nom que vous avez utilisé dans la macro [**TRACELOGGING \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) dans votre fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9e75e-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="9e75e-125">Ce descripteur reste valide tant qu’il est dans la portée.</span><span class="sxs-lookup"><span data-stu-id="9e75e-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="9e75e-126">Inscrire le handle du fournisseur</span><span class="sxs-lookup"><span data-stu-id="9e75e-126">Register the provider handle</span></span>

<span data-ttu-id="9e75e-127">Avant de pouvoir utiliser le handle du fournisseur pour consigner des événements, vous devez appeler [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) pour inscrire votre handle de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e75e-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="9e75e-128">Cette opération est généralement effectuée dans main () ou DLLMain (), mais peut être effectuée à tout moment, à condition qu’elle précède toute tentative de journalisation d’un événement.</span><span class="sxs-lookup"><span data-stu-id="9e75e-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="9e75e-129">Si vous consignez un événement avant d’inscrire le handle du fournisseur, aucune erreur ne se produit, mais l’événement n’est pas consigné.</span><span class="sxs-lookup"><span data-stu-id="9e75e-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="9e75e-130">Le code suivant de l’exemple ci-dessus inscrit le handle du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e75e-130">The following code from the example above registers the provider handle.</span></span>

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="9e75e-131">Consigner un événement Tracelogging</span><span class="sxs-lookup"><span data-stu-id="9e75e-131">Log a Tracelogging event</span></span>

<span data-ttu-id="9e75e-132">Une fois le fournisseur inscrit, le code suivant enregistre un événement simple.</span><span class="sxs-lookup"><span data-stu-id="9e75e-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="9e75e-133">La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) prend jusqu’à 99 arguments et s’exécute sous la forme de plusieurs instructions.</span><span class="sxs-lookup"><span data-stu-id="9e75e-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="9e75e-134">Cela signifie que les valeurs journalisées ne doivent pas être des objets temporaires C++.</span><span class="sxs-lookup"><span data-stu-id="9e75e-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="9e75e-135">Le nom de l’événement est stocké au format UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9e75e-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="9e75e-136">Vous ne devez pas utiliser `null` de caractères incorporés dans l’événement ou d’autres noms de champs.</span><span class="sxs-lookup"><span data-stu-id="9e75e-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="9e75e-137">Il n’y a pas d’autres limites sur les caractères autorisés.</span><span class="sxs-lookup"><span data-stu-id="9e75e-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="9e75e-138">Chaque argument qui suit le nom de l’événement doit être encapsulé à l’intérieur d’une [macro Wrapper TraceLogging](tracelogging-wrapper-macros.md).</span><span class="sxs-lookup"><span data-stu-id="9e75e-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="9e75e-139">Si vous utilisez C++, vous pouvez utiliser la `TraceLoggingValue` macro wrapper pour déduire automatiquement le type de l’argument.</span><span class="sxs-lookup"><span data-stu-id="9e75e-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="9e75e-140">Si vous écrivez votre pilote en C, vous devez utiliser des macros de champ spécifiques au type, telles que `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` , etc. Les macros Wrapper TraceLogging sont définies dans TraceLoggingProvider. h</span><span class="sxs-lookup"><span data-stu-id="9e75e-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="9e75e-141">En plus de la journalisation des événements uniques, vous pouvez également regrouper les événements par activité à l’aide des macros TraceLoggingWriteStop [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) ou [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)qui se / [](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) trouvent dans TraceLoggingActivity. h.</span><span class="sxs-lookup"><span data-stu-id="9e75e-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="9e75e-142">Les activités mettent en corrélation les événements et sont utiles pour les scénarios qui ont un début et une fin.</span><span class="sxs-lookup"><span data-stu-id="9e75e-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="9e75e-143">Par exemple, vous pouvez utiliser une activité pour mesurer un scénario qui commence par le lancement d’une application, y compris le temps nécessaire pour que l’écran de démarrage soit disponible et se termine lorsque l’écran initial de l’application devient visible.</span><span class="sxs-lookup"><span data-stu-id="9e75e-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="9e75e-144">Les activités capturent des événements uniques et imbriquent d’autres activités qui se produisent entre le début et la fin de cette activité.</span><span class="sxs-lookup"><span data-stu-id="9e75e-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="9e75e-145">Les activités ont une étendue par processus et doivent être transmises du thread au thread pour imbriquer correctement les événements multithread.</span><span class="sxs-lookup"><span data-stu-id="9e75e-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="9e75e-146">La portée d’un descripteur de fournisseur est strictement limitée au module (fichier DLL, EXE ou SYS) dans lequel il est défini : le descripteur ne doit pas être passé à d’autres dll.</span><span class="sxs-lookup"><span data-stu-id="9e75e-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="9e75e-147">Si une macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) est appelée dans A.DLL à l’aide d’un handle de fournisseur défini dans B.DLL, cela peut entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="9e75e-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="9e75e-148">La façon la plus sûre et la plus efficace de répondre à cette exigence est de toujours référencer directement le handle du fournisseur global et de ne jamais passer le descripteur du fournisseur en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e75e-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="9e75e-149">Annuler l’inscription du fournisseur</span><span class="sxs-lookup"><span data-stu-id="9e75e-149">Unregister the provider</span></span>

<span data-ttu-id="9e75e-150">Lorsque vous avez terminé la journalisation des événements, vous devez annuler l’inscription du fournisseur TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="9e75e-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="9e75e-151">Le code suivant annule l’inscription du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e75e-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="9e75e-152">Compatibilité</span><span class="sxs-lookup"><span data-stu-id="9e75e-152">Compatibility</span></span>

<span data-ttu-id="9e75e-153">En fonction de sa configuration, TraceLoggingProvider. h peut être à compatibilité descendante (compatible avec Windows Vista ou version ultérieure), ou peut être optimisé pour les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e75e-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="9e75e-154">TraceLoggingProvider. h utilise WINVER (mode utilisateur) et NTDDI_VERSION (mode noyau) pour déterminer s’il doit être compatible avec les versions antérieures du système d’exploitation ou être optimisé pour les versions plus récentes du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e75e-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="9e75e-155">Pour le mode utilisateur, si vous incluez <Windows. h> avant de définir WINVER, <Windows. h> définit WINVER sur la version du système d’exploitation cible par défaut du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9e75e-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="9e75e-156">Si WINVER a la valeur 0x602 ou une version ultérieure, TraceLoggingProvider. h optimise son comportement pour Windows 8 (votre application ne s’exécutera pas sur les versions antérieures de Windows).</span><span class="sxs-lookup"><span data-stu-id="9e75e-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="9e75e-157">Si vous avez besoin que votre programme s’exécute sur Vista ou Windows 7, veillez à définir WINVER sur la valeur appropriée avant d’inclure <Windows. h>.</span><span class="sxs-lookup"><span data-stu-id="9e75e-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="9e75e-158">De même, si vous incluez <WDM. h> avant de définir NTDDI_VERSION, <WDM. h> définit NTDDI_VERSION sur une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e75e-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="9e75e-159">Si NTDDI_VERSION a la valeur 0x06040000 ou une version ultérieure, TraceLoggingProvider. h optimise son comportement pour Windows 10 (votre pilote ne fonctionnera pas sur les versions antérieures de Windows).</span><span class="sxs-lookup"><span data-stu-id="9e75e-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="9e75e-160">Résumé et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9e75e-160">Summary and next steps</span></span>

<span data-ttu-id="9e75e-161">Pour savoir comment capturer et afficher des données TraceLogging à l’aide des dernières versions internes des outils de performances Windows (WPT), consultez [enregistrement et affichage des événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="9e75e-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="9e75e-162">Pour plus d’exemples de TraceLogging C++, consultez [exemples Tracelogging C/c++](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="9e75e-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




