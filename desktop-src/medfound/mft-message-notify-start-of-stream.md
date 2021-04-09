---
description: Avertit une transformation de Media Foundation (MFT) que le premier échantillon est sur le point d’être traité.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034161"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="0a9f1-103">\_ \_ début de la notification par message MFT \_ \_ du \_ flux</span><span class="sxs-lookup"><span data-stu-id="0a9f1-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="0a9f1-104">Avertit une transformation de Media Foundation (MFT) que le premier échantillon est sur le point d’être traité.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="0a9f1-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="0a9f1-105">Message Parameter</span></span>

<span data-ttu-id="0a9f1-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9f1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0a9f1-107">Remarks</span></span>

<span data-ttu-id="0a9f1-108">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="0a9f1-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="0a9f1-109">Pour les MFTs synchrones, il est facultatif d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="0a9f1-110">Pour les MFTs asynchrones, le client doit envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="0a9f1-111">Implémentation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-111">Implementation</span></span>

<span data-ttu-id="0a9f1-112">Une table MFT synchrone n’est pas requise pour répondre au message.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="0a9f1-113">Une table MFT asynchrone doit implémenter ce message, comme décrit dans [MFTS asynchrone](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="0a9f1-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9f1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a9f1-114">Requirements</span></span>



| <span data-ttu-id="0a9f1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a9f1-115">Requirement</span></span> | <span data-ttu-id="0a9f1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a9f1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9f1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a9f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9f1-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a9f1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0a9f1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a9f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9f1-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a9f1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0a9f1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a9f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a9f1-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a9f1-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9f1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a9f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9f1-124">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="0a9f1-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




