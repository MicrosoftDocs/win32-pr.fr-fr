---
description: Avertit une transformation de Media Foundation (MFT) qu’un flux d’entrée est terminé.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517626"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="b27da-103">\_ \_ \_ fin \_ de flux de notification de message MFT \_</span><span class="sxs-lookup"><span data-stu-id="b27da-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="b27da-104">Avertit une transformation de Media Foundation (MFT) qu’un flux d’entrée est terminé.</span><span class="sxs-lookup"><span data-stu-id="b27da-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="b27da-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="b27da-105">Message Parameter</span></span>

<span data-ttu-id="b27da-106">Le paramètre *ulParam* contient l’identificateur du flux d’entrée, spécifié sous la forme d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b27da-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="b27da-107">Dans les applications 64 bits, placez cette valeur dans les 32 bits inférieurs du **\_ pointeur PTR**.</span><span class="sxs-lookup"><span data-stu-id="b27da-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b27da-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b27da-108">Remarks</span></span>

<span data-ttu-id="b27da-109">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="b27da-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="b27da-110">Le client n’est pas obligé d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="b27da-110">The client is not required to send this message.</span></span>

<span data-ttu-id="b27da-111">Après la fin d’un flux, le client peut appeler [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) à nouveau pour envoyer de nouvelles données pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="b27da-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="b27da-112">Dans ce cas, le client doit définir l’attribut discontinu ([**MFSampleExtension \_ discontinu**](mfsampleextension-discontinuity-attribute.md) ) sur le premier exemple d’entrée après la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="b27da-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="b27da-113">(Le client doit toujours définir cet attribut sur le premier nouvel échantillon après la fin d’un flux, que le client ait envoyé le message **\_ \_ \_ de fin \_ de \_ message de fin de message MFT** ou non).</span><span class="sxs-lookup"><span data-stu-id="b27da-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="b27da-114">Pour plus d’informations sur la gestion des discontinuités, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).)</span><span class="sxs-lookup"><span data-stu-id="b27da-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="b27da-115">Après l’envoi de ce message pour chaque flux d’entrée, le client envoie généralement une commande de **\_ drainage de \_ commande \_ de message MFT** , puis collecte la sortie restante.</span><span class="sxs-lookup"><span data-stu-id="b27da-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="b27da-116">Toutefois, le client n’est pas obligé de vider la MFT.</span><span class="sxs-lookup"><span data-stu-id="b27da-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="b27da-117">Si le client ne draine pas la MFT, la MFT ignore généralement les données non traitées lors de l’appel suivant à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), lorsqu’il détecte la discontinuité du flux.</span><span class="sxs-lookup"><span data-stu-id="b27da-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="b27da-118">Le client peut également vider la MFT avant d’appeler **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="b27da-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="b27da-119">Ce message ne supprime pas le flux d’entrée ou ne réinitialise pas le type de média.</span><span class="sxs-lookup"><span data-stu-id="b27da-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="b27da-120">Implémentation</span><span class="sxs-lookup"><span data-stu-id="b27da-120">Implementation</span></span>

<span data-ttu-id="b27da-121">Aucune table MFT n’est requise pour répondre à ce message.</span><span class="sxs-lookup"><span data-stu-id="b27da-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b27da-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b27da-122">Requirements</span></span>



| <span data-ttu-id="b27da-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b27da-123">Requirement</span></span> | <span data-ttu-id="b27da-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b27da-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27da-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27da-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b27da-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b27da-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b27da-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27da-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b27da-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b27da-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b27da-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b27da-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27da-130"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27da-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27da-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b27da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27da-132">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="b27da-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




