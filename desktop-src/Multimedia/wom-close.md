---
title: Message WOM_CLOSE (mmsystem. h)
description: Le \_ message WOM Close est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- Message WOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510130"
---
# <a name="wom_close-message"></a><span data-ttu-id="a1b75-105">WOM \_ Fermer le message</span><span class="sxs-lookup"><span data-stu-id="a1b75-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="a1b75-106">Le message **WOM \_ Close** est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est fermé.</span><span class="sxs-lookup"><span data-stu-id="a1b75-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="a1b75-107">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a1b75-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="a1b75-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1b75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b75-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a1b75-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a1b75-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a1b75-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1b75-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a1b75-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a1b75-112">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a1b75-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b75-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1b75-113">Return Value</span></span>

<span data-ttu-id="a1b75-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a1b75-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b75-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1b75-115">Requirements</span></span>



| <span data-ttu-id="a1b75-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1b75-116">Requirement</span></span> | <span data-ttu-id="a1b75-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1b75-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b75-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1b75-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b75-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1b75-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a1b75-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1b75-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b75-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1b75-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a1b75-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1b75-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b75-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1b75-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b75-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1b75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b75-125">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="a1b75-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="a1b75-126">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="a1b75-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





