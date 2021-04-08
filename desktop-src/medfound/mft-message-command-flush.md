---
description: Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753949"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="a652e-103">\_vidage de \_ commande de message MFT \_</span><span class="sxs-lookup"><span data-stu-id="a652e-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="a652e-104">Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.</span><span class="sxs-lookup"><span data-stu-id="a652e-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="a652e-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="a652e-105">Message Parameter</span></span>

<span data-ttu-id="a652e-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a652e-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a652e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a652e-107">Remarks</span></span>

<span data-ttu-id="a652e-108">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="a652e-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="a652e-109">Une fois ce message envoyé, la MFT peut accepter de nouveaux exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a652e-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="a652e-110">Les types de médias actuels ne sont pas invalidés.</span><span class="sxs-lookup"><span data-stu-id="a652e-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="a652e-111">Implémentation</span><span class="sxs-lookup"><span data-stu-id="a652e-111">Implementation</span></span>

<span data-ttu-id="a652e-112">Toutes les MFTs doivent implémenter ce message.</span><span class="sxs-lookup"><span data-stu-id="a652e-112">All MFTs must implement this message.</span></span> <span data-ttu-id="a652e-113">Lorsqu’il reçoit ce message, la MFT doit supprimer tous les échantillons de support qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="a652e-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="a652e-114">[MFTS asynchrone](asynchronous-mfts.md): la table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) jusqu’à ce qu’elle reçoive un message [**\_ \_ \_ \_ de \_ flux de message de démarrage de flux MFT**](mft-message-notify-start-of-stream.md) du client.</span><span class="sxs-lookup"><span data-stu-id="a652e-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="a652e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a652e-115">Requirements</span></span>



| <span data-ttu-id="a652e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a652e-116">Requirement</span></span> | <span data-ttu-id="a652e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a652e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a652e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a652e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a652e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a652e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a652e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a652e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a652e-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a652e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a652e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a652e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a652e-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a652e-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a652e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a652e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a652e-125">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="a652e-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




