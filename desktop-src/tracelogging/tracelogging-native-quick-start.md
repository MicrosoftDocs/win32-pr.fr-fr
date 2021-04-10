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
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/C++ Démarrage rapide

La section suivante décrit les étapes de base requises pour ajouter TraceLogging au code en mode utilisateur natif.

## <a name="prerequisites"></a>Prérequis

-   Windows 10
-   Microsoft Visual Studio 2013
-   Le kit de développement logiciel (SDK) Windows 10 est requis pour écrire un fournisseur en mode utilisateur
-   Windows Driver Kit (WDK) pour Windows 10 est requis pour écrire un fournisseur en mode noyau

> [!IMPORTANT]
> Pour compiler ces exemples, liez advapi32. lib.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample. h

Cet en-tête d’exemple comprend les API TraceLogging et Forward déclare le handle du fournisseur qui sera utilisé pour enregistrer les événements. Toute classe qui souhaite utiliser TraceLogging inclura cet en-tête et pourra ensuite commencer la journalisation.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Le fichier d’en-tête comprend TraceLoggingProvider. h qui définit l’API TraceLogging native. Vous devez d’abord inclure Windows. h, car il définit les constantes utilisées par TraceLoggingProvider. h.

Le fichier d’en-tête Forward déclare le descripteur de fournisseur `g_hMyComponentProvider` que vous allez transmettre aux API TraceLogging pour enregistrer les événements. Ce descripteur doit être accessible à tout code qui souhaite utiliser TraceLogging.

[**TRACELOGGING \_ Le \_ fournisseur DECLARE**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) est une macro qui crée un `extern const TraceLoggingHProvider` handle en utilisant le nom que vous fournissez, dans l’exemple ci-dessus `g_hMyComponentProvider` . Vous allez allouer la variable de handle du fournisseur réel dans un fichier de code.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample. cpp

L’exemple suivant inscrit le fournisseur, journalise un événement et annule l’inscription du fournisseur.

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

L’exemple ci-dessus inclut SimpleTraceLoggingExample. h, qui contient la variable de fournisseur globale que votre code utilisera pour consigner les événements.

La macro de [**\_ définition de \_ fournisseur TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) alloue le stockage et définit la variable de handle du fournisseur. Le nom de la variable que vous fournissez à cette macro doit correspondre au nom que vous avez utilisé dans la macro [**TRACELOGGING \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) dans votre fichier d’en-tête. Ce descripteur reste valide tant qu’il est dans la portée.

### <a name="register-the-provider-handle"></a>Inscrire le handle du fournisseur

Avant de pouvoir utiliser le handle du fournisseur pour consigner des événements, vous devez appeler [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) pour inscrire votre handle de fournisseur. Cette opération est généralement effectuée dans main () ou DLLMain (), mais peut être effectuée à tout moment, à condition qu’elle précède toute tentative de journalisation d’un événement. Si vous consignez un événement avant d’inscrire le handle du fournisseur, aucune erreur ne se produit, mais l’événement n’est pas consigné. Le code suivant de l’exemple ci-dessus inscrit le handle du fournisseur.

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

### <a name="log-a-tracelogging-event"></a>Consigner un événement Tracelogging

Une fois le fournisseur inscrit, le code suivant enregistre un événement simple.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) prend jusqu’à 99 arguments et s’exécute sous la forme de plusieurs instructions. Cela signifie que les valeurs journalisées ne doivent pas être des objets temporaires C++. Le nom de l’événement est stocké au format UTF-8. Vous ne devez pas utiliser `null` de caractères incorporés dans l’événement ou d’autres noms de champs. Il n’y a pas d’autres limites sur les caractères autorisés.

Chaque argument qui suit le nom de l’événement doit être encapsulé à l’intérieur d’une [macro Wrapper TraceLogging](tracelogging-wrapper-macros.md). Si vous utilisez C++, vous pouvez utiliser la `TraceLoggingValue` macro wrapper pour déduire automatiquement le type de l’argument. Si vous écrivez votre pilote en C, vous devez utiliser des macros de champ spécifiques au type, telles que `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` , etc. Les macros Wrapper TraceLogging sont définies dans TraceLoggingProvider. h

En plus de la journalisation des événements uniques, vous pouvez également regrouper les événements par activité à l’aide des macros TraceLoggingWriteStop [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) ou [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)qui se / [](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) trouvent dans TraceLoggingActivity. h. Les activités mettent en corrélation les événements et sont utiles pour les scénarios qui ont un début et une fin. Par exemple, vous pouvez utiliser une activité pour mesurer un scénario qui commence par le lancement d’une application, y compris le temps nécessaire pour que l’écran de démarrage soit disponible et se termine lorsque l’écran initial de l’application devient visible.

Les activités capturent des événements uniques et imbriquent d’autres activités qui se produisent entre le début et la fin de cette activité. Les activités ont une étendue par processus et doivent être transmises du thread au thread pour imbriquer correctement les événements multithread.

La portée d’un descripteur de fournisseur est strictement limitée au module (fichier DLL, EXE ou SYS) dans lequel il est défini : le descripteur ne doit pas être passé à d’autres dll. Si une macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) est appelée dans A.DLL à l’aide d’un handle de fournisseur défini dans B.DLL, cela peut entraîner des problèmes. La façon la plus sûre et la plus efficace de répondre à cette exigence est de toujours référencer directement le handle du fournisseur global et de ne jamais passer le descripteur du fournisseur en tant que paramètre.

### <a name="unregister-the-provider"></a>Annuler l’inscription du fournisseur

Lorsque vous avez terminé la journalisation des événements, vous devez annuler l’inscription du fournisseur TraceLogging. Le code suivant annule l’inscription du fournisseur.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilité

En fonction de sa configuration, TraceLoggingProvider. h peut être à compatibilité descendante (compatible avec Windows Vista ou version ultérieure), ou peut être optimisé pour les versions ultérieures du système d’exploitation. TraceLoggingProvider. h utilise WINVER (mode utilisateur) et NTDDI_VERSION (mode noyau) pour déterminer s’il doit être compatible avec les versions antérieures du système d’exploitation ou être optimisé pour les versions plus récentes du système d’exploitation.

Pour le mode utilisateur, si vous incluez <Windows. h> avant de définir WINVER, <Windows. h> définit WINVER sur la version du système d’exploitation cible par défaut du kit de développement logiciel (SDK). Si WINVER a la valeur 0x602 ou une version ultérieure, TraceLoggingProvider. h optimise son comportement pour Windows 8 (votre application ne s’exécutera pas sur les versions antérieures de Windows). Si vous avez besoin que votre programme s’exécute sur Vista ou Windows 7, veillez à définir WINVER sur la valeur appropriée avant d’inclure <Windows. h>.

De même, si vous incluez <WDM. h> avant de définir NTDDI_VERSION, <WDM. h> définit NTDDI_VERSION sur une valeur par défaut. Si NTDDI_VERSION a la valeur 0x06040000 ou une version ultérieure, TraceLoggingProvider. h optimise son comportement pour Windows 10 (votre pilote ne fonctionnera pas sur les versions antérieures de Windows).

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

Pour savoir comment capturer et afficher des données TraceLogging à l’aide des dernières versions internes des outils de performances Windows (WPT), consultez [enregistrement et affichage des événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md).

Pour plus d’exemples de TraceLogging C++, consultez [exemples Tracelogging C/c++](tracelogging-c-cpp-tracelogging-examples.md) .

 

 




