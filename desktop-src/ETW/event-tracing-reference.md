---
description: Répertorie les éléments utilisés avec le suivi d’événements.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Référence de suivi d’événements
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973659"
---
# <a name="event-tracing-reference"></a><span data-ttu-id="07a0c-103">Référence de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-103">Event Tracing Reference</span></span>

<span data-ttu-id="07a0c-104">Vous utilisez les éléments de programmation suivants pour écrire des applications qui intègrent le suivi d’événements :</span><span class="sxs-lookup"><span data-stu-id="07a0c-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="07a0c-105">Énumérations de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="07a0c-106">Fonctions de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="07a0c-107">Interfaces de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="07a0c-108">Structures de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="07a0c-109">Constantes de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="07a0c-110">Pour plus d’informations sur les exemples qui utilisent ces éléments de programmation, consultez [exemples de traçage d’événements](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="07a0c-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="07a0c-111">Cette section contient également des informations sur les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="07a0c-111">This section also contains information on:</span></span>

-   <span data-ttu-id="07a0c-112">[Outils](event-tracing-tools.md) fournis par ETW</span><span class="sxs-lookup"><span data-stu-id="07a0c-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="07a0c-113">[Définitions de classe MOF](event-tracing-mof-classes.md) pour les événements de noyau</span><span class="sxs-lookup"><span data-stu-id="07a0c-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="07a0c-114">[Qualificateurs de classe MOF](event-tracing-mof-qualifiers.md) utilisés lors de la définition de vos classes d’événements</span><span class="sxs-lookup"><span data-stu-id="07a0c-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="07a0c-115">Traiter les traces ETW dans le code .NET</span><span class="sxs-lookup"><span data-stu-id="07a0c-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="07a0c-116">Vous pouvez également utiliser l' [API .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) pour analyser les traces ETW pour vos applications et d’autres composants logiciels.</span><span class="sxs-lookup"><span data-stu-id="07a0c-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="07a0c-117">Cette API est utilisée en interne chez Microsoft pour analyser les données ETW produites par le système d’ingénierie Windows, et elle est également utilisée pour alimenter plusieurs tables dans l' [Analyseur de performances Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="07a0c-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="07a0c-118">Cette API est disponible sous la forme d’un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="07a0c-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="07a0c-119">Pour plus d’informations, consultez [cet article](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="07a0c-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
