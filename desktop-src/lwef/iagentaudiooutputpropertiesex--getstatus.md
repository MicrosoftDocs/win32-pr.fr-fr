---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380743"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="3eb54-103">IAgentAudioOutputPropertiesEx :: GetStatus</span><span class="sxs-lookup"><span data-stu-id="3eb54-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="3eb54-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3eb54-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="3eb54-105">Récupère l’état du canal audio.</span><span class="sxs-lookup"><span data-stu-id="3eb54-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="3eb54-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3eb54-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3eb54-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="3eb54-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="3eb54-108">État du canal de sortie audio, qui peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eb54-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="3eb54-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eb54-109">Value</span></span>                                                                         | <span data-ttu-id="3eb54-110">Description</span><span class="sxs-lookup"><span data-stu-id="3eb54-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb54-111">État audio **abrégé non signé const** **\_ \_ disponible = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="3eb54-112">Le canal de sortie audio est disponible (inoccupé).</span><span class="sxs-lookup"><span data-stu-id="3eb54-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="3eb54-113">**const unsigned short** **audio \_ Status \_ noaudio = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="3eb54-114">Il n’existe pas de prise en charge de la sortie audio. par exemple, parce qu’il n’y a pas de carte audio.</span><span class="sxs-lookup"><span data-stu-id="3eb54-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="3eb54-115">**const unsigned short** **audio \_ Status \_ CANTOPENAUDIO = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="3eb54-116">Impossible d’ouvrir le canal de sortie audio (est occupé). par exemple, parce qu’une autre application est en train de diffuser du contenu audio.</span><span class="sxs-lookup"><span data-stu-id="3eb54-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="3eb54-117">**const unsigned short** **audio \_ Status \_ USERSPEAKING = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="3eb54-118">Le canal de sortie audio est occupé car le serveur traite l’entrée vocale de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3eb54-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="3eb54-119">**const unsigned short** **audio \_ Status \_ CHARACTERSPEAKING = 4 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="3eb54-120">Le canal de sortie audio est occupé car un caractère est actuellement en cours de discours.</span><span class="sxs-lookup"><span data-stu-id="3eb54-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="3eb54-121">**const unsigned short** **audio \_ Status \_ SROVERRIDEABLE = 5 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="3eb54-122">Le canal de sortie audio n’est pas occupé, mais il attend une entrée vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3eb54-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="3eb54-123">erreur d’État audio **short non signé const** **\_ \_ = 6 ;**</span><span class="sxs-lookup"><span data-stu-id="3eb54-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="3eb54-124">Un autre problème (inconnu) s’est produit lors de la tentative d’accès au canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="3eb54-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="3eb54-125">Ce paramètre permet à votre application cliente d’interroger l’état du canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="3eb54-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="3eb54-126">Vous pouvez l’utiliser pour déterminer si votre caractère doit être parlant ou pour activer le mode d’écoute (à l’aide de **IAgentCharacterEx :: Listen**).</span><span class="sxs-lookup"><span data-stu-id="3eb54-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





