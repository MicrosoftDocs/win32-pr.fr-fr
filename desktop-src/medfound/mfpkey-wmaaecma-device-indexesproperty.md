---
description: Spécifie les périphériques audio utilisés par le DSP de capture vocale pour la capture et le rendu audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863438"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="4531a-103">Propriété d’index de l' \_ appareil MFPKEY WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="4531a-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="4531a-104">Spécifie les périphériques audio utilisés par le DSP de capture vocale pour la capture et le rendu audio.</span><span class="sxs-lookup"><span data-stu-id="4531a-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4531a-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4531a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4531a-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="4531a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4531a-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="4531a-107">Data Type</span></span>

<span data-ttu-id="4531a-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="4531a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4531a-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4531a-109">Default Value</span></span>

<span data-ttu-id="4531a-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="4531a-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4531a-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="4531a-111">Applies To</span></span>

-   [<span data-ttu-id="4531a-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="4531a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="4531a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4531a-113">Remarks</span></span>

<span data-ttu-id="4531a-114">Définissez cette propriété si vous utilisez le DSP en mode Source.</span><span class="sxs-lookup"><span data-stu-id="4531a-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="4531a-115">Le DSP ignore cette propriété en mode filtre.</span><span class="sxs-lookup"><span data-stu-id="4531a-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="4531a-116">La valeur de la propriété est compressée par un **mot** de 2 16 bits dans une valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="4531a-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="4531a-117">Les 16 bits supérieurs spécifient le périphérique de rendu audio (généralement un orateur) et les 16 bits inférieurs spécifient l’appareil de capture (généralement un microphone).</span><span class="sxs-lookup"><span data-stu-id="4531a-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="4531a-118">Chaque appareil est spécifié en tant qu’index dans le regroupement de périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="4531a-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="4531a-119">Si l’index est-1, l’appareil par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4531a-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="4531a-120">L’index de l’appareil correspond à l’index de collection utilisé dans l’interface [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) .</span><span class="sxs-lookup"><span data-stu-id="4531a-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="4531a-121">L’application doit jouer la voix extrême sur le périphérique de rendu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4531a-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="4531a-122">(La voix extrême est la voix de la personne à l’autre extrémité de la ligne téléphonique, qui est jouée par l’orateur sur l’ordinateur de l’utilisateur.) Si le périphérique de rendu sélectionné n’a pas de flux actif, le DSP ne peut pas traiter de sortie.</span><span class="sxs-lookup"><span data-stu-id="4531a-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="4531a-123">La valeur par défaut de cette propriété est (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="4531a-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="4531a-124">L’exemple suivant montre comment initialiser le **PROPVARIANT** pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4531a-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="4531a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4531a-125">Requirements</span></span>



| <span data-ttu-id="4531a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4531a-126">Requirement</span></span> | <span data-ttu-id="4531a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4531a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4531a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4531a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4531a-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4531a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4531a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4531a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4531a-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4531a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4531a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4531a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4531a-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4531a-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4531a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4531a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4531a-135">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4531a-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4531a-136">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="4531a-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
