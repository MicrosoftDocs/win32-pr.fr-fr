---
title: Informations de référence sur l’API Services Bureau à distance AudioEndpoint
description: Prend en charge les interfaces pour l’inscription du point de terminaison audio et le transport des données.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, informations de référence sur l’API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380192"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="240a8-104">Informations de référence sur l’API Services Bureau à distance AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="240a8-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="240a8-105">Un *point de terminaison audio* représente un périphérique audio, une API audio, ou toute autre source ou récepteur audio, et permet d’envoyer des données à ou de consommer des données à partir du moteur audio.</span><span class="sxs-lookup"><span data-stu-id="240a8-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="240a8-106">Un point de terminaison audio doit être connecté au moteur audio via une *connexion*, et chaque connexion ne peut être connectée qu’à un seul point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="240a8-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="240a8-107">Une fois qu’un point de terminaison est inscrit, le moteur audio joint le point de terminaison à la connexion.</span><span class="sxs-lookup"><span data-stu-id="240a8-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="240a8-108">Chaque objet de point de terminaison doit implémenter les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="240a8-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="240a8-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) pour permettre au moteur audio d’obtenir des informations sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="240a8-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="240a8-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) pour obtenir des informations sur la mémoire tampon de données avant d’effectuer un passage de traitement et de notifier le point de terminaison lorsque la passe est terminée.</span><span class="sxs-lookup"><span data-stu-id="240a8-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="240a8-111">L’interface [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) ou [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , selon que l’objet de point de terminaison capture ou restitue l’audio.</span><span class="sxs-lookup"><span data-stu-id="240a8-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="240a8-112">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="240a8-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="240a8-113">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="240a8-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="240a8-114">Le moteur audio utilise ces interfaces pour obtenir des informations sur les points de terminaison attachés au moteur.</span><span class="sxs-lookup"><span data-stu-id="240a8-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="240a8-115">L’implémentation du point de terminaison doit fournir le mécanisme permettant de fournir des données à ou de consommer des données du moteur comme spécifié par ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="240a8-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="240a8-116">L’API Services Bureau à distance AudioEndpoint prend en charge les types d’énumération, les interfaces et les structures.</span><span class="sxs-lookup"><span data-stu-id="240a8-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="240a8-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="240a8-117">In this section</span></span>

-   [<span data-ttu-id="240a8-118">Types d’énumération AudioEndpoint Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="240a8-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="240a8-119">Services Bureau à distance les fonctions AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="240a8-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="240a8-120">Services Bureau à distance les interfaces AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="240a8-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="240a8-121">Structures AudioEndpoint Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="240a8-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="240a8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="240a8-122">Remarks</span></span>

<span data-ttu-id="240a8-123">L’API Services Bureau à distance AudioEndpoint est destinée à être utilisée dans Bureau à distance scénarios ; ce n’est pas le cas pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="240a8-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




