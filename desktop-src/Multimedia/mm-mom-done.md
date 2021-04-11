---
title: Message MM_MOM_DONE (mmsystem. h)
description: Le message de fin de la \_ \_ configuration MOM est envoyé à une fenêtre lorsque la mémoire tampon de flux ou exclusive système midi spécifiée a été lue et est retournée à l’application.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- Message MM_MOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032464"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="b8da4-104">MM \_ \_ message terminé MOM</span><span class="sxs-lookup"><span data-stu-id="b8da4-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="b8da4-105">Le message de **\_ \_ fin** de la configuration MOM est envoyé à une fenêtre lorsque la mémoire tampon de flux ou exclusive système midi spécifiée a été lue et est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="b8da4-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="b8da4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8da4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8da4-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="b8da4-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-108">Handle sur le périphérique de sortie MIDI qui a joué la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b8da4-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b8da4-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="b8da4-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-110">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b8da4-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8da4-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8da4-111">Return Value</span></span>

<span data-ttu-id="b8da4-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b8da4-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8da4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8da4-113">Requirements</span></span>



| <span data-ttu-id="b8da4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8da4-114">Requirement</span></span> | <span data-ttu-id="b8da4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8da4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8da4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8da4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8da4-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8da4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8da4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8da4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8da4-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8da4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8da4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8da4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8da4-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8da4-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8da4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8da4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8da4-123">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="b8da4-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

