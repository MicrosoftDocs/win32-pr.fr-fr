---
description: Une erreur récupérable s’est produite lors de la diffusion en continu.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Événement MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318825"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="33877-103">Événement MENonFatalError</span><span class="sxs-lookup"><span data-stu-id="33877-103">MENonFatalError event</span></span>

<span data-ttu-id="33877-104">Une erreur récupérable s’est produite lors de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="33877-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="33877-105">Tout composant Media Foundation peut envoyer cet événement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="33877-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="33877-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="33877-106">Event values</span></span>

<span data-ttu-id="33877-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="33877-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="33877-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="33877-108">VARTYPE</span></span>            | <span data-ttu-id="33877-109">Description</span><span class="sxs-lookup"><span data-stu-id="33877-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="33877-110">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="33877-110">VT\_UI4</span></span><br/> | <span data-ttu-id="33877-111">Valeur **HRESULT** qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="33877-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="33877-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="33877-112">Attributes</span></span>

<span data-ttu-id="33877-113">Aucun attribut n’est défini pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="33877-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="33877-114">Notes</span><span class="sxs-lookup"><span data-stu-id="33877-114">Remarks</span></span>

<span data-ttu-id="33877-115">Cet événement signale une erreur inattendue mais récupérable pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="33877-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="33877-116">Par exemple, une source de média peut envoyer cet événement si elle supprime un paquet.</span><span class="sxs-lookup"><span data-stu-id="33877-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="33877-117">N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué.</span><span class="sxs-lookup"><span data-stu-id="33877-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="33877-118">Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="33877-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="33877-119">Si une erreur de diffusion en continu non récupérable se produit, envoyez l’événement [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="33877-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="33877-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33877-120">Requirements</span></span>



| <span data-ttu-id="33877-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33877-121">Requirement</span></span> | <span data-ttu-id="33877-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="33877-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33877-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33877-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33877-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33877-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="33877-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33877-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33877-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33877-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="33877-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="33877-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="33877-128"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33877-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33877-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33877-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33877-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33877-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




