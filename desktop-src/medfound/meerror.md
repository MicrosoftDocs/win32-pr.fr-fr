---
description: 'Signale une erreur grave. Tout composant Media Foundation peut envoyer cet événement à tout moment. Appelez IMFMediaEvent :: GetStatus pour recevoir le code d’erreur de l’opération qui a échoué.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Événement MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534164"
---
# <a name="meerror-event"></a><span data-ttu-id="a2b05-105">Événement MEError</span><span class="sxs-lookup"><span data-stu-id="a2b05-105">MEError event</span></span>

<span data-ttu-id="a2b05-106">Signale une erreur grave.</span><span class="sxs-lookup"><span data-stu-id="a2b05-106">Signals a serious error.</span></span> <span data-ttu-id="a2b05-107">Tout composant Media Foundation peut envoyer cet événement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="a2b05-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="a2b05-108">Appelez [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pour recevoir le code d’erreur de l’opération qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="a2b05-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="a2b05-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="a2b05-109">Event values</span></span>

<span data-ttu-id="a2b05-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2b05-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a2b05-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a2b05-111">VARTYPE</span></span>              | <span data-ttu-id="a2b05-112">Description</span><span class="sxs-lookup"><span data-stu-id="a2b05-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a2b05-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="a2b05-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a2b05-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="a2b05-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a2b05-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a2b05-115">Remarks</span></span>

<span data-ttu-id="a2b05-116">Cet événement doit être utilisé uniquement pour les erreurs inattendues.</span><span class="sxs-lookup"><span data-stu-id="a2b05-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="a2b05-117">N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué.</span><span class="sxs-lookup"><span data-stu-id="a2b05-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="a2b05-118">Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a2b05-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="a2b05-119">Si une erreur récupérable se produit pendant la diffusion en continu, envoyez l’événement [MENonFatalError](menonfatalerror.md) .</span><span class="sxs-lookup"><span data-stu-id="a2b05-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b05-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b05-120">Requirements</span></span>



| <span data-ttu-id="a2b05-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2b05-121">Requirement</span></span> | <span data-ttu-id="a2b05-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b05-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b05-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b05-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b05-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b05-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a2b05-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b05-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b05-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b05-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2b05-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2b05-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b05-128"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b05-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b05-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b05-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b05-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2b05-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




