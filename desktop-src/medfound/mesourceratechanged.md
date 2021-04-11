---
description: 'Déclenché par une source de média lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode IMFRateControl :: sesente se termine de façon asynchrone.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Événement MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113694"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="99082-104">Événement MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="99082-104">MESourceRateChanged event</span></span>

<span data-ttu-id="99082-105">Déclenché par une source de média lorsque la vitesse de lecture change.</span><span class="sxs-lookup"><span data-stu-id="99082-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="99082-106">Cet événement est envoyé une fois que la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) sesente se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="99082-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="99082-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="99082-107">Event values</span></span>

<span data-ttu-id="99082-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="99082-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="99082-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="99082-109">VARTYPE</span></span>           | <span data-ttu-id="99082-110">Description</span><span class="sxs-lookup"><span data-stu-id="99082-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="99082-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="99082-111">VT\_R4</span></span><br/> | <span data-ttu-id="99082-112">Nouveau taux de lecture.</span><span class="sxs-lookup"><span data-stu-id="99082-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="99082-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99082-113">Requirements</span></span>



| <span data-ttu-id="99082-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99082-114">Requirement</span></span> | <span data-ttu-id="99082-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="99082-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99082-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99082-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99082-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99082-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99082-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99082-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99082-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99082-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99082-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="99082-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99082-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99082-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99082-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99082-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99082-123">Mise en œuvre du contrôle de taux</span><span class="sxs-lookup"><span data-stu-id="99082-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="99082-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99082-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="99082-125">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="99082-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="99082-126">**IMFRateControl :: setraverse**</span><span class="sxs-lookup"><span data-stu-id="99082-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




