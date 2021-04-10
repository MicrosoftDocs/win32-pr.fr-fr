---
title: Message WOM_DONE (mmsystem. h)
description: Le \_ message WOM Done est envoyé à une fonction de rappel de sortie Waveform Audio lorsque la mémoire tampon de sortie donnée est retournée à l’application.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- Message WOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103025"
---
# <a name="wom_done-message"></a><span data-ttu-id="e8409-104">\_Message WOM terminé</span><span class="sxs-lookup"><span data-stu-id="e8409-104">WOM\_DONE message</span></span>

<span data-ttu-id="e8409-105">Le message **WOM \_ done** est envoyé à une fonction de rappel de sortie Waveform Audio lorsque la mémoire tampon de sortie donnée est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="e8409-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="e8409-106">Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="e8409-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e8409-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8409-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8409-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e8409-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e8409-109">Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identifiant la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e8409-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e8409-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e8409-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e8409-111">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e8409-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8409-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8409-112">Return Value</span></span>

<span data-ttu-id="e8409-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e8409-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8409-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8409-114">Requirements</span></span>



| <span data-ttu-id="e8409-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8409-115">Requirement</span></span> | <span data-ttu-id="e8409-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8409-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8409-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8409-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8409-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8409-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8409-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8409-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8409-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8409-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8409-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8409-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8409-122"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8409-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8409-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8409-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8409-124">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="e8409-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="e8409-125">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="e8409-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

