---
title: Message MM_MIXM_LINE_CHANGE (mmsystem. h)
description: Le \_ \_ message de modification de la ligne mm MIXM \_ est envoyé par un appareil de mixage pour avertir une application que l’état d’une ligne audio sur l’appareil spécifié a changé. L’application doit actualiser ses valeurs d’affichage et de mise en cache pour la ligne audio spécifiée.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- Message MM_MIXM_LINE_CHANGE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509731"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="0b7f2-105">Message de modification de la \_ ligne mm MIXM \_ \_</span><span class="sxs-lookup"><span data-stu-id="0b7f2-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="0b7f2-106">Le message de modification de la **\_ \_ ligne \_ mm MIXM** est envoyé par un appareil de mixage pour avertir une application que l’état d’une ligne audio sur l’appareil spécifié a changé.</span><span class="sxs-lookup"><span data-stu-id="0b7f2-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="0b7f2-107">L’application doit actualiser ses valeurs d’affichage et de mise en cache pour la ligne audio spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0b7f2-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="0b7f2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b7f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7f2-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="0b7f2-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="0b7f2-110">Handle vers le périphérique de mixage qui a envoyé le message de notification.</span><span class="sxs-lookup"><span data-stu-id="0b7f2-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="0b7f2-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span><span class="sxs-lookup"><span data-stu-id="0b7f2-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="0b7f2-112">Identificateur de ligne pour la ligne audio dont l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="0b7f2-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="0b7f2-113">Cet identificateur est le même que le membre **dwLineID** de la structure **MIXERLINE** retournée par la fonction **mixerGetLineInfo**.</span><span class="sxs-lookup"><span data-stu-id="0b7f2-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b7f2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0b7f2-114">Remarks</span></span>

<span data-ttu-id="0b7f2-115">Une application doit ouvrir un dispositif de mixage et spécifier une fenêtre de rappel pour recevoir le message de modification de la **\_ \_ ligne \_ mm MIXM** .</span><span class="sxs-lookup"><span data-stu-id="0b7f2-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7f2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b7f2-116">Requirements</span></span>



| <span data-ttu-id="0b7f2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b7f2-117">Requirement</span></span> | <span data-ttu-id="0b7f2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b7f2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7f2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b7f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b7f2-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b7f2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0b7f2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b7f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b7f2-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b7f2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0b7f2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b7f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b7f2-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b7f2-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b7f2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b7f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7f2-126">Mixages audio</span><span class="sxs-lookup"><span data-stu-id="0b7f2-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="0b7f2-127">Messages de mixage audio</span><span class="sxs-lookup"><span data-stu-id="0b7f2-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





