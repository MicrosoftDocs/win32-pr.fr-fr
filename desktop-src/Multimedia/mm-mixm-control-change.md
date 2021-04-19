---
title: Message MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: Le \_ \_ message de modification du contrôle MIXM mm \_ est envoyé par un appareil de mixage pour avertir une application que l’état d’un contrôle associé à une ligne audio a changé. L’application doit actualiser son affichage et les valeurs mises en cache pour le contrôle spécifié.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- Message MM_MIXM_CONTROL_CHANGE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509540"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="977ad-105">\_Message de \_ modification du contrôle MIXM mm \_</span><span class="sxs-lookup"><span data-stu-id="977ad-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="977ad-106">Le message de **\_ \_ \_ modification du contrôle MIXM mm** est envoyé par un appareil de mixage pour avertir une application que l’état d’un contrôle associé à une ligne audio a changé.</span><span class="sxs-lookup"><span data-stu-id="977ad-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="977ad-107">L’application doit actualiser son affichage et les valeurs mises en cache pour le contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="977ad-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="977ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="977ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="977ad-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="977ad-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="977ad-110">Handle vers le périphérique de mixage (**HMIXER**) qui a envoyé le message de notification.</span><span class="sxs-lookup"><span data-stu-id="977ad-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="977ad-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span><span class="sxs-lookup"><span data-stu-id="977ad-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="977ad-112">Identificateur de contrôle pour le contrôle de mixage qui a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="977ad-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="977ad-113">Cet identificateur est le même que le membre **dwControlID** de la structure **MIXERCONTROL** retournée par la fonction **mixerGetLineControls**.</span><span class="sxs-lookup"><span data-stu-id="977ad-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="977ad-114">Notes</span><span class="sxs-lookup"><span data-stu-id="977ad-114">Remarks</span></span>

<span data-ttu-id="977ad-115">Une application doit ouvrir un dispositif de mixage et spécifier une fenêtre de rappel pour recevoir le message de **\_ modification de \_ contrôle \_ mm MIXM** .</span><span class="sxs-lookup"><span data-stu-id="977ad-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="977ad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="977ad-116">Requirements</span></span>



| <span data-ttu-id="977ad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="977ad-117">Requirement</span></span> | <span data-ttu-id="977ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="977ad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="977ad-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="977ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="977ad-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="977ad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="977ad-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="977ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="977ad-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="977ad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="977ad-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="977ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="977ad-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="977ad-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="977ad-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="977ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977ad-126">Mixages audio</span><span class="sxs-lookup"><span data-stu-id="977ad-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="977ad-127">Messages de mixage audio</span><span class="sxs-lookup"><span data-stu-id="977ad-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





