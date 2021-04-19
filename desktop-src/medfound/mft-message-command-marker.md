---
description: Marque un point dans le flux. Ce message s’applique uniquement aux MFTs asynchrones.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527822"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="ed44e-104">\_ \_ marqueur de commande de message MFT \_</span><span class="sxs-lookup"><span data-stu-id="ed44e-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="ed44e-105">Marque un point dans le flux.</span><span class="sxs-lookup"><span data-stu-id="ed44e-105">Marks a point in the stream.</span></span> <span data-ttu-id="ed44e-106">Ce message s’applique uniquement aux [MFTS asynchrones](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="ed44e-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="ed44e-107">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="ed44e-107">Message Parameter</span></span>

<span data-ttu-id="ed44e-108">Valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ed44e-108">An arbitrary value.</span></span> <span data-ttu-id="ed44e-109">La table MFT retourne la valeur au client dans l’événement [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="ed44e-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed44e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ed44e-110">Remarks</span></span>

<span data-ttu-id="ed44e-111">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="ed44e-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="ed44e-112">La table MFT répond à ce message, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ed44e-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="ed44e-113">La table MFT génère autant d’exemples de sortie que possible des données d’entrée existantes, en envoyant un événement [METransformHaveOutput](metransformhaveoutput.md) pour chaque exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="ed44e-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="ed44e-114">Une fois que toutes les sorties sont générées, la table MFT envoie un événement [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="ed44e-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="ed44e-115">Cet événement doit être envoyé après tous les événements [METransformHaveOutput](metransformhaveoutput.md) .</span><span class="sxs-lookup"><span data-stu-id="ed44e-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="ed44e-116">Le client n’est pas obligé d’envoyer ce message et ne doit envoyer ce message qu’à un MFTs asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ed44e-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="ed44e-117">Une table MFT synchrone n’enverra pas d’événement [METransformMarker](metransformmarker.md) en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="ed44e-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="ed44e-118">Implémentation</span><span class="sxs-lookup"><span data-stu-id="ed44e-118">Implementation</span></span>

<span data-ttu-id="ed44e-119">Les MFTs asynchrones doivent répondre à ce message comme décrit.</span><span class="sxs-lookup"><span data-stu-id="ed44e-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="ed44e-120">Le MFTs synchrone doit ignorer ce message.</span><span class="sxs-lookup"><span data-stu-id="ed44e-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed44e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed44e-121">Requirements</span></span>



| <span data-ttu-id="ed44e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed44e-122">Requirement</span></span> | <span data-ttu-id="ed44e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed44e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed44e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed44e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed44e-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed44e-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed44e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed44e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed44e-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed44e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed44e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed44e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed44e-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed44e-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed44e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed44e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed44e-131">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="ed44e-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




