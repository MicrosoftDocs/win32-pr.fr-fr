---
title: Définition des niveaux de gravité
description: Les niveaux sont utilisés pour regrouper les événements et indiquent généralement la gravité ou le niveau de détail d’un événement.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104381726"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="6c8a4-103">Définition des niveaux de gravité</span><span class="sxs-lookup"><span data-stu-id="6c8a4-103">Defining Severity Levels</span></span>

<span data-ttu-id="6c8a4-104">Les niveaux sont utilisés pour regrouper les événements et indiquent généralement la gravité ou le niveau de détail d’un événement.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="6c8a4-105">Pour définir un niveau, utilisez l’élément **Level** .</span><span class="sxs-lookup"><span data-stu-id="6c8a4-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="6c8a4-106">Le fichier Winmeta.xml définit les niveaux de gravité couramment utilisés suivants :</span><span class="sxs-lookup"><span data-stu-id="6c8a4-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="6c8a4-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="6c8a4-107">win:Critical</span></span>
-   <span data-ttu-id="6c8a4-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="6c8a4-108">win:Error</span></span>
-   <span data-ttu-id="6c8a4-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="6c8a4-109">win:Warning</span></span>
-   <span data-ttu-id="6c8a4-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="6c8a4-110">win:Informational</span></span>
-   <span data-ttu-id="6c8a4-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="6c8a4-111">win:Verbose</span></span>

<span data-ttu-id="6c8a4-112">Les consommateurs utilisent des niveaux pour rechercher des événements qui contiennent une valeur de niveau spécifique.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="6c8a4-113">Une session de suivi ETW peut également utiliser des niveaux pour limiter les événements écrits dans le fichier journal de suivi d’événements ; les événements avec une valeur de niveau inférieure ou égale à la valeur de niveau spécifiée sont écrits dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="6c8a4-114">Par exemple, si la session spécifiait la valeur de niveau pour Win : Warning, le fichier journal contiendrait des événements d’avertissement, d’erreur et critiques.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="6c8a4-115">L’exemple suivant montre comment définir un niveau.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-115">The following example shows how to define a level.</span></span> <span data-ttu-id="6c8a4-116">Vous devez spécifier les attributs **Name** et **value** du niveau.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="6c8a4-117">La valeur de l’attribut **value** doit être comprise entre 16 et 255.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="6c8a4-118">Les attributs **symbol** et **message** sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="6c8a4-118">The **symbol** and **message** attributes are optional.</span></span>


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
