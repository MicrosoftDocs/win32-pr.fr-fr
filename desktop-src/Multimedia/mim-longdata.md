---
title: Message MIM_LONGDATA (mmsystem. h)
description: Le \_ message MIM LONGDATA est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un tampon système exclusif a été rempli de données et est retourné à l’application.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- Message MIM_LONGDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106528"
---
# <a name="mim_longdata-message"></a><span data-ttu-id="5383a-104">\_Message MIM LONGDATA</span><span class="sxs-lookup"><span data-stu-id="5383a-104">MIM\_LONGDATA message</span></span>

<span data-ttu-id="5383a-105">Le message **MIM \_ LONGDATA** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un tampon système exclusif a été rempli de données et est retourné à l’application.</span><span class="sxs-lookup"><span data-stu-id="5383a-105">The **MIM\_LONGDATA** message is sent to a MIDI input callback function when a system-exclusive buffer has been filled with data and is being returned to the application.</span></span>


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="5383a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5383a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5383a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="5383a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="5383a-108">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5383a-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5383a-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="5383a-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="5383a-110">Heure à laquelle les données ont été reçues par le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5383a-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="5383a-111">L’horodatage est spécifié en millisecondes, en commençant à zéro lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="5383a-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5383a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5383a-112">Return Value</span></span>

<span data-ttu-id="5383a-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5383a-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5383a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5383a-114">Remarks</span></span>

<span data-ttu-id="5383a-115">La mémoire tampon retournée n’est peut-être pas pleine.</span><span class="sxs-lookup"><span data-stu-id="5383a-115">The returned buffer might not be full.</span></span> <span data-ttu-id="5383a-116">Pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée, utilisez le membre **dwBytesRecorded** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) spécifiée par *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="5383a-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5383a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5383a-117">Requirements</span></span>



| <span data-ttu-id="5383a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5383a-118">Requirement</span></span> | <span data-ttu-id="5383a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5383a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5383a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5383a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5383a-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5383a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5383a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5383a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5383a-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5383a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5383a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5383a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5383a-125"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5383a-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5383a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5383a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5383a-127">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="5383a-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5383a-128">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="5383a-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

