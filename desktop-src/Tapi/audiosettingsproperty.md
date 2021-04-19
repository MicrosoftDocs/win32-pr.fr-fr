---
description: 'L’énumération AudioSettingsProperty est utilisée par les méthodes ITAudioSettings :: GetRange, ITAudioSettings :: obten et ITAudioSettings :: Set pour indiquer que la propriété de paramètre audio est traitée.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Énumération AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536018"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="247ad-103">Énumération AudioSettingsProperty</span><span class="sxs-lookup"><span data-stu-id="247ad-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="247ad-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="247ad-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="247ad-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="247ad-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="247ad-106">L’énumération **AudioSettingsProperty** est utilisée par les méthodes [**ITAudioSettings :: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings :: obten**](itaudiosettings-get.md)et [**ITAudioSettings :: Set**](itaudiosettings-set.md) pour indiquer que la propriété de paramètre audio est traitée.</span><span class="sxs-lookup"><span data-stu-id="247ad-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="247ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="247ad-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="247ad-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="247ad-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="247ad-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**</span><span class="sxs-lookup"><span data-stu-id="247ad-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-110">Propriété des paramètres de signal.</span><span class="sxs-lookup"><span data-stu-id="247ad-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**</span><span class="sxs-lookup"><span data-stu-id="247ad-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-112">Propriété de seuil de silence.</span><span class="sxs-lookup"><span data-stu-id="247ad-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="247ad-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-114">Propriété de volume.</span><span class="sxs-lookup"><span data-stu-id="247ad-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ solde**</span><span class="sxs-lookup"><span data-stu-id="247ad-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-116">Propriété balance.</span><span class="sxs-lookup"><span data-stu-id="247ad-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_**</span><span class="sxs-lookup"><span data-stu-id="247ad-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-118">Propriété intensité.</span><span class="sxs-lookup"><span data-stu-id="247ad-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**\_Aigus AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="247ad-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-120">Propriété aigus.</span><span class="sxs-lookup"><span data-stu-id="247ad-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**\_Basses AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="247ad-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-122">Propriété Bass.</span><span class="sxs-lookup"><span data-stu-id="247ad-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="247ad-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="247ad-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="247ad-124">Propriété mono.</span><span class="sxs-lookup"><span data-stu-id="247ad-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="247ad-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="247ad-125">Requirements</span></span>



| <span data-ttu-id="247ad-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="247ad-126">Requirement</span></span> | <span data-ttu-id="247ad-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="247ad-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="247ad-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="247ad-128">TAPI version</span></span><br/> | <span data-ttu-id="247ad-129">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="247ad-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="247ad-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="247ad-130">Header</span></span><br/>       | <dl> <span data-ttu-id="247ad-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="247ad-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="247ad-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="247ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247ad-133">**ITAudioSettings :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="247ad-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="247ad-134">**ITAudioSettings :: obtient**</span><span class="sxs-lookup"><span data-stu-id="247ad-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="247ad-135">**ITAudioSettings :: Set**</span><span class="sxs-lookup"><span data-stu-id="247ad-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 




