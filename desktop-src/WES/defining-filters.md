---
title: Définition de filtres
description: Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102208"
---
# <a name="defining-filters"></a><span data-ttu-id="3fac6-103">Définition de filtres</span><span class="sxs-lookup"><span data-stu-id="3fac6-103">Defining Filters</span></span>

<span data-ttu-id="3fac6-104">Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="3fac6-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="3fac6-105">Avec le niveau et les mots clés, ETW détermine si l’événement est écrit dans le journal.</span><span class="sxs-lookup"><span data-stu-id="3fac6-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="3fac6-106">Toutefois, avec les filtres, le fournisseur utilise les critères de données de filtre que la session de contrôle transmet (voir la fonction [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) pour déterminer s’il écrit l’événement dans cette session.</span><span class="sxs-lookup"><span data-stu-id="3fac6-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="3fac6-107">Les filtres s’appliquent uniquement quand une session de suivi ETW active votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3fac6-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="3fac6-108">En règle générale, les fournisseurs écrivent simplement des événements et la session identifie les types d’événements qu’il souhaite utiliser au niveau et aux mots clés.</span><span class="sxs-lookup"><span data-stu-id="3fac6-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="3fac6-109">Si le fournisseur a défini un filtre de données pour un type d’événement, la session peut l’utiliser pour filtrer les événements pour ce type d’événement en fonction des données d’événement (la sémantique du filtre est définie par le fournisseur).</span><span class="sxs-lookup"><span data-stu-id="3fac6-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="3fac6-110">Par exemple, si votre fournisseur génère des événements de processus, vous pouvez définir un filtre de données qui filtrant les événements de processus en fonction d’un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="3fac6-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="3fac6-111">La session peut ensuite passer un identificateur de processus comme données de filtre au fournisseur et recevoir uniquement les événements de processus pour cet identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="3fac6-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="3fac6-112">L’exemple suivant montre comment utiliser l’élément **Filter** pour définir un filtre.</span><span class="sxs-lookup"><span data-stu-id="3fac6-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="3fac6-113">Vous devez spécifier les attributs **Name** et **value** du filtre. les autres attributs sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="3fac6-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="3fac6-114">L’attribut **TID** est requis si le filtre exige que les données de filtre de la session passent.</span><span class="sxs-lookup"><span data-stu-id="3fac6-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```