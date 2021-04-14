---
title: Message WIM_CLOSE (mmsystem. h)
description: Le \_ message de fermeture Wim est envoyé à la fonction de rappel d’entrée Wave-Audio donnée lorsqu’un périphérique d’entrée Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- Message WIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466642"
---
# <a name="wim_close-message"></a><span data-ttu-id="d1a41-105">\_Message de fermeture Wim</span><span class="sxs-lookup"><span data-stu-id="d1a41-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="d1a41-106">Le message de **\_ fermeture Wim** est envoyé à la fonction de rappel d’entrée Wave-Audio donnée lorsqu’un périphérique d’entrée Waveform-Audio est fermé.</span><span class="sxs-lookup"><span data-stu-id="d1a41-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="d1a41-107">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="d1a41-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d1a41-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1a41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a41-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d1a41-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d1a41-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d1a41-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1a41-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d1a41-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d1a41-112">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d1a41-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a41-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1a41-113">Return Value</span></span>

<span data-ttu-id="d1a41-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1a41-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a41-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1a41-115">Requirements</span></span>



| <span data-ttu-id="d1a41-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1a41-116">Requirement</span></span> | <span data-ttu-id="d1a41-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1a41-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a41-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a41-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1a41-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d1a41-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a41-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1a41-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d1a41-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1a41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a41-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a41-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a41-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a41-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a41-125">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="d1a41-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="d1a41-126">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="d1a41-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





