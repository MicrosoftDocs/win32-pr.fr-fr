---
description: 'L’énumération AudioDeviceProperty est utilisée par les méthodes ITAudioDeviceControl :: GetRange, ITAudioDeviceControl :: obten et ITAudioDeviceControl :: Set pour indiquer la propriété qui est adressée.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Énumération AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539690"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="3387d-103">Énumération AudioDeviceProperty</span><span class="sxs-lookup"><span data-stu-id="3387d-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="3387d-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3387d-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3387d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3387d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3387d-106">L’énumération **AudioDeviceProperty** est utilisée par les méthodes [**ITAudioDeviceControl :: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl :: obten**](itaudiodevicecontrol-get.md)et [**ITAudioDeviceControl :: Set**](itaudiodevicecontrol-set.md) pour indiquer la propriété qui est adressée.</span><span class="sxs-lookup"><span data-stu-id="3387d-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3387d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3387d-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="3387d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="3387d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3387d-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**</span><span class="sxs-lookup"><span data-stu-id="3387d-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="3387d-110">Indique que le mode duplex de l’appareil est en cours de définition ou de récupération.</span><span class="sxs-lookup"><span data-stu-id="3387d-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3387d-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**</span><span class="sxs-lookup"><span data-stu-id="3387d-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="3387d-112">Indique que le contrôle du gain automatique de l’appareil est en cours de définition ou de récupération.</span><span class="sxs-lookup"><span data-stu-id="3387d-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3387d-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**</span><span class="sxs-lookup"><span data-stu-id="3387d-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="3387d-114">Indique que les propriétés d’annulation de l’écho acoustique de l’appareil sont en cours de définition ou de récupération.</span><span class="sxs-lookup"><span data-stu-id="3387d-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3387d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3387d-115">Requirements</span></span>



| <span data-ttu-id="3387d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3387d-116">Requirement</span></span> | <span data-ttu-id="3387d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3387d-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3387d-118">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3387d-118">TAPI version</span></span><br/> | <span data-ttu-id="3387d-119">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3387d-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="3387d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3387d-120">Header</span></span><br/>       | <dl> <span data-ttu-id="3387d-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3387d-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3387d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3387d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3387d-123">**ITAudioDeviceControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="3387d-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="3387d-124">**ITAudioDeviceControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="3387d-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="3387d-125">**ITAudioDeviceControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="3387d-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




