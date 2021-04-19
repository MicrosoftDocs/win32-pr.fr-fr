---
description: "L' \\_ \\_ événement d’événement EC CODECAPI est envoyé par un encodeur pour signaler un événement d’encodage. Le client s’inscrit à l’événement d’encodeur en appelant la méthode ICodecAPI :: RegisterForEvent."
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533085"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="d9119-104">\_événement EC CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="d9119-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="d9119-105">L' \_ \_ événement d’événement EC CODECAPI est envoyé par un encodeur pour signaler un événement d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d9119-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="d9119-106">Le client s’inscrit à l’événement d’encodeur en appelant la méthode [**ICodecAPI :: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="d9119-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9119-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9119-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9119-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d9119-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d9119-109">Données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9119-109">User data.</span></span> <span data-ttu-id="d9119-110">La valeur de ce paramètre est le pointeur que l’appelant a spécifié dans le paramètre *UserData* de la méthode [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="d9119-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="d9119-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d9119-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d9119-112">Pointeur vers les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="d9119-112">Pointer to the event data.</span></span> <span data-ttu-id="d9119-113">Ces données sont allouées par l’encodeur et doivent être libérées par l’application, à l’aide de la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="d9119-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="d9119-114">Le bloc de données commence par une structure [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Effectuez un cast du paramètre *lParam2* en un pointeur vers cette structure.</span><span class="sxs-lookup"><span data-stu-id="d9119-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d9119-115">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="d9119-115">Default Action</span></span>

<span data-ttu-id="d9119-116">Aucune action par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9119-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9119-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9119-117">Requirements</span></span>



| <span data-ttu-id="d9119-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9119-118">Requirement</span></span> | <span data-ttu-id="d9119-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9119-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9119-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9119-120">Header</span></span><br/> | <dl> <span data-ttu-id="d9119-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9119-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9119-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9119-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9119-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="d9119-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d9119-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9119-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




