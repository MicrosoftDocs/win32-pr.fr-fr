---
title: Message WIM_DATA (mmsystem. h)
description: Le \_ message de données Wim est envoyé à la fonction de rappel d’entrée Wave-Audio donnée quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- Message WIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510167"
---
# <a name="wim_data-message"></a><span data-ttu-id="1a44e-104">\_Message de données Wim</span><span class="sxs-lookup"><span data-stu-id="1a44e-104">WIM\_DATA message</span></span>

<span data-ttu-id="1a44e-105">Le message de **\_ données Wim** est envoyé à la fonction de rappel d’entrée Wave-Audio donnée quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="1a44e-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="1a44e-106">Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="1a44e-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1a44e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a44e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a44e-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1a44e-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a44e-109">Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon contenant les données.</span><span class="sxs-lookup"><span data-stu-id="1a44e-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="1a44e-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1a44e-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a44e-111">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1a44e-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a44e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a44e-112">Return Value</span></span>

<span data-ttu-id="1a44e-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a44e-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a44e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1a44e-114">Remarks</span></span>

<span data-ttu-id="1a44e-115">La mémoire tampon retournée n’est peut-être pas pleine.</span><span class="sxs-lookup"><span data-stu-id="1a44e-115">The returned buffer might not be full.</span></span> <span data-ttu-id="1a44e-116">Utilisez le membre **dwBytesRecorded** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) spécifiée par *lpwvhdr* pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="1a44e-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a44e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a44e-117">Requirements</span></span>



| <span data-ttu-id="1a44e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a44e-118">Requirement</span></span> | <span data-ttu-id="1a44e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a44e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a44e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a44e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a44e-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a44e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a44e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a44e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a44e-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a44e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1a44e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a44e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a44e-125"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a44e-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a44e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a44e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a44e-127">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="1a44e-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="1a44e-128">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="1a44e-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

