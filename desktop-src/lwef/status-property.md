---
title: Propriété Status
description: Propriété Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509602"
---
# <a name="status-property"></a><span data-ttu-id="503bc-103">Propriété Status</span><span class="sxs-lookup"><span data-stu-id="503bc-103">Status Property</span></span>

<span data-ttu-id="503bc-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="503bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="503bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="503bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="503bc-106">Retourne l’état du canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="503bc-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="503bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="503bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="503bc-108">*agent \* \* *. AudioOutput. Status**</span><span class="sxs-lookup"><span data-stu-id="503bc-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="503bc-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="503bc-109">Value</span></span> | <span data-ttu-id="503bc-110">Description</span><span class="sxs-lookup"><span data-stu-id="503bc-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503bc-111">0</span><span class="sxs-lookup"><span data-stu-id="503bc-111">0</span></span>     | <span data-ttu-id="503bc-112">Le canal de sortie audio est disponible (inoccupé).</span><span class="sxs-lookup"><span data-stu-id="503bc-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="503bc-113">1</span><span class="sxs-lookup"><span data-stu-id="503bc-113">1</span></span>     | <span data-ttu-id="503bc-114">Il n’existe pas de prise en charge de la sortie audio. par exemple, parce qu’il n’y a pas de carte audio.</span><span class="sxs-lookup"><span data-stu-id="503bc-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="503bc-115">2</span><span class="sxs-lookup"><span data-stu-id="503bc-115">2</span></span>     | <span data-ttu-id="503bc-116">Impossible d’ouvrir le canal de sortie audio (est occupé). par exemple, parce qu’une autre application est en train de diffuser du contenu audio.</span><span class="sxs-lookup"><span data-stu-id="503bc-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="503bc-117">3</span><span class="sxs-lookup"><span data-stu-id="503bc-117">3</span></span>     | <span data-ttu-id="503bc-118">Le canal de sortie audio est occupé car le serveur traite l’entrée vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="503bc-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="503bc-119">4</span><span class="sxs-lookup"><span data-stu-id="503bc-119">4</span></span>     | <span data-ttu-id="503bc-120">Le canal de sortie audio est occupé car un caractère est actuellement en cours de discours.</span><span class="sxs-lookup"><span data-stu-id="503bc-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="503bc-121">5</span><span class="sxs-lookup"><span data-stu-id="503bc-121">5</span></span>     | <span data-ttu-id="503bc-122">Le canal de sortie audio n’est pas occupé, mais il attend une entrée vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="503bc-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="503bc-123">6</span><span class="sxs-lookup"><span data-stu-id="503bc-123">6</span></span>     | <span data-ttu-id="503bc-124">Un autre problème (inconnu) s’est produit lors de la tentative d’accès au canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="503bc-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="503bc-125">Notes</span><span class="sxs-lookup"><span data-stu-id="503bc-125">Remarks</span></span>

<span data-ttu-id="503bc-126">Ce paramètre permet à votre application cliente d’interroger le canal de sortie audio, en retournant une valeur entière qui indique l’état du canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="503bc-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="503bc-127">Vous pouvez l’utiliser pour déterminer s’il est approprié d’avoir votre caractère parlant ou s’il est approprié d’essayer d’activer le mode d’écoute (à l’aide de la méthode [**Listen**](listen-method.md) ).</span><span class="sxs-lookup"><span data-stu-id="503bc-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="503bc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="503bc-128">See Also</span></span>

[<span data-ttu-id="503bc-129">**Événement ListenComplete**</span><span class="sxs-lookup"><span data-stu-id="503bc-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




