---
title: Informations de référence sur le journal des événements Windows
description: Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger les événements à partir des canaux et des fichiers journaux
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033617"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="a6449-103">Informations de référence sur le journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-103">Windows Event Log Reference</span></span>

<span data-ttu-id="a6449-104">Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger des événements à partir des canaux et des fichiers journaux :</span><span class="sxs-lookup"><span data-stu-id="a6449-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="a6449-105">Schéma EventManifest</span><span class="sxs-lookup"><span data-stu-id="a6449-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="a6449-106">Schéma d’événement</span><span class="sxs-lookup"><span data-stu-id="a6449-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="a6449-107">Schéma de requête</span><span class="sxs-lookup"><span data-stu-id="a6449-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="a6449-108">Constantes du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="a6449-109">Types de données du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="a6449-110">Énumérations des journaux des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="a6449-111">Fonctions du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="a6449-112">Structures du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="a6449-113">Outils du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="a6449-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="a6449-114">Pour les applications écrites à l’aide d’un langage .NET, telles que C# ou Visual Basic, consultez les espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="a6449-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="a6449-115">Pour écrire des événements, utilisez les classes et méthodes définies dans l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="a6449-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="a6449-116">Pour consommer des événements à partir d’un canal ou d’un journal des événements Windows, utilisez les classes et méthodes définies dans l’espace de noms [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="a6449-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="a6449-117">Comme alternative à l’utilisation de l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) pour écrire des événements, vous pouvez utiliser l’argument **-CS** ou **-CSS** pour que le compilateur de message génère le code pour écrire les événements.</span><span class="sxs-lookup"><span data-stu-id="a6449-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="a6449-118">Pour plus d’informations, consultez [**message compiler**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="a6449-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
