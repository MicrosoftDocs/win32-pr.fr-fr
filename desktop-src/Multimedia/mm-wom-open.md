---
title: Message MM_WOM_OPEN (mmsystem. h)
description: Le \_ \_ message d’ouverture WOM mm est envoyé à une fenêtre lorsque l’appareil de sortie Waveform-Audio donné est ouvert.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- Message MM_WOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106519"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="ebf04-104">MM \_ WOM \_ ouvrir le message</span><span class="sxs-lookup"><span data-stu-id="ebf04-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="ebf04-105">Le message d' **\_ \_ ouverture WOM mm** est envoyé à une fenêtre lorsque l’appareil de sortie Waveform-Audio donné est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ebf04-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ebf04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf04-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="ebf04-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="ebf04-108">Handle de l’appareil qui a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="ebf04-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="ebf04-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebf04-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ebf04-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ebf04-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf04-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ebf04-111">Return Value</span></span>

<span data-ttu-id="ebf04-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ebf04-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf04-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf04-113">Requirements</span></span>



| <span data-ttu-id="ebf04-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf04-114">Requirement</span></span> | <span data-ttu-id="ebf04-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf04-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf04-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf04-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf04-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf04-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ebf04-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf04-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf04-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf04-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ebf04-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebf04-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf04-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebf04-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf04-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf04-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf04-123">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="ebf04-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="ebf04-124">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="ebf04-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





