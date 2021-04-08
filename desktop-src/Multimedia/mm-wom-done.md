---
title: Message MM_WOM_DONE (mmsystem. h)
description: Le \_ message mm WOM \_ done est envoyé à une fenêtre lorsque la mémoire tampon de sortie donnée est retournée à l’application. Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- Message MM_WOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743916"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="7ab2d-105">MM \_ \_ message terminé WOM</span><span class="sxs-lookup"><span data-stu-id="7ab2d-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="7ab2d-106">Le message **mm \_ WOM \_ done** est envoyé à une fenêtre lorsque la mémoire tampon de sortie donnée est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="7ab2d-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="7ab2d-107">Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="7ab2d-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="7ab2d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ab2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab2d-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="7ab2d-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="7ab2d-110">Handle sur le périphérique de sortie Waveform-Audio qui a joué la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ab2d-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab2d-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="7ab2d-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="7ab2d-112">Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identifiant la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ab2d-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab2d-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ab2d-113">Return Value</span></span>

<span data-ttu-id="7ab2d-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7ab2d-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab2d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ab2d-115">Requirements</span></span>



| <span data-ttu-id="7ab2d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ab2d-116">Requirement</span></span> | <span data-ttu-id="7ab2d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ab2d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab2d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ab2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab2d-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ab2d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ab2d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ab2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab2d-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ab2d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ab2d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ab2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab2d-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ab2d-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab2d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ab2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab2d-125">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="7ab2d-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="7ab2d-126">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="7ab2d-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

