---
title: Message MOM_DONE (Mciapi. h)
description: Le \_ message de travail effectué par MOM est envoyé à une fonction de rappel de sortie MIDI lorsque la mémoire tampon de flux ou l’exclusivité système spécifiée a été lue et est retournée à l’application.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- Message MOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384395"
---
# <a name="mom_done-message"></a><span data-ttu-id="d8774-104">Message de fin de MOM \_</span><span class="sxs-lookup"><span data-stu-id="d8774-104">MOM\_DONE message</span></span>

<span data-ttu-id="d8774-105">Le message de **\_ travail effectué par MOM** est envoyé à une fonction de rappel de sortie MIDI lorsque la mémoire tampon de flux ou l’exclusivité système spécifiée a été lue et est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="d8774-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d8774-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8774-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="d8774-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="d8774-108">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d8774-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d8774-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d8774-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d8774-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="d8774-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8774-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8774-111">Return Value</span></span>

<span data-ttu-id="d8774-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d8774-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8774-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8774-113">Requirements</span></span>



| <span data-ttu-id="d8774-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8774-114">Requirement</span></span> | <span data-ttu-id="d8774-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8774-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d8774-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8774-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8774-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8774-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d8774-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8774-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8774-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8774-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d8774-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8774-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8774-121"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8774-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8774-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8774-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8774-123">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="d8774-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

