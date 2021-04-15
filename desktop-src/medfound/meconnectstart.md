---
description: Déclenché par la source réseau au démarrage de l’ouverture d’une URL.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Événement MEConnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e45d723a62854c34ba7b297e462d03fed97a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527430"
---
# <a name="meconnectstart-event"></a><span data-ttu-id="f6bbc-103">Événement MEConnectStart</span><span class="sxs-lookup"><span data-stu-id="f6bbc-103">MEConnectStart event</span></span>

<span data-ttu-id="f6bbc-104">Déclenché par la source réseau au démarrage de l’ouverture d’une URL.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-104">Raised by the network source when it starts opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="f6bbc-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="f6bbc-105">Event values</span></span>

<span data-ttu-id="f6bbc-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f6bbc-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f6bbc-107">VARTYPE</span></span>              | <span data-ttu-id="f6bbc-108">Description</span><span class="sxs-lookup"><span data-stu-id="f6bbc-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f6bbc-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="f6bbc-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f6bbc-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f6bbc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f6bbc-111">Remarks</span></span>

<span data-ttu-id="f6bbc-112">La source réseau envoie cet événement directement à l’application par le biais de la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) de l’application, et non par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) habituelle.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6bbc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6bbc-113">Requirements</span></span>



| <span data-ttu-id="f6bbc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6bbc-114">Requirement</span></span> | <span data-ttu-id="f6bbc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6bbc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6bbc-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6bbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6bbc-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6bbc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6bbc-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6bbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6bbc-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6bbc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6bbc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6bbc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6bbc-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6bbc-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6bbc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6bbc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6bbc-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="f6bbc-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="f6bbc-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6bbc-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




