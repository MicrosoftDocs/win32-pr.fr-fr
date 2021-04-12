---
title: Écriture d’un manifeste d’instrumentation
description: Les applications et les DLL utilisent un manifeste d’instrumentation pour identifier leurs fournisseurs d’instrumentation et les événements que les fournisseurs écrivent.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381993"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="c29e5-103">Écriture d’un manifeste d’instrumentation</span><span class="sxs-lookup"><span data-stu-id="c29e5-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="c29e5-104">Les applications et les DLL utilisent un manifeste d’instrumentation pour identifier leurs fournisseurs d’instrumentation et les événements que les fournisseurs écrivent.</span><span class="sxs-lookup"><span data-stu-id="c29e5-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="c29e5-105">Un manifeste est un fichier XML qui contient les éléments qui identifient votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c29e5-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="c29e5-106">La Convention consiste à utiliser. Man comme extension pour votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="c29e5-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="c29e5-107">Le manifeste doit être conforme au fichier XSD du manifeste d’événements.</span><span class="sxs-lookup"><span data-stu-id="c29e5-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="c29e5-108">Pour plus d’informations sur le schéma, consultez [schéma EventManifest](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c29e5-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="c29e5-109">Un fournisseur d’instrumentation est une application ou une DLL qui appelle les fonctions [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)ou [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) pour écrire des événements dans une session de suivi de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) ou un canal de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c29e5-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="c29e5-110">Une application peut définir un fournisseur d’instrumentation unique qui couvre tous les événements qu’elle écrit ou elle peut définir un fournisseur pour l’application et un fournisseur pour chacune de ses dll.</span><span class="sxs-lookup"><span data-stu-id="c29e5-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="c29e5-111">Le nombre de fournisseurs que l’application définit dans le manifeste dépend uniquement de la façon dont l’application souhaite organiser les événements qu’elle écrit.</span><span class="sxs-lookup"><span data-stu-id="c29e5-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="c29e5-112">L’avantage de spécifier un fournisseur pour chaque DLL est que vous pouvez ensuite activer et désactiver les fournisseurs individuels et donc les événements qu’ils génèrent.</span><span class="sxs-lookup"><span data-stu-id="c29e5-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="c29e5-113">Cet avantage s’applique uniquement si le fournisseur est activé par une session de suivi ETW.</span><span class="sxs-lookup"><span data-stu-id="c29e5-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="c29e5-114">Tous les événements qui spécifient un canal du journal des événements sont toujours écrits sur ce canal.</span><span class="sxs-lookup"><span data-stu-id="c29e5-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="c29e5-115">Le manifeste doit identifier le fournisseur et les événements qu’il écrit, mais les autres métadonnées, telles que les canaux, les niveaux et les mots clés, sont facultatives. la définition des métadonnées facultatives dépend de la personne qui utilisera les événements.</span><span class="sxs-lookup"><span data-stu-id="c29e5-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="c29e5-116">Par exemple, si les administrateurs ou le personnel du support technique consomment les événements à l’aide d’un outil tel que le observateur d’événements Windows qui lit les événements à partir de canaux du journal des événements, vous devez définir les canaux sur lesquels les événements sont écrits.</span><span class="sxs-lookup"><span data-stu-id="c29e5-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="c29e5-117">Toutefois, si le fournisseur est activé uniquement par une session de suivi ETW, vous n’avez pas besoin de définir de canaux.</span><span class="sxs-lookup"><span data-stu-id="c29e5-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="c29e5-118">Bien que les métadonnées des niveaux, des tâches, des OpCodes et des mots clés soient facultatives, vous devez les utiliser pour regrouper ou compartir les événements de manière logique.</span><span class="sxs-lookup"><span data-stu-id="c29e5-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="c29e5-119">Le regroupement des événements permet aux consommateurs de consommer uniquement les événements intéressants.</span><span class="sxs-lookup"><span data-stu-id="c29e5-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="c29e5-120">Par exemple, le consommateur peut interroger tous les événements où le niveau est « critique » et le mot clé « écriture », ou interroger tous les événements écrits par une tâche spécifique.</span><span class="sxs-lookup"><span data-stu-id="c29e5-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="c29e5-121">En plus des consommateurs utilisant le niveau et les mots clés pour utiliser des types spécifiques d’événements, une session de suivi ETW peut utiliser les métadonnées de niveau et de mot clé pour indiquer à ETW de limiter les événements écrits dans le journal de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="c29e5-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="c29e5-122">Par exemple, la session peut limiter les événements aux événements où le niveau est « erreur » ou « critique » et le mot clé est « lecture ».</span><span class="sxs-lookup"><span data-stu-id="c29e5-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="c29e5-123">Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="c29e5-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="c29e5-124">Avec le niveau et les mots clés, ETW détermine si l’événement est écrit dans le journal, mais avec des filtres, le fournisseur utilise les critères de données de filtre pour déterminer s’il écrit l’événement dans cette session.</span><span class="sxs-lookup"><span data-stu-id="c29e5-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="c29e5-125">Les filtres s’appliquent uniquement quand une session de suivi ETW active votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c29e5-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="c29e5-126">Les sections suivantes montrent comment définir les composants du manifeste :</span><span class="sxs-lookup"><span data-stu-id="c29e5-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="c29e5-127">Identification du fournisseur</span><span class="sxs-lookup"><span data-stu-id="c29e5-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="c29e5-128">Définition des canaux à l’endroit où les événements sont écrits</span><span class="sxs-lookup"><span data-stu-id="c29e5-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="c29e5-129">Définition des niveaux de gravité des événements écrits par le fournisseur</span><span class="sxs-lookup"><span data-stu-id="c29e5-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="c29e5-130">Définition des tâches et des opérations effectuées par votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="c29e5-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="c29e5-131">Définition des mots clés qui classent les événements écrits par le fournisseur</span><span class="sxs-lookup"><span data-stu-id="c29e5-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="c29e5-132">Définition des filtres que le fournisseur utilise pour filtrer les événements qu’il écrit</span><span class="sxs-lookup"><span data-stu-id="c29e5-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="c29e5-133">Définition des mappages nom/valeur référencés par vos données de modèle</span><span class="sxs-lookup"><span data-stu-id="c29e5-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="c29e5-134">Définition des modèles qui définissent les données spécifiques aux événements</span><span class="sxs-lookup"><span data-stu-id="c29e5-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="c29e5-135">Définition des événements que le fournisseur écrit</span><span class="sxs-lookup"><span data-stu-id="c29e5-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="c29e5-136">Bien que vous puissiez créer un manifeste d’instrumentation manuellement, vous devez envisager d’utiliser l’outil ECManGen.exe inclus dans le \\ dossier bin du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c29e5-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="c29e5-137">L’outil ECManGen.exe utilise une interface utilisateur graphique qui vous guide tout au long de la création d’un manifeste sans jamais avoir à utiliser des balises XML.</span><span class="sxs-lookup"><span data-stu-id="c29e5-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="c29e5-138">La connaissance des informations contenues dans cette section et dans la section [schéma EventManifest](eventmanifestschema-schema.md) vous aidera lors de l’utilisation de l’outil.</span><span class="sxs-lookup"><span data-stu-id="c29e5-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="c29e5-139">Si vous utilisez Visual Studio comme éditeur XML, vous pouvez ajouter le schéma [EventManifest](eventmanifestschema-schema.md) au projet (consultez le menu XML) pour tirer parti d’IntelliSense, de la validation de schéma inline et d’autres fonctionnalités pour faciliter l’écriture du manifeste.</span><span class="sxs-lookup"><span data-stu-id="c29e5-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="c29e5-140">Après avoir écrit votre manifeste, utilisez le compilateur de message pour valider le manifeste et générer les fichiers de ressources et d’en-tête que vous incluez dans votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c29e5-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="c29e5-141">Pour plus d’informations, consultez [compilation d’un manifeste d’instrumentation](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="c29e5-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="c29e5-142">L’exemple suivant illustre la structure d’un manifeste d’événements entièrement défini.</span><span class="sxs-lookup"><span data-stu-id="c29e5-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 