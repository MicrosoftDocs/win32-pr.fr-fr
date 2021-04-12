---
title: Message MM_WIM_CLOSE (mmsystem. h)
description: Le \_ message de \_ fermeture de fichier WIM mm est envoyé à une fenêtre lorsqu’un périphérique d’entrée Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- Message MM_WIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032324"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="f2da9-105">MM \_ \_ message de fermeture Wim</span><span class="sxs-lookup"><span data-stu-id="f2da9-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="f2da9-106">Le message de **\_ \_ fermeture de fichier WIM mm** est envoyé à une fenêtre lorsqu’un périphérique d’entrée Waveform-Audio est fermé.</span><span class="sxs-lookup"><span data-stu-id="f2da9-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="f2da9-107">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="f2da9-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f2da9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2da9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2da9-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="f2da9-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="f2da9-110">Handle sur le périphérique d’entrée Waveform-Audio qui a été fermé.</span><span class="sxs-lookup"><span data-stu-id="f2da9-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="f2da9-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2da9-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f2da9-112">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f2da9-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2da9-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f2da9-113">Return Value</span></span>

<span data-ttu-id="f2da9-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2da9-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2da9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2da9-115">Requirements</span></span>



| <span data-ttu-id="f2da9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2da9-116">Requirement</span></span> | <span data-ttu-id="f2da9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2da9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2da9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2da9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2da9-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2da9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2da9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2da9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2da9-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2da9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f2da9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2da9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2da9-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2da9-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2da9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2da9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2da9-125">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="f2da9-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="f2da9-126">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="f2da9-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





