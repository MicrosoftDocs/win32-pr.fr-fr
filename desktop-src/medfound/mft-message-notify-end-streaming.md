---
description: Demande une table de Media Foundation (MFT) à laquelle la diffusion en continu est sur le point de se terminer.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527915"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="1f900-103">\_notification de \_ fin \_ de \_ diffusion de message MFT</span><span class="sxs-lookup"><span data-stu-id="1f900-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="1f900-104">Demande une table de Media Foundation (MFT) à laquelle la diffusion en continu est sur le point de se terminer.</span><span class="sxs-lookup"><span data-stu-id="1f900-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="1f900-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="1f900-105">Message Parameter</span></span>

<span data-ttu-id="1f900-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1f900-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f900-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1f900-107">Remarks</span></span>

<span data-ttu-id="1f900-108">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="1f900-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="1f900-109">Le client n’est pas obligé d’envoyer ce message, même si le client a précédemment envoyé le message de notification de démarrage de la **\_ diffusion en \_ \_ \_ continu du message MFT** .</span><span class="sxs-lookup"><span data-stu-id="1f900-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="1f900-110">Implémentation</span><span class="sxs-lookup"><span data-stu-id="1f900-110">Implementation</span></span>

<span data-ttu-id="1f900-111">La table MFT peut répondre à ce message en libérant des mémoires tampons et d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="1f900-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="1f900-112">La table MFT n’efface pas les données d’entrée et ne réinitialise pas les types de média en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="1f900-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="1f900-113">Aucune table MFT n’est requise pour répondre à ce message.</span><span class="sxs-lookup"><span data-stu-id="1f900-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f900-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f900-114">Requirements</span></span>



| <span data-ttu-id="1f900-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f900-115">Requirement</span></span> | <span data-ttu-id="1f900-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f900-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f900-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f900-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f900-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f900-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f900-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f900-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f900-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f900-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1f900-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f900-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f900-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f900-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f900-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f900-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f900-124">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="1f900-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




