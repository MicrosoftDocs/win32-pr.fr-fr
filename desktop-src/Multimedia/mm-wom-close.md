---
title: Message MM_WOM_CLOSE (mmsystem. h)
description: Le \_ message de \_ fermeture de mm WOM est envoyé à une fenêtre lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- Message MM_WOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512214"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="a8a3b-105">MM \_ WOM \_ Fermer le message</span><span class="sxs-lookup"><span data-stu-id="a8a3b-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="a8a3b-106">Le message de **\_ \_ fermeture de mm WOM** est envoyé à une fenêtre lorsqu’un appareil de sortie Waveform-Audio est fermé.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="a8a3b-107">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="a8a3b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8a3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a3b-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="a8a3b-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="a8a3b-110">Handle vers l’appareil qui a été fermé.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="a8a3b-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8a3b-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a8a3b-112">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a3b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8a3b-113">Return Value</span></span>

<span data-ttu-id="a8a3b-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a3b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8a3b-115">Requirements</span></span>



| <span data-ttu-id="a8a3b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8a3b-116">Requirement</span></span> | <span data-ttu-id="a8a3b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8a3b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a3b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a3b-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a3b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8a3b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a3b-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a3b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8a3b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8a3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a3b-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8a3b-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a3b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a3b-125">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="a8a3b-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="a8a3b-126">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="a8a3b-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





