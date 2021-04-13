---
description: Énumérations audio principales
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Énumérations audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483920"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="8acbf-103">Énumérations audio principales</span><span class="sxs-lookup"><span data-stu-id="8acbf-103">Core Audio Enumerations</span></span>

<span data-ttu-id="8acbf-104">Cette section décrit les énumérations utilisées par les API audio principales dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8acbf-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="8acbf-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="8acbf-105">Enumeration</span></span>                                                                   | <span data-ttu-id="8acbf-106">Description</span><span class="sxs-lookup"><span data-stu-id="8acbf-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8acbf-107">**\_AUDCLNT \_ BUFFERFLAGS**</span><span class="sxs-lookup"><span data-stu-id="8acbf-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="8acbf-108">Indicateurs d’État pour une mémoire tampon de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="8acbf-109">**AUDCLNT \_ SHAREMODE**</span><span class="sxs-lookup"><span data-stu-id="8acbf-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="8acbf-110">Mode de partage d’un flux.</span><span class="sxs-lookup"><span data-stu-id="8acbf-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="8acbf-111">**AUDCLNT \_ STREAMOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="8acbf-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="8acbf-112">Définit des valeurs qui décrivent les caractéristiques d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="8acbf-113">**\_catégorie de flux audio \_**</span><span class="sxs-lookup"><span data-stu-id="8acbf-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="8acbf-114">Spécifie la catégorie d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="8acbf-115">**AudioSessionState**</span><span class="sxs-lookup"><span data-stu-id="8acbf-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="8acbf-116">État d’une session audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="8acbf-117">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="8acbf-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="8acbf-118">Type de connecteur dans une topologie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8acbf-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="8acbf-119">**DataFlow**</span><span class="sxs-lookup"><span data-stu-id="8acbf-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="8acbf-120">Direction du flux de données d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="8acbf-121">**EDataFlow**</span><span class="sxs-lookup"><span data-stu-id="8acbf-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="8acbf-122">Sens dans lequel les données audio circulent entre un périphérique de point de terminaison audio et une application cliente.</span><span class="sxs-lookup"><span data-stu-id="8acbf-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="8acbf-123">**EndpointFormFactor**</span><span class="sxs-lookup"><span data-stu-id="8acbf-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="8acbf-124">Attributs physiques généraux d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="8acbf-125">**ERole**</span><span class="sxs-lookup"><span data-stu-id="8acbf-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="8acbf-126">Rôle de système d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="8acbf-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="8acbf-127">**\_récepteur KSJACK \_ ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="8acbf-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="8acbf-128">Type de connexion.</span><span class="sxs-lookup"><span data-stu-id="8acbf-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="8acbf-129">**PartType**</span><span class="sxs-lookup"><span data-stu-id="8acbf-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="8acbf-130">Type de partie d’une partie (connecteur ou sous-unité) dans une topologie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8acbf-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="8acbf-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8acbf-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8acbf-132">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="8acbf-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




