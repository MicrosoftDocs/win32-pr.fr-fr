---
title: Définition des canaux
description: Les événements peuvent être écrits dans des canaux de journaux des événements, des fichiers journaux de suivi des événements ou les deux. Un canal est fondamentalement un récepteur qui collecte des événements.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101361"
---
# <a name="defining-channels"></a><span data-ttu-id="2e762-104">Définition des canaux</span><span class="sxs-lookup"><span data-stu-id="2e762-104">Defining Channels</span></span>

<span data-ttu-id="2e762-105">Les événements peuvent être écrits dans des canaux de journaux des événements, des fichiers journaux de suivi des événements ou les deux.</span><span class="sxs-lookup"><span data-stu-id="2e762-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="2e762-106">Un canal est fondamentalement un récepteur qui collecte des événements.</span><span class="sxs-lookup"><span data-stu-id="2e762-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="2e762-107">Si le public cible de vos événements utilise des consommateurs d’événements tels que les observateur d’événements Windows, vous devez définir de nouveaux canaux pour collecter vos événements ou importer un canal existant défini par un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2e762-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="2e762-108">Pour définir vos propres canaux, utilisez l’élément **Channel** .</span><span class="sxs-lookup"><span data-stu-id="2e762-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="2e762-109">Pour définir un canal importé, utilisez l’élément **importChannel** .</span><span class="sxs-lookup"><span data-stu-id="2e762-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="2e762-110">Vous pouvez spécifier jusqu’à huit canaux dans n’importe quelle combinaison de canaux ou de canaux importés que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="2e762-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="2e762-111">Le canal doit être de l’un des quatre types suivants : admin, opérationnel, analyse et débogage.</span><span class="sxs-lookup"><span data-stu-id="2e762-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="2e762-112">Chaque type de canal a une audience prévue, qui détermine le type d’événements que vous écrivez sur le canal.</span><span class="sxs-lookup"><span data-stu-id="2e762-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="2e762-113">Pour obtenir une description de chaque type, consultez le type complexe [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2e762-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="2e762-114">Pour spécifier le canal sur lequel un événement est écrit, affectez à l’attribut de **canal** de la définition de l’événement la même valeur que l’attribut **enfants** de la définition de canal.</span><span class="sxs-lookup"><span data-stu-id="2e762-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="2e762-115">Les événements peuvent uniquement être écrits sur un canal à la fois, mais ils peuvent également être collectés simultanément jusqu’à 7 autres sessions ETW.</span><span class="sxs-lookup"><span data-stu-id="2e762-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="2e762-116">L’exemple suivant montre comment importer un canal.</span><span class="sxs-lookup"><span data-stu-id="2e762-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="2e762-117">Vous devez définir les attributs **enfants** et **Name** .</span><span class="sxs-lookup"><span data-stu-id="2e762-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="2e762-118">L’attribut **enfants** identifie de façon unique le canal : chaque identificateur de canal dans votre liste de canaux doit être unique.</span><span class="sxs-lookup"><span data-stu-id="2e762-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="2e762-119">Affectez à l’attribut **Name** le même nom que celui utilisé lors de la définition du canal.</span><span class="sxs-lookup"><span data-stu-id="2e762-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

<span data-ttu-id="2e762-120">Bien que Winmeta.xml définisse des canaux hérités que vous pouvez importer, vous ne devez pas les utiliser, sauf si vous prenez en charge des consommateurs hérités qui consomment des événements hors des canaux hérités (par exemple, une application ou un système).</span><span class="sxs-lookup"><span data-stu-id="2e762-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="2e762-121">Le fichier Winmeta.xml est inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2e762-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="2e762-122">L’exemple suivant montre comment définir un canal.</span><span class="sxs-lookup"><span data-stu-id="2e762-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="2e762-123">Vous devez définir les attributs **enfants**, **Name** et **type** .</span><span class="sxs-lookup"><span data-stu-id="2e762-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="2e762-124">L’attribut **enfants** identifie de façon unique le canal : chaque identificateur de canal dans votre liste de canaux doit être unique.</span><span class="sxs-lookup"><span data-stu-id="2e762-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="2e762-125">Affectez à l’attribut **enfants** une valeur unique pour les canaux que votre fournisseur répertorie ; l’identificateur de canal est référencé dans une ou plusieurs de vos définitions d’événements.</span><span class="sxs-lookup"><span data-stu-id="2e762-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="2e762-126">La Convention pour nommer le canal consiste à utiliser le nom et le type de canal du fournisseur sous la forme, *providerName* / *channelType*.</span><span class="sxs-lookup"><span data-stu-id="2e762-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
