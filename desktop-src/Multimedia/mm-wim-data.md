---
title: Message MM_WIM_DATA (mmsystem. h)
description: Le \_ message de \_ données Wim mm est envoyé à une fenêtre quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application. Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- Message MM_WIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517325"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="88ec6-105">\_Message de données Wim de mm \_</span><span class="sxs-lookup"><span data-stu-id="88ec6-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="88ec6-106">Le message de **\_ \_ données Wim mm** est envoyé à une fenêtre quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="88ec6-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="88ec6-107">Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="88ec6-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="88ec6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ec6-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="88ec6-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="88ec6-110">Handle sur le périphérique d’entrée Waveform-Audio qui a reçu les données.</span><span class="sxs-lookup"><span data-stu-id="88ec6-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="88ec6-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="88ec6-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="88ec6-112">Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon contenant les données.</span><span class="sxs-lookup"><span data-stu-id="88ec6-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ec6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88ec6-113">Return Value</span></span>

<span data-ttu-id="88ec6-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="88ec6-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ec6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="88ec6-115">Remarks</span></span>

<span data-ttu-id="88ec6-116">La mémoire tampon retournée n’est peut-être pas pleine.</span><span class="sxs-lookup"><span data-stu-id="88ec6-116">The returned buffer might not be full.</span></span> <span data-ttu-id="88ec6-117">Utilisez le membre **dwBytesRecorded** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) spécifiée par *lParam* pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="88ec6-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ec6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88ec6-118">Requirements</span></span>



| <span data-ttu-id="88ec6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88ec6-119">Requirement</span></span> | <span data-ttu-id="88ec6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="88ec6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ec6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88ec6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88ec6-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88ec6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88ec6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88ec6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88ec6-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88ec6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88ec6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="88ec6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="88ec6-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ec6-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ec6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88ec6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ec6-128">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="88ec6-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="88ec6-129">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="88ec6-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

