---
title: Resume, commande
description: La commande Resume continue à être lue ou enregistrée sur un appareil qui a été suspendu à l’aide de la commande pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- commande Resume Windows multimédia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509295"
---
# <a name="resume-command"></a><span data-ttu-id="f41e1-104">Resume, commande</span><span class="sxs-lookup"><span data-stu-id="f41e1-104">resume command</span></span>

<span data-ttu-id="f41e1-105">La commande Resume continue à être lue ou enregistrée sur un appareil qui a été suspendu à l’aide de la commande [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="f41e1-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="f41e1-106">Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="f41e1-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="f41e1-107">Bien que les périphériques CD audio, MIDI Sequencer et videodisc reconnaissent également cette commande, les pilotes de périphérique MCICDA, MCISEQ et MCIPIONR ne le prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="f41e1-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="f41e1-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="f41e1-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f41e1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f41e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f41e1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f41e1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f41e1-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="f41e1-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f41e1-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f41e1-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f41e1-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f41e1-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f41e1-114">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f41e1-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f41e1-115">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="f41e1-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f41e1-116">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f41e1-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f41e1-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f41e1-117">Return Value</span></span>

<span data-ttu-id="f41e1-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="f41e1-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="f41e1-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="f41e1-119">Examples</span></span>

<span data-ttu-id="f41e1-120">La commande suivante poursuit la diffusion ou l’enregistrement de l’appareil « newsound ».</span><span class="sxs-lookup"><span data-stu-id="f41e1-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="f41e1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f41e1-121">Requirements</span></span>



| <span data-ttu-id="f41e1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f41e1-122">Requirement</span></span> | <span data-ttu-id="f41e1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f41e1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f41e1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f41e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f41e1-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f41e1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f41e1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f41e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f41e1-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f41e1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f41e1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f41e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f41e1-129">MCI</span><span class="sxs-lookup"><span data-stu-id="f41e1-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f41e1-130">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="f41e1-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f41e1-131">pause</span><span class="sxs-lookup"><span data-stu-id="f41e1-131">pause</span></span>](pause.md)
</dt> </dl>

 

