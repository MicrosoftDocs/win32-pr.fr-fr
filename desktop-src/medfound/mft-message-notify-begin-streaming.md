---
description: Avertit une transformation de Media Foundation (MFT) que la diffusion en continu est sur le point de commencer.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201873"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="6b5a4-103">\_notification de \_ début \_ de \_ diffusion de message MFT</span><span class="sxs-lookup"><span data-stu-id="6b5a4-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="6b5a4-104">Avertit une transformation de Media Foundation (MFT) que la diffusion en continu est sur le point de commencer.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="6b5a4-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="6b5a4-105">Message Parameter</span></span>

<span data-ttu-id="6b5a4-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b5a4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6b5a4-107">Remarks</span></span>

<span data-ttu-id="6b5a4-108">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="6b5a4-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="6b5a4-109">Le client n’est pas obligé d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-109">The client is not required to send this message.</span></span> <span data-ttu-id="6b5a4-110">Si le client envoie ce message, il doit le faire après avoir défini tous les types de média sur la MFT, et avant d’appeler [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="6b5a4-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="6b5a4-111">La table MFT peut répondre en allouant des tampons ou d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="6b5a4-112">Si le client n’envoie pas ce message, la table MFT alloue des ressources lors du premier appel à **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="6b5a4-113">Par conséquent, l’envoi de ce message peut réduire la latence initiale au démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="6b5a4-114">Implémentation</span><span class="sxs-lookup"><span data-stu-id="6b5a4-114">Implementation</span></span>

<span data-ttu-id="6b5a4-115">Aucune table MFT n’est requise pour répondre à ce message.</span><span class="sxs-lookup"><span data-stu-id="6b5a4-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5a4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b5a4-116">Requirements</span></span>



| <span data-ttu-id="6b5a4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b5a4-117">Requirement</span></span> | <span data-ttu-id="6b5a4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5a4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b5a4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b5a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5a4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b5a4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6b5a4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b5a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5a4-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b5a4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6b5a4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b5a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b5a4-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b5a4-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b5a4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b5a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5a4-126">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="6b5a4-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




